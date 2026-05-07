---
name: glossary-builder
description: >
  Build and maintain a standardized internal glossary in Markdown format by scanning
  documents, transcripts, and materials across a repo. Use this skill whenever the user
  wants to create a terminology glossary, standardize vocabulary across documentation,
  extract terms from existing files, identify synonym variants or terms to avoid, or
  update/expand an existing glossary. Trigger even if the user just says "update the
  glossary", "add terms from this file", or "what terms are we using inconsistently".
---

# Glossary Builder

Creates and maintains a Markdown glossary by scanning repo files to extract terminology,
infer preferred terms vs. variants to avoid, and tag entries by domain/category.
Definitions can be left empty for later discussion.

---

## Workflow

### 1. Discover Files

Search broadly across the repo for source material. Look in all subdirectories.
Relevant file types:
- Transcripts: `.txt`, `.md`, `.vtt`, `.srt`, `.docx`, `.pdf`
- Documentation: `.md`, `.rst`, `.html`, `.docx`, `.pdf`
- Notes, specs, meeting notes, any prose content

```bash
# Find all candidate files (exclude build artifacts, node_modules, etc.)
find . -type f \( -name "*.md" -o -name "*.txt" -o -name "*.docx" \
  -o -name "*.pdf" -o -name "*.vtt" -o -name "*.rst" -o -name "*.html" \) \
  ! -path "*/node_modules/*" ! -path "*/.git/*" ! -path "*/dist/*" \
  ! -path "*/build/*" | sort
```

Tell the user which files you found and which ones you'll scan. If the list is very
large (>50 files), summarize by folder and ask if any areas should be excluded.

### 2. Extract Terminology

Read through the files and collect:
- **Domain-specific nouns and noun phrases** — product names, process names, roles,
  technical concepts, actions, artifacts
- **Variations** — the same concept referred to in multiple ways across different files
  (e.g. "onboarding flow" vs "user onboarding" vs "activation flow")
- **Capitalization inconsistencies** — "API key" vs "api key" vs "API Key"
- **Abbreviations and their expansions** — e.g. "SLA", "PO", "QA"

Focus on terms that appear **more than once** or across **more than one file** — single
occurrences of generic words are not glossary candidates.

### 3. Infer Preferred Terms and Variants to Avoid

For each cluster of synonyms/variants, infer the **preferred term** based on:
- Frequency (most-used form)
- Recency (appears in newer documents)
- Formality (more formal/precise wins in documentation contexts)
- Consistency with product names or official naming if detectable

Mark the other forms as **"avoid"** — terms that exist in the corpus but should be
replaced with the preferred term for standardization.

If it's genuinely unclear which is preferred, leave `preferred_term` as the most
common form and add a note: `"⚠️ Discuss: no clear consensus found"`.

### 4. Assign Category Tags

Tag each entry with one or more domain/category labels inferred from context.
Examples (adapt to what you find in the repo):
- `product`, `engineering`, `design`, `process`, `role`, `legal`, `marketing`,
  `onboarding`, `data`, `support`

Use consistent, lowercase tags. Don't create more than ~10 distinct tags unless
clearly needed.

### 5. Write the Glossary

Output a single Markdown file: `glossary.md`

Use the structure below. Sort entries **alphabetically by preferred term**.

---

## Output Format

```markdown
# Glossary

> Internal terminology reference. Use preferred terms in all documentation.
> Last updated: YYYY-MM-DD

---

## [Category Tag]

### [Preferred Term]

- **Definition**: A plain-prose explanation of what this term means in the context of
  the platform or product. If no definition could be inferred from the source material,
  write `_(to be defined)_` here.

- **Avoid**: term-a, term-b (brief note explaining when/why to avoid them, if useful)

- **Usage Notes**: Any nuance about when alternate terms are acceptable in clinical or
  general prose vs. the platform object name; known limitations; related terms.

---

### [Another Term]

- **Definition**: _(to be defined)_

- **Avoid**: —

- **Usage Notes**: —
```

**Rules:**
- Write **Definition** as natural prose — not a table cell, not a bullet fragment
- If no synonyms to avoid, write `—` on the Avoid line
- If no usage notes, write `—` on the Usage Notes line
- If a definition was found in the source material (e.g. an explicit "X means Y"
  statement), fill it in; otherwise write `_(to be defined)_`
- Group entries under `## [Category Tag]` headings, alphabetically within each group
- Omit the **Tags** field from entry bodies — category is already conveyed by the
  `## [Category Tag]` section heading
- Add a summary table at the top of the file after the intro blurb

---

## Summary Table (top of glossary)

After the intro, include a quick-reference table of all terms:

```markdown
## Quick Reference

| Preferred Term | Avoid | Category | Defined? |
|---|---|---|---|
| term-a | old-term, alt-term | product | ✅ |
| term-b | — | engineering | ⬜ |
```

Use ✅ for defined entries and ⬜ for entries still needing a definition.

---

## Updating an Existing Glossary

If a `glossary.md` already exists in the repo:
1. Load it and parse the existing entries
2. Scan new/changed files since the last update (ask user for date or files if unclear)
3. Add new terms; **do not overwrite existing definitions**
4. Flag new synonym variants found that conflict with existing preferred terms
5. Update the `Last updated` date

---

## Edge Cases

- **Acronyms**: Always include the expansion as the preferred term; the acronym goes in
  a `Also known as` note. E.g. preferred: "Service Level Agreement", avoid: —,
  note: "Abbreviated as SLA"
- **Proper nouns / product names**: Include only if there are known misspellings or
  variant capitalizations in the corpus
- **Very large repos**: If scanning would take too long, ask the user to prioritize
  folders. Process in batches and merge results.
- **Non-English terms**: If the repo is multilingual, note the language in the Tags
  field and keep English as the primary glossary language unless instructed otherwise
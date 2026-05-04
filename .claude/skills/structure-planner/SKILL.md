# Create Diataxis Documentation Outline (Subflow / Featurebase)

Analyze this project and generate a documentation navigation outline structured around the [Diataxis](https://diataxis.fr) framework.

This outline is intended to be published in **Featurebase** as a Guides-only knowledge base. Do not include an API Reference tab.

**Do not create documentation pages or write any content.** Your only output is the outline file described below.

---

## Step 0 — Read all available source materials

Before doing anything else, read every file you can find in the following locations:

- **`/mnt/transcripts/`** — conversation or interview transcripts that describe how users interact with the product, pain points, workflows, and language they use
- **`materials/`** (relative to the project root, if it exists) — raw materials such as specs, internal docs, README drafts, design docs, or feature descriptions

Extract from these sources:
- What the product does and who it's for
- All features, workflows, and concepts mentioned
- Terminology and naming conventions used — **preserve these exactly**
- User pain points, questions, and goals surfaced in transcripts

Treat these files as the single source of truth. Do not invent features or capabilities not mentioned in them.

---

## Step 1 — Determine the input mode

After reading the source materials above, detect which input mode applies based on what else the user provides:

---

### Mode A — Improve existing documentation

**Triggered when:** the project already contains a docs folder, a README, or existing documentation files (in addition to the materials above).

Explore the project and extract:
- What the product does and who it's for
- The existing documentation structure: what's covered, what's missing, what's duplicated
- Pages or sections that don't fit their Diataxis type (e.g. a "tutorial" that's actually reference)
- Gaps in the user journey — concepts assumed but never explained, tasks with no how-to guide
- The main surfaces: APIs, CLI, SDK, UI, integrations

Use the existing structure as a starting point but reorganize freely. The goal is an improved outline, not a faithful copy of what exists.

---

### Mode B — Create from source materials only

**Triggered when:** there are no existing docs — only the transcripts and materials folders read in Step 0.

Use everything gathered in Step 0 to construct the outline from scratch. The likely user journey (from zero to productive) should be the organizing principle.

---

In both modes, use everything you've gathered to inform every decision in the outline — section names, page titles, and page types must all reflect the actual product and its users' language.

---

## Step 2 — Design the outline

Structure the outline around **one tab: Guides**.

The Guides tab contains all learning and task-oriented content. Organize it into sections that follow the user journey — from understanding what the product is, to completing their first meaningful task, to mastering advanced workflows.

### Sections within the Guides tab
Group related pages into named sections. Each section must have:
- A short title
- A 1–2 sentence description of what the section covers and what the user will be able to do after reading it

### Pages within each section
Each page entry must include:
- **Title** — clear, user-facing name
- **Page type** — one of: `Concept`, `Tutorial`, `How-to Guide`, `Reference`
- **Description** — one sentence explaining what the page covers and its specific value to the reader

Apply Diataxis page types as follows:

| Type | Use when… |
|---|---|
| `Concept` | The page explains *what* something is or *why* it works a certain way |
| `Tutorial` | The page walks the user through a complete task to *learn by doing* |
| `How-to Guide` | The page gives step-by-step instructions to *accomplish a specific goal* |
| `Reference` | The page is a precise, exhaustive description of a config option, setting, or field list |

> **Note:** Reference pages within the Guides tab are acceptable for things like settings panels or field definitions — but do not add a separate API Reference tab.

---

## Step 3 — Write the outline file

Create a single file: **`docs/outline.md`**

Use exactly this format:

```markdown
# Documentation Outline: {Product Name}

{2–3 sentence description of the product and who this documentation is for. Mention that it is published in Featurebase.}

---

## Tab: Guides

This tab contains all documentation for {Product Name}: conceptual overviews, step-by-step tutorials, how-to guides for specific tasks, and reference material for settings and configuration.

### {Section Name}

{1–2 sentences describing what this section covers and what the reader will get from it.}

* **{Page Title}** [`{Page Type}`]: {One sentence describing what this page covers and its value to the reader.}
* **{Page Title}** [`{Page Type}`]: {One sentence describing what this page covers and its value to the reader.}

### {Section Name}

{1–2 sentences describing what this section covers and what the reader will get from it.}

* **{Page Title}** [`{Page Type}`]: {One sentence describing what this page covers and its value to the reader.}
```

---

## User Navigation Flow

After the outline, append a **User Navigation Flow** section to `docs/outline.md`.

This section envisions the ideal path a new user takes from the Featurebase knowledge base homepage to their first meaningful win — the moment they've successfully used the product for the first time.

Use this format:

```markdown
---

## User Navigation Flow

{1–2 sentences describing the type of user this flow is designed for and what "winning" looks like for them.}

1. **Featurebase Homepage** → {Describe what the user sees and what draws them in — value proposition, key CTA.}
2. **{Page Title}** → {What the user does here and what they take away.}
3. **{Page Title}** → {What the user does here and what they take away.}
4. **{Page Title}** → {What the user does here and what they take away.}
5. **First win** → {Describe the concrete moment of success — e.g. "User successfully sets up their first automated flow and sees it run end-to-end."}
```

Guidelines:
- The flow should be **linear and opinionated** — pick the single best path, not every possible path
- Every step must reference a real page from the outline above
- Steps should be **5–8 total** — enough to be meaningful, short enough to be a quick win
- The final step must describe a tangible, specific success moment (not "user understands the product")

---

## Quality checklist

Before finishing, verify:

- [ ] `/mnt/transcripts/` was read (or noted as empty) before designing the outline
- [ ] `materials/` folder was read (or noted as absent) before designing the outline
- [ ] Input mode was correctly identified (A = existing docs present, B = source materials only)
- [ ] No placeholder text (`{...}`) remains anywhere in the file
- [ ] Every page has a title, a page type, and a one-sentence description
- [ ] Page types are used consistently per the Diataxis definitions above
- [ ] Section descriptions explain the reader's goal, not just the content
- [ ] Tab and section names reflect the actual product — not generic labels
- [ ] There is **only one tab**: Guides (no API Reference tab)
- [ ] The Guides tab follows a logical user journey (introduction → quick start → concepts → advanced)
- [ ] The User Navigation Flow is 5–8 steps, linear, and every step references a real page from the outline
- [ ] The flow ends with a concrete, specific success moment
- [ ] The outline intro mentions Featurebase as the publishing platform
# Page types

> **How to use this file:** This file defines the structure template for each page type. The Writer skill loads only the page type relevant to the current task. Adjust section names or required frontmatter fields to match the project's platform before writing begins.
>
> For deeper guidance on the theory behind each page type, refer to the [Diátaxis framework](https://diataxis.fr) and [The Good Docs Project templates](https://www.thegooddocsproject.dev).

---

## Page type overview

| Page type | Goal | Reader stage | When to use |
|---|---|---|---|
| **Concept** | Explain what something is and why it matters | Learner | Introducing a feature, system, or idea the user needs to understand before taking action |
| **How-to guide** | Walk the user through completing a specific task | Practitioner | When the user needs step-by-step instructions to accomplish one specific goal |
| **Reference** | Provide structured, scannable facts | Experienced | Configuration options, error codes, API fields, CLI flags |
| **Tutorial** | Guide the user through a complete, end-to-end scenario | Newcomer | Onboarding flows, first-use walkthroughs, learning a workflow from scratch |

> One URL, one page type. Do not mix tutorial content with reference tables, or concept explanations with how-to steps.

---

## Concept page

**Goal:** Explain what something is and why it matters. Answer "what" and "why" — not "how."

> Concept pages are the most open-ended page type. The right structure depends heavily on what is being explained. Before writing, read the [Good Docs Project concept guide](https://gitlab.com/tgdp/templates/-/blob/main/concept/guide_concept.md) to understand the options and choose the most appropriate structure for the topic.

### Frontmatter

```yaml
---
title: "{Concept name}"
description: "{Why this concept matters — one sentence}"
slug: /concepts/{slug}
---
```

### Structure

```
# [Concept name]

One or two sentences: what this is and why the user needs to understand it.
Do not bold any words in this introduction.

## What it is

Explanation of the concept. Use plain language. Avoid internal jargon
not defined in the glossary.

## How it works (if applicable)

Explanation of the underlying mechanism or model — only include if
understanding the mechanism helps the user make decisions.

## Key terms (if applicable)

Define any terms that appear on this page and are not yet in the glossary.
Use the same definitions from glossary.md.

## Examples (if applicable)

Concrete examples that illustrate the concept in context.

## Related articles

Use the CardList and Card components as defined in style-guide.md and ProjectConvention.md.
```

### Notes

- Do not include step-by-step instructions on a concept page. If you feel the need to, that content belongs in a how-to guide.
- Concepts and processes are different things. A concept is a *thing* (entity, model, construct). A process is a *sequence of steps*. If source material conflates them, split them.

---

## How-to guide

**Goal:** Help the user accomplish a specific, real-world task. Answer "how."

### Frontmatter

```yaml
---
title: "{How-to title — starts with an imperative verb}"
description: "{Specific problem this guide solves}"
slug: /guides/{slug}
audience: "{role + assumed experience level}"
---
```

### Structure

```
# [Imperative verb + task, e.g. "Create a webhook"]

Short introduction: state what the user will accomplish and when or why
they would do it. Keep it brief — do not teach theory here.
Do not bold any words in this introduction.

## Before you begin

List everything the user needs before starting the steps. This is one consolidated section — do not split it into separate "Prerequisites" and "Before you begin" sections.

Include, in this order:
- Account, access, or permissions required.
- Tools, software, or prior setup (with links if necessary).
- Prior knowledge or previous guides the user should have completed (with links to the relevant guides).
- Content, values, or decisions the user must bring to the procedure (inferred from the steps — see "Inferred preparation items" below).

Be specific and assertive. Avoid vague phrases like "a good knowledge of the tools."
Include links to related pages where relevant.

Only omit this section if the procedure genuinely requires nothing — no access, no setup, no prior knowledge, and no user-supplied input. This is rare.

> [Insert callout for known limitations or caveats if needed.]

## [Step section — follow the convention chosen in style-guide.md]

[Option A — Narrative steps]
### Step 1: [Descriptive title]
Paragraph explaining the step in detail.

[Option B — Numbered list steps]
1. **[Imperative verb]** — concise action.
   - Optional sub-steps, screenshots, or code.
   - Expected result or verification.
2. **[Next action]** …

## Troubleshooting (optional)

- **Problem:** [Symptom or error message]
  - **Solution:** [Steps to resolve.]
  - **Prevention:** [Optional tip to avoid the problem in future.]

## Related articles (optional)

Use the CardList and Card components as defined in style-guide.md and ProjectConvention.md.

## What's next (optional)

If this guide is part of a larger workflow, describe the next required task
and include a link.
```

### Inferred preparation items

Most of what goes in "Before you begin" can be read directly from the source material — required permissions, tools, prior setup. But there is a second category that is almost never stated explicitly: the **content, values, and decisions the user must bring with them** to complete the steps. These must be inferred from the procedure itself.

Do not skip this inference. A "Before you begin" section that lists only access and tools, when the steps actually require the user to supply content or make choices, is incomplete.

**How to derive the items:**

1. Draft the full step sequence first, or at minimum outline every step, before finalizing the "Before you begin" section.
2. For each step, ask: "What input, content, or decision does this step require the user to bring, that is not produced by an earlier step?" Examples:
   - A step says "enter the template body" → the user needs the text content, or a clear idea of what it should say.
   - A step says "select the contact properties to insert" → the user needs to know which properties they want to use.
   - A step says "apply tags" → the user needs the tags, or a tagging scheme.
   - A step says "choose a workspace" → the user needs to know which workspace.
3. Add each inferred item to the "Before you begin" list alongside the access and setup items.
4. Write each item as a noun phrase describing the input, followed by the acceptable form. Allow for "or a clear idea of what it should be" when the input is creative content rather than a fixed value. Example: "The text you want the template to contain, or a clear idea of what it should say."

**When to flag instead of inferring:**

If a step requires user input but you cannot tell from the source what kind of input is valid (format constraints, allowed values), raise a flag rather than writing a vague item. Example: `> FLAG: Insufficient source — Step 3 asks the user to enter a "condition value" but the source does not state what values are accepted. Need clarification before listing this in "Before you begin".`

---

## Reference page

**Goal:** Provide definitive, structured, scannable facts. Answer "what exactly."

> Reference pages are often auto-generated from code or schemas. If this project auto-generates reference content, set `generated: true` in the frontmatter and note the source.

### Frontmatter

```yaml
---
title: "{Component / API / Field catalogue}"
description: "{Scope of this reference — one sentence}"
slug: /reference/{slug}
generated: false   # set to true if auto-generated
---
```

### Structure

```
# [Component, option set, or topic] reference

One sentence describing what this page documents.
Do not bold any words in this introduction.

## [Entity group heading]

Overview of this group of entries and any shared context.

| Field | Type | Required | Default | Description | Notes |
|---|---|---|---|---|---|
| `[field]` | `[type]` | Yes / No | `[value]` | [Description] | [Caveats] |

(Repeat tables, lists, or schemas as needed for each entity group.)

## Related resources

Links to tutorials or how-to guides that use this reference material.
```

### Notes

- Keep descriptions factual and scannable. This is not the place for explanation or narrative.
- If a field has accepted values, list them explicitly.
- If a field has constraints, state them (e.g. "Maximum 255 characters").

---

## Tutorial

**Goal:** Teach by doing. Guide the user through a complete, end-to-end scenario on the "happy path." Answer "how do I learn this from scratch."

### Frontmatter

```yaml
---
title: "{Tutorial title}"
description: "{One-sentence elevator pitch}"
slug: /tutorials/{slug}
time_to_complete: "≈ {NN} min"
audience: "{e.g. new users | data admins}"
prerequisites:
  - "{e.g. SDK installed}"
  - "{e.g. Sample dataset downloaded}"
---
```

### Structure

```
# [Goal or scenario]

What the user will build or accomplish. Set context: who this is for
and what they will have at the end.

**Learning objectives:** By the end of this tutorial, you will be able to:
- [Objective 1]
- [Objective 2]

Do not bold any words in the introduction paragraph itself.

## Before you begin

List everything the user needs before starting the tutorial — this is one consolidated section. Apply the same rules as for how-to guides, including inferring the content, values, and decisions the user must bring to the steps. See "Inferred preparation items" under the How-to guide section.

Include, in this order:
- Access, tokens, or permissions needed.
- Environment setup, tools, or installed software.
- Knowledge and concepts required (link to concept pages).
- Content, values, or decisions the user must bring to the procedure.

Include links to related pages where relevant.

## Steps summary (optional)

Only include this section if the tutorial has more than seven steps.
A bulleted list of step titles with anchor links so the user can
get an overview before starting.

## Step 1: [Milestone name]

Narrative and instructions. Tutorials can and should include more
explanation than how-to guides — the goal is learning, not just doing.

## Step 2: [Next milestone]

…

## Related articles (optional)

Use the CardList and Card components as defined in style-guide.md and ProjectConvention.md.
```

### Notes

- Tutorials follow the "happy path" — do not include extensive troubleshooting. A brief note on the most common failure point is acceptable.
- Every step should produce a visible or verifiable result. The user should be able to confirm they are on track.
- Keep the scope tight. If the tutorial is growing beyond 10–12 steps, consider splitting it into two tutorials with a clear handoff.

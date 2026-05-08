# Project Convention

> **How to use this file:** Fill in the platform-specific details for this project before writing begins. If a platform MCP is available (e.g. Mintlify MCP, Fumadocs MCP), note it here — the Writer skill will prefer the MCP over this file when both are available, and use this file as fallback or to resolve conflicts.

---

## Platform

**Documentation framework:** Featurebase

## Components

List the available components for this project. The Writer skill will only use components listed here.

| Component | Usage | Syntax |
|---|---|---|
| [e.g. Callout / Note / Warning] | [When to use it] | [Exact syntax] |
| `CardList` | Wrapper for a group of Card components in the "Related articles" section | `<CardList cols={N}>...</CardList>` — set `cols` to match the number of cards (max 3) |
| `Card` | A single related article card with title, icon, link, and short description | `<Card title="..." icon="..." link="...">Description.</Card>` |

---

## Callout Types

| Type | When to use |
|---|---|
| [e.g. Note] | [e.g. Additional context that is helpful but not critical] |
| [e.g. Warning] | [e.g. Actions that may cause data loss or irreversible changes] |
| [e.g. Tip] | [e.g. Optional shortcuts or best practices] |

---

## File Naming Conventions

**Format:** [e.g. kebab-case]
**Extension:** [e.g. `.mdx` / `.md`]
**Example:** `[example-file-name.mdx]`

---

## Notes

Since Featurebase you can disregard most ocmponents as it is not react based. 

WHENEVER A COMPONENT IS USED ADD A NOTE TO FILE AND WE WILL MANUALLY CONFIgURE It ON THE FEATUREBASE PORTAL.

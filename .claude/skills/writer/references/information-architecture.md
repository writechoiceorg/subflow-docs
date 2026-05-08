> **How to use this file:** Map the full documentation structure for this project before writing begins. The Writer skill will not save a file to a path that is not listed here — if a path is missing, the skill will pause and ask. Update this file as the structure evolves. The skill may add new entries automatically when new pages are scoped during a writing session.

---

## Structure Map

### Overview

Introduces the platform's purpose and core concepts so new users can build a mental model before they open the product for the first time.

| Page title | File path | Page type | Status |
|---|---|---|---|
| What is Subflow? | /docs/overview/what-is-subflow.md | Concept | Pending |
| Key Concepts: Care Plans, Workflows, and Tasks | /docs/overview/key-concepts-care-plans-workflows-and-tasks.md | Concept | Pending |
| The Patient Journey in Subflow | /docs/overview/the-patient-journey-in-subflow.md | Concept | Pending |
| User Roles and Teams | /docs/overview/user-roles-and-teams.md | Concept | Pending |

### Compliance & Security

Explains HIPAA requirements in the context of Subflow so clinical staff know when and why to use the platform's secure messaging features before they start communicating with patients.

| Page title | File path | Page type | Status |
|---|---|---|---|
| HIPAA Compliance in Subflow | /docs/compliance-and-security/hipaa-compliance-in-subflow.md | Concept | Pending |
| When to Use Secure Chat | /docs/compliance-and-security/when-to-use-secure-chat.md | How-to Guide | Pending |

### Get Started

Guides newly onboarded staff through first login and platform orientation so they can begin their daily work immediately without needing a walkthrough from a colleague.

| Page title | File path | Page type | Status |
|---|---|---|---|
| Logging In for the First Time | /docs/get-started/logging-in-for-the-first-time.md | How-to Guide | Pending |
| Navigate the Platform | /docs/get-started/navigate-the-platform.md | How-to Guide | Pending |
| Create a Task | /docs/get-started/create-a-task.md | How-to Guide | Pending |
| Manage Your Tasks | /docs/get-started/manage-your-tasks.md | How-to Guide | Pending |

### Contacts & Segments

Covers patient record management, tagging, and dynamic grouping so clinical staff can keep contact data organized and target the right patients with the right communication at the right time.

| Page title | File path | Page type | Status |
|---|---|---|---|
| Contacts in Subflow | /docs/contacts-and-segments/contacts-in-subflow.md | Concept | Pending |
| Create a Contact | /docs/contacts-and-segments/create-a-contact.md | How-to Guide | Pending |
| Add and Manage Tags | /docs/contacts-and-segments/add-and-manage-tags.md | How-to Guide | Pending |
| Create a Segment | /docs/contacts-and-segments/create-a-segment.md | How-to Guide | Pending |
| Manage Contacts and Segments | /docs/contacts-and-segments/manage-contacts-and-segments.md | How-to Guide | Pending |

### Messaging

Explains how to communicate with patients at scale and in real time using SMS broadcasts, email campaigns, two-way conversations, and reusable message templates — and when to use each channel.

| Page title | File path | Page type | Status |
|---|---|---|---|
| Messaging in Subflow | /docs/messaging/messaging-in-subflow.md | Concept | Pending |
| Create an SMS Broadcast | /docs/messaging/create-an-sms-broadcast.md | How-to Guide | Pending |
| Manage a Broadcast | /docs/messaging/manage-a-broadcast.md | How-to Guide | Pending |
| Create an Email Campaign | /docs/messaging/create-an-email-campaign.md | How-to Guide | Pending |
| Create a Message Template | /docs/messaging/create-a-message-template.md | How-to Guide | Pending |
| Manage Two-Way Conversations | /docs/messaging/manage-two-way-conversations.md | How-to Guide | Pending |
| Use Secure Chat | /docs/messaging/use-secure-chat.md | How-to Guide | Pending |

### Forms

Explains how digital patient questionnaires are built and used in Subflow, so clinical staff can understand the forms patients receive, review their submissions, and identify alarming responses that require follow-up.

| Page title | File path | Page type | Status |
|---|---|---|---|
| Forms in Subflow | /docs/forms/forms-in-subflow.md | Concept | Pending |
| Contact Fields | /docs/forms/contact-fields.md | Reference | Pending |
| Build a Form | /docs/forms/build-a-form.md | How-to Guide | Pending |
| View and Manage Form Submissions | /docs/forms/view-and-manage-form-submissions.md | How-to Guide | Pending |

### Workflows

Explains Subflow's automation engine — how workflows are triggered, what actions they can take, and how to build and manage them — so clinical staff can understand the automation running in the background and, over time, create their own workflows for new use cases.

| Page title | File path | Page type | Status |
|---|---|---|---|
| Workflows in Subflow | /docs/workflows/workflows-in-subflow.md | Concept | Pending |
| Create a Workflow | /docs/workflows/create-a-workflow.md | How-to Guide | Pending |
| Workflow Node Reference | /docs/workflows/workflow-node-reference.md | Reference | Pending |
| Manage Workflows | /docs/workflows/manage-workflows.md | How-to Guide | Pending |

### Care Plans

Explains Subflow's macro-level patient journey visualization so clinical staff can see where each patient stands in their care protocol, understand how workflows attach to stages, and eventually create and manage their own care plans.

| Page title | File path | Page type | Status |
|---|---|---|---|
| Care Plans in Subflow | /docs/care-plans/care-plans-in-subflow.md | Concept | Pending |
| Understand the Care Plan View | /docs/care-plans/understand-the-care-plan-view.md | How-to Guide | Pending |
| Create a Care Plan | /docs/care-plans/create-a-care-plan.md | How-to Guide | Pending |

---

## Naming Conventions

**URL structure:** /docs/[section]/[page-name]
**Folder structure:** mirrors URL structure
**File names:** kebab-case, lowercase, `.md` extension
**Folder names:** kebab-case, lowercase, no special characters (e.g. `contacts-and-segments`)
**Page title:** H1 at the top of each file, matches the title in the Structure Map above
**Page types:** One of — Concept, How-to Guide, Reference
**Category placement:** Each page lives in exactly one category — no cross-listing

---

## Notes

- Order of sections in the Structure Map reflects the intended reading order for a new user — Overview first, Care Plans last.
- "User Roles and Teams" is documented as a forward-looking page; role-based permissions are planned for Q3 2026 and the page should be updated when released.
- "Use Secure Chat" appears under **Messaging** as the how-to for the feature itself; "When to Use Secure Chat" appears under **Compliance & Security** as the policy/decision guidance. These are intentionally separate pages with different scopes — do not merge.
- "Contact Fields" is a Reference page (field-type catalog), distinct from "Build a Form" which is the procedural how-to. Keep field-type details in the Reference and link to it from the how-to rather than duplicating.
- If a proposed new page does not fit any existing section, update this file before writing. Do not create a file at a path that is not listed in the Structure Map.

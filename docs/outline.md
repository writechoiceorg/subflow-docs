# Documentation Outline: Subflow Health

Subflow is a healthcare SaaS platform that helps clinical organizations automate and deliver patient care beyond the clinical visit — through structured workflows, SMS and email messaging, digital forms, and actionable task management. This documentation is written for non-technical clinical staff, including nurses, nurse navigators, and administrative assistants, and is published in **Featurebase** as a single Guides knowledge base.

---

## Tab: Guides

This tab contains all documentation for Subflow: conceptual overviews that explain what the platform is and how it works, how-to guides for specific day-to-day tasks, and reference material for settings and field types.

---

### Overview

Introduces the platform's purpose and core concepts so new users can build a mental model before they open the product for the first time.

* **What is Subflow?** [`Concept`]: Explains how Subflow helps healthcare organizations automate patient care beyond the clinical visit — through workflows, messaging, forms, and actionable data — and what problem it solves for clinical staff.
* **Key Concepts: Care Plans, Workflows, and Tasks** [`Concept`]: Clarifies the relationship between care plans (the macro patient journey map), workflows (the automation sequences that power it), and tasks (the staff actions workflows create), so users understand how the three work together before using any of them.
* **The Patient Journey in Subflow** [`Concept`]: Walks through a patient's progression from initial interest and intake to post-visit follow-up, illustrating how care plans, workflows, forms, messaging, and tasks each support a different stage — and how they hand off to one another automatically.
* **User Roles and Teams** [`Concept`]: Describes the different roles that exist within Subflow, what each role can see and do, and how team assignments control which patients each staff member has access to. *(Role-based permissions are planned for Q3 2026; this page will be updated when released.)*

---

### Compliance & Security

Explains HIPAA requirements in the context of Subflow so clinical staff know when and why to use the platform's secure messaging features before they start communicating with patients.

* **HIPAA Compliance in Subflow** [`Concept`]: Explains what HIPAA compliance means in the context of the platform, which types of patient communication are standard and which require additional protection, and how Subflow's activity log supports audit trails.
* **When to Use Secure Chat** [`How-to Guide`]: Shows how to toggle Secure Chat on during a conversation, explains what changes for the patient (an encrypted web chat link instead of a plain SMS reply), and describes the clinical scenarios — such as sharing lab results or discussing sensitive diagnoses — that require it.

---

### Get Started

Guides newly onboarded staff through first login and platform orientation so they can begin their daily work immediately without needing a walkthrough from a colleague.

* **Logging In for the First Time** [`How-to Guide`]: Step-by-step instructions for accessing Subflow after receiving login credentials from the administrative team, including what to do if the link has expired.
* **Navigate the Platform** [`How-to Guide`]: Explains how to move between Subflow's main applications — Home, My Tasks, and Care Plans — and describes what each area is used for, so new users can orient themselves on their first session.
* **Create a Task** [`How-to Guide`]: Shows how to manually create a task from the My Tasks view, including how to set the title, description, priority, due date, assignee, and benefiting patient.
* **Manage Your Tasks** [`How-to Guide`]: Shows how to view, filter, prioritize, and complete tasks from the My Tasks view, including how to add comments, attach resources such as form submissions, assign subtasks, and update status from Requested through In Progress to Completed.

---

### Contacts & Segments

Covers patient record management, tagging, and dynamic grouping so clinical staff can keep contact data organized and target the right patients with the right communication at the right time.

* **Contacts in Subflow** [`Concept`]: Explains what a contact record contains — personal details, tags, contact fields, form submission history, and the activity log — and how the record updates automatically as a patient moves through a care plan.
* **Create a Contact** [`How-to Guide`]: Step-by-step instructions for creating a new patient contact record and editing an existing one, including which fields are required and where to find them in the platform.
* **Add and Manage Tags** [`How-to Guide`]: Explains how to apply tags to contact records to categorize patients by attributes such as language preference, condition, or care status, and how to remove tags when circumstances change — since removing a tag can automatically move a patient out of a segment.
* **Create a Segment** [`How-to Guide`]: Shows how to build a dynamic patient group by combining tag conditions and form-response criteria, and explains that the segment list updates automatically whenever a contact record changes to meet or stop meeting the defined conditions.
* **Manage Contacts and Segments** [`How-to Guide`]: Covers how to search and filter your contact list, view which segments a contact belongs to, and review or edit segment criteria after creation.

---

### Messaging

Explains how to communicate with patients at scale and in real time using SMS broadcasts, email campaigns, two-way conversations, and reusable message templates — and when to use each channel.

* **Messaging in Subflow** [`Concept`]: Explains the differences between SMS broadcasts (one-to-many, sent to up to three segments), email campaigns (visual email builder, same send-or-schedule model), two-way conversations (patients reply by standard SMS, no portal required), and message templates (reusable text or email content), and describes when each channel is most appropriate.
* **Create an SMS Broadcast** [`How-to Guide`]: Step-by-step guide to creating a broadcast, selecting up to three recipient segments, composing or selecting a templated message with contact-field personalization, and sending immediately or scheduling for a later date.
* **Manage a Broadcast** [`How-to Guide`]: Explains how to cancel a scheduled broadcast before it sends, archive a completed or canceled broadcast to keep the list clean, and restore an archived broadcast to active record when needed.
* **Create an Email Campaign** [`How-to Guide`]: Explains how to use the drag-and-drop email editor to design a campaign, add recipient segments or individual contacts, preview the email, and send or schedule it.
* **Create a Message Template** [`How-to Guide`]: Shows how to create a reusable SMS or email template — including how to name it, add personalization tags, and tag it for searchability — so it can be selected in broadcasts, two-way conversations, and workflow messaging nodes.
* **Manage Two-Way Conversations** [`How-to Guide`]: Explains how patients reply to SMS messages directly from their phone without a portal, how incoming replies appear in the conversation view with automated vs. staff-sent messages clearly distinguished, and how to respond using a template or free-form text.
* **Use Secure Chat** [`How-to Guide`]: Shows how to switch a conversation to Secure Chat mode when discussing sensitive health information, what the patient experiences when they receive a secure link instead of a plain SMS, and how to toggle back to standard SMS when the secure exchange is complete.

---

### Forms

Explains how digital patient questionnaires are built and used in Subflow, so clinical staff can understand the forms patients receive, review their submissions, and identify alarming responses that require follow-up.

* **Forms in Subflow** [`Concept`]: Explains what forms are, how they are built from contact fields, how they are sent to patients via SMS link (no patient portal needed), and how submitted answers update contact records, feed into segments, and trigger workflow paths.
* **Contact Fields** [`Reference`]: Lists all available contact field types — single-line text, multi-line text, email, dropdown, multiple-checkbox, and yes/no — and describes the options for each type, including character limits, number validation, alarming answer highlighting, and required-field rules.
* **Build a Form** [`How-to Guide`]: Step-by-step walkthrough of creating a new form: naming it, adding and reordering contact fields from the field library, organizing questions into multi-step pages, setting required fields and validation rules, and configuring conditional (hidden) fields that appear only when a controlling question is answered a certain way.
* **View and Manage Form Submissions** [`How-to Guide`]: Shows how to open the submissions view for any form, read individual responses (including answers highlighted in red for alarming values), and understand how submitted data flows back into contact records and segments.

---

### Workflows

Explains Subflow's automation engine — how workflows are triggered, what actions they can take, and how to build and manage them — so clinical staff can understand the automation running in the background and, over time, create their own workflows for new use cases.

* **Workflows in Subflow** [`Concept`]: Explains what a workflow is, how it is triggered (manually, by form submission, by task completion, or by EHR API events), and the range of actions it can take — sending messages, waiting for form responses, splitting on conditions, and creating tasks — so users understand what is happening automatically behind the scenes.
* **Create a Workflow** [`How-to Guide`]: Step-by-step guide to building a new workflow from scratch: choosing a trigger event, adding action nodes, configuring a path split that branches on form answers or segment membership, and setting wait conditions before activating the workflow.
* **Workflow Node Reference** [`Reference`]: Describes every available workflow node type — Trigger, Send Message, Wait for Event, Wait for Time, Path Split, Create Task, and Add/Remove Tag — with the configuration options for each, so staff can look up exactly what a node does when reading or editing a workflow.
* **Manage Workflows** [`How-to Guide`]: Covers how to view active and inactive workflows, edit a workflow that is already running, pause or deactivate a workflow without deleting it, and search and filter the workflow list.

---

### Care Plans

Explains Subflow's macro-level patient journey visualization so clinical staff can see where each patient stands in their care protocol, understand how workflows attach to stages, and eventually create and manage their own care plans.

* **Care Plans in Subflow** [`Concept`]: Explains what a care plan is — a digitized clinical protocol showing the stages and milestones a patient must move through — and how it differs from a workflow: the care plan is the visualization and reporting layer, while workflows automate the actions that move patients through it.
* **Understand the Care Plan View** [`How-to Guide`]: Walks through the care plan interface: how to read which stage each patient is in, what the milestone statuses mean, and how to manually move a patient to the next stage when a human review is required before the workflow can continue.
* **Create a Care Plan** [`How-to Guide`]: Step-by-step instructions for setting up a new care plan — defining its stages and milestones, attaching workflows to specific points in the journey, and enrolling contacts so their progress is tracked from the start.

---

## User Navigation Flow

This flow is designed for a newly hired nurse navigator who has just received their Subflow login credentials and needs to complete their first workflow-generated task on their first day using the platform.

1. **Featurebase Homepage** → The user lands on the Subflow knowledge base and sees a list of collections organized from Overview through Care Plans. They recognize "Get Started" as the right place for a first-time user and click through.
2. **What is Subflow?** → The user reads a brief explanation of how Subflow automates patient care beyond the clinical visit. They understand why the platform exists and what role it plays alongside their EHR.
3. **Key Concepts: Care Plans, Workflows, and Tasks** → The user learns that tasks are automatically created by workflows responding to patient events — so when they see a task in their queue, it was placed there by the system based on a patient's care journey, not manually assigned by a colleague.
4. **Logging In for the First Time** → Following the numbered steps, the user opens the login link from their welcome email, creates a password, and reaches the Home dashboard for the first time.
5. **Navigate the Platform** → The user reads how to move between Home, My Tasks, and Care Plans, and understands that My Tasks is where their daily work lives.
6. **Manage Your Tasks** → The user opens My Tasks, finds a workflow-created task assigned to them, clicks into it, reads the patient's attached form submission, adds a comment noting what they found, and marks the task Completed.
7. **First win** → The user successfully completes their first workflow-generated task: they reviewed a patient's form response flagged as alarming, left a comment for their team, and marked the task Completed — which triggers the next step in the patient's workflow automatically.

# Workflows in Subflow

A workflow is a sequence of automated steps that you can configure in Subflow to run when a specific event occurs. Instead of sending follow-up messages manually after every form submission or creating tasks one by one, you configure a workflow once and let it run in the background.

Workflows are built in a visual canvas builder. Most are set up during onboarding, and you can create or adjust them over time as your care programs evolve.

## What a workflow can do

Each step in a workflow is called a workflow node, and nodes can perform different tasks depending on the workflow's needs.

A workflow can send an SMS message or email to a contact at any point in the automation, either by composing the message directly or by using a saved message template. It can pause and wait: either for a set amount of time before continuing (a **Wait Until** node) or until a specific event occurs, such as a contact submitting a form (a **Wait For Event** node). When a contact submits the form and the workflow is waiting for that response, the workflow takes the "On Event" path and continues; if the time runs out before the form is submitted, it takes the "On Timeout" path instead, which can lead to a different set of follow-up actions.

Workflows can also branch into different tracks. A **Paths** node splits the workflow based on conditions you define, so patients in different situations move down different paths and receive the appropriate follow-up. Along the way, a workflow can create and assign a task to a staff member when a human response is needed, and it can add or remove a tag on a contact's record to reflect a change in their status. When the workflow has finished what it needs to do, an **Exit Workflow** node ends the run for that contact.

## How a workflow is triggered

Every workflow begins with a trigger event: the event that tells Subflow to start running the workflow for a specific contact. When you set up a workflow, you choose which event should start it.

The table below shows the available trigger event types.

| Category | Trigger event | What it means |
|---|---|---|
| Manual | Manual | A staff member manually starts the workflow for a specific contact |
| Audience | Contacts: Created | A new contact record is created |
| Audience | Contacts: Updated | A contact record is updated |
| Audience | Contacts: Added to Segment | A contact is added to a segment |
| Audience | Contacts: Removed from Segment | A contact is removed from a segment |
| Audience | Form: New Submission | A contact submits a form |
| Audience | Form Request: Completed | A form request sent to a contact is completed |
| Commerce | Subscription: Created | A new subscription is created |
| Default | E-Sign: Document Completed | A document is signed by the contact |
| Default | E-Sign: Document signed by Party | A specific party signs a document |
| Task | Task: Completed | A task assigned to a staff member is completed |
| Care Plan | Care Plan: Created | A contact is enrolled in a care plan |
| Care Plan | Care Plan: Task Completed | A task within a care plan is completed |
| Care Plan | Care Plan: All Phase Tasks Completed | All tasks in a care plan phase are completed |
| Care Plan | Care Plan: Phase Status Changed | A care plan phase changes business status |

Additional trigger event types may be available in your account. The list above covers the most common ones for clinical use.

## Workflows and care plans

A care plan and a workflow are different things that work together. The care plan is the visualization layer: it shows where each patient stands in a clinical protocol, with stages and milestones that map out the steps of their journey. The workflow is the automation engine underneath: it is what actually sends messages, creates tasks, and moves patients forward through each stage.

Multiple workflows can attach to a single care plan, and one workflow can serve multiple care plans when the automation logic is general enough to apply across programs. A satisfaction survey workflow, for example, can be shared across several care plans without being rebuilt for each one.

## A workflow in practice

The nodes described above work together to automate clinical processes from end to end. The following example shows what a pre-admission workflow might look like. A patient submits their pre-admission form, and from that point on, the workflow handles every step automatically, with no staff action required until a clinical review is needed.

- **Trigger (Form: New Submission):** The workflow starts the moment the patient submits the pre-admission form. This is the event that sets the rest of the automation in motion.
- **Send Message:** Subflow sends the patient a confirmation SMS to acknowledge receipt of their form and let them know what to expect next.
- **Wait For Event:** The workflow pauses and waits for the patient to complete a follow-up questionnaire, up to a set time limit. Two outcomes are possible:
  - If the patient submits the questionnaire in time (On Event), the workflow continues down the main path.
  - If the time limit passes without a submission (On Timeout), the workflow takes a separate path and sends the patient a reminder message.
- **Assign Task:** Once the questionnaire is received, the workflow creates a task and assigns it to the care team to review the patient's answers before the appointment.
- **Add Resource to Task:** The submitted questionnaire is attached directly to the task, so the assigned staff member can open the patient's answers without searching elsewhere.
- **Exit Workflow:** The run ends for this contact. The care team's task remains open until someone reviews and completes it.

## Related articles

Now that you understand what workflows are and how they fit into the platform, check these related articles to start building and managing your own.

- **Create a Workflow:** Follow a step-by-step walkthrough to build a new workflow from scratch, from choosing a trigger event to saving and activating it.
- **Workflow Node Reference:** Look up what each workflow node type does and what options are available when configuring it.
- **Key Concepts: Care Plans, Workflows, and Tasks:** Understand how care plans, workflows, and tasks connect to each other and what role each plays in a patient's journey through Subflow.

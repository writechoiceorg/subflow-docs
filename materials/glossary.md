# Glossary

> Internal terminology reference for the Subflow Health documentation project. Use preferred terms in all documentation — especially for UI element names, which must match the product exactly.  
> Last updated: 2026-05-05



## Quick Reference

| Preferred Term | Avoid | Category | Defined? |
|||||
| Activity Log | audit log, activity history | platform, compliance | ✅ |
| Alarming Answer | concerning response, flagged answer, red answer | forms, workflow | ✅ |
| Application | module, feature, app, section | navigation, platform | ✅ |
| Care Plan | plan, protocol, flow (as platform term) | care-plans | ✅ |
| Contact | patient (as platform record term) | contacts | ✅ |
| Contact Field | field, form field, question | contacts, forms | ✅ |
| Dashboard | — | navigation | ✅ |
| EHR | EMR (in most contexts) | integration | ✅ |
| Email Campaign | email broadcast | messaging | ✅ |
| Form | questionnaire, survey (as platform object name) | forms | ✅ |
| HIPAA | — | compliance | ✅ |
| Message Template | template, pre-saved message | messaging | ✅ |
| Milestone | checkpoint | care-plans | ⬜ |
| My Tasks | task list, tasks view | navigation | ✅ |
| Path Split | branch, conditional path, split | workflow | ✅ |
| Patient Tasks | — | future, care-plans | ✅ |
| Referral Coordination | — | future | ✅ |
| Resource | attachment, document (as task object) | tasks | ✅ |
| Sandbox | test account | platform | ✅ |
| Secure Chat | secure messaging, encrypted messaging, HIPAA chat | messaging, compliance | ✅ |
| Segment | group, list, dynamic list, grouping | contacts | ✅ |
| SMS Broadcast | SMS campaign, message blast, bulk text | messaging | ✅ |
| Stage | phase, step (in care plan context) | care-plans | ⬜ |
| Subtask | sub-task | tasks | ✅ |
| Tag | label | contacts | ✅ |
| Task | action item, to-do | tasks | ✅ |
| Teams | — | roles, compliance | ✅ |
| Trigger Event | trigger, event (too generic) | workflow | ✅ |
| Two-Way Conversation | chat, two-way texting | messaging | ✅ |
| User Roles | — | roles, future | ✅ |
| Workflow | flow, automation flow | workflow | ✅ |
| Workflow Node | step, action (in workflow context) | workflow | ✅ |

### Care Plan

- **Definition**: The macro-level visualization of a patient's full care journey, built from defined stages and milestones. It is the reporting and visualization layer that shows where each patient stands in a clinical protocol. Workflows run in and out of a care plan to automate actions at each stage. Care Plans are still in active development as of 2026-05.

- **Avoid**: plan, protocol (as a platform term), flow (as a platform term)

- **Usage Notes**: Multiple workflows can attach to one care plan; one workflow can also serve multiple care plans. The core distinction is that the care plan is the visualization layer while the workflow is the automation engine. Do not document or screenshot unfinished Care Plans UI without confirming with Audra first.



### Milestone

- **Definition**: _(to be defined)_

- **Avoid**: checkpoint

- **Usage Notes**: ⚠️ Discuss: "Stages" and "milestones" are both referenced in CLAUDE.md and the outline but their precise hierarchy in the UI has not been confirmed. Confirm the stage/milestone relationship with Audra before writing Care Plans content.



### Stage

- **Definition**: _(to be defined)_

- **Avoid**: phase, step (in care plan context)

- **Usage Notes**: ⚠️ Discuss: A stage appears to be a high-level phase within a care plan (e.g., Interest, Intake, Program Delivery). Confirm the stage/milestone hierarchy with Audra before writing Care Plans content.

### HIPAA

- **Definition**: Health Insurance Portability and Accountability Act. The U.S. federal law governing the privacy and security of patient health information. In Subflow, HIPAA requirements determine when Secure Chat must be used instead of standard SMS and how Teams restrict patient record access.

- **Avoid**: —

- **Usage Notes**: Always write as "HIPAA" (all caps). Spell out "Health Insurance Portability and Accountability Act" on first use in a document. The activity log supports HIPAA audit trails by recording who accessed which records.



### Secure Chat

- **Definition**: A HIPAA-compliant messaging mode that staff toggle on within a conversation when discussing sensitive health information such as lab results or diagnoses. Routes messages through an encrypted web experience — the patient receives an SMS link to a secure web page instead of a plain text reply. Staff see the exchange in the same conversation view; the only change on their end is a toggle.

- **Avoid**: secure messaging, encrypted messaging, HIPAA chat

- **Usage Notes**: Standard SMS is acceptable for non-sensitive content (form links, appointment reminders). Secure Chat is required when sending or discussing protected health information. See the Compliance & Security section of the documentation for detailed guidance on when to use each mode.

### Contact

- **Definition**: A patient or staff member record stored in Subflow. Contains personal details, tags, contact field values, form submission history, and the activity log. The platform object is called a "contact" — "patient" is acceptable in clinical prose but should not be used when referring to the platform record itself.

- **Avoid**: patient (when referring to the platform record object)

- **Usage Notes**: Staff members are also stored as contacts. The distinction between patient contacts and staff contacts matters for HIPAA team assignments, which control who can see which records.

### Contact Field

- **Definition**: A custom data field created by Subflow during client onboarding to store a specific piece of patient information. Field types include single-line text, multi-line text, email, dropdown, multiple-checkbox, and yes/no. Contact fields are the building blocks of forms — a form is assembled by selecting fields from a shared library.

- **Avoid**: field, form field, question (when referring specifically to the Contact Field object)

- **Usage Notes**: A contact field belongs to the contact record, not to a specific form — the same field can appear on multiple forms. Answers can be marked as "alarming" at the field level. If a field is updated after being added to a form, it must be removed and re-added for the update to take effect. Templated FHIR-standard fields are planned for a future release; currently all fields are created manually by Subflow.



### Segment

- **Definition**: A dynamic list of contacts that updates automatically whenever a contact record changes to meet or stop meeting defined conditions. Conditions are based on tags, contact field values, or form responses, combined with AND/OR logic. Used as recipient lists for SMS broadcasts and as conditions in workflow path splits.

- **Avoid**: group, list, dynamic list, grouping

- **Usage Notes**: A segment cannot be manually populated — contacts enter and exit when their record conditions change. To remove a contact from a segment, change the contact record condition that qualified them (e.g., reset a field value or remove a tag) rather than editing the segment itself. A broadcast requires at least one segment (up to three).

### Tag

- **Definition**: A label applied to a contact record to categorize a patient by attributes such as language preference, condition, or care status. Tags are the primary building blocks of segment conditions — adding or removing a tag from a contact can automatically move them in or out of segments.

- **Avoid**: label

- **Usage Notes**: Tags can be added manually on the contact record or added/removed automatically by a workflow action. Removing a tag may trigger segment exits and downstream workflow changes.

### Alarming Answer

- **Definition**: A form response option marked during contact field setup as requiring clinical attention. Displayed in red on the form submission view. Workflow path splits can listen for alarming answers to route patients down escalation paths automatically.

- **Avoid**: concerning response, flagged answer, red answer

- **Usage Notes**: "Alarming" is the term used in the product and consistently by Audra. The flag is set at the contact field level. If a field is updated after being added to a form, it must be removed and re-added to the form for the alarming setting to take effect — a known UI limitation flagged for a future fix.

### Form

- **Definition**: A digital questionnaire built from contact fields and delivered to patients via SMS link. Forms can be multi-step, include required fields, validation rules (character limits, number-only), and conditional fields that appear based on a controlling question's answer. No patient portal or app is required — the patient opens a link from their text message. Submitted answers update the contact record and can trigger workflow paths.

- **Avoid**: questionnaire, survey (when referring to the Form object in the platform)

- **Usage Notes**: "Questionnaire" and "survey" are acceptable in clinical prose to describe what a form does, but the platform object is called a Form. Conditional (hidden) field visibility is currently limited to one controlling field per hidden field. Forms can be set to public (anyone with the link) or private (sent contact only).

### EHR

- **Definition**: Electronic Health Record. The clinical system of record used by healthcare organizations for full clinical documentation. Subflow integrates with EHRs via API to receive trigger events such as appointment scheduled or surgery date, but does not replace the EHR as the legal system of record.

- **Avoid**: EMR (use EHR unless a specific system uses the EMR designation)

- **Usage Notes**: Abbreviated as EHR. Spell out "Electronic Health Record" on first use in a document. EHR integration is managed by Subflow's technical team — end users do not configure integrations. API documentation for EHR integrations is a future deliverable (contact: Will).

### Email Campaign

- **Definition**: A one-to-many email message built using the drag-and-drop email editor and sent to a segment or individual contact. Can be sent immediately or scheduled for a future date. Displays the rendered email in the campaign record after sending.

- **Avoid**: email broadcast

- **Usage Notes**: Email campaigns use a visual editor; SMS broadcasts use plain text composition. Both support message templates and the send-or-schedule model. Distinct from two-way conversations, which are ad hoc direct exchanges.



### Message Template

- **Definition**: A saved SMS or email template reusable across workflows, two-way conversations, and broadcasts. Supports personalization tags (contact field values inserted dynamically) and can be tagged for searchability. Templates can be selected and edited before sending.

- **Avoid**: template, pre-saved message, pre-built template

- **Usage Notes**: Message templates can be SMS or email type. In workflows, a template can be referenced in a Send Message node. In two-way conversations, staff can select a template and edit it before sending. Templates should be named clearly for search discoverability.



### SMS Broadcast

- **Definition**: A one-to-many SMS message sent to up to three segments simultaneously. Must be created manually — workflows cannot trigger broadcast creation. Can be sent immediately or scheduled for a future date and time. Requires at least one segment before creation. Once sent or scheduled, a broadcast cannot be edited.

- **Avoid**: SMS campaign, message blast, bulk text

- **Usage Notes**: "Broadcast" alone is acceptable shorthand in context. Broadcasts send individual messages to each contact — not a group text. Archived broadcasts are removed from the primary list view but remain in the system record and can be restored. Whether a scheduled broadcast targets segment membership at scheduling time or at send time is unconfirmed — flag this in documentation until verified with Audra.



### Two-Way Conversation

- **Definition**: The direct SMS exchange between a staff member and a patient. Patients reply to platform-sent messages directly from their phone without accessing a portal or app. Incoming replies appear in the conversation view with automated (workflow) messages and staff-sent messages clearly distinguished.

- **Avoid**: chat (reserved for Secure Chat), two-way texting (informal)

- **Usage Notes**: Audra uses "two-way texting" informally; the documentation term is "Two-Way Conversation." Staff can reply using a message template or free-form text. The conversation view shows the full message history for a contact. Toggle Secure Chat on within a conversation when discussing sensitive health information.

### Application

- **Definition**: One of the top-level navigation sections of the Subflow platform, accessible from the main sidebar. Current applications include Contacts, Messaging, Forms, Workflows, and Care Plans. Each application groups related features.

- **Avoid**: module, feature, app, section

- **Usage Notes**: ⚠️ Audra confirmed "applications" as the preferred term in meeting 3 (2026-04-24) but noted she would verify with Mitch. Use "application" until told otherwise. "Module" was explicitly rejected by Audra in the second meeting.



### Dashboard

- **Definition**: The Home screen that users see when they first log into Subflow. Displays a summary view of platform activity. Currently being revamped to support additional customizable reports.

- **Avoid**: —

- **Usage Notes**: "Home" is the navigation label for this screen; "Dashboard" is the common informal name. Use "Home" when referring to the navigation item. "Dashboard" is acceptable in conceptual descriptions.



### My Tasks

- **Definition**: The primary navigation area where staff view, manage, filter, and complete tasks assigned to them. The main daily working view for most clinical staff.

- **Avoid**: task list, tasks view

- **Usage Notes**: "My Tasks" is the exact UI label — match capitalization in all documentation.

### Activity Log

- **Definition**: The record of all actions and events associated with a contact, including form submissions, messages sent, workflow steps executed, staff views, and task activity. Accessible from the contact record. Used for reporting and HIPAA audit trails.

- **Avoid**: audit log, activity history

- **Usage Notes**: The activity log captures both automated actions (workflow steps) and manual staff actions. It can surface who accessed a record if a HIPAA compliance issue is investigated. Will serve as training data for planned AI insights features.



### Sandbox

- **Definition**: The Subflow account environment that the WriteChoice team uses for documentation purposes. Distinct from the support account (which Audra uses) and from production client accounts. All example content created by Audra for documentation reference must be placed in the sandbox.

- **Avoid**: test account

- **Usage Notes**: WriteChoice has access to the sandbox only — not the support account. Some sandbox behaviors (e.g., search indexing) may differ from production. Always verify you are in the sandbox before taking screenshots.


### Teams

- **Definition**: The current grouping mechanism that controls which staff members can see which patient contacts. A HIPAA compliance measure ensuring staff only access records relevant to their care team. Serves as the interim access-control system until role-based permissions (User Roles) are released.

- **Avoid**: —

- **Usage Notes**: Teams will be partially superseded by the User Roles feature planned for Q3 2026. Current documentation should explain Teams as the mechanism in place today.



### User Roles

- **Definition**: A planned role-based permissions system (Q3 2026) that will define what different staff types can see and do in Subflow. Will allow administrators to see everything while front-desk users see only their own tasks. Currently, Teams serve a similar access-control function.

- **Avoid**: —

- **Usage Notes**: Do not document User Roles until the feature is released. Acknowledge its future existence in the User Roles concept page but mark it clearly as upcoming.



## tasks

### Resource

- **Definition**: A file, link, or form submission attached to a task to give the assigned staff member the context needed to complete it. Can be attached automatically by the workflow that created the task, or manually added by a staff member viewing the task.

- **Avoid**: attachment, document (when referring to the Resource object specifically)

- **Usage Notes**: A resource is typically a submitted form that flagged an alarming answer — e.g., the workflow creates a task and attaches the form submission so the nurse can see what was answered before calling the patient.



### Subtask

- **Definition**: A smaller action item nested within a parent task, assigned to a specific staff member. Subtasks are visible within the parent task view and allow work to be delegated to a colleague as part of completing a larger task.

- **Avoid**: sub-task (no hyphen)

- **Usage Notes**: Subtasks can be added manually within a task view or pre-configured in the workflow that creates the parent task. Currently there is no automatic notification when a subtask is assigned — the assignee must check their dashboard.



### Task

- **Definition**: An action item assigned to a staff member, typically created automatically by a workflow in response to a patient event such as an alarming form answer. Has three statuses: Requested, In Progress, and Completed. Completing a task can trigger further workflow steps. Includes a title, description, due date, priority, assignee, benefiting patient, and optional resources and subtasks.

- **Avoid**: action item, to-do

- **Usage Notes**: Tasks can also be created manually from My Tasks. Status progression is always Requested → In Progress → Completed. Distinct from Patient Tasks, which is a future feature for tracking patient-facing action items.

### Path Split

- **Definition**: A workflow node that branches the workflow into multiple paths based on defined conditions. Conditions can be form answers (specific question and value), segment membership, or contact field values, combined with AND/OR logic. Each path leads to different subsequent workflow actions. An "otherwise" fallback path handles contacts that match no defined condition.

- **Avoid**: branch, conditional path, split

- **Usage Notes**: A path split can branch into more than two paths. Multiple conditions on the same path use AND/OR logic. Used to send patients down different automation tracks based on their responses — e.g., a pain score above 8 goes down an escalation path while lower scores continue normally.



### Trigger Event

- **Definition**: The event that initiates a workflow. Types include: manual (staff-initiated), form submission, task completion, segment entry/exit, and EHR API events such as appointment scheduled or surgery date. A workflow begins executing its nodes when its trigger event fires for a specific contact.

- **Avoid**: trigger, event (too generic in workflow context)

- **Usage Notes**: Each workflow has one trigger event. EHR-based triggers require an active integration. For the sandbox, manual triggers are most commonly used for testing.



### Workflow

- **Definition**: The automation engine that powers care plans and drives patient engagement. Triggered by an event, a workflow can send messages, wait for form responses or time delays, split into conditional paths, create tasks, and add or remove tags. Multiple workflows can attach to one care plan; one workflow can serve multiple care plans.

- **Avoid**: flow, automation flow

- **Usage Notes**: Workflows are the core automation mechanism of Subflow. The care plan is the visualization/reporting layer; the workflow is the automation engine running within it. Avoid "flow" as shorthand — it creates confusion with "patient flow" or "care flow."



### Workflow Node

- **Definition**: A single step or action block within a workflow. Node types include: Trigger, Send Message, Wait for Event, Wait for Time, Path Split, Create Task, and Add/Remove Tag. Nodes are connected in sequence to define the full automation logic.

- **Avoid**: step, action (too generic in workflow context)

- **Usage Notes**: "Node" is used in the platform UI and by Audra in transcripts. When documenting workflows, refer to individual steps as "nodes" or by their specific type name (e.g., "Send Message node," "Path Split node").

### Patient Tasks

- **Definition**: A planned feature (not yet in production) that will display a list of patient-facing action items — such as forms to complete — accessible by the patient within the care plan experience. Will allow staff to see which patient-side actions are complete or pending.

- **Avoid**: —

- **Usage Notes**: Patient Tasks is currently scaffolded in the platform UI but not active in production. Do not document it or include it in screenshots. If a sandbox screenshot shows the Patient Tasks area, obscure it or use a screenshot from a clean account.

### Referral Coordination

- **Definition**: A planned future feature for securely sharing patient records across multiple providers (e.g., primary care to specialist to physical therapist). Will enable pre-filled forms across providers and shared contact records across organizations. Currently on the roadmap but not yet in development.

- **Avoid**: —

- **Usage Notes**: Do not document Referral Coordination. Current referral workflows are handled via forms that collect "who referred you and from where." If asked, note it as a future capability only.

# Workflow Node Reference

This page describes every workflow node type, what it does, and what you can configure when it is selected in the Workflow Builder. Use it as a lookup reference when reading, editing, or building a workflow.

## Flow control nodes

Flow control nodes manage the timing and direction of a workflow run. They determine when the workflow pauses, which path it follows, and when it ends.

The flow control node types are:

- [Trigger](#trigger)
- [Wait Until](#wait-until)
- [Wait For Event](#wait-for-event)
- [Paths](#paths)
- [Exit Workflow](#exit-workflow)

### Trigger

The Trigger node is the first node in every workflow. It defines the event that starts the workflow run for a specific contact. Every workflow has exactly one Trigger node and it cannot be removed.

**Trigger Event dropdown options:**

| Category | Trigger event | Description |
|---|---|---|
| Manual | Manual | A staff member manually starts the workflow for a specific contact. No additional configuration is required. |
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

Additional trigger event types may be available in your account. Use the "Search events..." bar in the dropdown to find a specific event by name.

### Wait Until

The Wait Until node pauses the workflow run for a set amount of time before continuing to the next node. Use it when you want the workflow to wait a fixed period, such as sending a follow-up message 24 hours after the first.

[Note: Need confirmation on the Wait Until configuration panel — specifically whether duration is entered as a number of hours/days or as a specific date and time.]

### Wait For Event

The Wait For Event node pauses the workflow run and waits for a specific event to occur. It has two outputs:

- **On Event:** the workflow takes this path when the event fires within the configured time window.
- **On Timeout:** the workflow takes this path when the time window expires before the event occurs.

Both the On Event path and the On Timeout path must continue to at least one more node or an Exit Workflow node.

[Note: Need confirmation on the Wait For Event configuration panel — specifically which events can be waited for and how the timeout duration is set.]

### Paths

The Paths node splits the workflow into two or more branches based on conditions you define. Each branch leads to a different set of subsequent nodes, so the workflow can take different actions for different contacts.

[Note: Need confirmation on the Paths configuration panel — specifically how conditions are defined (form answers, segment membership, contact field values), how AND/OR logic between conditions works, and whether an "otherwise" fallback path exists for contacts that do not match any defined condition.]

### Exit Workflow

The Exit Workflow node ends the current workflow run for the contact. No configuration is required. Every path in a workflow should end with an Exit Workflow node so that runs close cleanly.

---

## Action nodes

Action nodes perform the work of the workflow: sending messages, assigning tasks, updating contact records, and more. A workflow can contain any number of action nodes in any order.

The action node types covered in this section are:

- [Send Message](#send-message)
- [Send Email](#send-email)
- [Assign Task](#assign-task)
- [Add Resource to Task](#add-resource-to-task)
- [Add Tag](#add-tag)
- [Remove Tag](#remove-tag)
- [Create Form Request](#create-form-request)

### Send Message

The Send Message node sends an SMS message to the contact in the workflow.

**Configuration options:**

| Setting | Description |
|---|---|
| Recipient | The contact to send the message to. Defaults to "Workflow contact" (the contact the workflow is currently running for). |
| Message | The SMS content. Type a message directly, insert a saved message template using the template toolbar button, add contact data using the personalization `{}` toolbar button, or attach a file, form, or link using the attach toolbar button. Maximum 1,530 characters. |

After configuring the node, click **Apply Changes** in the configuration panel to save the settings before saving the canvas.

### Send Email

The Send Email node sends an email to the contact in the workflow.

[Note: Need confirmation on the Send Email configuration panel — specifically whether it uses a plain text composer or the drag-and-drop email builder, and what fields are available (subject, recipient, body, template).]

### Assign Task

The Assign Task node creates a new task and assigns it to a staff member. Use this node when a step in the workflow requires a human response, such as reviewing an alarming form answer or following up with a patient by phone.

[Note: Need confirmation on the Assign Task configuration panel — specifically which fields are available (title, description, due date, priority, assignee, subtasks, resources).]

### Add Resource to Task

The Add Resource to Task node attaches a resource to a task that was created earlier in the same workflow run. The assigned staff member can then open the task and see the attached resource before taking action.

[Note: Need confirmation on the Add Resource to Task configuration panel — specifically what resource types can be attached and how a task from earlier in the run is referenced.]

### Add Tag

The Add Tag node adds one or more tags to the contact's record. Adding a tag can automatically move the contact into any segment that uses that tag as a condition, which may in turn trigger other workflows.

[Note: Need confirmation on the Add Tag configuration panel — specifically whether tags are selected from a list or typed in, and whether multiple tags can be added in one node.]

### Remove Tag

The Remove Tag node removes one or more tags from the contact's record. Removing a tag can automatically remove the contact from any segment that uses that tag as a condition.

[Note: Need confirmation on the Remove Tag configuration panel.]

### Create Form Request

The Create Form Request node creates a form request for the contact to complete. The contact typically receives the form link via SMS.

[Note: Need confirmation on the Create Form Request configuration panel — specifically which fields are available (which form to send, accompanying message, expiry date, etc.).]

---

## Additional nodes

The workflow builder includes more node types for advanced use cases. These cover updating contact details, managing team assignments, handling care plan enrollment and phase status, working with e-signature documents, and querying contact records. They are visible in the action picker when building a workflow. Contact your Subflow account team for guidance on using them.

## Related articles

Now that you have the full node reference, check these related articles to put it into practice.

- **Create a Workflow:** Step-by-step instructions for building a new workflow from scratch, from selecting a trigger event to activating the workflow.
- **Workflows in Subflow:** Concept overview explaining what workflows are, how they are triggered, and how they relate to care plans.
- **Manage Workflows:** How to view, edit, enable, disable, and archive workflows from the Active Workflows list.

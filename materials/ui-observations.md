# UI Observations

A running log of UI details confirmed from sandbox screenshots. Use this file to resolve flags in draft articles before publishing.

---

## Messaging > Conversations inbox

**Screenshot date:** 2026-05-11  
**Source:** Sandbox account, logged in as Evangelina Sorello / Sandbox Health

### Left sidebar structure

Under the **Messaging** app, the sidebar is divided into four groups:

**Conversations**
- Inbox (shows unread badge count — screenshot shows 5)
- Unread
- Scheduled
- Favorites
- Snoozed
- Archived (shows total count badge — screenshot shows 25)

**Campaigns**
- SMS Broadcasts
- E-mail Campaigns
- Message Templates
- E-mail Templates

**Analytics**
- Message Delivery

**Shortcuts**
- Pinned contacts appear here (shown: Jane Doe with a gold star icon)

**Bottom bar**
- Notifications (bell icon)
- Current workspace and logged-in user (shown: Sandbox Health / Evangelina Sorello)

---

### Conversations list (center panel)

- Header label: **Conversations** with a star icon (purpose unconfirmed — may allow favoriting the view)
- Search bar placeholder text: "Search conversations..."
- Filter icon (funnel) to the right of the search bar

**Conversation card layout** (confirmed from screenshot):
- Circular avatar showing the contact's **two-letter initials**
- **Contact name** (first and last)
- **Date** of last activity in MM/DD/YY format, aligned to the right
- **Message preview** (truncated with ellipsis), preceded by a small icon (icon type unconfirmed — may indicate message type, e.g. automated vs. staff-sent)

Contacts visible in screenshot: Jane Doe, Taylor Wallace, Joshua Miller, Audra Wallace, Mitch Lawson.

**Unread indicator:** A badge count appears on the **Inbox** sidebar item (not on individual cards in this screenshot). Whether individual cards also show a blue dot for unread messages is not confirmed from this screenshot — verify with a screenshot showing an unread conversation.

**End-of-list message:** "You've reached the end of the conversations list." appears below the last card.

---

**Selected conversation card:** The active card is highlighted with a solid blue/purple background and white text.

---

### Right panel — empty state

When no conversation is selected:
- Heading: **No conversation selected** (displayed in purple)
- Subtext: "Select a conversation to view messages."

---

## Messaging > Open conversation thread

**Screenshot date:** 2026-05-11  
**Source:** Sandbox account — Taylor Wallace conversation open

### Top action toolbar

A row of icon-only buttons appears above the thread (exact labels not shown, icons only):
- Flag/assign icon
- Inbox/outbox arrow icon
- Archive/trash icon
- Clipboard/notes icon
- Media/photo icon
- Play button icon
- Right side: green dot + **Participants** label (button)

### Thread view — message types

**Automated messages:**
- Labeled **"Automated Message"** in teal, with a bot/robot icon to the left
- Timestamp shown to the right (e.g. "Last Wednesday at 12:38 PM")
- Double checkmark icon after timestamp (delivery confirmation)
- Link cards render inline when a message contains a URL (shows site title, URL, and favicon)

### Reply area

**Toolbar (above the text input):**
- Two circular arrow buttons on the far left (undo / redo)
- **Templates** button (grid icon)
- **Personalize** button (`()` icon)
- **Attach** button (paperclip icon)

**Text input:**
- Open text field (no "Reply to [name]" label visible)
- Character counter bottom-left: format is `[count]/1530` — confirmed 1530 character limit

**Send button:**
- **Send SMS** button, blue, bottom-right, with a send/arrow icon
- A dropdown arrow sits next to the Send SMS button — confirmed as a **scheduled send** feature. Opens a menu with three options:
  - Tomorrow at 9:00 AM
  - Monday at 9:00 AM
  - Custom time

---

## Still unconfirmed (needs additional screenshots)

- Blue unread indicator on individual conversation cards
- Secure Chat toggle location and appearance
- Secure Chat toggle location and appearance (separate from blue unread indicator)

---

## Automation > Workflows

**Screenshot date:** 2026-05-12
**Source:** Sandbox account, logged in as Evangelina Sorello / Sandbox Health

### Application name and sidebar

The top-level application is **Automation** (not Workflows). Under Automation, the sidebar shows:

**Workflows**
- Active Workflows
- Workflow Builder
- Run History

**Analytics**
- Activity

**Shortcuts**
- Pinned contacts (shown: Jane Doe with gold star)

### Active Workflows list view

- Page heading: **Workflows** / subtitle: "All Workflows"
- Top-right button: **Create Workflow**
- Tabs: **Search** (with count badge) | **Archived**
- Controls: filter icon (funnel), search text input, **Search** button, **Columns** button (top-right)
- Table columns: **Name** (+ description line), **Auto Run**, **Trigger**, **Runs**, **Tags**, **Updated Date**, **Actions**
- **Auto Run** values: **Enabled** (green dot) | **Disabled** (red dot)
- Trigger column shows two lines: trigger type bold (e.g. "Form: New Submission") + description (e.g. "New form submission")
- Tags shown as pill badges; "No Tags" when none assigned
- Three-dot **Actions** menu per row. Options confirmed:
  - Trigger Run
  - Schedule Run
  - View Runs
  - Edit Workflow
  - Duplicate
  - **Archive Workflow** (shown in red)
- Footer: row selection count, total results, rows per page selector (default 20), pagination controls

> ⚠️ **Unconfirmed:** No Enable/Disable option appears in the row Actions menu. How the Auto Run Enabled/Disabled state is toggled is unknown — verify with Audra.

### Workflow Builder (canvas)

- Page heading: **Create Workflow** (when creating new) | workflow name (when editing)
- Canvas toolbar: zoom slider (−/+), zoom % display, fullscreen icon, auto-layout icon, tag icon, settings gear
- Canvas search bar: "**Search workflow actions...**" (searches for node types to add by name — unclear if this also adds nodes or is separate from connection-dot flow)
- New workflows start with a single **Trigger** node on the canvas
- **How to add a node:** Click the **connection dot** at the bottom of a node. The right panel changes to the **Action** picker ("Select an action type") with a "Search actions..." bar
- Clicking a node opens its config panel in the right panel
- **Apply Changes** button in the config panel confirms node settings (must click before Save)
- Bottom toolbar: **Unsaved Changes** warning (orange) | **Reset** | **Save**
- Back arrow (←) top-right to exit the builder without saving

### Node three-dot menu (on individual nodes in the canvas)

Each node has a three-dot menu with:
- **Rename**
- **Disable** (skips the node during a run without deleting it)
- **Change Type**
- **Duplicate**
- **Delete**

### Trigger Event types (from Trigger node dropdown)

The Trigger Event dropdown has a "Search events..." search bar. Confirmed event types (may be more below scroll):

| Category | Event | Description |
|---|---|---|
| Manual | Manual | Manually trigger the workflow |
| Audience | Contacts: Created | New contact created |
| Audience | Contacts: Updated | Contact updated |
| Audience | Contacts: Added to Segment | Contact added to segment |
| Audience | Contacts: Removed from Segment | Contact removed from segment |
| Audience | Form: New Submission | New form submission |
| Audience | Form Request: Completed | A form request has been completed |
| Commerce | Subscription: Created | New subscription created |
| Default | E-Sign: Document Completed | Triggers when document is signed (for contact) |
| Default | E-Sign: Document signed by Party | Triggers when a specific party signs the document |
| Task | Task: Completed | Triggers when a task is completed |
| Care Plan | Care Plan: Created | Triggers when a care plan is created |
| Care Plan | Care Plan: Task Completed | Triggers when a care plan task is completed |
| Care Plan | Care Plan: All Phase Tasks Completed | Triggers when all tasks in a care plan phase are completed |
| Care Plan | Care Plan: Phase Status Changed | Triggers when a care plan phase business status changes |

> ⚠️ Scrollbar visible in screenshot — more trigger types likely exist below.

### Action node types (from action picker)

**Flow Control group:**

| Node | Description |
|---|---|
| Wait Until | Wait until delay before continuing |
| Wait For Event | Wait for an event to occur before continuing — has On Event / On Timeout branches |
| ~~Wait For Event (Legacy)~~ | ~~Deprecated — do not use or document~~ |
| Paths | Split workflow into paths |
| Exit Workflow | Exit the workflow |

**Actions group:**

| Node | Description |
|---|---|
| Add Resource to Task | Add a resource to an existing task |
| Send Message | Send an SMS message to a contact |
| Send Email | Send an email to a contact |
| Send Notification | Send a notification |
| Update Contact Details | Update contact fields with specified values |
| Create Contact | Create a new contact with specified values |
| Add Tag | Add tags to a contact |
| Remove Tag | Remove tags from a contact |
| Assign Contact to Team | Assign a contact to teams |
| Unassign Contact from Team | Unassign a contact from teams |
| Assign Task | Create and assign a task to a user |
| Assign Task From Template | Create a care plan task from a selected task template within a phase |
| Invite to Portal | Invite a contact to the portal |
| Create E-Sign Document | Create a signature request from a template for selected signers |
| Create Form Request | Create a form request for a contact to fill out |
| Get Form Submission | Retrieve a form submission by its ID |
| Query Contact | Search for a contact |
| Create Care Plan | Enroll a contact in a plan definition |
| Update Care Plan Status | Update the status of a care plan |
| Update Care Plan Phase Status | Update the status of a specific phase in a care plan |
| Get Phase Tasks | Get tasks in a care plan phase |
| Get Phase Task | Get a specific care plan task by ID |
| Update Task | Update the status or performer of a task |

### Send Message node config panel

- **Recipient** dropdown — defaults to "Workflow contact"
- **Message** compose field — toolbar: undo, redo, template (grid icon), personalization `{}`, attach (paperclip), template-insert icon
- Character counter: `0/1530`
- Helper text: "The message to send to the recipient."
- **Apply Changes** button

### Run History view

- Left panel tabs: **Summary** | **Contact**
- **Run Summary** section: STATUS, TRIGGER, STARTED, COMPLETED, DURATION
- **Activity History** section: chronological list of each node executed with timestamp and label (e.g. "Send Message "Welcome and Pre Admit Q text"")
- Canvas (right): full workflow diagram; node statuses: **Completed** (green highlight), **Not taken** (muted/gray)
- Top-right: **Restart Run** button + three-dot menu

### Glossary discrepancies confirmed from UI

| Glossary term | Actual UI label |
|---|---|
| Path Split | Paths |
| Add/Remove Tag (one entry) | Add Tag + Remove Tag (two separate nodes) |
| Create Task | Assign Task |
| Wait for Time | Wait Until |

### Still unconfirmed for Workflows (needs additional screenshots)

- How Auto Run Enabled/Disabled is toggled
- Paths node config panel (conditions, AND/OR, fallback path)
- Wait Until config panel (delay format)
- Wait For Event config panel (which events; timeout duration)
- Assign Task config panel (fields)
- Whether Trigger Run prompts for a specific contact
- Whether more trigger event types exist below Care Plan in the dropdown
- Whether archived workflows can be restored

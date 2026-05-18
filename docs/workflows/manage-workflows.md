# Manage Workflows

This guide covers the day-to-day tasks you may need to perform after a workflow has been created: viewing and searching your workflows, editing a workflow, running one manually, reviewing its run history, and archiving it when it is no longer needed.

## Before you begin

You need at least one workflow in your account to follow this guide. If you have not created one yet, see [Create a Workflow](#).

## View your workflows

The Active Workflows list shows all workflows in your account along with their current status, trigger type, and run count.

1. Open **Automation** from the main navigation sidebar.
2. Under the **Workflows** heading in the sidebar, click **Active Workflows**.

The list displays each workflow with its name, description, **Auto Run** status (**Enabled** or **Disabled**), trigger type, number of runs, any assigned tags, and the date it was last updated. Workflows that have been archived are not shown in the main list but can be found under the **Archived** tab.

## Search and filter the workflow list

When your account has many workflows, you can search by name or use the filter to narrow the list.

1. On the **Active Workflows** page, type a workflow name or keyword into the search bar.
2. Click **Search** to apply the search.
3. To filter the list, click the filter icon to the left of the search bar. A **Search Facets** panel opens on the left. Expand any of the three filter fields to narrow results:
   - **Auto Run:** filter by Enabled or Disabled status
   - **Trigger:** filter by trigger event type
   - **Tags:** filter by tags assigned to workflows

To clear the search and return to the full list, remove the text from the search bar and click **Search** again.

## Edit a workflow

Use the Edit Workflow option to open a workflow in the Workflow Builder and make changes to its nodes or trigger event.

1. On the **Active Workflows** page, find the workflow you want to edit.
2. Click the three-dot **Actions** menu at the right end of the workflow's row.
3. Click **Edit Workflow**. The **Workflow Builder** opens with the workflow's current canvas.
4. Make your changes. Add, configure, or delete nodes as needed.
5. Click **Save** to save your changes.

> **Note:** If a workflow is currently enabled and has active runs in progress, editing it may affect contacts that are mid-run. Confirm the behavior with your Subflow administrator before editing a live workflow that has recently been triggered for contacts.

## Enable or disable Auto Run

The **Auto Run** setting controls whether a workflow runs automatically whenever its trigger event fires. Workflows with Auto Run set to **Enabled** start a new run for every contact that matches the trigger. Workflows set to **Disabled** do not start runs automatically, but can still be triggered manually.

Auto Run is toggled from within the **Workflow Builder**.

1. On the **Active Workflows** page, find the workflow you want to update.
2. Click the three-dot **Actions** menu and click **Edit Workflow**. The **Workflow Builder** opens.
3. Click the settings gear icon in the canvas toolbar. The **Workflow Settings** panel opens on the right.
4. Click the **Auto Run** toggle to enable or disable it.
5. Click **Save**. The Auto Run status on the **Active Workflows** list updates to reflect the change.

## Trigger a workflow manually

Use the Trigger Run option when you want to start a workflow run for one or more contacts without waiting for the trigger event to fire automatically. This is available for all workflows, including those with Auto Run set to **Disabled**.

1. On the **Active Workflows** page, find the workflow you want to run.
2. Click the three-dot **Actions** menu at the right end of the workflow's row.
3. Click **Trigger Run**. The **Trigger Workflow Run** dialog opens.
4. Use the **Search contacts** bar or scroll the list to find the contacts you want to run the workflow for. Click **Select** next to each contact. You can select up to 50 contacts at a time.
5. Click **Trigger Run** at the bottom of the dialog to start the run.

> **Note:** If the workflow uses an event-based trigger, a warning appears in the dialog explaining that running it manually may cause failures if the workflow depends on event data that will not be available. Review the warning before proceeding.

You can also schedule a run for a future time by clicking **Schedule Run** in the same Actions menu.

## View run history

The Run History view shows a record of every time a workflow has been triggered, including the result of each run and a step-by-step activity log.

1. On the **Active Workflows** page, find the workflow whose history you want to review.
2. Click the three-dot **Actions** menu and click **View Runs**, or click **Run History** in the sidebar under the **Workflows** heading.

Each run in the list shows its status (Completed, in progress, or failed), the trigger that started it, the start and end times, and the duration. Click a run to open its detail view, where the **Summary** tab shows the run metadata and the **Activity History** shows each node that executed, in order, with timestamps.

The canvas on the right side of the detail view shows the workflow diagram with each node marked as **Completed** (green) or **Not taken** (muted), so you can see exactly which path the workflow followed for that contact.

## Archive a workflow

Archiving a workflow removes it from the **Active Workflows** list and stops it from running for new trigger events. Archive a workflow when it is no longer needed but you want to keep a record of it rather than deleting it.

1. On the **Active Workflows** page, find the workflow you want to archive.
2. Click the three-dot **Actions** menu at the right end of its row.
3. Click **Archive Workflow**. The workflow moves to the **Archived** tab.

To view archived workflows, click the **Archived** tab at the top of the **Active Workflows** page.

[Note: Need confirmation on whether archived workflows can be restored to the active list, and if so, how.]

## Related articles

Now that you know how to manage workflows, check these related articles to make the most of this feature.

- **Create a Workflow:** Build a new workflow from scratch, from choosing a trigger event to saving and activating it.
- **Workflow Node Reference:** Look up what each node type does and what configuration options are available.
- **Workflows in Subflow:** Review the concept overview to understand how workflows are triggered and how they relate to care plans.

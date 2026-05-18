# Create a Workflow

This guide walks you through building a new workflow from scratch in the Workflow Builder, from choosing a trigger event to adding and connecting nodes and saving the finished workflow.

## Before you begin

Before you start building, have the following ready:

- A clear idea of what should start the workflow: which trigger event fires and for which type of contact. Refer to the [Workflow Node Reference](#) for the full list of available trigger event types.
- If you plan to use a **Form: New Submission** trigger, the form must already exist in Subflow.
- If you plan to use a **Paths** node to branch the workflow, decide in advance what conditions each branch should check, such as a specific form answer, segment membership, or contact field value. Create any needed segments beforehand.
- The message content you want to send, or the name of the message template you plan to use, if the workflow will send SMS messages or emails.
- The name of the staff member or role that tasks should be assigned to, if the workflow will create tasks.

> **Note:** Some trigger event types, such as EHR-based events, require an active integration between Subflow and your organization's electronic health record system. That integration is set up by the Subflow technical team, not by clinical staff. If you are not sure which trigger event types are available in your account, contact your Subflow administrator.

## Get started

Follow the steps below to create a workflow.

1. Open **Automation** from the main navigation sidebar.

2. Access the **Workflow Builder** using either of these paths:
   - Under **Workflows** in the sidebar, click **Active Workflows**, then select **Create Workflow** in the top-right corner.
   - Under **Workflows** in the sidebar, click **Workflow Builder**.

   The **Workflow Builder** opens with a single **Trigger** node on the canvas and the **Workflow Settings** panel on the right.

3. In the **Workflow Settings** panel, enter a name for your workflow in the **Name** field. Add a description and tags if needed.

4. Click the **Trigger** node on the canvas. The configuration panel opens on the right.

5. Under **Trigger Event**, click the dropdown to open the event picker. Use the "Search events..." bar to find a specific event, or scroll through the grouped list to find the one that should start this workflow. Click the event to select it.

6. If the trigger event requires additional configuration, complete the fields that appear in the **Configure** section below the Trigger Event dropdown. For the **Manual** trigger type, no additional configuration is needed.

7. Click the **connection dot** at the bottom of the **Trigger** node. The right panel changes to show the **Action** picker, with all available node types listed under **Flow Control** and **Actions**.

8. In the **Action** picker, select the node type you want to add as the first step. The node appears on the canvas connected to the Trigger node, and its configuration panel opens on the right.

   Use the "Search actions..." bar at the top of the picker to find a node type by name if the list is long.

9. Configure the node in the right panel. For a **Send Message** node, choose the recipient and compose or select the message content. For other node types, complete the fields shown. Refer to the [Workflow Node Reference](#) for details on each node's configuration options.

10. Click **Apply Changes** in the configuration panel to save the node's settings.

11. To add the next node, click the **connection dot** at the bottom of the node you just configured and repeat steps 8 through 10. Continue until the workflow covers all the steps you need.

12. If the workflow should branch based on patient conditions, add a **Paths** node by clicking the connection dot at the point where the workflow should split. Configure each branch with its conditions in the right panel.

    [Note: Need confirmation on the Paths configuration panel — specifically how conditions are defined and whether a fallback "otherwise" path is available for contacts that do not match any condition.]

13. End each path in the workflow by connecting it to an **Exit Workflow** node. Every path in a completed workflow should have a clear end point.

14. Enable **Auto Run** in the **Workflow Settings** panel to start running the workflow automatically for new contacts. The toggle turns blue when enabled.

15. Click **Save** at the bottom of the canvas to save the workflow and apply your settings.

## Duplicate an existing workflow

If the workflow you want to build is similar to one that already exists, you can duplicate it and modify the copy instead of building from scratch.

1. Open **Automation** from the main navigation sidebar.
2. Under **Workflows** in the sidebar, click **Active Workflows**.
3. Find the workflow you want to copy. Click the three-dot **Actions** menu at the right end of its row.
4. Click **Duplicate**. A copy of the workflow appears in the list named "Copy of [original name]".
5. Click the **Actions** menu on the copy and click **Edit Workflow** to open it in the Workflow Builder.
6. Make your changes to the nodes, trigger event, or settings.
7. Click **Save**.

## Related articles

Now that you know how to create a workflow, check these related articles to configure and manage it.

- **Workflow Node Reference:** Look up the configuration options for every node type, including Send Message, Assign Task, Paths, Wait For Event, and more.
- **Manage Workflows:** Learn how to edit a workflow that is already running, view its run history, and archive it when it is no longer needed.
- **Create a Segment:** Set up the dynamic contact groups that Paths nodes can use as conditions, so your workflow can route different patients down different branches.
- **Workflows in Subflow:** Review the concept overview to understand how workflows relate to care plans and what each node type is designed to do.

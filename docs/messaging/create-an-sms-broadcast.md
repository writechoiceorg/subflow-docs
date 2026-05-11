# Create an SMS Broadcast

An SMS Broadcast sends the same text message to every contact in one or more segments. Each recipient gets an individual message. Use this guide when you need to send a one-off or scheduled SMS to a group, such as an appointment reminder to all English-speaking COPD patients or a timesheet-approval prompt to all managers.

## Before you start

Make sure you have:

- A segment that contains the contacts you want to message. If you do not have one yet, create it first. A Broadcast cannot be sent without at least one segment selected.
- Permission to send messages from your Subflow account.
- The message content you want to send. You can type it directly or use a saved message template. See [Create a Message Template](#) for step-by-step instructions.

## Get started

Follow the steps below to create an SMS Broadcast.

1. Go to **Messaging** > **SMS Broadcast**.

2. Click **New Broadcast** in the top-right corner. In the **Create Broadcast** form that opens, you will need to complete:
   - **Broadcast Details**
   - **Recipients**
   - **Messages**

3. Type a label to identify your Broadcast in the **Name** field. (This name is internal; recipients do not see it.)

4. Select the segments to send to. Choose one or more segments from the segment picker. You can select up to three.
   - The picker displays each selected segment and the number of contacts in it.
   - If the segment you need is not listed, create it first under **Contacts** > **Segments**, then return to this step. To learn more, read [Create a Segment](#).

   > **Note:** To deselect a segment, click its tile in the picker. To remove all selections at once, click **Clear all**.

5. Add the message. You have two options:
   - Type the message directly into the message field.
   - Select a saved message template from the template picker. The template loads into the message field, and you can edit it before sending.

   You can also:
   - **Attach a resource** to the message: files, forms, courses, or meeting links hosted in Subflow.
   - **Personalize the message** using contact properties or form-data fields (for example, a contact's first name or a value from a previously submitted form).

6. Click **Save** to keep your changes. The Broadcast is now in draft status.

7. Send or schedule the Broadcast. From the draft, choose one of the following:
   - Click **Send Broadcast** to send the message to all selected segments immediately.
   - Click **Schedule Send** and pick a date and time to send the message later.

   > **Warning:** While the Broadcast is in draft status, you can still edit it. Once you send or schedule it, the content is locked.

## Troubleshooting

**The segment I need is not in the segment picker.**
Create the segment under **Contacts** > **Segments**, then return to the Broadcast and reopen the segment picker. Read [Create a Segment](#) for detailed step-by-step instructions.

**A contact I expected to receive the Broadcast did not.**
Check that the contact currently meets the conditions of at least one of the selected segments. Segments are dynamic: a contact may have been removed between when you selected the segment and when the Broadcast was sent.

## Related articles

Now that you know how to create an SMS Broadcast, check these related articles to make the most out of this feature.

- **Manage Broadcasts:** Learn how to edit or archive a Broadcast.
- **Create a Segment:** Group contacts by tag or form-data condition so you can target them with a Broadcast.
- **Create a Message Template:** Save reusable SMS and email message bodies for Broadcasts, workflows, and direct conversations.
- **Create a Contact:** Add a new person record so they can be included in a segment.

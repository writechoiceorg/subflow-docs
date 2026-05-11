# Manage two-way conversations

This guide explains how two-way conversations work in Subflow and how to respond to incoming patient messages from the Conversations inbox. Patients reply to your SMS messages directly from their phones, with no portal or app to log in to, and every reply lands in a single inbox where staff can read it and reply using a saved template or free-form text.

## How it works

Two-way conversations connect every SMS exchange between Subflow and a patient into a single, ongoing thread. The key things to know:

- Patients reply to Subflow messages from their own phone, the same way they would reply to any other text message. There is no portal to log in to and no app to install.
- Every patient reply lands in the Conversations inbox as a new unread message, regardless of whether the original message came from a workflow, a broadcast, or a staff member.
- Inside a conversation, the platform distinguishes automated messages (sent by a workflow) from messages sent by a staff member, so staff can quickly see who said what.
- Staff replies use the same SMS channel the patient is on. Anything you send from the conversation reply box goes to the patient as a standard text message.

> **Note:** If the conversation involves protected health information beyond logistics or general guidance, switch the conversation to Secure Chat before continuing the exchange. See [Use Secure Chat](#) for details.

## The Conversations inbox

The Conversations area is in the **Messaging** side menu, under the **Conversations** heading. The sidebar groups conversations into six views.

| Sidebar section | What it shows |
|---|---|
| **Inbox** | All active conversations across all patients. The number next to the label shows how many conversations contain unread messages. |
| **Unread** | Only conversations that contain at least one unread message, so staff can focus on what still needs a reply. |
| **Scheduled** | Messages queued to be sent at a future time but not yet delivered. |
| **Favorites** | Conversations that have been manually marked as favorites for quick access. |
| **Snoozed** | Conversations that have been temporarily set aside and will reappear in the inbox later. |
| **Archived** | Conversations that have been moved out of the active inbox to keep the list clean. Archived conversations are not deleted and can be restored. |

Inside any of these views, the conversations list shows each thread with the contact's initials, name, the date of the last activity, and a preview of the most recent message.

## Reading a conversation

Click any conversation in the list to open the full thread on the right. Within the thread, message style and metadata help staff distinguish automated workflow messages from those sent by a colleague.

- Automated messages are sent by a workflow node, for example, an intake reminder triggered when a patient reaches a stage in their care plan. The thread labels these as automated messages so staff can see they were not typed by a person.
- Staff-sent messages show the name of the staff member who sent them. If a colleague replied to a patient earlier, you can see who it was before sending a follow-up.
- Patient replies appear as inbound messages in the thread, in chronological order with the rest of the exchange.

## Respond to a conversation

The reply area at the bottom of the conversation lets you respond using free-form text or a saved template.

> **FLAG:** The specific button labels in the reply toolbar ("Templates", "Personalize", "Attach", "Send SMS") and the reply field label are not confirmed in transcripts. Verify against the sandbox before publishing.

1. Open **Messaging** from the main navigation, then select **Inbox** under the **Conversations** heading.
2. Click the conversation you want to reply to. The full message thread opens on the right.
3. In the reply field at the bottom, write your response. You can:
   - Type a free-form message directly into the field.
   - Click **Templates** in the toolbar to load a saved message template as the starting content. You can edit the template after inserting it.
   - Click **Personalize** to insert a dynamic field that pulls the patient's contact data or form responses into the message.
   - Click **Attach** to include a file, form, course, or meeting link in the reply.
4. Click **Send SMS** to send the message. The message appears in the thread as a staff-sent message and is delivered to the patient as a standard text.

> **Tip:** If you frequently reply with the same content, save it as a message template. The template can then be inserted with one click from the **Templates** button.

## Related articles

Now that you know how to manage two-way conversations, check these related articles to make the most out of this feature.

- **Create a Message Template:** Save a reusable SMS message you can insert into a conversation reply with one click.
- **Use Secure Chat:** Switch a conversation to encrypted web chat when discussing sensitive health information.
- **Create an SMS Broadcast:** Send a one-to-many text message to one or more segments when a single message needs to reach a group.
- **Messaging in Subflow:** Review the differences between SMS broadcasts, email campaigns, two-way conversations, and templates to choose the right tool for each message.

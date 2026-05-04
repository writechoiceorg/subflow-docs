# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a technical writing project for **WriteChoice** (client: **Subflow Health**). The goal is to produce end-user documentation for Subflow's healthcare SaaS platform, hosted on **Featurebase**. The primary audience is non-technical clinical staff: nurses, nurse navigators, and administrative assistants.

## Repository Structure

- `transcripts/` — Meeting transcripts between the WriteChoice team and Audra Wallace (Subflow). Source of truth for feature behavior, platform terminology, and documentation priorities.
- `materials/` — Reference documents provided by Subflow (e.g., white papers, product overviews).

## Subflow Platform — Key Concepts

Understanding these concepts is essential for producing accurate documentation. Terminology matters: Subflow calls the top-level navigation sections **applications** (not modules or features).

| Term | Definition |
|---|---|
| **Care Plan** | The macro-level visualization of a patient's full journey (digitized clinical protocol). Still actively being developed. Contains stages/milestones a patient moves through. |
| **Workflow** | The automation engine that powers care plans. Triggered by events (manual, form submissions, EHR API events, task completions). Can send messages, wait for responses, split on conditions, create tasks. Multiple workflows can attach to one care plan; one workflow can serve multiple care plans. |
| **Task** | An action item assigned to a staff member, usually created automatically by a workflow. Statuses: Requested → In Progress → Completed. Completing a task can trigger further workflow steps. |
| **Contact** | A patient (or staff member) record in the system. |
| **Contact Field** | A custom data field (text, dropdown, checkbox, etc.) created by Subflow staff during client onboarding. Fields are the building blocks of forms. |
| **Tag** | A label applied to a contact. Used as a basis for segment membership. |
| **Segment** | A dynamic list of contacts that automatically updates when contact records change (tag changes, form responses). Used as recipients for broadcasts and as conditions in workflow paths. |
| **Form** | A digital questionnaire built from contact fields. Can be multi-step, have conditional (hidden) fields, required fields, and "alarming" answer highlighting. Sent to patients via SMS link. |
| **Message Template** | A saved SMS or email template reusable across workflows, conversations, and broadcasts. |
| **SMS Broadcast** | A one-to-many SMS message sent to up to 3 segments at once. Requires a segment to exist first. Must be manually created (no automation yet). Can be scheduled. |
| **Email Campaign** | Same concept as broadcast but for email; uses a drag-and-drop email builder. |
| **Two-Way Conversation** | Patients reply to SMS messages directly from their phone (no patient portal). Staff see replies in the platform conversation view. |
| **Secure Chat** | A HIPAA-compliant toggle on conversations that routes messages through an encrypted web chat, used when sending or discussing sensitive health data. |
| **Referral Coordination** | A planned future feature for sharing patient records across providers — not yet implemented. |

## Documentation Platform

**Featurebase** is the hosting platform. Its constraints affect structure decisions:

- Structure is **collections** (top-level sections in sidebar) > **articles** (individual pages). Nesting is limited — don't plan deep sub-hierarchies.
- No inline commenting on published articles. Feedback is given via the Slack task list (task per article, with comment threads and Loom/video recordings).
- GIF embeds render at reduced size — prefer annotated screenshots or Supademo over GIFs.
- **Supademo** (interactive screenshot slideshow, embeds via iframe) is being tested for use inside Featurebase articles for step-by-step walkthroughs.

## Planned Documentation Structure

Validated with Audra Wallace (Subflow) in the 3rd meeting (2026-04-24):

1. **Overview** — Conceptual pages: what is Subflow, care plan, workflow, tasks, user roles (future feature)
2. **Compliance & Security** — HIPAA guidance, when to use Secure Chat vs. regular SMS
3. **Get Started** — First login, navigation, and tasks (first thing a new user does)
4. **Patient Journey** — Diagram explaining how all applications connect in a patient's care journey
5. **Contacts & Segments** — Contacts, tags, segments (concepts + how-to guides)
6. **Messaging** — SMS broadcast, email campaigns, message templates, two-way conversations, secure chat
7. **Forms** — (next priority after Messaging)
8. **Workflows** — (after Forms)
9. **Care Plans** — (last; still in active development by Subflow)

## Article Page Structure Convention

All how-to guide pages follow this layout:

1. **Before You Start** — Prerequisites (e.g., "You need at least one segment before creating a broadcast"). Link to prerequisite guides.
2. **Steps** — Numbered steps with annotated screenshots. UI element names always **bolded**.
3. **Related Articles** — Links to related guides (use placeholder text until other articles exist).

## Key Decisions & Constraints

- **Audience**: Non-technical clinical staff. Write for users who are not tech-savvy. Prefer visual walkthroughs and handholding over concise technical prose.
- **Glossary**: Being built collaboratively in Slack Canvas. Always use Subflow's official term for UI elements (confirm with Audra when uncertain — e.g., "applications" not "modules").
- **Unfinished features**: Some UI elements in the sandbox (e.g., Patient Tasks, some Care Plans screens) are scaffolded but not live in production. Avoid documenting or screenshotting features not yet in production.
- **Sandbox access**: The WriteChoice team has access to the Subflow **sandbox** account, not the support account. Example forms, workflows, and contacts created by Audra must be placed in the sandbox.
- **Style guide**: In progress (Evangelina leading). Standardize formatting before publishing final versions.

## Team

- **WriteChoice**: Marcos Briceno (lead), Heitor Tessaro, Evangelina Sorello (Vanja), Queendoline Akpan (Queen)
- **Subflow**: Audra Wallace (primary contact, CSM), Maddie (Audra's colleague), Mitch (CEO/decision-maker on tooling), Will (developer, future API documentation contact)

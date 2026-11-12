---
name: case-update-summary
description: |
  Writes customer-facing and internal leadership status updates for a support case (case number,
  tracking ID or subject), grounded in the latest case email thread and related Teams chats. Use when
  the user asks for a "case update", an "update on case ...", "summarize where this case stands", a
  "final update for the day", a "leadership update on the [X] case" or a "detailed hourly internal
  summary". Do NOT use for general emails, or for opening, closing or editing case records.
---

# Case Update Summary

Drafts case status updates from the newest activity on a case email thread (and related Teams chats).
Produces a customer-facing update, an internal leadership update, or both. Never sends anything.

## Setup: fill these in once

Replace these placeholders with your own defaults, or leave them and the skill will ask each time.

- Your sign-off name: `<YOUR_NAME>`
- Default time zone: `<TIME_ZONE>`
- Default leadership audience: `<LEADER_NAME>`
- Default customer distribution: To `<TO_RECIPIENTS>`, Cc `<CC_RECIPIENTS>`

Keep real customer names and addresses out of shared copies of this file.

## Ask before drafting

Search first, then ask the user only for what is still missing. Never guess.

1. **Case:** a case number, tracking ID or subject. If several cases match, list them and ask which one.
   If nothing matches, ask for the case number.
2. **Audience:** customer, internal, or both. If not stated, ask once.
3. **Variant:** first update, regular update or final update for the day (customer); quick or detailed (internal).
4. **Time and time zone** of the update, if not obvious.
5. **Recipients:** copy them from the latest message on the thread. If there is no thread and no default
   above, ask. Never construct an email address.

## Workflow

1. Find the case thread in mail and read the newest messages in full, including the user's previous update.
2. Check related Teams chats (bridge chat, engineering chat). Treat AI meeting summaries as unverified.
   If sources conflict, leave the point out or flag it as unconfirmed.
3. Capture: current status and severity, confirmed findings, root cause (if confirmed), actions and
   results, what each party is doing now, owners and confirmed dates.
4. Draft using the formats below, run the Final check, then show the draft. Do not send.

## Customer-facing format

Recipients block at the top (To and Cc lines, semicolon-separated) for the user to paste. Leave the
To and Cc fields empty.

Subject: `<CUSTOMER> <PLATFORM> - Case <CASE_NUMBER> - <ISSUE_NAME> - <UPDATE_TIME> <TIME_ZONE> Update`
(last update of the day ends with `- Final Update for the Day`). Keep the pattern on follow-ups.

Body:
1. `Hi Team,`
2. Opener: "I wanted to share an initial update on..." or "I wanted to share the latest update on..."
3. **Current status:** recurrence, investigation state, root cause status, next checkpoint.
4. **What happened** (early updates): when it started, what users saw, business impact, what was not affected.
5. **Progress since the case was opened / since the previous update:** confirmed findings only. If none:
   "Since the previous update, the teams have continued monitoring and no new confirmed finding has been identified."
6. **Current focus:** what each party is doing now, plus interim guidance for the customer.
7. **Next steps:** bullets, an owner on every one.
8. Closing: "Microsoft will continue working with the <PLATFORM> team until <milestone>."
9. `Best,` then `<YOUR_NAME>`.

Exclude from the customer version: internal incident numbers, machine or storage names, engineer names,
handoffs and coverage hours, missed calls and bridge logistics, internal chat commentary, AI diagnostic
output, customer temperature, inferences and unconfirmed leads.

## Internal formats

**Quick update (default):** optional header `[<CUSTOMER>: <PLATFORM>] Case <CASE_NUMBER>, <ISSUE_NAME>`,
then exactly 3 bullets: (1) Status and impact, (2) Customer temperature, (3) Next steps and owners.

**Detailed summary ("detailed", "hourly"):** Title `Internal Leadership Summary | <CUSTOMER> | <CASE_NUMBER>`,
with Status; What changed since the previous update; Technical status (mark unverified items);
Business impact; Customer temperature labeled `[Inference]`; Owners and next steps.

## Style rules

- Calm, factual, plain language. Short sentences. No acronyms in leadership updates.
- No em dashes. Never attribute with "per [person]".
- Never claim "service restored" unless the customer confirmed it on the thread.
- Never promise a date or time that isn't confirmed. If something is unknown, say so.

## Final check

1. Right audience; when both, customer version first, then the internal version.
2. Every fact traces to the thread or chats.
3. Customer version has all sections, an owner on every next step, and no internal details.
4. Internal quick version has exactly 3 bullets with named owners.
5. Recipients block at the top; nothing sent.

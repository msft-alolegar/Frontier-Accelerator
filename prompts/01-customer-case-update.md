# Customer-facing case update

**Use when:** you need a status update for the customer on an active support case.

**Short form (with the skill saved):** `<PLATFORM> update on case <CASE_NUMBER>`

## Prompt

```text
Draft a customer-facing status update for support case <CASE_NUMBER> affecting <CUSTOMER> <PLATFORM>.

Before you draft, check what you can find yourself, then ask me for anything still missing. Do not guess. Ask me for:
1. The case number, if I haven't given one or you can't find the thread.
2. Whether this is the first update, a regular update, or the final update for the day.
3. The time of this update and the time zone.
4. The To and Cc recipients, if there is no earlier update on the thread to copy them from.
If several cases match, list them and ask which one I mean.

Sources:
- Read the newest messages on the case email thread in full, including my previous update.
- Check related Teams chats (the bridge chat and the engineering chat) for confirmed findings.
- Treat AI meeting summaries as unverified. If two sources disagree, leave the point out or flag it to me.

Format:
Recipients block at the very top (To and Cc lines, semicolon-separated), so I can paste them myself. Do not fill in the To or Cc fields.
Subject: <CUSTOMER> <PLATFORM> - Case <CASE_NUMBER> - <ISSUE_NAME> - <UPDATE_TIME> <TIME_ZONE> Update

Hi Team,
One opening line: "I wanted to share an initial update on..." or "I wanted to share the latest update on..."

Current status: one short paragraph. Has it happened again? Is the investigation active? Is there a root cause yet? When is the next checkpoint?
What happened (first update only): when it started, what users saw, the business impact in plain words, and what was not affected.
Progress since the case was opened / since the previous update: bullets of confirmed findings only, credited to "Microsoft", "the <PLATFORM> team" or "<PARTNER>".
Current focus: what each party is doing now, plus any interim guidance for the customer.
Next steps: bullets, with an owner on every one.
Closing: "Microsoft will continue working with the <PLATFORM> team until <milestone>."
Best,
<YOUR_NAME>

Rules:
- Calm, factual, plain language. Short sentences. No jargon, no acronyms, no em dashes.
- No machine names, storage account names, internal incident numbers or engineer names.
- Leave out internal chat activity, customer temperature, engineer handoffs, missed calls and unconfirmed leads.
- Never say service is restored unless the customer confirmed it on the thread.
- Never promise a date or time that isn't confirmed on the thread. If something is unknown, say so.
- Show me the draft only. Do not send it.
```

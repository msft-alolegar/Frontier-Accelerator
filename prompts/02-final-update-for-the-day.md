# Final update for the day

**Use when:** you're closing out the day on a case that is still open.

**Short form (with the skill saved):** `Final update for the day on the <ISSUE_NAME> case`

## Prompt

```text
Draft the final customer update for the day on support case <CASE_NUMBER> for <CUSTOMER> <PLATFORM>.

Before you draft, ask me for anything you can't confirm from the case thread. Do not guess:
1. The case number or issue name, if you can't find the thread.
2. The time of this update and the time zone.
3. The recipients, if there's no earlier update on the thread to copy them from.

Read every message on the case thread since my previous update, plus any related Teams chats.

Subject: <CUSTOMER> <PLATFORM> - Case <CASE_NUMBER> - <ISSUE_NAME> - <UPDATE_TIME> <TIME_ZONE> - Final Update for the Day
Put the To and Cc lines at the top of the body for me to paste. Do not fill in the To or Cc fields.

Sections:
Current status: is the investigation active, mitigated or resolved? Has the issue come back since the last update? Can severity be raised again quickly if it returns?
Progress since the previous update: confirmed findings only. If nothing new, write: "Since the previous update, the teams have continued monitoring and no new confirmed finding has been identified."
Current focus: what is running or being reviewed overnight, and by whom.
Next steps: what each owner will do if the issue comes back, and when the teams reconvene.
Closing: "Microsoft will continue coordinating with <PARTNER> and the <CUSTOMER> team as the investigation progresses."

Rules: plain language, no em dashes, no internal details, no unconfirmed dates, and never "service restored" unless the customer confirmed it. Draft only. Do not send.
```

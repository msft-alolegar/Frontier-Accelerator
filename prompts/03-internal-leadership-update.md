# Internal leadership update

Two versions. Use the quick one by default. Use the detailed one when leadership wants the hourly or full view.

## A. Quick 3-bullet update

**Short form (with the skill saved):** `Leadership update on the <ISSUE_NAME> case`

```text
Write a quick internal leadership update on support case <CASE_NUMBER> (<CUSTOMER>, <PLATFORM>) for <LEADER_NAME>.

If you can't find the case thread, or you don't know who the update is for, ask me before drafting.

Read the latest case emails and the related Teams chats. Then write exactly 3 bullets:
1. Status and impact: active, mitigated or resolved; who or what is affected; root cause status.
2. Customer temperature: a one-line read and the signals behind it. If you can't tell, say so and ask me. Don't guess.
3. Next steps and owners: name the owner of every action, including me.

Optional header line: [<CUSTOMER>: <PLATFORM>] Case <CASE_NUMBER>, <ISSUE_NAME>
Plain language, no acronyms, no em dashes. Never attribute with "per [person]".
```

## B. Detailed hourly internal summary

**Short form (with the skill saved):** `Detailed hourly internal summary`

```text
Write a detailed internal leadership summary for support case <CASE_NUMBER> (<CUSTOMER>, <PLATFORM>).

Ask me first if you're missing the case number or the time window to cover (for example "since the 4:55 PM update yesterday, including overnight").

Title: Internal Leadership Summary | <CUSTOMER> | <CASE_NUMBER>

Sections:
- Status: active, monitoring, mitigated or resolved; severity and who confirmed it.
- What changed since the previous update: bullets, stating the period covered. If nothing material, say so and list what was checked.
- Technical status: confirmed symptoms; Microsoft findings; <PARTNER> findings; diagnostics completed; diagnostics pending; mitigation attempted; current investigation path. Mark anything unverified as "unverified" and leads as "unconfirmed lead".
- Business impact: users affected, how often it happens, and the customer's own description of impact.
- Customer temperature: labeled [Inference], a one-word rating (Stable, Elevated or Frustrated) and the signals used.
- Owners and next steps: one line per owner (customer team, partner, Microsoft Support, engineering, me).

Internal team names and severity are fine here. Still no em dashes and no "per [person]".
```

# Frontier Accelerator: Escalation Update Prompts

Prompts for **Week 8: Lead Delivery Risks, Escalations and Recovery Plans**.

During an escalation you usually owe two updates from the same case thread: a calm, plain-language update for the customer and a short, candid one for leadership. These prompts help AI draft both. You review every line and send it yourself.

## What's here

| File | Use it when |
|---|---|
| [prompts/01-customer-case-update.md](prompts/01-customer-case-update.md) | You need a customer-facing status update on an active case |
| [prompts/02-final-update-for-the-day.md](prompts/02-final-update-for-the-day.md) | You're closing out the day on an open case |
| [prompts/03-internal-leadership-update.md](prompts/03-internal-leadership-update.md) | Leadership needs a 3-bullet update or a detailed hourly summary |
| [prompts/04-human-checkpoint.md](prompts/04-human-checkpoint.md) | Every time, before anything is sent |
| [skill/case-update-summary/SKILL.md](skill/case-update-summary/SKILL.md) | You want to save the rules once as a reusable skill, so your prompts can stay one line long |

## How to use

1. Open Microsoft 365 Copilot or Copilot Cowork. Both need access to your mail and Teams.
2. Copy a prompt and paste it in. You can fill in the `<PLACEHOLDERS>` first or leave them as they are.
3. Each prompt tells the AI to **ask you** for any required detail it can't confirm from the case thread, such as the case number, the audience or the recipients. Answer those questions; it won't guess.
4. Review the draft with the [human checkpoint](prompts/04-human-checkpoint.md) before you send anything.

**Optional:** save `skill/case-update-summary/SKILL.md` as a personal skill. After that, short prompts work on their own:

- `<PLATFORM> update on case <CASE_NUMBER>`
- `Final update for the day on the <ISSUE_NAME> case`
- `Detailed hourly internal summary`

## Placeholders

| Placeholder | Meaning |
|---|---|
| `<CUSTOMER>` | Customer name |
| `<PLATFORM>` | Workload, platform or team the case affects |
| `<CASE_NUMBER>` | Support case number |
| `<ISSUE_NAME>` | Short issue name, for example "Application Crashes" |
| `<UPDATE_TIME>` / `<TIME_ZONE>` | Time of the update, for example 11:15 AM ET |
| `<PARTNER>` | Third-party vendor involved, if any |
| `<TO_RECIPIENTS>` / `<CC_RECIPIENTS>` | Customer and internal distribution lists |
| `<LEADER_NAME>` | Who the internal update is for |
| `<YOUR_NAME>` | Your sign-off name |

## Ground rules

- AI gathers and drafts. You own what the customer hears and when they hear it.
- Never put customer names, case numbers, machine names or recipient addresses into this repo. Keep real data in your mail and Teams only.
- Nothing is sent automatically. The prompts produce drafts.

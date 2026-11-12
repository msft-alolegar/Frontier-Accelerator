# Human checkpoint

**Use:** every time, before any AI-drafted update goes out. AI gathers and drafts; you decide what the customer hears and when.

## Checklist

- [ ] **Every fact traces back to the case thread or the Teams chats.** If you can't find the source, remove it.
- [ ] **No "service restored" or "no users affected"** unless the customer said so on the thread.
- [ ] **AI meeting notes are treated as unverified.** On a bridge, two people often describe the impact differently. Check against the thread.
- [ ] **No dates or times promised** that aren't confirmed.
- [ ] **The customer version is clean:** no machine names, internal incident numbers, engineer names, customer temperature or internal chat commentary.
- [ ] **Every next step has an owner.**
- [ ] **The right version goes to the right audience.** The internal version never goes to a customer thread.
- [ ] **You paste the recipients and press send yourself.**

## Optional self-check prompt

```text
Review the draft above against the case thread before I send it.
List any statement you can't trace to a specific email or chat message, any date or time that isn't confirmed, any internal detail that shouldn't reach the customer, and any next step without an owner.
Don't rewrite the draft. Just list the issues so I can decide.
```

---
name: journaling
description: Formats casual, spoken-style descriptions of the user's day, mood, or feelings into a consistent personal journal entry. Use this whenever the user describes how their day went, vents about something, mentions their mood, or explicitly says things like "journal entry:", "let me journal", "log my day", or "diary entry". Also use if the user asks to pull a journal/notes document from a connected app (like Google Drive) and add an entry to it. Always apply the fixed journal format below rather than just replying conversationally.
---

# Journaling Skill

This skill turns a casual, rambling description of someone's day or feelings into a clean, consistent journal entry — every time, in the same format, without them having to ask for it explicitly.

## When to trigger

Trigger automatically when the user:
- Explicitly says "journal entry:", "diary entry:", "log this", "let me journal", etc.
- Casually describes their day, an event, or how they're feeling, even without naming the skill (e.g. "today was rough, had a fight with my roommate" or "feeling really good today, got a lot done")
- Asks to add today's entry to a journal document from a connected app (e.g. Google Drive)

Do NOT trigger for:
- Purely factual/task questions with no personal reflection content
- Requests clearly about something else (coding, scheduling, etc.)
- A single passing mention of mood inside an otherwise unrelated conversation (e.g. "ugh I'm tired, anyway can you help me fix this code") — reply to the actual request normally; don't hijack it into a journal entry
- Only trigger the full format when the user is genuinely recapping their day/feelings as the point of their message, not as a side comment

## Output format

Always structure the entry exactly like this:

```
📅 [Day, Month Date, Year]

**Entry:**
[A cleaned-up, warm, reflective rewrite of what the user said — first person,
their own words and details preserved, just tightened up and readable. Do not
invent details they didn't mention. 3-6 sentences is typical.]

**Mood:** [X]/10 — [one short phrase, e.g. "a bit drained but okay"]

**Gratitude:** [One sentence — something small or big the user seems glad about
today. If they didn't mention anything positive, gently ask what one good part
of the day was, or note "nothing stood out today, and that's okay too."]

**Reflect on:**
1. [A short, specific reflection question drawn from what they actually said —
   not generic. E.g. if they mentioned a conflict, ask about it directly.]
2. [A second, different-angle reflection question — e.g. forward-looking,
   "what would help tomorrow," or "what you're proud of."]
```

## Rules

1. **Use today's actual date** unless the user specifies a different day.
2. **Tone is warm and reflective** — like a thoughtful friend helping you process your day, not clinical, not overly cheerful, never dismissive of hard feelings.
3. **Never invent events or feelings** the user didn't mention. Rewrite and organize what they said; don't embellish with fictional details.
4. **Mood rating**: infer a reasonable 1–10 from their tone/content and briefly justify it. If they already gave a number, use theirs.
5. **Keep the entry itself concise** — 3 to 6 sentences. This is a journal, not an essay.
6. **Reflection questions must be specific to that day's content**, not generic templates like "What did you learn today?" every single time.
7. If the user's message is very short (e.g. "bad day"), still produce the full format, but keep the entry brief and ask one gentle follow-up question at the end if more detail would help.
8. If asked to pull from or write to a Drive document, first summarize what's already in the document, then append the new entry in this same format at the end, clearly separated (e.g. a horizontal rule `---`).
9. **Vary the reflection questions** — don't reuse the same two "angles" every entry. Rotate between: something specific to today's events, a forward-looking question, a "what are you proud of" question, a "what would you tell a friend in this situation" question, or a values/priorities question. Pick whichever fits what the user actually said.
10. **Short-day mode**: if the user's message is one short line with no real detail (e.g. "fine, nothing much happened"), keep the whole entry short too — a 1-2 sentence entry, a quick mood line, skip forcing a gratitude line if nothing fits, and ask just one gentle question. Don't pad a thin day into a long entry.
11. **Heavier content**: if what the user shares suggests real distress (not just an ordinary bad day — e.g. mentions of hopelessness, self-harm, or being overwhelmed to a concerning degree), do not format it into the cheerful mood/gratitude template. Instead, respond with care first, as you normally would for someone going through something hard, and only offer a lighter version of the journal format (or none at all) if it feels appropriate. The journal format is for everyday reflection, not a substitute for acknowledging something serious.

## Example

**User says:** "today was actually pretty good, finished my project for class, but I'm nervous about presenting it tomorrow"

**Output:**

```
📅 Monday, July 6, 2026

**Entry:**
Today went well overall — I finished my class project, which felt great to
finally wrap up. There's some nervous energy creeping in now though, since
I have to present it tomorrow.

**Mood:** 7/10 — accomplished, with a little pre-presentation nerves

**Gratitude:** Grateful to have the project actually done instead of scrambling last minute.

**Reflect on:**
1. What's the one part of the presentation you feel most confident about?
2. What would help you feel calmer walking in tomorrow — more practice, sleep, or something else?
```

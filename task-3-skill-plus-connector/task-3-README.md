# Task 3 - Wiring the Skill and Connector Together

## What I did

Put Task 1 (the journaling Skill) and Task 2 (the Drive connector) together into one workflow. Instead of pulling data out of Drive and then separately asking for a journal entry, I did both in a single sentence.

## The prompt

"pull today's Drive activity and journal about working on this assignment, in my usual format"

## What happened

It pulled real, live info from Drive (confirmed the most recently viewed file really was the Lecture 8 assignment PDF, viewed that same day) and dropped that straight into a journal entry using my Skill's format - date, entry, mood, gratitude, reflection questions - without me having to re-explain anything.

## How I checked it

Compared the file name and the "viewed today" detail against my actual Drive account, it matched up, so it was pulling from the live connector and not just making something up.

## What worked / what didn't

One plain sentence was enough to get both the Skill and the connector to fire together, no extra prompting needed. Nothing really broke here since both pieces were already tested on their own in Tasks 1 and 2, this was mainly confirming they work fine combined.

# Task 1 - Journaling Skill

## What it does

I built a Skill that takes whatever I say about my day (however messy or casual) and turns it into a proper journal entry. So instead of typing "journal entry:" and then a perfectly formatted paragraph, I can just talk about my day like I normally would - "today was kind of rough, had a fight with my roommate" - and it picks up on that automatically and formats it for me.

Every entry ends up with the same structure so it actually looks like a journal and not just a random chat reply:
- date at the top
- a cleaned up version of what I said
- a mood rating out of 10 with a quick reason why
- one thing I'm grateful for
- two questions to think about, based on what actually happened that day (not the same two questions every time, it mixes it up)

I also made sure it doesn't go overboard - if I just mention being tired in the middle of talking about something else, it won't randomly turn that into a journal entry. And if I have a short, boring day, it keeps the entry short instead of making stuff up to fill space. If something actually heavy comes up, it's not supposed to just slap a mood rating on it like everything's fine.

## Why I picked this one

Honestly I've tried to start journaling like 5 times and never stick with it because actually sitting down and writing a "proper" entry every night feels like effort. This way I just ramble about my day for a sec and it does the formatting part for me. This is one I'd actually keep using, not something I just made for the assignment.

## Tool used

Claude, built it right in the chat.

## Prompts I used

First I wasn't sure what skill to make so I asked Claude for ideas that would work across all 5 tasks, and it suggested a journaling one that could connect to Google Drive later. Once I picked that, I just said:

"ok so make it"

Then I asked it to review its own work:

"can you rate my skill out of 10 and keep improving it"

which is when it caught a few issues on its own - it was going to trigger too easily (even on random mentions of being tired), the reflection questions would repeat, and it wasn't handling short/boring days or heavier stuff well. It fixed all of that in the same version.

## How I tested it

- Saved the SKILL.md as a Skill in Claude
- Opened a completely new chat
- Just described my day normally, didn't mention "journal" or the skill name at all
- It picked up on it and formatted the entry automatically

(screenshot of this is in this folder)

## What worked / what didn't

Worked:
- It actually triggers just from talking normally, don't have to say "use my skill" or anything
- Format stayed the same across a good day, a boring day, and a stressful one

Ran into issues:
- At first it was too trigger-happy, would try to format even a random one-off comment about being tired into a full entry. Had to add a rule so it only does the full format when I'm actually recapping my day, not just mentioning a mood in passing.
- The reflection questions were the same 2 every time which would get old fast if I'm actually using this daily, so I had it rotate between a few different types of questions instead.

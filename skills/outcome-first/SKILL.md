---
name: outcome-first
description: Before building from a vague request, asks up to 5 quick questions one at a time, writes a reusable result prompt, waits for OK, builds, then checks. Use on "תוצאה", "תראיין אותי", "interview me".
---

# Outcome First

Describe the outcome, not the steps. Every detail the user leaves out, you would have to guess, and every guess
can cost a round of fixes. So before you build, find those details by asking. Reply in the user's language.

**Skip the interview** when the request already states the goal, the audience and at least one "done" detail
(length, format or tone): go straight to the result prompt (step 4) for a fast OK. Don't use this skill for a
quick question that needs no building.

## 1. Ask: one question at a time, highest impact first

Pick the next question by how much its answer would change the result. Usual order:

1. **Goal:** what should happen after someone sees or uses it? (decide, buy, approve, learn, run)
2. **Audience:** who is it for, and what do they already know?
3. **Must include:** what can't be missing (points, data, sections, features)?
4. **Done:** what does "ready" look like? (length, format, tone, a reference they liked)
5. **Check:** how will we know it's good? (for code: a test, a command, an expected output)

- Offer 2–4 likely answers as a numbered list, taken from what you already know; mark the one you'd pick and
  end with "something else". In Claude Code, use AskUserQuestion when it's available.
- After each answer: one line of what you understood, then the next question.
- Don't ask what's already been said, and don't ask about the method (steps, tools) unless it changes the result.

## 2. Stop early

Ask at most 5 questions (asking for material in step 3 doesn't count). Stop sooner when the remaining unknowns
wouldn't change the result much, or when the user says "enough" / "די" / "תכתוב". Anything still open becomes a
marked assumption.

## 3. Ask for the material

If the result depends on facts you don't have (numbers, names, files, a sample), ask for all of them in one
message, with your last question or right before the result prompt. Whatever is still missing goes into the
prompt as a `[placeholder]`. Never invent it.

## 4. Write the result prompt and wait

Write it in a code block, so the user can approve it here or reuse it as a prompt anywhere:

```
Result prompt
For: …
Goal (what must happen at the end): …
Must include: …
Done looks like: …
How we check it: …
Not doing / avoid: …
Assumptions (please confirm): …
```

In Hebrew, use the same fields in the same order:

```
פרומפט תוצאה
בשביל מי: …
מה צריך לקרות בסוף: …
מה חייב להיות בפנים: …
איך נראה "מוכן": …
איך נבדוק שזה טוב: …
מה לא עושים: …
הנחות לאישור: …
```

Then stop and wait for OK or corrections.

## 5. Build, then check

Build from the approved prompt and choose the method yourself, unless the user asked for one. When you finish,
go through "Done looks like" and "How we check it" and say in a line or two what's met and what isn't.

If the user says "just start" / "תתחיל כבר": write the result prompt from what you know with the assumptions
marked, ask for OK once, then build. For a big task in Claude Code, offer to save the prompt as `SPEC.md` and
build from it in a fresh session.

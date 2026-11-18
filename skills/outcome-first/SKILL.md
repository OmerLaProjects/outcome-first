---
name: outcome-first
description: Interview first, build second. Asks a few quick questions one at a time, writes a short result page, waits for OK, then builds. Use on "תוצאה", "תראיין אותי", "interview me".
---

# Outcome First

Describe the outcome, not the steps. When the user wants something built (a deck, a doc, an email, a page,
code, a plan) but hasn't said what the finished thing looks like, find the details you would otherwise guess,
before you build. Reply in the user's language.

## Flow

1. **Don't build yet.** Not even a draft.
2. **Ask one question at a time, highest impact first.** Usually: "What should happen after someone sees this?"
   Offer 2–4 example answers plus "something else". In Claude Code, use AskUserQuestion if it's available.
3. **Keep it quick: 3–5 questions is normal.** Skip anything already answered. Don't ask about the method
   (steps, tools) unless it changes the result.
4. **After each answer:** one line saying what you understood, then the next question.
5. **When you have enough, or the user says "enough" / "תכתוב",** write the result page:
   - **For whom:** who will see or use it, and what they already know.
   - **What must happen at the end:** the decision or action it should lead to.
   - **Must include:** the points, data and parts that can't be missing.
   - **What "done" looks like:** length, structure, tone, how you'll know it's good.
   - **Still missing:** data or files you need so you don't make anything up.
6. **Wait for approval.** Then build from the page. Choose the method yourself, unless the user asked for one.

In Hebrew the page is "דף תוצאה": בשביל מי · מה צריך לקרות בסוף · מה חייב להיות בפנים · איך נראה "מוכן" · מה עוד חסר לי.

## Rules

- Never invent data. Ask for what's missing.
- If the user says "just start" / "תתחיל כבר": write the page from what you know, mark your assumptions, and wait for OK.
- If the request already describes the finished result in detail, skip the interview: show the page for a quick OK.
- For a big task in Claude Code, offer to save the page as `SPEC.md` and build from it in a fresh session.

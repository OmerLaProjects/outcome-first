# outcome-first

**קודם שואלים, אחר כך בונים.** סקיל ל-Claude שמראיין אתכם בכמה שאלות קצרות, כותב בשבילכם "פרומפט תוצאה", מחכה לאישור, בונה, ובסוף בודק שהתוצאה עומדת במה שסיכמתם.

> "Describe the outcome, not the steps." (Anthropic, Claude Code docs)

## למה

כל פרט שלא כתבתם, Claude משלים לפי ניחוש, וכל ניחוש עלול לעלות עוד סבב תיקונים.
הסקיל הזה מוצא את הפרטים החסרים לפני שמתחילים: שאלה אחת בכל פעם, קודם השאלה שהכי משנה את התוצאה.

## איך משתמשים

כותבים ל-Claude **"תוצאה"** ואז מה שאתם רוצים, למשל:

```
תוצאה: מצגת לבוס על הרבעון האחרון
```

Claude ישאל עד 5 שאלות קצרות, כל פעם אחת, עם תשובות מוצעות לבחירה. אחר כך יכתוב "פרומפט תוצאה":
**בשביל מי · מה צריך לקרות בסוף · מה חייב להיות בפנים · איך נראה "מוכן" · איך נבדוק שזה טוב · מה לא עושים · הנחות לאישור**.
את הפרומפט אפשר לאשר, לתקן, או להעתיק ולהשתמש בו בכל צ'אט אחר. אחרי האישור Claude בונה, ובסוף בודק את התוצאה מול הפרומפט.

## התקנה

### claude.ai (אתר / אפליקציה)
1. מורידים את `outcome-first.zip` מ-[Releases](https://github.com/OmerLaProjects/outcome-first/releases/latest).
2. ב-Claude: **Customize → Skills → Upload skill**, ובוחרים את ה-ZIP.
3. אם אין אפשרות להעלות: בהגדרות צריך להפעיל יצירת קבצים / הרצת קוד.

### Claude Code
```
/plugin marketplace add OmerLaProjects/outcome-first
/plugin install outcome-first@outcome-first
```
או ידנית: מעתיקים את התיקייה `skills/outcome-first` אל `~/.claude/skills/`.

---

## English

**Interview first, build second.** A Claude skill that asks you up to five quick questions (one at a time,
highest impact first, with suggested answers), writes a reusable result prompt (for whom, goal, must include,
what "done" looks like, how we check it, what to avoid, assumptions), waits for your OK, builds, then checks the
result against the prompt.

- **claude.ai:** download `outcome-first.zip` from Releases → Customize → Skills → Upload.
- **Claude Code:** `/plugin marketplace add OmerLaProjects/outcome-first` then `/plugin install outcome-first@outcome-first`.
- **Use it:** start your request with "interview me" (or "תוצאה").

MIT License.

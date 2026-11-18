# outcome-first

**קודם שואלים, אחר כך בונים.** סקיל ל-Claude שמראיין אתכם בכמה שאלות קצרות, כותב "דף תוצאה", מחכה לאישור, ורק אז בונה.

> "Describe the outcome, not the steps." (Anthropic, Claude Code docs)

## למה

כל פרט שלא כתבתם, Claude משלים לפי ניחוש, וכל ניחוש עלול לעלות עוד סבב תיקונים.
הסקיל הזה מוצא את הפרטים החסרים לפני שמתחילים: שאלה אחת בכל פעם, קודם השאלה שהכי משנה את התוצאה.

## איך משתמשים

כותבים ל-Claude **"תוצאה"** ואז מה שאתם רוצים, למשל:

```
תוצאה: מצגת לבוס על הרבעון האחרון
```

Claude ישאל כמה שאלות (בדרך כלל 3–5), יכתוב דף תוצאה:
**בשביל מי · מה צריך לקרות בסוף · מה חייב להיות בפנים · איך נראה "מוכן" · מה עוד חסר**,
ויחכה ל"מאשר" לפני שהוא בונה.

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

**Interview first, build second.** A Claude skill that asks you a few quick questions (one at a time, highest
impact first), writes a short result page (for whom, what must happen, must include, what "done" looks like,
what's missing), waits for your OK, then builds.

- **claude.ai:** download `outcome-first.zip` from Releases → Customize → Skills → Upload.
- **Claude Code:** `/plugin marketplace add OmerLaProjects/outcome-first` then `/plugin install outcome-first@outcome-first`.
- **Use it:** start your request with "interview me" (or "תוצאה").

MIT License.

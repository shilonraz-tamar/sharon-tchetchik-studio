# 📤 איך להעלות לגיטהאב (הוראות לתמר)

## אופציה א׳ — דרך GitHub CLI (הכי פשוט, 2 דקות)

```bash
cd /Users/tamarshilo/Sharon-Tchetchik/plugin

# יצירת repo פרטי והעלאה בפקודה אחת:
gh repo create claude-code-sharon-studio \
  --private \
  --source=. \
  --description "יועץ עסקי ושיווקי אישי לסטודיו שרון צ׳צ׳יק" \
  --push
```

**אם לא מותקן gh:** `brew install gh && gh auth login`

---

## אופציה ב׳ — ידנית (אם gh לא עובד)

```bash
cd /Users/tamarshilo/Sharon-Tchetchik/plugin

git init
git add .
git commit -m "feat: initial Sharon Studio Claude Code plugin"

# ב-github.com: צור repo חדש פרטי בשם claude-code-sharon-studio
# אז:
git branch -M main
git remote add origin https://github.com/<USERNAME>/claude-code-sharon-studio.git
git push -u origin main
```

---

## 📱 הודעה לשרון (העתק-הדבק)

```
שרון! 🌸

בניתי לך יועץ עסקי-שיווקי אישי שמכיר את העסק שלך מבפנים.
כל פעם שתרצי לדבר, לקבל החלטה, או סתם לחשוב בקול — הוא פה.

3 צעדים של 5 דקות:

1. פתחי טרמינל (אייקון שחור בדוק, או: Cmd+Space → "Terminal")

2. הדביקי את זה (להתקין את קלוד):
curl -fsSL https://claude.ai/install.sh | sh

3. הדביקי את זה (להתקין את היועץ שלך):
claude plugin marketplace add tamarshilon/claude-code-sharon-studio
claude plugin install sharon-studio

זהו! עכשיו כל פעם שתרצי לדבר — פותחת טרמינל, כותבת:
claude

ושואלת מה שתרצי. למשל:
- "על מה להתמקד החודש?"
- "כמה לגבות על סט ל-30 איש?"
- "איך לבנות חבילת VIP?"

הוא מכיר הכל — ענייני הכסף, הלקוחות, החזון, הכלים.
תמר 💕
```

---

## 🔄 עדכונים עתידיים

אחרי שינויים בקבצי הסקיל:

```bash
cd /Users/tamarshilo/Sharon-Tchetchik/plugin
git add .
git commit -m "update: <מה שינית>"
git push
```

שרון תקבל את העדכונים בפעם הבאה שתריץ:
```bash
claude plugin update sharon-studio
```

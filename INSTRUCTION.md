# MYBLOG — Writing a New Post Instruction

## 📝 Quick Workflow

1. **Open Obsidian**, navigate to `content/posts/`
2. **Create new Markdown file** — use an existing post as template, or start fresh
3. **Write content** in Arabic (RTL), following the rules below
4. **Save** — Obsidian Git plugin will auto-stage, or use terminal:
   ```bash
   git add .
   git commit -m "Add: new post title"
   git push origin main
   ```
5. **Verify** at `https://naba-r.dev/`

---

## 📄 Frontmatter Format (keep exactly)

```yaml
---
title: "عنوان المقالة"
tags:
  - شروح
  - عن لينكس
draft: false
date: 2026-11-11
description: "اختياري: وصف مختصر للمقال"
---
```

**Rules:**
- `title`: Arabic title (required)
- `tags`: Use only from approved list: `شروح`, `عن لينكس`, `توزيعات`, `برامج`
- `draft`: `true` or `false` — set to `false` when ready to publish
- `date`: `YYYY-MM-DD` format — **must not be in the future**
- `description`: Optional summary (appears in meta tags)

---

## 🌐 Arabic Writing Rules (quick reference)

### Terminology (always use terms from `~/Documents/PersonalNotes/My Notes/مصطلحات المدونة`):
- **First mention**: ** Arabic term English ** (bold Arabic, English in parentheses, no separate brackets)
  - Example: **نظام الملفات (File System)** و**نافذة السياق (Context Window)**
- After first mention: use Arabic term alone
- **Never** use synonyms from the table — always the exact Arabic term listed

### Arabic Punctuation (use Arabic marks, not English):
- Comma: `،` (not `,`)
- Semicolon: `;` (not `;`)
- Colon: `:` (not `:`)
- Period: `.` (same)
- Question mark: `؟` (not `?`)
- Exclamation: `!` (same)
- Arabic quotes: `« »` (not `"` or `'`)

### Code & Commands:
- Inline code: `sudo apt update` (backticks)
- Paths: `/home/user/` (backticks)
- Never put Arabic inside code blocks unless it's part of a real file/program

### Writing Style:
- Modern Standard Arabic
- Friendly, flowing, human — not robotic
- Mentor-storyteller style with light metaphors
- Balance clarity + beauty
- Short paragraphs (≤4 lines preferred)
- Vary sentence length — mix balanced sentences with shorter confirming sentences

### What NOT to change (your approval rule):
- Do not modify frontmatter fields (`title`, `tags`, `draft`, `date`, `description`)
- Do not change approved tags
- Do not alter existing terminology in posts you're reviewing
- Do not translate product names or project names

---

## 🏷️ Approved Tags Only

Use exactly these tag values (expanded from 4 to 7):
- `مقال` - articles/personal posts (used 9 times)
- `لينكس` - Linux (used 19 times) *[approved form: `عن لينكس` for "about Linux" context]*
- `شروحات` - tutorials/guides *[approved alternative: `شروح`]* (used 6 times)
- `عن لينكس` - about Linux *[approved form: `لينكس` for standalone tag]* (common context)
- `توزيعات` - distributions (used 3 times)
- `برامج` - programs/software (used 1 time)
- `العاب` - games *[only if writing about games]* (used 1 time)

**Do not add other tags** or translate them to English.

**Tag spelling guidance:** 
- Use `شروح` as the singular/preferred form; `شروحات` (plural) is commonly used and acceptable
- Use `لينكس` as the standalone tag; `عن لينكس` is approved for "about Linux" context in frontmatter

**Variant note:** `برامح` is a common variant of `برامج` — both are acceptable, but `برامج` is the approved standard.

---

## 📌 Before You Start Writing

1. **Check the terminology table** for any key technical terms — use the exact Arabic entry, not a substitute
2. **Confirm your tag choice** is from the approved list of 4
3. **Ensure the date is not in the future** (use today's date or a past date)
4. **Review existing posts** in `content/posts/` for style consistency if this is your first post in a while

---

## 💾 After Writing

1. **Save in Obsidian** — the file appears in `content/posts/`
2. **Commit & push**:
   ```bash
   git add .
   git commit -m "Add: your title here"
   git push origin main
   ```
3. **GitHub Actions auto-builds** (1–2 minutes)
4. **Check your post at** `https://naba-r.dev/`

---

## ⚠️ Reminders

- **Your approval rule**: "don't change or delete anything without my approval"
- **Terminology**: Always use terms from the `مصطلحات المدونة` table — exact matches, no synonyms
- **Tags**: Only the 4 approved values
- **Frontmatter**: Keep the format as shown — do not add/remove fields
- **Date**: Must be `YYYY-MM-DD` and not in the future

*This file is your one-reference guide for writing new posts. Keep it in the repo root. It will not appear on your live site.*
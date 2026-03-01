# 🤝 Contributing Guide

> This guide is built by students, for students. Every contribution makes it better for the next person.

---

## Why Contribute?

- Help thousands of students get more out of their free tools
- Build your open source contribution history (visible on GitHub profile)
- Learn by explaining — teaching others solidifies your own understanding
- Add your project to the showcase and get visibility

---

## What We Need

### 🔥 Most Wanted Contributions

1. **Tool activation tips** — Did you find a faster or easier way to claim a specific tool? Add it to [`docs/activation.md`](docs/activation.md)

2. **Claude prompts** — Have a Claude prompt that helped you build something specific? Add it to [`docs/prompt-library.md`](docs/prompt-library.md)

3. **Project showcases** — Built something with the pack? Add it to the [Project Showcase](#project-showcase) below

4. **Bug reports** — Found outdated information (an offer changed, a link broke)? Open an issue

5. **New app ideas** — Have a revenue app idea with a solid build plan? Add it to [`docs/app-ideas.md`](docs/app-ideas.md)

6. **Translations** — Translate the guide to another language (create `docs/[language-code]/`)

---

## How to Contribute

### Option 1: Edit Directly on GitHub (Easiest)

1. Click the ✏️ edit button on any file on GitHub
2. Make your changes in the editor
3. Scroll down → "Propose changes"
4. GitHub automatically creates a fork and PR for you

### Option 2: Fork and Pull Request

```bash
# 1. Fork this repo on GitHub (click "Fork" button)

# 2. Clone your fork
git clone https://github.com/YOUR_USERNAME/student-pack-guide.git
cd student-pack-guide

# 3. Create a branch
git checkout -b add-my-tip

# 4. Make your changes
# Edit the relevant file

# 5. Commit
git add .
git commit -m "Add [description of what you added]"

# 6. Push
git push origin add-my-tip

# 7. Open a Pull Request on GitHub
# Go to the original repo → "Pull requests" → "New pull request"
```

---

## Contribution Guidelines

### For Tool Tips (activation.md)

When adding a tip for a tool, include:
- The tool name as a header
- What the tip is
- Why it helps

**Good tip format:**
```markdown
### MongoDB Atlas Pro Tip
When setting up your cluster, choose the free tier (M0) in a region 
closest to your DigitalOcean server (e.g., both in NYC). This reduces 
latency from ~80ms to ~5ms and makes your app noticeably faster.
```

### For Claude Prompts (prompt-library.md)

When adding a prompt, include:
- A descriptive title
- The phase (architecture / database / api / frontend / backend / monetization / marketing / debugging / devops / testing / growth)
- The prompt itself in a code block
- (Optional) What you used it for

**Good prompt format:**
```markdown
**Your Prompt Title**
```
[The actual prompt with [placeholders] for things users need to fill in]
```
```

### For App Ideas (app-ideas.md)

When adding an app idea, include:
- App name and one-line pitch
- The problem it solves
- Revenue model and target MRR
- Tech stack using only pack tools
- Claude AI role
- Cursor AI role
- Estimated time to MVP

### For the Project Showcase

When adding your project:
- App name (link to live URL or GitHub)
- What it does (one sentence)
- Pack tools you used
- Revenue (optional — only share if you're comfortable)
- Time it took to build

---

## What Not to Add

- Affiliate links or promotional content
- Information about non-pack tools (unless they're free and complement pack tools)
- Outdated offers (check the pack page before adding)
- Low-effort additions (single-word tips, placeholder content)

---

## Commit Message Format

Use clear, descriptive commit messages:

```
✅ Good:
"Add MongoDB Atlas latency optimization tip to activation.md"
"Add Claude prompt for Stripe webhook handler to prompt-library.md"
"Fix broken Namecheap activation link"

❌ Bad:
"Update file"
"Fix stuff"
"Added things"
```

---

## Project Showcase

*Add your project here! Edit this file and add a row to the table.*

| Project | Description | Pack Tools Used | Built By |
|---|---|---|---|
| *Your project here* | *What it does* | *Which tools* | *Your GitHub* |

**To add your project:**
1. Edit this file
2. Add a new row to the table above
3. Submit a PR with the title "Showcase: [Your Project Name]"

---

## Recognition

All contributors are listed in the [Contributors](https://github.com/zawar112/student-pack-guide/graphs/contributors) section automatically by GitHub.

Significant contributors (5+ merged PRs) get:
- Listed in the README acknowledgements section
- A shoutout on Twitter/X when we hit contribution milestones

---

## Questions?

Open a [Discussion](https://github.com/zawar112/student-pack-guide/discussions) — we're friendly and will help you get your contribution merged.

---

*Thank you for helping other students. Every tip you add saves someone hours of frustration.* 🙏

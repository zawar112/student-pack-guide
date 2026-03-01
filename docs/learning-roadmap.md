# 📚 Learning Roadmaps

> Three paths. All using free tools from your GitHub Student Developer Pack.
> Pick the one that matches where you are right now.

---

## 🟢 Beginner — Zero to First Project (30 Days)

**Who this is for:** You're new to coding or just getting started. You want to build something real as fast as possible.

**Goal by end:** A deployed personal project on GitHub Pages with a working backend.

---

### Week 1 — Learn the Fundamentals

**Day 1–3: HTML, CSS & JavaScript basics**
- Platform: **Codedex** (free 6 months with pack)
- Complete: Python or JavaScript beginner track
- Why Codedex: Gamified, modern, and explains things simply

**Day 4–5: Git & GitHub**
- Resource: GitHub's [Intro to GitHub](https://github.com/skills/introduction-to-github) experience (free, in browser)
- What to do: Complete the whole course — it takes 1 hour
- Install: **GitHub Desktop** (free, no command line needed yet)

**Day 6–7: Your first project**
- Use **GitHub Codespaces** to write code in the browser
- Build: A simple HTML page about yourself
- Deploy: Push to GitHub → enable **GitHub Pages** → you have a live website

**Tools used this week:** Codedex, GitHub Pro, GitHub Desktop, GitHub Codespaces, GitHub Pages

---

### Week 2 — JavaScript & Frontend

**Day 8–12: Interactive JavaScript**
- Platform: **Scrimba** (1 month free with pack)
- Complete: "Learn JavaScript for Free" course
- Why Scrimba: You code inside the video — fastest way to learn JS

**Day 13–14: Make your site interactive**
- Add JavaScript to your Week 1 project
- Use **GitHub Copilot** to help you write code
- How: Type a comment describing what you want, Copilot writes the code

**Tools used this week:** Scrimba, GitHub Copilot Pro, GitHub Codespaces

---

### Week 3 — Backend Basics

**Day 15–18: Node.js introduction**
- Platform: **FrontendMasters** (6 months free)
- Course: "Complete Intro to Web Dev" by Brian Holt
- Learn: How servers work, basic Node.js, APIs

**Day 19–21: Your first database**
- Set up **MongoDB Atlas** (free with pack)
- Use **Claude AI** to design your first schema:
  ```
  Ask Claude: "I want to build a simple todo app. 
  Design a MongoDB schema for it and show me how 
  to connect it with Node.js using Mongoose."
  ```

**Tools used this week:** FrontendMasters, MongoDB Atlas, Claude AI, GitHub Copilot

---

### Week 4 — Build & Deploy

**Day 22–25: Build your first full-stack app**
- Combine everything: HTML frontend + Node.js backend + MongoDB database
- Use **Cursor AI** to help write code faster:
  1. Describe what you want in a comment
  2. Press Ctrl+K → Cursor generates the code
  3. Review and accept what makes sense

**Day 26–28: Deploy to the internet**
- Deploy backend on **Heroku** (free credits in pack)
- Or deploy on **DigitalOcean** App Platform ($200 credit)
- Your site is live on a real server

**Day 29–30: Share your work**
- Add your project to **GitHub Community Exchange**
- Update your **GitHub profile README** (use the Profile README experience)
- Share on LinkedIn

**🎉 Milestone: You have a deployed full-stack app. You're no longer a beginner.**

---

### Beginner Resources Quick Reference

| Skill | Platform | Time |
|---|---|---|
| HTML/CSS/JS basics | Codedex | 2 weeks |
| JavaScript depth | Scrimba | 1 week |
| Node.js & backend | FrontendMasters | 1 week |
| Database | MongoDB (docs + Claude) | 3 days |
| Git | GitHub Skills | 1 day |
| Deployment | DigitalOcean / Heroku | 2 days |

---

## 🟡 Intermediate — Full-Stack Web Developer (60 Days)

**Who this is for:** You know HTML, CSS, JavaScript basics. You want to build proper full-stack web apps and understand modern development practices.

**Goal by end:** A full-stack web app with auth, a database, API, deployed to production with CI/CD.

---

### Month 1 — Modern Full-Stack Development

**Week 1: React & Modern Frontend**
- Platform: **FrontendMasters**
- Courses:
  - "Complete Intro to React v8" by Brian Holt
  - "CSS for JavaScript Developers" by Josh Comeau
- Use **GitHub Copilot** for autocomplete while practicing
- Build: Rewrite your beginner project as a React app

**Week 2: Backend APIs**
- Learn: REST API design, Express.js, middleware
- Use Claude AI to learn faster:
  ```
  Ask Claude: "Explain REST API design principles 
  with a practical example. Show me how to build 
  a user authentication API in Express.js with 
  JWT tokens, including registration, login, 
  and protected route middleware."
  ```
- Build with **Appwrite**: Replace your custom auth with Appwrite's built-in auth system
- Set up **Doppler** for secrets management — no more .env files

**Week 3: Databases at Depth**
- Platform: **Educative** (6 months free)
- Course: "MongoDB Essentials" or "Designing Data-Intensive Applications"
- Also: **DataCamp** SQL courses (3 months free) — SQL is essential even for NoSQL developers
- Practice: Use **PopSQL** or **SQLGate** to write and visualize queries

**Week 4: TypeScript**
- Platform: **FrontendMasters**
- Course: "TypeScript Fundamentals" by Mike North
- Convert your project to TypeScript
- Use Cursor AI to help with type errors:
  ```
  Select error in Cursor → Ctrl+K → "Fix this TypeScript error"
  ```

---

### Month 2 — Production-Ready Development

**Week 5: Testing**
- Learn: Jest for unit tests, Playwright for end-to-end tests
- Use Claude to write tests:
  ```
  Ask Claude: "Write a comprehensive Jest test suite 
  for this function: [paste your function]. Include 
  happy path, edge cases, and error handling tests."
  ```
- Set up **Codecov** to track your test coverage on every PR
- Run cross-browser tests on **BrowserStack** (real devices)

**Week 6: DevOps & CI/CD**
- Set up **Travis CI** or **GitHub Actions** for automated testing
- Learn Docker basics
- Deploy to **DigitalOcean** with automated deploys:
  ```yaml
  # .github/workflows/deploy.yml
  on:
    push:
      branches: [main]
  jobs:
    deploy:
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
        - run: npm test
        - run: ssh user@your-server 'cd /app && git pull && npm install && pm2 restart app'
  ```

**Week 7: Monitoring & Observability**
- Set up **Sentry** for error tracking (5 minutes to integrate)
- Configure **Datadog** or **New Relic** for performance monitoring
- Add **SimpleAnalytics** for privacy-friendly traffic data
- Learn to read logs, traces, and metrics

**Week 8: Security**
- Use **1Password** for all credentials
- Configure **Doppler** across all environments
- Set up **AstraSecurity** firewall on your app
- Learn: OWASP Top 10, input validation, rate limiting

**🎉 Milestone: You can build, test, deploy, and monitor production applications.**

---

### Intermediate Resources Quick Reference

| Skill | Platform | Time |
|---|---|---|
| React | FrontendMasters | 1.5 weeks |
| Backend APIs | Educative + Claude AI | 1 week |
| TypeScript | FrontendMasters | 1 week |
| Databases | DataCamp + MongoDB | 1 week |
| Testing | Claude AI + BrowserStack | 1 week |
| DevOps/CI/CD | GitHub Actions + Travis CI | 1 week |
| Monitoring | Sentry + Datadog | 3 days |
| Security | 1Password + Doppler | 2 days |

---

## 🔴 Advanced — Production SaaS With Paying Customers (90 Days)

**Who this is for:** You're already a capable developer. You want to go from "I can build things" to "I'm building things that make money."

**Goal by end:** A live SaaS product with at least $500 MRR (Monthly Recurring Revenue).

---

### Phase 1: Architecture (Days 1–14)

**Design your system before writing a line of code**

Use Claude AI to generate your entire technical architecture:
```
Prompt: "I'm building [app idea] for [audience]. 
Expected scale: 0–1,000 users in 6 months. 
Revenue model: [subscription/usage/etc].
Design: system architecture, database schema, 
API structure, authentication approach, 
deployment strategy. Use only free tools 
from the GitHub Student Developer Pack."
```

**Key decisions to make:**
- Multi-tenancy strategy (row isolation vs schema isolation vs separate DBs)
- Auth provider (Appwrite vs custom JWT vs Auth0)
- API style (REST vs GraphQL vs tRPC)
- Hosting strategy (DigitalOcean vs Azure vs Heroku)
- Background jobs approach (Bull.js vs Bee-Queue vs cloud functions)

**Tools for architecture phase:**
- **Claude AI** — design decisions, tradeoffs analysis
- **Cursor AI** — scaffold the project structure from your spec
- **Notion** — document all decisions as Architecture Decision Records (ADRs)
- **ToDiagram** — visualize your system architecture

---

### Phase 2: Build (Days 15–45)

**The Claude + Cursor workflow at advanced level:**

1. **Plan with Claude:**
   ```
   "Write a detailed spec for the [feature] module.
   Include: API endpoints (OpenAPI format), 
   database operations, business logic rules,
   error states, and edge cases to handle."
   ```

2. **Implement with Cursor:**
   - Open your project in Cursor
   - Create a new file
   - Paste Claude's spec as a comment block
   - Cursor generates the implementation

3. **Test immediately:**
   - Claude writes test cases
   - Cursor implements them
   - Travis CI runs them automatically

4. **Deploy continuously:**
   - Every merge to `main` → GitHub Actions → DigitalOcean
   - Zero-downtime deploys with health checks

**Advanced patterns to implement:**
- Event-driven architecture with webhooks
- Idempotent API operations (safe to retry)
- Background job queues for async operations
- Database connection pooling
- Redis caching layer
- Rate limiting per user tier

---

### Phase 3: Revenue (Days 46–70)

**Stripe integration (advanced)**

Use Claude to build your entire billing system:
```
Ask Claude: "Build a complete SaaS billing system 
with Stripe. Include: free trial with credit card, 
subscription tiers (Free/Pro/Team), usage metering 
for [feature], overage charges, annual vs monthly 
toggle with 20% discount, dunning emails for 
failed payments, and a customer billing portal."
```

**The $1,000 fee waiver strategy:**
- Stripe waives fees on your first $1,000 in revenue
- That's ~$30 saved on a $30/month product × 33 customers
- Front-load your acquisition — get your first 30 paying customers fast

**Pricing strategy:**
- Use **DevCycle** to A/B test your pricing page
- Track conversion rates in **SimpleAnalytics**
- Use **Appfigures** if you have a mobile companion app
- Analyze cohorts in **Datadog** dashboards

---

### Phase 4: Scale (Days 71–90)

**When things start working:**

**Performance optimization:**
- Profile with **Datadog APM** — find slow endpoints
- Use **Blackfire** for PHP apps — find slow functions
- Add **Imgbot** — automatic image optimization in your repo

**Feature development velocity:**
- Use **ConfigCat** feature flags for gradual rollouts
- Use **DevCycle** for A/B experiments
- Track code health with **CodeScene**
- Maintain test coverage above 80% with **Codecov**

**Security hardening:**
- Enable **AstraSecurity** WAF
- Rotate secrets in **Doppler**
- Audit dependencies with GitHub's Dependabot
- Implement rate limiting per user tier

**Team operations:**
- Use **DailyBot** for async standups if you have co-founders
- Track tasks in **Notion**
- Use **GitHub Projects** for sprint planning

**🎉 Milestone: Live SaaS product, real customers, recurring revenue.**

---

### Advanced Learning Resources

Even at this level, keep learning. The pack gives you:

| Topic | Resource | How |
|---|---|---|
| System Design | **Educative** — Grokking System Design | 6 months free |
| Data Engineering | **DataCamp** — Data Engineering track | 3 months free |
| Cloud Architecture | **Microsoft Azure** — learn.microsoft.com | Free with credit |
| Coding Interviews | **AlgoExpert** | 20 free questions |
| Geospatial Dev | **CARTO** | Free 2-year account |
| ML Integration | **Camber** | 200 CPU hours free |

---

## 🗺 Choosing Your Learning Path

Not sure which path to pick? Answer these:

**Q: Have you ever built a webpage from scratch?**
- No → 🟢 Beginner
- Yes, with HTML/CSS → continue

**Q: Have you built a backend API that reads/writes to a database?**
- No → 🟡 Intermediate
- Yes → continue

**Q: Have you shipped something with real users (even for free)?**
- No → 🟡 Intermediate (focus on the deployment/monitoring weeks)
- Yes → 🔴 Advanced

---

## 📅 Combined Timeline

If you're ambitious and want to go from beginner to revenue in 6 months:

```
Month 1:  Beginner track → first project deployed
Month 2:  Intermediate track (frontend + backend)
Month 3:  Intermediate track (testing + DevOps)
Month 4:  Advanced phase 1 → architecture your SaaS
Month 5:  Advanced phase 2 → build it
Month 6:  Advanced phases 3&4 → launch + first revenue
```

---

*Have a learning resource to add? [Contribute here](../CONTRIBUTING.md)*

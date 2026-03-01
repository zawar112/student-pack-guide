# 🛠 Tool Activation Guide

> Step-by-step instructions to claim every tool in the GitHub Student Developer Pack.
> **Start here first.** Claim tools in the order listed — infrastructure first, then everything else.

---

## ✅ Before You Begin

1. Go to [education.github.com/pack](https://education.github.com/pack)
2. Click **"Sign up for Student Developer Pack"**
3. Verify with your **school email** (.edu) or **student ID photo**
4. Wait 1–3 days for approval (usually faster)
5. Once approved, come back to this guide

> 💡 **Tip:** Use your university email address. It's the fastest verification method.

---

## 🔢 Priority Order (Claim These First)

These tools give you the most value immediately and are needed to build anything:

| Priority | Tool | Why First |
|---|---|---|
| 1 | GitHub Pro + Copilot | Free AI coding assistant — use it from day 1 |
| 2 | DigitalOcean | $200 credit — your hosting for the whole year |
| 3 | Namecheap | Free domain + SSL — you need this to launch |
| 4 | MongoDB | $50 credit + database for your apps |
| 5 | Stripe | Waived fees on first $1K revenue |
| 6 | Appwrite | Free backend-as-a-service |
| 7 | 1Password | Secure your credentials before you have many |
| 8 | Doppler | Manage secrets from the start |

---

## ☁️ Infrastructure & Hosting

### GitHub Pro
- **Offer:** Free GitHub Pro while you're a student
- **How to claim:** Go to [github.com/education](https://github.com/education) → sign in with your student-verified account → Pro is automatically applied
- **What you get:** Unlimited private repos, GitHub Actions minutes, Packages, advanced code insights
- **Use it for:** Every project you build. This is your foundation.

### GitHub Copilot Pro
- **Offer:** Free Copilot Pro while you're a student
- **How to claim:** Settings → Code, planning, and automation → Copilot → Sign up for free (requires GitHub Pro first)
- **What you get:** AI code autocomplete, multi-line suggestions, chat in editor
- **Use it for:** Speed up every line of code you write. Works in VS Code, JetBrains, Neovim.

### GitHub Codespaces
- **Offer:** Free Pro-level cloud dev environments
- **How to claim:** Automatically included with GitHub Pro
- **What you get:** Full VS Code in the browser, 60 hours/month of compute
- **Use it for:** Code from any device. No local setup needed. Pairs perfectly with Cursor.

### DigitalOcean
- **Offer:** $200 in platform credit for 1 year
- **How to claim:** Visit [digitalocean.com](https://digitalocean.com) → Connect GitHub account → Credit applied automatically
- **What you get:** Droplets (VMs), managed databases, App Platform, Spaces (object storage)
- **Use it for:** Hosting your web apps and APIs. $200 runs a basic app for 12+ months.
- **Pro tip:** Use App Platform for easy deploys — just connect your GitHub repo

### Microsoft Azure
- **Offer:** $100 credit + 25+ free services (age 18+)
- **How to claim:** [azure.microsoft.com/free/students](https://azure.microsoft.com/free/students) → Sign in with school email
- **What you get:** VM, Functions, AI services, SQL Database, Blob Storage, DevOps
- **Use it for:** Serverless functions, AI APIs (Azure OpenAI), and backup hosting

### Heroku
- **Offer:** $13/month credit for 24 months ($312 total)
- **How to claim:** Connect GitHub on the Heroku pack page
- **What you get:** Platform credits for dynos and add-ons
- **Use it for:** Quick deployments when you don't want to manage infrastructure

### GitHub Codespaces (Detailed Setup)
```bash
# Create a new codespace from any repo
# 1. Go to your repo on GitHub
# 2. Click green "Code" button → Codespaces tab → Create codespace
# 3. VS Code opens in your browser with full terminal
# 4. Install Cursor extension for AI assistance
```

### LocalStack
- **Offer:** Free license for AWS service emulation
- **How to claim:** [localstack.cloud](https://localstack.cloud) → Connect GitHub
- **What you get:** Run 80+ AWS services locally (S3, Lambda, DynamoDB, SQS, etc.)
- **Use it for:** Building AWS-compatible apps without an AWS account or costs

---

## 🗄 Backend & Database

### MongoDB Atlas
- **Offer:** $50 in Atlas credits + MongoDB Compass + $150 certification value
- **How to claim:** [mongodb.com](https://mongodb.com) → Connect GitHub account
- **What you get:** Cloud database, visual query tool, free certification
- **Use it for:** The database for almost every app you build. Scales from 0 to millions.
- **Quick start:**
  ```bash
  # After creating your cluster:
  npm install mongoose
  # Connect string format:
  # mongodb+srv://<user>:<pass>@cluster0.xxxxx.mongodb.net/<dbname>
  ```

### Appwrite
- **Offer:** Education plan — 10 projects at Pro limits ($160/month value)
- **How to claim:** [appwrite.io](https://appwrite.io) → Connect GitHub
- **What you get:** Auth, databases, storage, cloud functions, realtime — all in one
- **Use it for:** Replace your entire backend for small-to-medium apps
- **Quick start:**
  ```bash
  npm install appwrite
  # Then in your app:
  import { Client, Account } from 'appwrite';
  const client = new Client().setEndpoint('https://cloud.appwrite.io/v1').setProject('YOUR_PROJECT_ID');
  ```

### Doppler
- **Offer:** Free Team subscription
- **How to claim:** [doppler.com](https://doppler.com) → Connect GitHub
- **What you get:** Centralized secrets management, syncs to all environments
- **Use it for:** Replace .env files. Never commit a secret again.
- **Quick start:**
  ```bash
  npm install -g @dopplerhq/cli
  doppler login
  doppler setup
  doppler run -- node server.js  # injects secrets automatically
  ```

### Testmail
- **Offer:** Free Essential plan
- **How to claim:** [testmail.app](https://testmail.app) → Connect GitHub
- **What you get:** Unlimited email addresses for automated testing
- **Use it for:** Testing email flows (signup, password reset, notifications)

### Requestly
- **Offer:** Professional plan free for 1 year ($270 value)
- **How to claim:** [requestly.io](https://requestly.io) → Connect GitHub
- **What you get:** Intercept and mock HTTP requests, redirect APIs, inject scripts
- **Use it for:** Frontend development without a real backend, API debugging

### Pageclip
- **Offer:** Free basic plan
- **How to claim:** [pageclip.co](https://pageclip.co) → Connect GitHub
- **What you get:** Form backend for static sites
- **Use it for:** Contact forms, waitlist signups on GitHub Pages sites

### ConfigCat
- **Offer:** 1,000 feature flags, unlimited users
- **How to claim:** [configcat.com](https://configcat.com) → Connect GitHub
- **What you get:** Feature flag management, A/B testing capability
- **Use it for:** Ship features to specific users, run experiments safely

---

## 💳 Payments & Revenue

### Stripe
- **Offer:** Waived transaction fees on your first $1,000 in revenue
- **How to claim:** Use your unique pack link → create Stripe account
- **What you get:** Keep 100% of your first $1,000 (normally Stripe takes 2.9% + 30¢)
- **Use it for:** Every app that charges money. The industry standard.
- **Quick start with Claude:**
  ```
  Ask Claude: "Write a complete Stripe integration for a $29/month SaaS subscription 
  in Node.js. Include: customer creation, subscription, webhook handler for 
  payment_intent.succeeded and customer.subscription.deleted events."
  ```

### Blockchair
- **Offer:** 100,000 free API requests
- **How to claim:** [blockchair.com](https://blockchair.com) → Connect GitHub
- **What you get:** Blockchain data API for Bitcoin, Ethereum, and 15+ chains
- **Use it for:** Crypto analytics tools, blockchain explorers, wallet trackers

---

## 🎨 Frontend & Design

### Bootstrap Studio
- **Offer:** Free license while a student
- **How to claim:** [bootstrapstudio.io](https://bootstrapstudio.io) → Connect GitHub
- **What you get:** Visual drag-and-drop web design with Bootstrap
- **Use it for:** Build landing pages and UI mockups without writing raw HTML/CSS

### Polypane
- **Offer:** Free individual plan for 1 year
- **How to claim:** [polypane.app](https://polypane.app) → Connect GitHub
- **What you get:** Developer browser showing multiple screen sizes simultaneously
- **Use it for:** Responsive design — see mobile, tablet, and desktop at the same time

### Icons8
- **Offer:** 3-month subscription (icons, photos, illustrations, music)
- **How to claim:** [icons8.com](https://icons8.com) → Connect GitHub
- **What you get:** Millions of icons, UI illustrations, stock photos, background music
- **Use it for:** Making your app look professional without a designer

### IconScout
- **Offer:** 60 premium icons monthly for 1 year
- **How to claim:** [iconscout.com](https://iconscout.com) → Connect GitHub
- **What you get:** Access to 4.9M+ icons, illustrations, 3D assets, Lottie animations
- **Use it for:** App icons, UI elements, marketing assets

### Octicons
- **Offer:** Free open-source icon library
- **How to claim:** [primer.style/octicons](https://primer.style/octicons) — free, no signup needed
- **What you get:** GitHub's official icon system via Figma and npm
- **Use it for:** Developer-focused apps that should feel like GitHub

### Visme
- **Offer:** 3 months free Starter plan
- **How to claim:** [visme.co](https://visme.co) → Connect GitHub
- **What you get:** Presentations, data visualizations, infographics, short videos
- **Use it for:** Pitch decks, demo videos, marketing materials for your app

### Bootstrap Studio Setup
```bash
# After designing in Bootstrap Studio:
# Export your design → get clean HTML/CSS/JS
# Drop exported files into your project
# Use Cursor to add interactivity and backend connections
```

---

## ⚙️ DevOps, CI/CD & Testing

### Travis CI
- **Offer:** Free private builds while a student
- **How to claim:** [travis-ci.com](https://travis-ci.com) → Connect GitHub
- **What you get:** Automated testing on every push
- **Quick setup:**
  ```yaml
  # .travis.yml in your repo root
  language: node_js
  node_js:
    - 18
  script:
    - npm test
    - npm run build
  deploy:
    provider: script
    script: bash deploy.sh
    on:
      branch: main
  ```

### BrowserStack
- **Offer:** Free Automate Mobile Plan (1 parallel, 1 year)
- **How to claim:** [browserstack.com](https://browserstack.com) → Connect GitHub
- **What you get:** Real device cloud — test on 2,000+ real browsers and devices
- **Use it for:** Making sure your app works on Android Chrome, Safari iOS, etc.

### LambdaTest
- **Offer:** Free Live plan for 1 year
- **How to claim:** [lambdatest.com](https://lambdatest.com) → Connect GitHub
- **What you get:** Cross-browser testing on 2,000+ browser/OS combinations
- **Use it for:** Automated Selenium/Cypress tests in the cloud

### Codecov
- **Offer:** Free for public and private repos
- **How to claim:** [codecov.io](https://codecov.io) → Connect GitHub
- **What you get:** Code coverage reports on every pull request
- **Quick setup:**
  ```yaml
  # Add to .github/workflows/test.yml
  - name: Upload coverage
    uses: codecov/codecov-action@v3
    with:
      token: ${{ secrets.CODECOV_TOKEN }}
  ```

### DeepScan
- **Offer:** Free 6-month trial
- **How to claim:** [deepscan.io](https://deepscan.io) → Connect GitHub
- **What you get:** Advanced JavaScript static analysis (finds bugs Eslint misses)
- **Use it for:** Catching runtime errors before production

### CodeScene
- **Offer:** Free student account
- **How to claim:** [codescene.com](https://codescene.com) → Connect GitHub
- **What you get:** Technical debt analysis, complexity hotspots, code health metrics
- **Use it for:** Understanding which parts of your codebase need refactoring

### Imgbot
- **Offer:** Free for all repos while a student
- **How to claim:** [imgbot.net](https://imgbot.net) → Install GitHub App
- **What you get:** Automatic image compression via pull requests
- **Use it for:** Better page load speeds without any effort

### Zyte / Scrapy Cloud
- **Offer:** 1 free forever unit, unlimited requests, 120-day data retention
- **How to claim:** [zyte.com](https://zyte.com) → Connect GitHub
- **What you get:** Cloud platform for running web crawlers at scale
- **Use it for:** Data scraping pipelines for analytics or lead generation apps

---

## 📊 Monitoring & Analytics

### Datadog
- **Offer:** Pro Account with 10 servers, free for 2 years ($3,600 value)
- **How to claim:** [datadoghq.com](https://datadoghq.com) → Connect GitHub
- **What you get:** Infrastructure monitoring, APM, logs, dashboards
- **Use it for:** Know exactly what's happening in your app at all times
- **Quick setup:**
  ```bash
  # Install the agent on your DigitalOcean server
  DD_API_KEY=your_key DD_SITE="datadoghq.com" bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"
  ```

### New Relic
- **Offer:** Free while a student ($300/month value)
- **How to claim:** [newrelic.com](https://newrelic.com) → Connect GitHub
- **What you get:** Full observability — traces, metrics, logs, errors, synthetics
- **Use it for:** The monitoring setup of a $10M startup, for free

### Sentry
- **Offer:** 50K errors, 100K transactions, 500 session replays
- **How to claim:** [sentry.io](https://sentry.io) → Connect GitHub
- **What you get:** Real-time error tracking across every language and framework
- **Quick setup:**
  ```bash
  npm install @sentry/node
  # In your app:
  import * as Sentry from "@sentry/node";
  Sentry.init({ dsn: "YOUR_DSN" });
  ```

### Honeybadger
- **Offer:** Free Small account for 1 year
- **How to claim:** [honeybadger.io](https://honeybadger.io) → Connect GitHub
- **What you get:** Exception, uptime, and cron monitoring
- **Use it for:** Lightweight alternative to Sentry with great UX

### SimpleAnalytics
- **Offer:** Starter plan free for 1 year (100K page views/month)
- **How to claim:** [simpleanalytics.com](https://simpleanalytics.com) → Connect GitHub
- **What you get:** Privacy-friendly, GDPR-compliant website analytics
- **Use it for:** Understand your traffic without selling user data

### Appfigures
- **Offer:** Free universal analytics for 1 year
- **How to claim:** [appfigures.com](https://appfigures.com) → Connect GitHub
- **What you get:** App Store analytics — downloads, revenue, ratings across platforms
- **Use it for:** If you build a mobile app, track its performance here

### DevCycle
- **Offer:** Free 1-year Starter plan (unlimited seats, flags, usage)
- **How to claim:** [devcycle.com](https://devcycle.com) → Connect GitHub
- **What you get:** Feature flag management, A/B testing, gradual rollouts
- **Use it for:** Ship features safely with instant rollbacks

### Blackfire
- **Offer:** Free Developer subscription
- **How to claim:** [blackfire.io](https://blackfire.io) → Connect GitHub
- **What you get:** PHP code performance profiling
- **Use it for:** PHP/Symfony apps — find and fix performance bottlenecks

---

## 🔒 Security & Secrets

### 1Password
- **Offer:** 1Password free for 1 year including Developer Tools
- **How to claim:** [1password.com](https://1password.com) → Connect GitHub
- **What you get:** Password manager + SSH key management + secret automation
- **Use it for:** Secure every credential you have from day one

### Dashlane
- **Offer:** Dashlane Premium free for 6 months
- **How to claim:** [dashlane.com](https://dashlane.com) → Connect GitHub
- **What you get:** Password manager with dark web monitoring
- **Use it for:** Alternative to 1Password

### AstraSecurity
- **Offer:** 6 months website firewall and malware scanner
- **How to claim:** [getastra.com](https://getastra.com) → Connect GitHub
- **What you get:** WAF (Web Application Firewall) + malware detection
- **Use it for:** Protect your launched app from attacks

### Termius
- **Offer:** Free Pro and Team features while a student
- **How to claim:** [termius.com](https://termius.com) → Connect GitHub
- **What you get:** SSH client for desktop and mobile with synced credentials
- **Use it for:** Securely manage your DigitalOcean servers from any device

---

## 🧪 Data Science & ML

### DataCamp
- **Offer:** 3 months free subscription
- **How to claim:** [datacamp.com](https://datacamp.com) → Connect GitHub
- **What you get:** 350+ courses in Python, R, SQL, ML, AI, data visualization
- **Use it for:** Learning data skills to build smarter apps

### Deepnote
- **Offer:** Free Team plan (30-day history, 5GB RAM, premium integrations)
- **How to claim:** [deepnote.com](https://deepnote.com) → Connect GitHub
- **What you get:** Collaborative Jupyter notebooks with Snowflake, BigQuery integrations
- **Use it for:** Data analysis, ML prototyping, data science apps

### Camber
- **Offer:** 200 CPU hours, 75GB storage, 200 LLM messages/month
- **How to claim:** [cambercloud.com](https://cambercloud.com) → Connect GitHub
- **What you get:** AI-powered cloud platform for scientific computing
- **Use it for:** Running ML models and simulations at scale

### CARTO
- **Offer:** Free account with Location Data Services, 2 years
- **How to claim:** [carto.com](https://carto.com) → Connect GitHub
- **What you get:** Geospatial analysis, mapping, location intelligence
- **Use it for:** Location-based apps, delivery trackers, geographic market analysis

### SQLGate
- **Offer:** Standard Subscription features for 1 year
- **How to claim:** [sqlgate.com](https://sqlgate.com) → Connect GitHub
- **What you get:** Professional SQL IDE for MySQL, PostgreSQL, Oracle, SQL Server
- **Use it for:** Writing and debugging complex database queries

### PopSQL
- **Offer:** Free Premium subscription
- **How to claim:** [popsql.com](https://popsql.com) → Connect GitHub
- **What you get:** Collaborative SQL editor with data visualization
- **Use it for:** Analyzing your app's data with your team

---

## 🌐 Domains & Deployment

### Namecheap
- **Offer:** 1 .me domain free for 1 year + free SSL certificate
- **How to claim:** [namecheap.com](https://namecheap.com) → Connect GitHub
- **What you get:** yourapp.me + HTTPS from day one
- **Pro tip:** Use this for your main project. Set up DNS to point to DigitalOcean.

### Name.com
- **Offer:** Free domain with .live, .studio, .software, .app, .dev extensions
- **How to claim:** [name.com](https://name.com) → Connect GitHub
- **What you get:** A premium domain extension for your project
- **Pro tip:** `.dev` is perfect for developer tools. `.app` for apps. `.live` for events.

### .TECH Domain
- **Offer:** One standard .TECH domain free for 1 year
- **How to claim:** Connect GitHub on the .TECH pack page
- **What you get:** yourproject.tech — signals technology

### GitHub Pages
- **Offer:** 1 site per account + unlimited project sites
- **How to claim:** Automatic with GitHub — no claiming needed
- **How to use:**
  ```bash
  # Option 1: Deploy from /docs folder
  # Settings → Pages → Source: main branch, /docs folder

  # Option 2: Deploy from gh-pages branch
  npm install gh-pages --save-dev
  # Add to package.json scripts:
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
  npm run deploy
  ```

---

## 🔀 Git, Version Control & IDEs

### JetBrains
- **Offer:** Free subscription to all JetBrains IDEs, renewable annually
- **How to claim:** [jetbrains.com/student](https://jetbrains.com/student) → Connect GitHub
- **What you get:** IntelliJ IDEA (Java), PyCharm (Python), WebStorm (JS), GoLand, Rider, and more
- **Use it for:** Professional-grade IDE with built-in refactoring, debugging, and profiling

### GitKraken / GitLens
- **Offer:** Free 6 months, then 80% off while a student
- **How to claim:** [gitkraken.com](https://gitkraken.com) → Connect GitHub
- **What you get:** Best visual Git client + Launchpad for PR management
- **Use it for:** Understanding Git visually, managing branches, reviewing PRs

### Tower
- **Offer:** Free Tower Pro while a student
- **How to claim:** [git-tower.com](https://git-tower.com) → Connect GitHub
- **What you get:** Professional Git client for Mac and Windows
- **Use it for:** Undo mistakes, manage stashes, resolve conflicts visually

### GitHub Desktop
- **Offer:** Free and open source
- **How to claim:** [desktop.github.com](https://desktop.github.com) — just download
- **Use it for:** Simple Git GUI for beginners. No command line needed.

---

## 📅 Productivity

### Notion
- **Offer:** Education plan with AI responses (everything in Plus)
- **How to claim:** [notion.so](https://notion.so) → Connect GitHub
- **What you get:** Workspace for notes, wikis, project management, databases, + AI
- **Use it for:** Document your app idea, track tasks, write specs with AI assistance

### Notion Template Collection
- **Offer:** Free student-specific templates
- **How to claim:** [notion.so/github-education-templates](https://notion.so/github-education-templates)
- **What you get:** CS dashboards, hackathon planners, portfolio templates
- **Use it for:** Instantly organized workspace for any project

### DailyBot
- **Offer:** Business plan free for 10 users, 6 months
- **How to claim:** [dailybot.com](https://dailybot.com) → Connect GitHub
- **What you get:** Automated standups, retrospectives, surveys in Slack/Teams
- **Use it for:** Run your student project team like a remote-first startup

### PomoDone
- **Offer:** Lite plan free for 2 years
- **How to claim:** [pomodoneapp.com](https://pomodoneapp.com) → Connect GitHub
- **What you get:** Pomodoro timer integrated with your task manager
- **Use it for:** Deep focus coding sessions. 25 minutes on, 5 minutes off.

### SlideCoach
- **Offer:** 2,000 credits (40 AI coaching sessions) for 1 year
- **How to claim:** [slidecoach.ai](https://slidecoach.ai) → Connect GitHub
- **What you get:** AI presentation coach with feedback on your delivery
- **Use it for:** Practice your demo day pitch, investor presentation, or conference talk

---

## 📚 Learning Platforms

### FrontendMasters
- **Offer:** Free 6 months access to all courses
- **How to claim:** [frontendmasters.com](https://frontendmasters.com) → Connect GitHub
- **What you get:** In-depth JS, React, Node.js, CSS, TypeScript, Vue from industry experts
- **Best courses:** Complete Intro to Web Dev, JavaScript: The Hard Parts, Full Stack for Frontend

### Educative
- **Offer:** 6 months free, 70+ interactive courses + 30% off after
- **How to claim:** [educative.io](https://educative.io) → Connect GitHub
- **What you get:** Browser-based coding playgrounds — learn by doing
- **Best courses:** Web Development with React, Grokking the Coding Interview

### Scrimba
- **Offer:** 1 month free Pro (40+ courses, interactive video coding)
- **How to claim:** [scrimba.com](https://scrimba.com) → Connect GitHub
- **What you get:** Pause videos and edit the code inside them
- **Best for:** JavaScript, CSS, React beginners

### Codedex
- **Offer:** 6 months free Codédex Club
- **How to claim:** [codedex.io](https://codedex.io) → Connect GitHub
- **What you get:** Python, HTML, CSS, JavaScript, React, Git with a gamified approach
- **Best for:** Complete beginners who want a fun, modern learning experience

### GoRails
- **Offer:** Free 12 months access to all videos
- **How to claim:** [gorails.com](https://gorails.com) → Connect GitHub
- **What you get:** Ruby, Rails, Turbo, Stimulus, Hotwire video tutorials
- **Best for:** Building web apps fast with Ruby on Rails

### SymfonyCasts
- **Offer:** Free 3-month subscription
- **How to claim:** [symfonycasts.com](https://symfonycasts.com) → Connect GitHub
- **What you get:** Symfony, PHP, API Platform tutorials
- **Best for:** PHP developers building professional web apps

### AlgoExpert
- **Offer:** 20 free coding questions + 10% off all products
- **How to claim:** [algoexpert.io](https://algoexpert.io) → Connect GitHub
- **What you get:** 165 interview questions with video explanations
- **Use it for:** Coding interview prep for FAANG and top tech companies

### InterviewCake
- **Offer:** 1 week full access to the prep course
- **How to claim:** [interviewcake.com](https://interviewcake.com) → Connect GitHub
- **What you get:** Algorithmic thinking practice (not just memorization)
- **Use it for:** Building deep problem-solving skills for interviews

### Microsoft Visual Studio Dev Essentials
- **Offer:** VS Community, Pluralsight, $200 Azure credit first month
- **How to claim:** [visualstudio.microsoft.com/dev-essentials](https://visualstudio.microsoft.com/dev-essentials)
- **What you get:** Microsoft's complete developer package

### GitHub Certification Voucher
- **Offer:** 1 free exam voucher (Foundations or Copilot) — expires June 2026
- **How to claim:** Request directly from the pack page (while supplies last)
- **What you get:** Sit the official GitHub certification exam for free
- **Use it for:** Add a verified GitHub credential to your LinkedIn and resume

---

## 📱 Mobile Development

### NativeScript
- **Offer:** Free access
- **How to claim:** [nativescript.org](https://nativescript.org) — open source, free
- **What you get:** Build native iOS and Android apps with JavaScript/TypeScript
- **Use it for:** One codebase → two native mobile apps

### WorkingCopy
- **Offer:** All Pro features free while a student
- **How to claim:** [workingcopyapp.com](https://workingcopyapp.com) → Connect GitHub
- **What you get:** Full Git client for iPhone and iPad
- **Use it for:** Push code, manage branches, review PRs from your phone

---

## 🎓 Career & Community

### GitHub Campus Experts
- **Offer:** Apply to the leadership program
- **How to claim:** [education.github.com/experts](https://education.github.com/experts) → Apply
- **What you get:** Training, resources, and recognition from GitHub for building community
- **Use it for:** Build your profile as a tech leader on campus

### GitHub Community Exchange
- **Offer:** Open source project exposure
- **How to claim:** [education.github.com/globalcampus/exchange](https://education.github.com/globalcampus/exchange)
- **What you get:** Share your projects, find collaborators, get visibility
- **Use it for:** Find contributors for your open source side projects

### OpenSauced
- **Offer:** Included with pack
- **How to claim:** [opensauced.pizza](https://opensauced.pizza) → Connect GitHub
- **What you get:** Dashboard of your open source contributions and impact
- **Use it for:** Build a public portfolio of your GitHub contributions for employers

---

## 🔌 IoT & Hardware

### Arduino
- **Offer:** 6 months Arduino Cloud free + hardware discounts
- **How to claim:** [cloud.arduino.cc](https://cloud.arduino.cc) → Connect GitHub
- **What you get:** IoT cloud platform, device management, remote monitoring
- **Use it for:** Connected hardware projects, smart home devices, sensors

### Adafruit
- **Offer:** 1 year Adafruit IO+ + hardware discounts
- **How to claim:** [adafruit.com](https://adafruit.com) → Connect GitHub
- **What you get:** IoT data platform + discounts on hardware components
- **Use it for:** Maker projects, wearables, sensor networks

---

## 🔧 Specialized Tools

### POEditor
- **Offer:** Free Plus Plan for 1 year
- **How to claim:** [poeditor.com](https://poeditor.com) → Connect GitHub
- **What you get:** Localization management platform for translating your app
- **Use it for:** If you want to reach international users, manage translations here

### ToDiagram
- **Offer:** Pro Plan — full editor, 10 cloud documents
- **How to claim:** [todiagram.com](https://todiagram.com) → Connect GitHub
- **What you get:** Turn JSON, YAML, CSV, XML into editable diagrams
- **Use it for:** Visualizing data structures, API schemas, system architecture

### Vaadin
- **Offer:** Free Pro subscription license
- **How to claim:** [vaadin.com](https://vaadin.com) → Connect GitHub
- **What you get:** Java-based Progressive Web App framework
- **Use it for:** Java developers building enterprise web UIs

### Xojo
- **Offer:** Free Pro license while a student
- **How to claim:** [xojo.com](https://xojo.com) → Connect GitHub
- **What you get:** Cross-platform development (Desktop, Mobile, Web, Raspberry Pi)
- **Use it for:** Building native apps for multiple platforms from one codebase

---

## 📋 Activation Checklist

Copy this checklist into your Notion workspace and check off as you go:

```
CRITICAL (Week 1)
[ ] GitHub Pro + Copilot Pro
[ ] DigitalOcean ($200 credit)
[ ] Namecheap (.me domain + SSL)
[ ] MongoDB Atlas
[ ] Stripe
[ ] 1Password
[ ] Doppler

INFRASTRUCTURE (Week 1-2)  
[ ] Microsoft Azure
[ ] Heroku
[ ] GitHub Codespaces
[ ] LocalStack
[ ] Appwrite

MONITORING (Week 2)
[ ] Datadog
[ ] New Relic  
[ ] Sentry
[ ] Honeybadger
[ ] SimpleAnalytics

DEVOPS (Week 2)
[ ] Travis CI
[ ] BrowserStack
[ ] LambdaTest
[ ] Codecov
[ ] DeepScan

DESIGN (Week 2-3)
[ ] Bootstrap Studio
[ ] Icons8
[ ] IconScout
[ ] Polypane
[ ] Visme

PRODUCTIVITY (Week 3)
[ ] Notion + Templates
[ ] DailyBot
[ ] PomoDone
[ ] SlideCoach

LEARNING (Ongoing)
[ ] FrontendMasters
[ ] Educative
[ ] Scrimba
[ ] Codedex
[ ] DataCamp
[ ] GitHub Certification Voucher

DOMAIN & LAUNCH
[ ] Name.com (.dev or .app)
[ ] .TECH domain
[ ] GitHub Pages (automatic)

CAREER
[ ] GitHub Campus Experts (apply)
[ ] OpenSauced
[ ] GitHub Community Exchange
[ ] AlgoExpert

SPECIALIZED (As needed)
[ ] Blockchair
[ ] CARTO
[ ] Deepnote
[ ] POEditor
[ ] Termius
[ ] AstraSecurity
[ ] Arduino / Adafruit
```

---

*See something outdated? [Open a PR](../CONTRIBUTING.md) to update it.*

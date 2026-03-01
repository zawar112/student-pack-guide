# 🤖 Claude + Cursor AI Development Workflow

> The exact 8-phase workflow used to build production apps with AI assistance.
> Every phase includes sample Claude prompts you can copy and use immediately.

---

## The Core Concept

```
Claude AI     → Thinks, plans, designs, writes logic
Cursor AI     → Implements in your actual codebase
GitHub Copilot → Autocompletes as you type
Pack Tools    → Infrastructure, hosting, monitoring, payments
```

You are the **architect and product manager**. The AI is your **engineering team**. Your job is to give clear instructions and review the output.

---

## Phase 1: Planning & Architecture

**Goal:** Turn your idea into a concrete, buildable spec before writing a single line of code.

**Claude Prompt — Full PRD:**
```
I want to build [describe your app in 2-3 sentences].

Target audience: [who will use it]
Revenue model: [subscription / usage-based / one-time / freemium]
Desired tech stack: Node.js + React + MongoDB (or describe your preference)

Please write a complete Product Requirements Document with:
1. Executive summary (3 sentences)
2. User personas (2-3 personas with name, job, and pain point)
3. Core MVP features — maximum 5, ruthlessly prioritized
4. Features explicitly OUT of scope for v1
5. Technical architecture using only GitHub Student Pack tools
6. MongoDB data model with all collections and fields
7. API endpoints list (method + path + description)
8. Success metrics for the first 90 days
```

**Claude Prompt — Tech Stack Decision:**
```
I'm building a [app type] for [audience] with a [revenue model].
I have access to: DigitalOcean ($200 credit), MongoDB Atlas, 
Appwrite (backend-as-a-service), Microsoft Azure ($100 credit), 
GitHub Codespaces, Heroku ($13/month credit).

Compare 3 different infrastructure approaches and recommend 
the best one for a solo student developer building their first 
SaaS. Prioritize: speed to launch, lowest maintenance burden, 
and cost after my student credits expire.
```

**Cursor AI Role:**
- Open a new project folder in Cursor
- Create `SPEC.md` and paste Claude's PRD
- Ask Cursor to generate the project folder structure: `Ctrl+K → "Create the folder structure for this project based on the spec in SPEC.md"`

**Tools this phase:** Claude AI, Cursor AI, Notion (document decisions)

---

## Phase 2: Environment Setup

**Goal:** Working local dev environment connected to all your free pack services.

**Claude Prompt — Setup Script:**
```
Generate a complete project setup for a [Node.js/Python/etc] application.

Include:
1. package.json with all dependencies and scripts
2. Full directory structure with explanations
3. List of all environment variables needed (for Doppler)
4. GitHub Actions CI workflow that runs tests on every PR
5. .gitignore file
6. Docker compose for local development
7. README setup instructions

Tech stack: [your stack]
Database: MongoDB Atlas
Secrets: Doppler
Hosting: DigitalOcean App Platform
```

**Step-by-step setup:**
```bash
# 1. Create your GitHub repo
gh repo create my-app --public --clone
cd my-app

# 2. Open in Cursor
cursor .

# 3. Set up Doppler secrets
doppler login
doppler setup
# Add all your API keys in Doppler dashboard

# 4. Connect MongoDB
# Paste your Atlas connection string into Doppler as MONGODB_URI

# 5. Initialize Appwrite project
# Create project at cloud.appwrite.io
# Add APPWRITE_PROJECT_ID and APPWRITE_API_KEY to Doppler

# 6. Test your connection
doppler run -- node scripts/test-connections.js
```

**Ask Claude to generate `scripts/test-connections.js`:**
```
Write a Node.js script that tests connections to:
1. MongoDB Atlas using the MONGODB_URI env var
2. Appwrite Cloud using APPWRITE_PROJECT_ID and APPWRITE_API_KEY
3. Stripe using STRIPE_SECRET_KEY

Each test should log success or failure with a helpful error message.
Run all tests in parallel and summarize at the end.
```

**Tools this phase:** GitHub Codespaces, Doppler, MongoDB Atlas, Appwrite, Termius

---

## Phase 3: Backend Development

**Goal:** Working API with auth, database operations, and business logic.

**Claude Prompt — Complete Route Handler:**
```
Write a complete [feature name] module for Express.js/Node.js.

Requirements:
- Database: MongoDB with Mongoose
- Auth: JWT middleware (user is available as req.user)
- Include these endpoints:
  [list your endpoints]

For each endpoint include:
1. Input validation (use Joi or Zod)
2. Business logic
3. Error handling with appropriate HTTP status codes
4. JSDoc comments
5. Unit test stubs (Jest)

Follow these conventions:
- Async/await with try/catch
- Centralized error handling middleware
- Consistent response format: { success, data, error }
```

**Claude Prompt — Authentication System:**
```
Write a complete authentication system for my Express.js app using:
- MongoDB for user storage (Mongoose)
- JWT access tokens (15 min expiry)
- Refresh tokens stored in MongoDB (7 day expiry)
- Bcrypt for password hashing

Implement these endpoints:
POST /auth/register - email + password
POST /auth/login - returns both tokens
POST /auth/refresh - exchange refresh for new access token
POST /auth/logout - invalidate refresh token
POST /auth/forgot-password - send reset email via Testmail API
POST /auth/reset-password - validate token and set new password

Include: rate limiting (5 attempts per 15 min per IP),
email verification flow, and the authentication middleware.
```

**Cursor AI Workflow for Backend:**
1. Create `src/modules/[feature]/` folder
2. Paste Claude's spec as a comment block at top of file
3. `Ctrl+K` → "Implement this module based on the spec in the comments"
4. Review each function — don't accept blindly
5. `Ctrl+K` → "Write Jest tests for all the functions in this file"

**Tools this phase:** MongoDB Atlas, Appwrite, Doppler, Testmail, Requestly (mock APIs during dev)

---

## Phase 4: Frontend Development

**Goal:** Polished, responsive UI that non-technical users can actually use.

**Claude Prompt — Component Design:**
```
Design a React component for [component name] in [app name].

The component should:
- [describe what it does]
- Handle these states: loading, error, empty, populated
- Be fully responsive (mobile-first)
- Use Tailwind CSS classes only (no custom CSS)

Include:
1. TypeScript props interface with JSDoc
2. Complete component implementation
3. Storybook story (optional)
4. Basic accessibility (aria labels, keyboard navigation)

Design inspiration: [Linear / Vercel / Stripe / Notion / etc]
```

**Claude Prompt — Full Dashboard Page:**
```
Design a React dashboard page for [app name] with:
- Sidebar navigation (collapsible on mobile)
- Stats row: [metric 1], [metric 2], [metric 3] with trend arrows
- Main content: [describe what goes here]
- User dropdown in top-right with avatar, settings, logout

Use Tailwind CSS. Make it look professional like Vercel's dashboard.
Include loading skeletons for all data sections.
The sidebar should collapse to icons on screens < 1024px.
```

**Design Assets Workflow:**
1. Source icons from **Icons8** or **IconScout** (free with pack)
2. Design mockups in **Bootstrap Studio** (free with pack)
3. Test responsiveness in **Polypane** (free with pack) — see mobile + tablet + desktop simultaneously
4. Use **Octicons** for developer-focused app icons (GitHub's icon library)

**Cursor AI Frontend Workflow:**
```
1. Open your components folder in Cursor
2. Describe the component in a comment:
   // A pricing card with: plan name, price, feature list, 
   // CTA button. Highlighted state for recommended plan.
   // Uses Tailwind CSS. TypeScript props.
3. Ctrl+K → Cursor generates the component
4. Ctrl+L → Ask "Make this responsive for mobile"
5. Ctrl+L → Ask "Add loading and error states"
```

**Tools this phase:** Bootstrap Studio, Polypane, Icons8, IconScout, Octicons, Cursor AI, GitHub Copilot

---

## Phase 5: Testing & Quality

**Goal:** Catch bugs before your users do.

**Claude Prompt — Test Suite:**
```
Write a comprehensive Jest test suite for this module:

[paste your module code]

Include:
1. Unit tests for each function (happy path)
2. Unit tests for each edge case
3. Unit tests for each error state
4. Integration tests for database operations (use mongodb-memory-server)
5. Mock implementations for: Stripe, email service, external APIs

Target: 90%+ line coverage.
Group tests logically with describe blocks.
Use test factories/fixtures for test data — no random data.
```

**Claude Prompt — E2E Test Plan:**
```
Write a Playwright end-to-end test suite for [app name].

Cover these critical user journeys:
1. New user signup → email verification → onboarding → first action
2. Login → perform core feature → see result
3. Upgrade to paid plan → Stripe checkout → feature unlocked
4. [add your own critical paths]

Use Page Object Model pattern.
Include: test setup/teardown, screenshots on failure, 
and a CI configuration to run on BrowserStack.
```

**Testing Workflow:**
```bash
# Run unit tests
npm test

# Run tests with coverage (uploads to Codecov automatically)
npm test -- --coverage

# Run E2E tests locally
npx playwright test

# Run on real devices via BrowserStack
# (configure in playwright.config.ts with BrowserStack credentials from Doppler)
BROWSERSTACK=true npx playwright test
```

**Quality Checks:**
- **DeepScan** — connects to GitHub, auto-scans every push
- **CodeScene** — weekly code health report
- **Imgbot** — opens PRs to compress any images you add

**Tools this phase:** BrowserStack, LambdaTest, Codecov, DeepScan, CodeScene, Travis CI

---

## Phase 6: Deployment & CI/CD

**Goal:** Automated, repeatable deployments where `git push` = shipped.

**Claude Prompt — GitHub Actions Workflow:**
```
Write a complete GitHub Actions CI/CD pipeline for a Node.js app.

On pull request:
- Install dependencies
- Run linting (ESLint)
- Run type checking (TypeScript)
- Run unit tests
- Run E2E tests on BrowserStack
- Check test coverage with Codecov (fail if below 80%)
- Run DeepScan analysis

On merge to main:
- All of the above
- Build Docker image
- Push to Docker Hub (or GitHub Container Registry)
- SSH into DigitalOcean server
- Pull new image
- Run database migrations
- Restart application (zero downtime with PM2)
- Run smoke tests against production
- Post summary to Slack

Use: secrets from GitHub Secrets (populated from Doppler)
```

**DigitalOcean Deployment Setup:**
```bash
# 1. Create a Droplet (Ubuntu 22.04, $6/month Basic plan)
# 2. SSH in
ssh root@your-droplet-ip

# 3. Install Node.js, PM2, Nginx
curl -fsSL https://deb.nodesource.com/setup_18.x | bash -
apt-get install -y nodejs
npm install -g pm2
apt-get install -y nginx

# 4. Clone your repo
git clone https://github.com/zawar112/your-app.git
cd your-app

# 5. Set up Doppler on the server
doppler login --no-interactive --token $DOPPLER_TOKEN
doppler setup

# 6. Start with PM2
doppler run -- pm2 start server.js --name my-app
pm2 startup
pm2 save

# 7. Configure Nginx as reverse proxy
# Claude can generate your nginx.conf
```

**Claude Prompt — Nginx Config:**
```
Write a production Nginx config for a Node.js app on DigitalOcean.
Include: reverse proxy to localhost:3000, SSL with Let's Encrypt,
HTTP → HTTPS redirect, gzip compression, security headers 
(HSTS, X-Frame-Options, CSP), and rate limiting at the Nginx level.
Domain: myapp.me
```

**Tools this phase:** GitHub Actions, Travis CI, DigitalOcean, Namecheap (DNS), Imgbot

---

## Phase 7: Monitoring & Observability

**Goal:** Know about problems before your users do.

**Sentry Setup (5 minutes):**
```bash
npm install @sentry/node @sentry/tracing
```
```javascript
// At the top of your server.js
import * as Sentry from "@sentry/node";
Sentry.init({
  dsn: process.env.SENTRY_DSN, // from Doppler
  tracesSampleRate: 0.1, // 10% of requests
  environment: process.env.NODE_ENV,
});
// Add Sentry.Handlers.requestHandler() before routes
// Add Sentry.Handlers.errorHandler() after routes
```

**Datadog Setup:**
```bash
# On your DigitalOcean server:
DD_API_KEY=your_key DD_SITE="datadoghq.com" \
bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"

# In your Node.js app:
npm install dd-trace
# Add at the very top of server.js:
require('dd-trace').init()
```

**Claude Prompt — Monitoring Strategy:**
```
Design a monitoring strategy for my [app type] using:
- Datadog (infrastructure + APM)
- Sentry (errors)
- New Relic (additional APM)
- Honeybadger (uptime + cron)
- SimpleAnalytics (web traffic)

Define:
1. The 5 most important metrics to track for a SaaS app
2. Alert thresholds for each metric
3. On-call runbook for the 3 most common failure modes
4. Weekly metrics review template
5. Dashboard layout for Datadog
```

**Key Metrics to Track:**
| Metric | Tool | Alert Threshold |
|---|---|---|
| Error rate | Sentry | > 1% of requests |
| P95 response time | Datadog | > 500ms |
| Uptime | Honeybadger | < 99.9% |
| CPU usage | Datadog | > 80% sustained |
| Memory usage | New Relic | > 90% |
| Failed payments | Stripe Dashboard | Any |
| New signups | SimpleAnalytics | Drop > 50% week-over-week |

**Tools this phase:** Datadog, New Relic, Sentry, Honeybadger, SimpleAnalytics

---

## Phase 8: Revenue & Growth

**Goal:** Turn your app into a business.

**Stripe Integration:**
```bash
npm install stripe
```

**Claude Prompt — Complete Billing System:**
```
Build a complete Stripe billing system for a SaaS with:
- 3 tiers: Free (no card), Pro ($19/month), Team ($49/month)
- Free 14-day trial on Pro (card required)
- Annual pricing with 20% discount
- Usage metering for [your metered feature] with monthly reset
- Customer Portal (Stripe-hosted) for self-service billing management
- Webhook handler for all billing events:
  * customer.subscription.created
  * customer.subscription.updated  
  * customer.subscription.deleted
  * invoice.payment_succeeded
  * invoice.payment_failed

Include:
- Idempotency keys on all Stripe API calls
- Retry logic for webhook processing
- Database sync on every billing event
- Email notifications via Testmail on key events
```

**Growth Workflow:**

1. **A/B test your pricing** with **DevCycle** feature flags
2. **Track conversions** in **SimpleAnalytics**
3. **Analyze user behavior** with **Datadog** dashboards
4. **Use Claude to interpret data:**
   ```
   Ask Claude: "I have these metrics from last month:
   - Signups: 87
   - Activated (used core feature): 43 (49%)
   - Converted to paid: 8 (9%)
   - Churned: 2
   
   Identify the biggest bottleneck in my funnel and 
   give me 3 specific experiments to run this week."
   ```

5. **Ship experiments fast** with Cursor AI:
   - Claude designs the experiment
   - Cursor implements it
   - DevCycle deploys it to 10% of users
   - Datadog measures the result
   - If it wins → roll out to 100%

**Tools this phase:** Stripe, DevCycle, SimpleAnalytics, Datadog, Appfigures, Sentry, Claude AI, Cursor AI

---

## The Daily Development Loop

Once you're in active development, this is your daily rhythm:

```
Morning (30 min):
├── Check Sentry for overnight errors
├── Review Datadog dashboards
└── Plan today's features in Notion

Build Loop:
├── Open Claude → describe the feature
├── Claude writes the spec/logic
├── Open Cursor → implement from spec
├── Run tests: npm test
├── Git commit + push
└── Travis CI runs automatically

End of Day (15 min):
├── Review CI/CD results
├── Check SimpleAnalytics for traffic
└── Update Notion task board
```

---

## Quick Reference: When to Use Each AI Tool

| Task | Use |
|---|---|
| Design system architecture | Claude |
| Write technical specs | Claude |
| Generate complex business logic | Claude |
| Write database queries | Claude |
| Generate test cases | Claude |
| Write marketing copy | Claude |
| Analyze metrics and data | Claude |
| Implement code from specs | Cursor (Ctrl+K) |
| Refactor existing code | Cursor (Ctrl+K) |
| Fix specific bugs | Cursor (Ctrl+K) |
| Autocomplete while typing | GitHub Copilot |
| Explain unfamiliar code | Cursor (Ctrl+L chat) |
| Multi-file changes | Cursor (Ctrl+Shift+I) |

---

*Got a workflow tip? [Add it here](../CONTRIBUTING.md)*

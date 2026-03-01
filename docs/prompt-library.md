# 📋 Claude AI Prompt Library

> 40+ ready-to-use Claude prompts for every phase of building your app.
> Copy any prompt, fill in the [brackets], and paste into Claude.

---

## 🏗 Architecture & Planning

**Full Product Requirements Document**
```
I want to build [describe your app in 2-3 sentences].
Target audience: [who will use it]
Revenue model: [subscription / usage-based / freemium]
Tech preference: [Node.js/Python/etc + React + MongoDB or your choice]

Write a complete Product Requirements Document:
1. Executive summary (3 sentences max)
2. User personas (2 personas: name, role, pain point)
3. Core MVP features — max 5, prioritized by user value
4. Explicitly out of scope for v1
5. Technical architecture using GitHub Student Pack tools only
6. MongoDB data model (all collections + fields)
7. API endpoints (method + path + one-line description)
8. Success metrics for 90 days
```

**Tech Stack Decision**
```
I'm building a [type] app for [audience].
Scale expectation: 0–500 users in 6 months.
I have: DigitalOcean $200 credit, MongoDB Atlas, Appwrite,
Azure $100 credit, Heroku $13/month credit, GitHub Codespaces.

Compare 3 infrastructure approaches:
1. DigitalOcean-first (App Platform + Managed DB)
2. Appwrite-first (backend-as-a-service)
3. Azure-first (serverless functions + Azure DB)

For each: pros, cons, monthly cost after credits, maintenance burden.
Recommend the best one for a solo student developer launching fast.
```

**System Architecture Diagram (Text)**
```
I'm building [app name] with this stack: [your stack].
Draw an ASCII architecture diagram showing:
- User → Frontend → API layer
- API → Database, Auth, External services
- Background jobs and queues
- CI/CD flow (GitHub → CI → Server)
- Monitoring (what reports to what)

Keep it clean and readable. Include a legend.
```

**Feature Prioritization**
```
Here's my feature backlog for [app]:
[paste your feature list]

Prioritize using the ICE framework (Impact, Confidence, Effort).
Score each 1-10 on each dimension.
Recommend the top 5 to build for v1 MVP.
Explain what to cut and why.
```

---

## 🗄 Database Design

**MongoDB Schema Design**
```
Design MongoDB schemas for [app name].
Users will [describe core actions].

For each collection include:
- Collection name and purpose
- All fields with types and descriptions
- Required vs optional fields
- Default values
- Indexes (for common query patterns)
- Relationships to other collections
- Example document

Also include: soft delete pattern, timestamps, and 
tenant isolation strategy for multi-user SaaS.
```

**SQL Schema Design**
```
Design a PostgreSQL schema for [app name].
Core entities: [list your main data objects]

Include:
- CREATE TABLE statements with all columns and types
- Foreign key relationships
- Indexes for common queries
- Constraints (unique, check, not null)
- Enum types where appropriate
- Migration file format (numbered)

Optimize for: read-heavy workload, 
[specific query patterns you know you'll need]
```

**Data Migration Plan**
```
I need to migrate my data from this schema:
[paste current schema]

To this new schema:
[paste new schema]

Write a complete migration plan:
1. Step-by-step migration script (MongoDB/SQL)
2. How to run with zero downtime
3. Rollback plan if something goes wrong
4. Validation checks to confirm migration succeeded
5. Estimated time for [X records]
```

**Query Optimization**
```
This query is too slow (taking [X]ms):
[paste your query]

Database: [MongoDB/PostgreSQL/MySQL]
Relevant indexes that exist: [list them]
Collection/table size: [approximate row count]

Diagnose the bottleneck, rewrite the query optimally,
and suggest what indexes to add.
```

---

## 🔌 API Development

**Complete REST API Module**
```
Write a complete [feature name] REST API module for Express.js.

Endpoints needed:
[list each endpoint with method and description]

Requirements:
- MongoDB with Mongoose for data
- JWT auth middleware (user available as req.user)
- Input validation with Zod
- Consistent response format: { success, data, error, meta }
- Proper HTTP status codes
- Error handling (validation, not found, unauthorized, server error)
- JSDoc comments on each function

Include: controller, service, model, routes, and validation schema files.
```

**Authentication System**
```
Write a complete JWT authentication system for Node.js/Express.

Include:
POST /auth/register - email + password validation
POST /auth/login - returns access token (15min) + refresh token (7 days)
POST /auth/refresh - exchange refresh token for new access token
POST /auth/logout - invalidate refresh token
POST /auth/forgot-password - send reset link via email
POST /auth/reset-password - validate token + update password

Security requirements:
- Bcrypt for password hashing (rounds: 12)
- Refresh tokens stored in MongoDB (revocable)
- Rate limiting: 5 failed attempts → 15 minute lockout
- Secure HttpOnly cookies for refresh tokens
- CSRF protection

Write all route handlers, middleware, and MongoDB models.
```

**Stripe Billing Integration**
```
Write a complete Stripe billing integration for a SaaS with:
- 3 tiers: Free (no card), Pro ($[X]/month), Team ($[Y]/month)
- 14-day free trial on Pro and Team (card required)
- Annual pricing with 20% discount
- Stripe Customer Portal for self-service billing
- Usage metering for [feature] with monthly billing

Webhook handler for:
- checkout.session.completed
- customer.subscription.updated
- customer.subscription.deleted
- invoice.payment_succeeded
- invoice.payment_failed (trigger dunning email)

Include: idempotency keys on all Stripe calls,
webhook signature verification,
database sync on every event,
and the UI components for the pricing page and billing page.
```

**Rate Limiting Middleware**
```
Write Express.js rate limiting middleware that:
- Limits by IP: 100 requests per 15 minutes for unauthenticated
- Limits by API key: depends on user's plan tier
  - Free: 60 requests/hour
  - Pro: 1,000 requests/hour  
  - Team: 10,000 requests/hour
- Uses Redis for storage (or MongoDB if Redis not available)
- Returns proper 429 response with: retry-after header, 
  current limit, remaining requests, reset time
- Logs rate limit hits to Datadog

Include middleware function + Redis setup + test cases.
```

**Webhook Handler**
```
Write a production-grade webhook handler for [service: Stripe/GitHub/etc].

Include:
1. Signature verification (reject invalid requests)
2. Event type routing (switch on event type)
3. Idempotency: check if this event was already processed
4. Retry handling: idempotent operations safe to retry
5. Dead letter queue: failed events stored for manual review
6. Logging: log every event to Datadog with outcome
7. Error handling: never return 500 to webhook sender

Handle these specific events: [list your events]
```

---

## 🎨 Frontend Development

**React Dashboard Page**
```
Design a React dashboard page for [app name].

Layout:
- Top navigation bar with: logo, search, notifications, user avatar dropdown
- Sidebar with navigation links: [list your nav items]
- Main content area with:
  - Stats row: [metric 1], [metric 2], [metric 3] with % change badges
  - [main content section]
  - [secondary content section]

Requirements:
- Tailwind CSS only (no custom CSS)
- Fully responsive (sidebar collapses to bottom nav on mobile)
- Loading skeletons for all data sections
- Dark mode support via Tailwind dark: classes
- TypeScript with proper prop types

Design inspiration: Linear, Vercel, or Stripe dashboard
```

**Pricing Page Component**
```
Write a complete React pricing page component with:
- 3 tiers: Free, Pro ($[X]/month), Team ($[Y]/month)
- Monthly/Annual toggle (annual shows 20% savings badge)
- Feature comparison table (12 features, checkmarks/crosses)
- "Most Popular" badge on Pro tier
- FAQ section (8 common questions — generate good ones for [app type])
- CTA buttons that call onSelectPlan(planId, billingPeriod)

Use Tailwind CSS. Make it feel premium, not cheap.
The toggle should animate smoothly.
Annual prices should animate when toggle switches.
```

**Landing Page Copy + Components**
```
Write a complete landing page for [app name].

Target customer: [describe precisely]
Core promise: [the exact outcome they get]

Include:
1. Hero section: headline (3 variants), subheadline, CTA button, hero image description
2. Social proof bar: "Trusted by X developers at [type of companies]"
3. Problem section: "The old way" vs "The new way"
4. Feature sections (3): each with: icon, title, description, screenshot description
5. Testimonials: 3 realistic quotes from [target persona]
6. Pricing section: link to pricing component
7. FAQ: 8 questions + answers
8. Footer CTA

Tone: direct, developer-friendly, specific outcomes (not vague benefits).
No corporate speak. Write like a smart developer talking to peers.
```

**Form with Validation**
```
Write a React form component for [form purpose] with:
Fields: [list all fields with types]

Validation:
- [field]: [validation rule]
- [field]: [validation rule]

Requirements:
- React Hook Form + Zod for validation
- Error messages appear on blur (not on submit)
- Submit button disabled until form is valid
- Loading state during submission
- Success state after submission
- Inline error messages below each field
- TypeScript types for form data

Include: the Zod schema, the form component, and the API call on submit.
```

---

## 🔧 Backend Logic

**Background Job System**
```
Design a background job system for [task description] in Node.js.

Requirements:
- Job queue: Bull.js with Redis (or BullMQ)
- Job types: [list your job types]
- Retry logic: 3 attempts with exponential backoff (1min, 5min, 30min)
- Dead letter queue: failed jobs after max retries → store in MongoDB
- Job scheduling: some jobs run on cron schedule
- Monitoring: log to Datadog on job start, complete, fail
- Dashboard: use Bull Board for visual job monitoring

Write: queue setup, worker implementation for each job type, 
cron scheduler, and the Bull Board Express integration.
```

**Multi-Tenant Architecture**
```
Explain how to implement multi-tenancy for my SaaS using Node.js + MongoDB.

My app: [brief description]
Expected tenants in year 1: [estimate]
Expected data per tenant: [estimate]

Compare these approaches:
1. Row-level isolation (tenant_id field on every document)
2. Separate MongoDB databases per tenant
3. Separate collections per tenant

For each: implementation complexity, query complexity, 
data isolation guarantee, cost at scale, migration path.

Recommend the best approach for my scale and implement it.
Show me: the middleware, the query pattern, and how to 
switch between tenants safely.
```

**Caching Layer**
```
Add a Redis caching layer to this Express.js endpoint:
[paste your endpoint code]

Current response time: [X]ms (too slow)
Data freshness requirement: [how stale can the data be?]

Implement:
1. Cache on first request (with [X] minute TTL)
2. Cache invalidation when data changes
3. Cache stampede prevention (only one request rebuilds cache)
4. Cache hit/miss logging to Datadog
5. Manual cache clear endpoint (admin only)

Include the Redis setup, caching middleware, and invalidation logic.
```

---

## 🧪 Testing

**Unit Test Suite**
```
Write a comprehensive Jest test suite for this module:

[paste your module code]

Include:
1. Tests for every exported function
2. Happy path tests (expected inputs)
3. Edge case tests (empty arrays, null, undefined, 0, max values)
4. Error case tests (invalid input, network failure, DB error)
5. Mocks for: MongoDB, Redis, external APIs, email service
6. Test fixtures/factories (consistent test data, no random values)

Target: 90%+ line and branch coverage.
Group with describe blocks. Use descriptive test names.
Follow Arrange-Act-Assert pattern.
```

**E2E Test Plan**
```
Write a Playwright end-to-end test suite for [app name].

Critical user journeys to test:
1. New user: signup → email verification → onboarding → [first key action]
2. Returning user: login → [main use case] → logout
3. Billing: free user → upgrade → Stripe checkout → feature unlocked
4. Error case: [most common failure mode] → see helpful error message

For each journey:
- Use Page Object Model
- Include: setup, assertions, cleanup
- Screenshot on failure
- Works on: Chrome, Firefox, Safari, Mobile Chrome

Include: playwright.config.ts for local + BrowserStack CI.
```

**Load Test Script**
```
Write a k6 load test for my API.

Endpoints to test:
[list endpoints with expected request body]

Test scenarios:
1. Warm-up: 10 users for 1 minute
2. Load: ramp to 100 users over 5 minutes, hold for 10 minutes
3. Stress: ramp to 500 users, find breaking point

Thresholds (fail the test if exceeded):
- p95 response time > 500ms
- p99 response time > 2000ms
- Error rate > 1%

Include: realistic test data, authentication headers, 
and a summary report format.
```

---

## 💰 Monetization & Growth

**Pricing Strategy**
```
I'm building [app] for [audience].
Competitors charge: [list competitor prices]
Current free users: [number]
Most used features: [list top 3]

Design a pricing strategy:
1. Free tier: what's included, what gates to paid
2. Pro tier: price point + features + positioning
3. Team tier: price point + features + who it's for
4. Annual discount: what percentage makes sense

Include: the psychological rationale for each price point,
feature gate recommendations (what creates urgency to upgrade),
and the exact pricing page copy for each tier.
```

**Freemium Conversion Analysis**
```
Here's my funnel data for last month:
- Signups: [X]
- Activated (completed onboarding): [Y] ([%])
- Used core feature at least once: [Z] ([%])
- Converted to paid: [W] ([%])
- Churned paid users: [V]

Diagnose the biggest bottleneck.
For each stage of the funnel, give me:
1. The most likely reason people are dropping off
2. Two specific experiments to improve that stage
3. How to measure if the experiment worked

Prioritize by estimated revenue impact.
```

**Product Hunt Launch**
```
Write everything I need for a Product Hunt launch of [app name].

Deliverables:
1. Tagline: 5 variants under 60 characters
2. Short description: 260 characters
3. Full product description: 3 paragraphs
4. First comment from maker: personal story of why I built this
5. Answers to likely first 5 questions from PH community
6. Launch day schedule (what to post where, when)

Tone: authentic, not corporate. Tell the story of a student 
who built something real with free tools.
```

**Cold Email Sequence**
```
Write a 5-email cold outreach sequence for [app] targeting [job title] at [company type].

Each email:
- Under 150 words
- Plain text (no HTML, no images)
- One clear CTA
- Personal, not templated-feeling

Sequence:
Email 1 (Day 1): Cold introduction + specific value prop
Email 2 (Day 3): Different angle, social proof
Email 3 (Day 7): Case study or specific result
Email 4 (Day 14): "Last try" + direct ask
Email 5 (Day 30): Break-up email (often gets the most replies)

Include subject lines for each. Make them curiosity-inducing.
```

**Churn Analysis**
```
I have [X]% monthly churn. Here's what I know about users who churned:
[paste any data you have: usage patterns, support tickets, exit survey answers]

Analyze:
1. Most likely root causes (ranked by probability)
2. Which users are at highest risk of churning next (signals to watch)
3. What to change in the product to prevent churn
4. A win-back email sequence for recently churned users
5. An exit survey (5 questions) to collect better churn data

Give me specific, actionable recommendations — not generic advice.
```

---

## 🚀 DevOps & Deployment

**GitHub Actions Workflow**
```
Write a complete GitHub Actions CI/CD pipeline for a [Node.js/Python] app.

On pull request:
- Run tests (Jest/pytest)
- Check TypeScript types
- Lint (ESLint/flake8)
- Check test coverage (fail if < 80%)
- Comment coverage report on PR

On merge to main:
- All pull request checks
- Build Docker image
- Push to GitHub Container Registry
- SSH into DigitalOcean server
- Docker pull + restart with zero downtime
- Run database migrations
- Smoke test production
- Notify Slack of successful deploy

Secrets needed: list them all (I'll add to Doppler)
```

**Docker Configuration**
```
Write an optimized Dockerfile and docker-compose.yml for [app].

Dockerfile requirements:
- Multi-stage build (build stage + production stage)
- Non-root user for security
- Health check endpoint
- Minimize image size (target: < 200MB)
- Layer caching optimized for npm install

Docker Compose (local dev):
- App service with hot reload
- MongoDB service
- Redis service  
- Nginx service (reverse proxy)
- Admongo or similar for DB UI

Production docker-compose:
- App service
- Nginx (with SSL via Let's Encrypt)
- Environment variables from Doppler
```

**Nginx Configuration**
```
Write a production Nginx configuration for a Node.js app.

Requirements:
- Reverse proxy to Node.js on localhost:3000
- SSL termination with Let's Encrypt (certbot)
- HTTP → HTTPS redirect (301)
- Security headers: HSTS, X-Frame-Options, X-Content-Type-Options,
  Content-Security-Policy, Referrer-Policy
- Gzip compression for JS, CSS, HTML, JSON
- Rate limiting: 30 requests/minute per IP
- Static files served directly by Nginx (not Node.js)
- Websocket support (if applicable)
- Access logs in JSON format (for Datadog parsing)

Domain: [your domain]
```

---

## 🐛 Debugging

**Error Analysis**
```
I'm getting this error in production:

Error: [paste error message]
Stack trace: [paste stack trace]

Relevant code:
[paste the function or file where the error occurs]

Context:
- Happens: [always / intermittently / only under load / only for certain users]
- Started: [when did it start? what changed?]
- Environment: [Node.js version, OS, dependencies]

Explain: what caused this error, why it only appeared now,
how to fix it immediately, and how to prevent this class of error.
```

**Performance Bottleneck**
```
My [API endpoint / page load / database query] is too slow.

Current performance: [Xms average, Yms p95]
Target: [Zms]

Code:
[paste the slow code]

Datadog shows: [any relevant metrics you have]

Find the bottleneck, suggest fixes in order of impact,
and show me the optimized implementation.
```

**Memory Leak Investigation**
```
My Node.js process memory grows from 200MB to 2GB over 24 hours.

Here's my main server code:
[paste server.js or relevant sections]

Background jobs:
[describe your background jobs]

Help me:
1. Identify the most likely memory leak causes
2. How to profile it (Node.js --inspect + Chrome DevTools)
3. What patterns to look for in the heap snapshot
4. The fix for each common cause

Then review my code above and flag any obvious memory issues.
```

---

*Missing a prompt you need? [Open an issue](https://github.com/zawar112/student-pack-guide/issues) and we'll add it.*

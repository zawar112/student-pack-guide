# 💰 Revenue Guide — From $0 to First Paying Customer

> Everything you need to generate income using your free GitHub Student Pack tools.
> This guide assumes you've picked an app idea and are ready to build.

---

## The Revenue Stack

These are the pack tools directly involved in making money:

| Tool | Role | Why It Matters |
|---|---|---|
| **Stripe** | Payment processing | Waived fees on first $1K revenue |
| **DigitalOcean** | Hosting | $200 credit = 12 months of free hosting |
| **Appwrite** | Auth + backend | Free user management = no backend cost |
| **Namecheap** | Domain + SSL | Free domain + HTTPS = professional credibility |
| **SimpleAnalytics** | Traffic | Know where customers come from |
| **Datadog** | Performance | Catch issues before they cause churn |
| **Sentry** | Error tracking | Fix bugs before customers notice |
| **DevCycle** | A/B testing | Optimize pricing and conversion |
| **GitHub Pages** | Landing page | Free hosting for your marketing site |

---

## The $1,000 Fee Waiver Strategy

Stripe normally charges **2.9% + $0.30** per transaction.

With your student pack, Stripe waives all fees on your first $1,000 in revenue.

**What this means in practice:**

If you charge $19/month:
- Without the waiver: you keep $18.25 per customer
- With the waiver: you keep $19.00 per customer
- On first 52 customers: you save ~$39 in fees

More importantly: **you can offer better pricing** to early adopters knowing you're keeping 100%.

**Strategy:**
1. Offer a "Founder Pricing" plan to your first 20 customers at $9/month (lifetime)
2. Use the fee waiver period to optimize your product
3. Launch at full price ($19-29/month) after 20 founder customers

---

## Pricing Psychology

### The 3-Tier Structure

Almost every successful SaaS uses this structure:

```
FREE / TRIAL           PRO                    TEAM
──────────────         ──────────────         ──────────────
Limited usage          Full features          Everything in Pro
No credit card         $19/month              $49/month
Perfect for            Perfect for            Perfect for
  exploring              individuals            small teams

[Start Free]           [Start 14-day trial]   [Start 14-day trial]
```

**Why this works:**
- Free tier drives acquisition (no friction to sign up)
- Pro tier is your main revenue driver
- Team tier makes your average revenue per customer higher

### Pricing Your Product

Use this formula as a starting point:
- What problem does your app solve?
- How much does the user currently spend (time or money) on this problem?
- Price your product at 10-20% of what they currently spend

**Example:** If developers spend 4 hours/month on manual browser testing at $50/hour = $200/month cost. Your testing SaaS at $29/month is a 85% saving. Easy sell.

### The Annual Plan Trick

Always offer annual pricing with a ~20% discount:
- Monthly: $19/month
- Annual: $182/year ($15.17/month — "Save $46")

Annual customers:
- Pay 12 months upfront (great for your cash flow)
- Churn at lower rates (committed for the year)
- Are your most engaged users

---

## 90-Day Launch Plan {#90-day-plan}

### Month 1 — Build (Days 1–30)

**Day 1: Choose and validate**
- Pick your idea from the [App Ideas guide](app-ideas.md)
- Use Claude to run a quick validation:
  ```
  Ask Claude: "Generate 10 questions I should ask potential customers 
  to validate [my app idea]. Focus on: do they have the problem, 
  how do they currently solve it, what would they pay."
  ```
- Post in 1 relevant subreddit or Discord asking if people have this problem
- If 5+ people respond positively → build it

**Day 2–3: Claim your infrastructure**
- Register your .me domain on Namecheap (free)
- Set up MongoDB Atlas
- Set up DigitalOcean ($200 credit)
- Create Stripe account (activate fee waiver)
- Set up Doppler for secrets
- Set up Appwrite for auth

**Day 4–7: Dev environment**
- GitHub Codespaces + Cursor AI setup
- Connect all services via Doppler
- Deploy "hello world" to DigitalOcean
- Verify your domain points to your server

**Day 8–21: Build MVP**
- Follow the [AI Workflow Guide](ai-workflow.md)
- Claude + Cursor for all development
- Focus: core value proposition only
- Skip: settings pages, admin dashboards, edge cases

**Day 22–28: Add payments**
- Integrate Stripe checkout
- Build free trial flow (14 days, card required)
- Set up webhook handler
- Test the full signup → trial → payment flow

**Day 29–30: Soft launch**
- Deploy to production
- Set up Sentry + Datadog
- Invite 10 friends/classmates to test it
- Fix the most critical bugs they find

### Month 2 — Validate (Days 31–60)

**Days 31–40: Get 25 beta users**

Where to find beta users:
- Reddit: r/SaaS, r/entrepreneur, r/webdev, r/indiehackers + niche subreddits
- Twitter/X: Post your build with screenshots
- Discord: Find communities of your target audience
- IndieHackers: Post your product story
- ProductHunt: Submit to "Coming Soon" page
- Your university: Post in student groups

What to offer:
- Free access for beta period
- Lifetime deal at 50% off for the first 10 who give feedback
- Personal 30-minute onboarding call

**Days 41–50: Collect and act on feedback**

Use Claude to analyze feedback:
```
Ask Claude: "Here are 15 pieces of feedback from beta users:
[paste feedback]

Categorize into:
1. Critical bugs to fix now
2. Missing features blocking usage  
3. UX improvements
4. Nice-to-have features

Prioritize ruthlessly for a solo developer with 2 weeks of time."
```

Then use Cursor to implement the top 3 fixes.

**Days 51–60: Build your marketing page**

Your GitHub Pages landing page needs:
- Headline: the specific outcome you deliver ("Ship tested code on every browser in 5 minutes")
- Social proof: screenshots or quotes from beta users
- Clear pricing section
- FAQ section (use Claude to generate it)
- One clear CTA button

Use Claude to write it:
```
Ask Claude: "Write a complete landing page for [app].
Target customer: [describe them precisely]
Core promise: [the outcome they get]
Tone: direct, developer-friendly, no corporate speak
Include: headline (3 variants), subheadline, 
3 feature sections with benefits (not features), 
testimonials section (placeholder), pricing section, FAQ."
```

### Month 3 — Revenue (Days 61–90)

**Days 61–65: Public launch**

Launch checklist:
- [ ] ProductHunt submission (Tuesday–Thursday, submit by midnight PST)
- [ ] Hacker News "Show HN" post
- [ ] Tweet/X thread with the story of building it
- [ ] Post in all relevant subreddits
- [ ] Email your beta users asking them to upvote on PH
- [ ] Post in university student groups
- [ ] LinkedIn post with demo video

ProductHunt post template (use Claude to refine):
```
Ask Claude: "Write a ProductHunt launch post for [app].
Tagline: [max 60 chars]
Description: [260 chars]  
First comment from maker: [explain the why behind building it]
Make it feel personal and genuine, not like marketing copy."
```

**Days 66–75: Convert beta users to paid**

Email sequence (use Testmail + Claude):
- Email 1: "Your beta access is ending — here's what's next"
- Email 2: "Founder pricing — 40% off forever, today only"
- Email 3: "Last chance — beta access ends [date]"

Track conversion in SimpleAnalytics and Datadog.

**Days 76–85: Growth experiments**

Run 3 experiments using DevCycle feature flags:
1. Pricing test: $15 vs $19 vs $29 (which converts better?)
2. Trial length: 7 days vs 14 days (which retains better?)
3. Onboarding: video tutorial vs checklist vs blank (which activates users faster?)

Use Claude to design each experiment:
```
Ask Claude: "Design an A/B test for my pricing page.
Control: $19/month. 
Variants: $15/month and $29/month.
What metric should I measure? What sample size do I need?
How long should I run the test? How do I interpret the results?"
```

**Days 86–90: Hit $500 MRR**

At $19/month, you need 27 paying customers.
At $29/month, you need 18 paying customers.

If you launched on ProductHunt, had 25 beta users, and converted 20% → that's 5 paying customers.

The remaining 12-22 customers come from:
- Organic search (your GitHub Pages site will rank for long-tail keywords)
- Twitter/X followers who saw your build
- Word of mouth from beta users
- Continued posting in communities

---

## Reducing Churn

Churn is your #1 enemy. Every customer who leaves costs you twice — once in lost revenue, once in acquisition cost.

**The most common churn reasons:**
1. User never completed onboarding (never reached "aha moment")
2. User ran into a bug and gave up
3. User didn't use the product enough to see value
4. User found a cheaper alternative

**Fix #1: Onboarding sequence**
- Day 1: Welcome email with quick start guide (Testmail)
- Day 3: "Did you complete [core action]?" check-in
- Day 7: Tips and tricks email
- Day 10: "Here's what you can do with [feature]"
- Day 13: "Your trial ends tomorrow" — upgrade prompt

Use Claude to write all emails. Use Testmail to send them automatically.

**Fix #2: Error tracking**
- Sentry catches every error your users hit
- Set up alerts in Slack for high-severity errors
- Fix within 24 hours — email the affected user proactively

**Fix #3: Feature usage tracking**
- Add custom events to Datadog when users complete key actions
- If a user hasn't completed the "aha moment" action in 3 days → trigger an email

---

## The Revenue Formula

```
Monthly Revenue = (New Customers × Plan Price) - Churned Customers × Plan Price

To grow revenue:
1. Increase new customers (marketing, SEO, product hunt, communities)
2. Increase plan price (better features, better positioning)
3. Decrease churn (better onboarding, faster bug fixes, more value)

The fastest lever: Reduce churn.
A 5% monthly churn = 46% of customers gone in 12 months.
A 2% monthly churn = 21% of customers gone in 12 months.
```

---

## When to Apply for Startup Programs

Once you have 3+ months of revenue data, apply to:

- **Y Combinator** — $500K for 7% equity, most prestigious accelerator
- **Antler** — Equity-free early stage, global
- **Microsoft for Startups** — Free Azure credits, no equity
- **AWS Activate** — Free AWS credits, no equity
- **Stripe Atlas** — $1 to incorporate, startup-friendly

Your GitHub Student Pack experience is a strong signal — you built something real with $0 budget using free tools. That's exactly what investors want to see.

---

*Have a revenue tip or success story? [Add it here](../CONTRIBUTING.md)*

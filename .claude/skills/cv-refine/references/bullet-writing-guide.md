# Bullet Writing Guide for Software Engineers

This guide provides the methodology for transforming weak CV bullets into
high-impact achievement statements that pass recruiter screening.

---

## The XYZ Formula

Google's internal resume guidance uses this template:

> **Accomplished [X] as measured by [Y], by doing [Z]**

Not every bullet needs all three components rigidly, but every bullet MUST
have at least X (what you accomplished) and either Y (how it was measured)
or Z (how you did it). The best bullets have all three.

**Example transformation:**

- BEFORE: "Worked on improving the search feature"
- AFTER: "Reduced search latency by 65 % (P99: 400ms → 140ms) by redesigning
  the query pipeline with Elasticsearch and implementing result caching"

The "AFTER" version has:
- X = Reduced search latency
- Y = 65 %, from 400ms to 140ms
- Z = Redesigned query pipeline with Elasticsearch + caching

---

## The Quantification Framework

Engineers often say "I don't have metrics." They almost always do — they just
haven't thought about it yet. Use this framework to help extract numbers:

### Direct metrics (the user measured this)
- Latency improvements (P50, P95, P99)
- Error rate reduction
- Throughput increase
- Cost savings (infra, headcount, vendor)
- Revenue impact
- Deployment frequency improvement
- Test coverage increase
- Uptime improvement (99.5 % → 99.99 %)

### Scale metrics (the system has these)
- Requests per second / day
- Number of users (DAU, MAU)
- Data volume processed
- Number of services / endpoints
- Transaction volume
- Database size

### Scope metrics (the org has these)
- Team size led or mentored
- Number of engineers onboarded
- Number of teams impacted
- Number of stakeholders
- Cross-office / cross-timezone coordination

### Proxy metrics (estimate these if nothing else)
- "~40 % reduction" is better than nothing
- "serving millions of users" is fine if exact DAU is unknown
- Engineer-hours saved per week/month
- Number of manual steps automated
- Lines of legacy code removed or replaced
- Review cycle time reduction

### The estimation conversation

When the user says "I don't know the exact number", ask:

1. "Was it closer to 10 %, 50 %, or 2x?"
2. "How many users / requests / records were involved?"
3. "How much time did this save per week?"
4. "What was the before and after?"

A reasonable estimate is infinitely better than no number at all. Use "~"
or "approximately" if needed, but include the number.

---

## Action Verb Reference

### Tier 1 — High-impact verbs (prefer these)
Architected, Built, Delivered, Designed, Drove, Eliminated, Engineered,
Established, Implemented, Launched, Led, Migrated, Optimized, Pioneered,
Reduced, Redesigned, Scaled, Shipped, Spearheaded, Transformed

### Tier 2 — Good supporting verbs
Accelerated, Automated, Configured, Created, Debugged, Defined, Deployed,
Developed, Enhanced, Extracted, Improved, Integrated, Introduced, Mentored,
Negotiated, Orchestrated, Refactored, Resolved, Simplified, Streamlined

### Tier 3 — Weak verbs (avoid or replace)
Assisted, Contributed to, Helped, Involved in, Participated in, Responsible
for, Supported, Utilized, Was part of, Worked on

If you catch yourself writing a Tier 3 verb, stop and ask: "What did this
person actually DO?" The answer is usually a Tier 1 or 2 verb.

---

## Domain-Specific Bullet Templates

### Backend / Infrastructure

```
- Designed and deployed [service/system] handling [X] req/s, reducing
  [metric] by [Y]% while maintaining [Z]% uptime
- Migrated [N] services from [old] to [new], cutting [deployment time /
  infra cost / incident rate] by [Y]%
- Built [data pipeline / ETL system] processing [X] events/day with
  [latency] end-to-end latency
- Reduced [database / API / service] costs by $[X]K/yr by [optimization
  technique]
```

### Frontend / Full-stack

```
- Shipped [feature/product] used by [X] users, increasing [engagement
  metric] by [Y]%
- Reduced bundle size by [X]% ([Y]MB → [Z]MB) through [technique],
  improving LCP by [W]s
- Built [component library / design system] adopted by [N] teams,
  reducing frontend dev time by [X]%
- Led migration from [old framework] to [new framework] across [N]
  pages, improving [Core Web Vital] by [X]%
```

### Data / ML

```
- Developed [model/pipeline] achieving [X]% [accuracy/precision/recall],
  deployed to production serving [Y] predictions/day
- Built feature engineering pipeline processing [X]TB of data, reducing
  model training time from [Y] hours to [Z] hours
- Designed A/B testing framework used by [N] teams, accelerating
  experiment velocity by [X]%
```

### DevOps / Platform / SRE

```
- Designed CI/CD pipeline reducing deployment cycle from [X] to [Y],
  enabling [N] deploys/day (up from [M])
- Reduced MTTR from [X] hours to [Y] minutes by implementing
  [observability / alerting / runbook automation]
- Built internal developer platform serving [N] engineers, reducing
  environment setup time from [X] to [Y]
```

### Leadership / Staff+

```
- Defined technical strategy for [domain], adopted across [N] teams
  ([X] engineers), reducing [metric] by [Y]%
- Mentored [N] engineers ([junior → mid / mid → senior] promotions),
  establishing [code review / design doc / RFC] culture
- Led cross-functional initiative with [Product, Design, Data] to
  deliver [feature], driving [X]% increase in [business metric]
- Identified and resolved [systemic problem] affecting [N] services,
  preventing estimated $[X]K/yr in [downtime / customer churn / tech debt]
```

---

## Common Rewrite Patterns

### Pattern 1: Responsibility → Achievement

BEFORE: "Responsible for maintaining the payment processing system"

Think: What did maintaining it actually involve? What improved because of you?

AFTER: "Maintained 99.99 % uptime for payment processing system handling
$12M monthly transaction volume, resolving 3 critical incidents with zero
customer-facing downtime"

### Pattern 2: Vague Improvement → Specific Impact

BEFORE: "Improved application performance"

Think: What specifically? By how much? How did you do it?

AFTER: "Reduced API response time by 3x (900ms → 300ms) by implementing
Redis caching layer and optimizing N+1 database queries across 8 endpoints"

### Pattern 3: Team Activity → Personal Contribution

BEFORE: "Part of a team that launched the new mobile app"

Think: What was YOUR role? What did YOU specifically do?

AFTER: "Architected offline-first data sync layer for mobile app (React
Native), enabling 30 % of user sessions to function without connectivity"

### Pattern 4: Tech Listing → Tech in Context

BEFORE: "Used Python, FastAPI, PostgreSQL, Redis, Docker, and AWS to build
backend services"

Think: What did these services DO? What was the impact?

AFTER: "Built event-driven order processing pipeline (Python/FastAPI) handling
50K orders/day with sub-second confirmation, backed by PostgreSQL and Redis"

### Pattern 5: Feature Description → User/Business Impact

BEFORE: "Developed a recommendation engine using collaborative filtering"

Think: Who used it? What happened to the metrics?

AFTER: "Shipped collaborative filtering recommendation engine that increased
average session duration by 22 % and drove 15 % of total platform revenue"

---

## Bullets to Delete

Some bullets add negative value — they make the candidate look weaker or
waste precious page space. Remove or replace these:

- "Participated in daily standups and sprint planning" — everyone does this
- "Wrote unit tests for code" — this is baseline expectation, not achievement
  (UNLESS you can say "Increased test coverage from 30 % to 85 %, reducing
  production incidents by 60 %")
- "Collaborated with team members" — show collaboration through the
  achievement itself
- "Fixed bugs and resolved issues" — too generic; pick one impressive bug
  fix and tell that story with impact
- "Followed agile methodology" — not an achievement
- "Attended technical workshops and training" — save space for what you
  *produced*, not what you consumed

---

## The "Above the Fold" Rule

The first bullet of your most recent role is the single most important line
on your entire CV. It gets read by virtually every recruiter who looks at
your resume. This bullet should be:

1. Your most impressive, most relevant achievement
2. Quantified with a compelling metric
3. Demonstrating the scope/seniority appropriate for the target role
4. Using technology relevant to the target role

Spend disproportionate time getting this bullet perfect. If this bullet
doesn't make someone want to keep reading, the rest of the CV doesn't matter.

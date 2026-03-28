---
name: cv-refine
description: >
  Refine, review, and improve software engineer CVs/resumes written in LaTeX.
  Use this skill whenever the user asks to review, refine, improve, polish, or
  rewrite their CV or resume — especially for software engineering roles. Also
  trigger when the user wants to tailor their CV for a specific job description,
  add quantified achievements, fix bullet points, or prepare their resume for
  job applications. Handles LaTeX source files directly. Even if the user just
  says "look at my CV" or "help me with my resume", use this skill.
---

# CV Refine — Software Engineer Resume Optimizer

This skill helps refine LaTeX-based software engineer CVs so they survive
recruiter screening, ATS keyword filters, and hiring-manager review. It
operates directly on `.tex` source files.

## How recruiter screening actually works

Understand the funnel your CV must survive:

1. **ATS keyword filter (0 seconds)** — Software scans for role-relevant
   keywords. If the match score is too low the CV is never seen by a human.
2. **Recruiter glance (6–10 seconds)** — A recruiter scans for: current title,
   company names, years of experience, education, and one or two standout
   bullets. If nothing grabs them, it's a pass.
3. **Recruiter deep read (30–60 seconds)** — Only ~20 % of CVs reach this
   stage. The recruiter checks for role fit, career progression, and red flags.
4. **Hiring manager review** — Looks for technical depth, scope of impact,
   relevant domain experience, and signals of seniority.

Your job is to optimize for ALL four stages simultaneously.

## Workflow

### Step 1 — Gather context

Before touching the LaTeX file, collect:

- **The target role** — job title, company, and (ideally) the job description.
  If the user doesn't have a specific JD, ask what *type* of role they're
  targeting (e.g. "senior backend at a mid-stage startup" or "forward-deployed
  engineer at an AI company").
- **The user's career narrative** — what story should this CV tell? Bridge
  role? IC depth? Leadership transition? This shapes what to emphasize.
- **Years of experience** — determines page count guidance (≤10 yr → 1 page,
  10–20 yr → 1–2 pages, 20+ yr → 2 pages max).

### Step 2 — Read and audit the current CV

Read the `.tex` file thoroughly. Then perform a structured audit using the
checklist in `references/review-checklist.md`. Produce a short written report
for the user covering:

- Overall impression (the 6-second glance test: what jumps out?)
- Section-by-section issues
- Bullet quality score (how many bullets pass the "So What?" test?)
- Keyword gap analysis (if a JD was provided)
- Top 3 highest-impact changes

Present this report to the user and discuss before making edits.

### Step 3 — Rewrite bullets

This is where most of the value is. Read `references/bullet-writing-guide.md`
for the full methodology. The core formula:

> **Accomplished [X] as measured by [Y], by doing [Z]**

Every bullet must answer: *"So what? Why should the hiring manager care?"*

Rules for rewriting bullets:

- **Lead with impact, not activity.** "Reduced API latency by 40 %" beats
  "Worked on API performance improvements."
- **Quantify everything possible.** Revenue, users, latency, uptime,
  team size, lines of code reduced, deployment frequency — any number is
  better than no number. If the user doesn't know exact numbers, ask them
  to estimate. Rough numbers are vastly better than no numbers.
- **Show scope.** Mention scale signals: DAU, request volume, team size,
  number of services, revenue impacted. This is how readers calibrate
  seniority.
- **Use strong action verbs.** Start every bullet with a past-tense action
  verb. Avoid weak verbs: "helped", "assisted", "was responsible for",
  "worked on", "involved in". Prefer: "architected", "led", "shipped",
  "reduced", "accelerated", "migrated", "designed", "automated",
  "mentored", "negotiated".
- **One accomplishment per bullet.** Don't cram two achievements into one
  bullet — split them.
- **3–5 bullets per role.** More than 5 dilutes impact. Fewer than 3 looks
  thin. For the most recent role, 4–5 is ideal. Older roles can have 2–3.
- **Recency bias is real.** Put your best, most relevant bullets at the top of
  each role. Recruiters read the first bullet and maybe the second. The
  third bullet onward is for the hiring manager deep-read.

### Step 4 — Optimize sections

**Section ordering** (for most SWE CVs):

```
1. Header (name, contact, links)
2. Work Experience
3. Skills / Technologies
4. Projects (if relevant — especially for < 5 yr experience)
5. Education
```

Do NOT include: objective/summary statements (unless senior/staff+ level where
a 1-line positioning statement adds clarity), references, headshot, age,
marital status, or hobbies (unless directly relevant to the target role).

**Header must include:**
- Full name
- Email, phone
- LinkedIn URL, GitHub URL (if active)
- Location (city only — no full address)
- Portfolio/personal site (if it's good; if it's not, leave it out)

**Skills section guidelines:**
- Group by category: Languages, Frameworks, Infrastructure, Tools
- List only technologies you can discuss confidently in an interview
- Put the most relevant tech for the target role first
- Don't list soft skills here (leadership, communication) — demonstrate
  those through your bullets instead
- Don't list basic tools everyone knows (Git, JIRA, VS Code) unless the
  JD specifically asks for them

**Education:**
- For > 3 years of experience, education moves to the bottom and gets
  minimal space (school, degree, year)
- GPA only if > 3.5 and < 3 years out of school
- Relevant coursework only for new grads

### Step 5 — Keyword optimization (if JD provided)

Extract keywords from the job description in these categories:

- **Required technologies** (languages, frameworks, tools)
- **Domain keywords** (fintech, e-commerce, ML, distributed systems)
- **Seniority signals** (mentorship, architecture, cross-functional, strategy)
- **Methodology keywords** (agile, CI/CD, TDD, microservices)

Cross-reference with the CV. For each missing keyword that's genuinely part
of the user's experience, find a natural place to weave it in. Never stuff
keywords — they must fit organically in real achievement bullets.

### Step 6 — LaTeX-specific polish

- Ensure consistent formatting: date formats, bullet styles, spacing
- Keep to the target page count — adjust `\\vspace`, font size, or margins
  if needed, but don't go below 10pt or margins below 0.5in
- Make sure the PDF compiles cleanly with no warnings
- Verify hyperlinks work (`\\href` for LinkedIn, GitHub, portfolio)
- Use `\\textbf` sparingly for emphasis — bolding metrics in bullets can
  help them pop during the 6-second scan
- If using multi-column layouts, ensure ATS can still parse the content
  (some ATS systems struggle with complex column layouts)

### Step 7 — Final review

Before delivering the final version:

1. Read every bullet aloud — does it sound like a human achievement or a
   job description copy-paste?
2. Run the "stranger test" — if someone who doesn't know the user reads
   this CV, can they tell what this person is *good at* within 10 seconds?
3. Check for consistency: tense (past tense for past roles, present for
   current), date formats, bullet punctuation (period or no period — pick
   one and stick with it)
4. Verify no orphan lines or awkward page breaks

## Anti-patterns to watch for and fix

These are the most common CV mistakes. Flag and fix all of them:

| Anti-pattern | Example | Fix |
|---|---|---|
| Responsibility listing | "Responsible for maintaining microservices" | "Migrated 12 microservices to Kubernetes, reducing deployment time from 2hr to 8min" |
| Tech-name dropping | "Used React, Node.js, PostgreSQL, Redis, Docker, Kubernetes" | Weave tech into achievement bullets: "Built real-time dashboard (React + WebSocket) serving 5K concurrent users" |
| Vague impact | "Improved system performance" | "Reduced P99 API latency from 800ms to 120ms by implementing query optimization and connection pooling" |
| Passive voice | "System was redesigned to handle more traffic" | "Redesigned ingestion pipeline to handle 10x traffic increase (2M → 20M events/day)" |
| Burying the lead | "Worked with team to deliver features that resulted in 30 % revenue increase" | "Drove 30 % revenue increase ($2.1M ARR) by shipping personalized recommendation engine" |
| Filler bullets | "Participated in code reviews and team meetings" | Remove entirely or replace with a real achievement |
| Wall of text | 8+ bullets per role, each 3 lines long | Trim to 4–5 sharp, single-line bullets |

## Seniority calibration

Tailor the CV voice to match the target seniority level:

**Junior / New grad (0–2 yr):**
- Emphasize projects, internships, open source contributions
- Show learning velocity and breadth
- Include hackathons, relevant coursework
- "Built X using Y" is fine

**Mid-level (3–6 yr):**
- Focus on independent ownership and delivery
- Show you can take a problem end-to-end
- Start showing mentorship, tech decisions
- "Designed and shipped X, resulting in Y"

**Senior (6–10 yr):**
- Emphasize cross-team impact, architecture decisions
- Show multiplier effect (mentoring, setting standards, improving processes)
- Include scope signals: team size, org impact
- "Led/Architected X across N teams, enabling Y"

**Staff+ (10+ yr):**
- Emphasize organizational impact, technical strategy
- Show you identified problems, not just solved assigned ones
- Include business-level metrics (revenue, cost savings, customer impact)
- A 1-line positioning statement at the top can work here
- "Defined technical strategy for X, resulting in Y across the organization"

## Reference files

- `references/review-checklist.md` — Structured audit checklist to run on
  every CV before making changes
- `references/bullet-writing-guide.md` — Detailed guide with examples for
  writing high-impact achievement bullets, including industry-specific
  templates and the quantification framework

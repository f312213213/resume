# CV Review Checklist

Run through every item before proposing changes. Mark each as PASS, WARN, or
FAIL with a short note.

---

## 1. First Impression (the 6-second scan)

- [ ] **Name is the largest text on the page** — immediately visible
- [ ] **Current role + company** are obvious within 2 seconds
- [ ] **Years of experience** can be inferred from work history dates
- [ ] **Key tech stack** is visible without hunting
- [ ] **No visual clutter** — clean whitespace, consistent alignment
- [ ] **Page count is appropriate** for experience level

## 2. Header / Contact

- [ ] Full name present
- [ ] Professional email (not `cooldude99@yahoo.com`)
- [ ] Phone number present
- [ ] LinkedIn URL (shortened: `linkedin.com/in/handle`)
- [ ] GitHub URL (if profile has meaningful activity)
- [ ] Location (city, country — not full street address)
- [ ] No photo, age, marital status, or nationality (unless required by
      country norms — e.g. some European/Asian markets expect photos)
- [ ] All links are clickable `\href{}` in the LaTeX source

## 3. Work Experience

- [ ] Reverse chronological order
- [ ] Each entry has: company name, role title, location, date range
- [ ] Date format is consistent (e.g., "Jan 2022 – Present" throughout)
- [ ] No unexplained gaps > 6 months (if gaps exist, they should be
      addressed somehow — sabbatical, personal project, etc.)
- [ ] Current role is in present tense, past roles in past tense
- [ ] Company context is provided for non-famous companies (1-line
      description: "Series B fintech startup, 50 employees" or similar)

## 4. Bullet Quality Audit

For EACH bullet, check:

- [ ] **Starts with a strong action verb** (not "Responsible for",
      "Helped with", "Involved in", "Worked on")
- [ ] **Contains at least one metric or quantification** — this is the
      single most impactful improvement for most CVs
- [ ] **Passes the "So What?" test** — would a hiring manager care?
- [ ] **Shows YOUR contribution**, not the team's. Use "I" language even
      if it's implied (Led, Designed, Built — not "The team built")
- [ ] **Single achievement per bullet** — not a compound sentence with
      two unrelated things
- [ ] **Appropriate length** — 1 to 2 lines. If > 2 lines, split or trim.

Scoring: Count the total bullets and how many pass ALL checks above.
- \> 80 % pass → Good, minor tweaks needed
- 50–80 % pass → Significant rewriting needed
- < 50 % pass → Full rewrite recommended

## 5. Skills Section

- [ ] Technologies are grouped by category
- [ ] Most relevant tech for target role appears first
- [ ] No obsolete tech that doesn't serve the narrative (e.g., jQuery
      when targeting a modern React role — unless it shows breadth)
- [ ] No soft skills listed (communication, teamwork — these are shown
      through bullets, not listed)
- [ ] No trivially obvious tools (Git, VS Code, JIRA) unless JD lists them
- [ ] Skill list matches what's actually demonstrated in the bullets

## 6. Projects Section (if present)

- [ ] Each project has: name, tech stack, 1-2 line description, link
- [ ] Projects are relevant to the target role
- [ ] For experienced engineers (5+ yr), projects should be exceptional
      to justify the space — open source with stars, published tools,
      significant side projects with real users
- [ ] No school assignments (unless truly impressive or for new grads)

## 7. Education

- [ ] Positioned appropriately (top for new grads, bottom for 3+ yr exp)
- [ ] Includes: institution, degree, field, graduation year
- [ ] GPA included only if > 3.5 and < 3 years post-graduation
- [ ] Relevant coursework only for new grads or career changers
- [ ] No high school

## 8. ATS Compatibility

- [ ] Standard section headings used (Experience, Education, Skills —
      not creative alternatives like "My Journey" or "Arsenal")
- [ ] No text embedded in images
- [ ] LaTeX compiles to a PDF where text is selectable (not scanned image)
- [ ] Key role-relevant terms appear in natural language, not only in
      the skills list
- [ ] If using multi-column layout, critical content is not lost when
      columns are linearized

## 9. Keyword Gap Analysis (requires JD)

If a target job description is available:

- [ ] List required technologies from JD → check which appear in CV
- [ ] List domain terms from JD → check which appear in CV
- [ ] List seniority signals from JD → check which appear in CV
- [ ] Identify top 5 missing keywords that the user genuinely has
      experience with
- [ ] Flag any JD requirements that are NOT in the user's background
      (the user should decide whether to address or ignore these)

## 10. LaTeX / Formatting

- [ ] Compiles without errors or warnings
- [ ] Consistent font usage throughout
- [ ] Margins ≥ 0.5 inches on all sides
- [ ] Font size ≥ 10pt for body text
- [ ] No orphan lines or widows
- [ ] Dates are right-aligned and consistent
- [ ] Bullet symbols are consistent
- [ ] Hyperlinks are styled but not distracting
- [ ] PDF metadata is clean (no random `\author{}` from a template)
- [ ] No page break in the middle of a role's bullet list

## 11. Narrative Coherence

- [ ] Career progression tells a clear story
- [ ] Each role shows growth from the previous one
- [ ] The CV positions the candidate for the TARGET role, not just
      documenting history
- [ ] If there's a career pivot, the narrative bridges old → new naturally
- [ ] The overall impression matches the target seniority level

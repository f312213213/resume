# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

A single-file LaTeX resume (`david_chien_resume.tex`) with Docker-based builds and GitHub Actions CI.

## Build Commands

```bash
# Local build (requires Docker)
./build.sh

# Or manually
docker build -t latex .
docker run --rm -i -v "$PWD":/data latex pdflatex david_chien_resume.tex
```

No local LaTeX installation needed — Docker handles everything.

## CI/CD

Pushing `.tex` changes to `master` triggers GitHub Actions which:
1. Builds PDF via Docker (runs pdflatex twice for cross-references)
2. Auto-commits the updated PDF with a robot emoji prefix
3. Uploads PDF as artifact (30-day retention)

## Resume Structure

The `.tex` file uses custom commands defined at the top:
- `\resumeSubheading{Company}{Location}{Title}{Dates}` — job header
- `\resumeSubSubheading{Title}{Dates}` — promoted role under same company
- `\resumeItem{Title}{Description}` — bullet point under a job
- `\resumeSubItem{Title}{Description}` — project entry
- `\resumeSubHeadingListStart/End` and `\resumeItemListStart/End` — list wrappers

Section order: Summary > Experience > Projects > Skills > Education

## Editing Guidelines

- Keep bullet points to ~1.5 lines max — recruiters scan in 6 seconds
- Every bullet should have a quantified result when possible (%, Nx, time saved)
- Use the format: **Action** + **What** + **Impact with numbers**
- The template is based on Sourabh Bajaj's resume template (MIT license)

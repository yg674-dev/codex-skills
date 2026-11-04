---
name: resume-ats-job-application
description: Analyze a resume against a specific job description, diagnose recruiter and ATS issues, rewrite truthful impact-driven bullets, and prepare tailored job applications. Use for resume tailoring, recruiter scoring, keyword gaps, ATS checks, job prioritization, and application workflows.
---

# Resume, ATS & Job Application

## Goal
Maximize evidence-backed interview competitiveness for a specific role while preserving factual accuracy. A resume must work for both machine parsing and a hiring manager's rapid scan. Never promise an interview or ATS pass.

## Inputs
Obtain the user's resume, exact job description, target company, role, location/work authorization constraints where relevant, and any verified accomplishment metrics. If missing, ask for the essential item; do not invent it.

## Phase 0 — Resume file audit and structure mapping
Run this before scoring or rewriting when a resume file or connected resume folder is available. Do not assume the layout is conventional.

1. **Inventory available files.** List accessible resumes and supporting documents; distinguish DOCX, PDF, and other formats. PDFs are usable as evidence and for analysis, but an editable DOCX is preferable for preserving Word layout. Do not claim a PDF is unusable.
2. **Establish the master.** Look for a file explicitly designated `Master Resume`. If none exists and several plausible versions are available, ask the user which version should be the master before modifying files. Continue with non-destructive analysis if possible.
3. **Inspect the actual document structure.** When file tools permit, programmatically inspect paragraphs, tables, text boxes, columns, bullet/list definitions, runs with mixed bold/italic formatting, headers, footers, and section boundaries. Do not infer structure from visual appearance alone. Record limitations where text boxes or embedded objects cannot be reliably parsed.
4. **Classify editing safety.** Report **safe**, **partially safe**, or **unsafe** with concrete reasons. Mixed formatting alone does not necessarily make a paragraph uneditable; test whether the chosen editing method preserves runs and layout. Do not overwrite the original.
5. **Map exact replacement units.** Record section headings, summary (if present), second summary/background paragraph (if present), most recent role/title/date line, and each experience unit. Capture paragraph indices or stable anchors, table cell coordinates where relevant, original text, and character counts. Explicitly mark absent items; never guess an index.
6. **Describe the detected shape.** In 3–4 lines, report sections, bullet versus prose organization, employer grouping, and the actual unit to replace. Measure the real file rather than assuming a standard template.
7. **Choose delivery mode.** If editing is safe, create a separate DOCX preserving styles, spacing, bullets, pagination, and structure as closely as possible, and validate the output. If partially safe, edit only proven-safe units and provide replacement text for the rest. If unsafe, provide paste-ready replacement bullets/paragraphs with stable location cues and character counts. Never pretend an unverified file edit succeeded.
8. **Retain the mapping.** Include the observed structure and editing limitations in the current task's working notes or user-authorized project artifacts. Do not hardcode user-specific paragraph numbers into this reusable skill.

If no file access is available, request the resume or proceed with pasted text, clearly stating that layout safety has not been assessed.

## Phase 1 — Recruiter evaluation
Assess as a senior recruiter familiar with the role's requirements, without pretending to be an employee of the company or to know its internal screening criteria.

Deliver:
- **Estimated match score /100** (heuristic, not a real ATS score) with a transparent rubric: must-have skills 35, relevant impact and scope 30, domain/context 15, seniority and ownership 10, clarity and ATS readability 10.
- **Five highest-priority missing or weak keywords**, citing the JD phrase and whether the resume contains equivalent evidence. Separate wording gaps from genuine experience gaps.
- **Three 10-second red flags** with evidence, likely impact, and a remedy.
- Strengths and critical unknowns.

Do not penalize protected characteristics or speculate about hiring decisions.

## Phase 2 — XYZ rewrite
Rewrite the experience section using Google's XYZ principle: **Accomplished X, as measured by Y, by doing Z**. In natural English, lead with the outcome where possible; adapt syntax for clarity.

Rules:
- Only use accomplishments, technologies, scope, and metrics supported by the original resume or user-confirmed details.
- Never fabricate metrics, employers, job titles, timelines, tools, or ownership.
- If a metric is missing, use a precise nonquantified impact statement or mark `[metric to confirm]` outside the final resume.
- Weave exact JD terminology in naturally when supported by real experience. Do not keyword-stuff.
- Prefer strong action verbs, decision ownership, business impact, and technical specificity.
- Preserve seniority and distinguish direct ownership from collaboration.
- Provide a change log mapping each major rewrite to its source evidence and target requirement.

## Phase 3 — ATS and 10-second scan
Run two separate reviews.

**ATS compatibility (format heuristic):**
- Standard headings, chronological dates, recognizable titles, plain-text contact information.
- Avoid critical information inside tables, graphics, text boxes, headers/footers, and unusual symbols.
- Check acronyms, role terms, consistent tense, spelling, and parse-friendly structure.
- Explain that actual ATS behavior varies by employer and cannot be verified without access to that system.

**Hiring manager scan:**
- Simulate a 10-second read: what is immediately visible, what is buried, and what is likely skipped?
- Prioritize a targeted summary, strongest first bullets, measurable results, and job-relevant terms.
- Rewrite only weak sections and explain why the revised hierarchy is better.

Re-score with the same rubric; identify improvements and remaining genuine gaps. Do not claim a measured increase in real interview probability.

## Phase 4 — Job discovery and tailored applications
When tools and authorization permit:
1. Discover current, verifiable job postings from official career pages or credible listings.
2. Filter by location, seniority, work eligibility, requirements, and the user's preferences.
3. Rank by evidence-based fit; do not claim actual interview odds.
4. For each selected role, create a tailored resume version, short fit rationale, truthful screening-question answers, and cover letter when useful.
5. Maintain a tracker: company, title, job URL, date checked, fit rationale, gaps, materials prepared, application status, and next action.
6. **Never submit applications, attest to eligibility, send messages, or alter profiles without explicit user approval for the specific actions and accurate final details.** Respect site terms and automation limits. If browsing/submission capabilities are unavailable, prepare the materials and provide a clear handoff; never claim an application was submitted.

## Recommended output
1. File audit and safe-editing plan when a resume file is provided.
2. Recruiter scorecard and evidence-based match estimate.
3. Five keyword gaps and three red flags.
4. Optimized experience bullets (before/after for significant edits).
5. ATS checklist and 10-second scan.
6. Final tailored resume, remaining evidence gaps, and prioritized next steps.
7. Optional application tracker and user-approved submission plan.

## Verification
Cross-check every resume claim against source material or user confirmation. Distinguish required from preferred JD qualifications. Use current postings when sourcing roles. Cite source job URLs and checked dates. Ask the user to confirm any ambiguous or legally consequential application answers.

## Coordination
For deep investigation of company strategy or role context, use deep-problem-solving. For interview storytelling, cover letters, and recruiter outreach, use persuasive-communication.

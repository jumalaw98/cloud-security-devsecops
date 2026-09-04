# Cloud Security & DevSecOps: A Frontend Developer's Journey In

This is my working record of moving from React/TypeScript frontend development into Cloud Security and DevSecOps — not a portfolio highlight reel, but the actual roadmap, curriculum, notes, labs, and evidence, kept in one place and pushed as I go.

I'm building this in public for two reasons. First, writing it down and publishing it is part of the learning method itself — teaching a concept, even to an empty room, is one of the fastest ways to find out whether I actually understand it. Second, if you're a developer looking at the same jump — from building things to securing them — I'd rather leave a real trail than a polished one. The stalled weeks are in here too.

## Where I started

React, TypeScript, JavaScript, HTML/CSS. Some experience deploying applications. Basic exposure to Linux, VMs, Azure, Git/GitHub, and CI/CD concepts. A working but non-expert understanding of application and web security. Strong communication, documentation, and stakeholder-facing skills from a non-engineering background.

## Where I'm headed

Cloud Security Engineer / DevSecOps Engineer, with the application-security angle as my differentiator — most people entering this field come from networking or generalist IT, not from having actually shipped production frontend code. That combination is the bet this whole roadmap is built around.

## The deployed site

This repo is also a GitHub Pages site, built with Jekyll and the [`just-the-docs`](https://just-the-docs.com) theme — sidebar navigation, search, no build step to run yourself. `index.md` is the site homepage (separate from this file, which is what GitHub shows on the repo's own landing page). See `DEPLOY.md` for the two-step setup: push, then flip on Pages in repo settings.

Not everything in the repo is part of the styled site on purpose — `weekly-notes/`, `monthly-reviews/`, and each phase's `notes.md`/`articles.md`/`labs/`/`project/`/`evidence/` stay as plain files, browsable on GitHub normally. The curated pages (roadmap, curriculum, skills matrix, phase overviews) are what's built into the nav.

## How this repo is organized

```
.
├── README.md            ← this file
├── ROADMAP.md            ← the strategy: skills-gap analysis, staged plan, cloud/cert strategy, career mapping
├── CURRICULUM.md          ← the execution system: every phase broken into modules, labs, and projects
├── skills-matrix.md       ← my living, dated self-assessment — the real progress tracker, not the calendar
├── weekly-notes/           ← short, dated, honest — some weeks are a paragraph
├── monthly-reviews/         ← what I learned, built, published, and what's still weak
└── phases/
    ├── 00-orientation/
    ├── 01-linux-fundamentals/
    ├── 02-networking/
    ├── 03-git-github-workflows/
    ├── 04-bash-python-automation/
    ├── 05-web-app-security/
    ├── 06-cloud-fundamentals/
    ├── 07-azure-security/
    ├── 08-aws-security/
    ├── 09-docker-container-security/
    ├── 10-infrastructure-as-code/
    ├── 11-cicd-devsecops/
    ├── 12-kubernetes-fundamentals/
    ├── 13-kubernetes-security/
    ├── 14-monitoring-detection-ir/
    ├── 15-supply-chain-policy-as-code/
    ├── 16-cloud-security-architecture/
    └── 17-capstone-job-readiness/
```

**`ROADMAP.md` is the why.** Why Azure before AWS, why this certification order, why Kubernetes waits until Phase 12 instead of showing up on day one. If a decision in here looks odd, the reasoning lives there.

**`CURRICULUM.md` is the how.** Every phase, broken into modules, each with objectives, essential vs. optional concepts, a primary learning resource, a hands-on lab, a phase-ending project, article ideas, and a certification checkpoint that's honest about *now* vs. *later*.

**Every `phases/NN-name/` folder is identical inside:**

| File/folder | What goes there |
|---|---|
| `README.md` | Phase summary, objectives, and completion-gate checklist |
| `notes.md` | My dated, unpolished learning log for that phase |
| `labs/` | Scripts, configs, command output from each lab |
| `project/` | Actual project code/config for that phase's project(s) |
| `evidence/` | Before/after scans, screenshots, scan output — the proof, not just the claim |
| `articles.md` | Published articles plus ideas not yet written |

A phase is only marked complete when its completion gate is fully checked — not when the lessons are technically "done." See `CURRICULUM.md` for what that means concretely, phase by phase.

## The loop

Every phase runs the same cycle:

**Learn → Lab → Build → Break → Secure → Automate → Document → Write → Publish → Assess → Certify → Reflect → Advance**

Nothing here is a course-completion checklist. If I can't demonstrate a control live — configure it, break it, detect it, fix it, explain why — I don't count it as learned yet, regardless of how many modules say otherwise.

## Certifications along the way

Terraform Associate → SC-500 (Microsoft's Cloud and AI Security Engineer Associate — AZ-500's replacement) → CKA → CKS → AWS Certified Security – Specialty. Full reasoning, free/premium breakdown, and links in `ROADMAP.md` Section 8 and `CURRICULUM.md`'s consolidated certification strategy.

## Following along

If you're attempting something similar: start with `ROADMAP.md` for the reasoning, then `CURRICULUM.md` Phase 0 for the first concrete steps. The `phases/01-linux-fundamentals/README.md` is written out at full template depth as a worked example of what every later phase's structure means in practice.

## Status

Currently in: **Phase 0 — Orientation & Learning Environment**
Last updated: _(update this line whenever you touch the repo)_

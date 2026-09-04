---
title: Curriculum
nav_order: 3
---

# Cloud Security & DevSecOps Curriculum
*My step-by-step apprenticeship, built from my own master roadmap — written for me to actually follow, and put on GitHub in case it's useful to anyone else attempting the same jump from frontend into cloud security.*

**How this document relates to the roadmap:** `cloud-security-devsecops-roadmap.md` is my **strategy** — why Azure-first, why this cert order, why this project sequence. This document is the **execution system** — the actual phases, modules, labs, and gates I work through week by week. I keep both open; when this curriculum says "see roadmap Section X," that's where the reasoning lives.

**A note on how detail is allocated:** Phase 0 and Phase 1 (Linux) are written out at full depth as a worked example of the module template. From Phase 2 onward, every module still covers the same fields — purpose, objectives, concepts, tools, resources, the 8-step sequence, labs — but in a tightened card format so the document stays usable instead of becoming 300 pages of repeated boilerplate. Flagship labs and every phase-ending project still get full detail throughout.

**A note on project and article counts:** every "Project" and "Articles" list below is a floor, not a ceiling. Where a phase clearly warrants a second smaller project (a variant, a deeper dive on one control, a repeat rep on a different app), I'll build it — the point is reps and evidence, not matching a fixed count. Same with articles: the lists give 2–5 solid ideas per phase as a starting menu, but if a phase generates more real, evidence-backed things worth writing about, I write them. The only rule that doesn't bend: never publish an article without real evidence behind it (a screenshot, a scan result, a diff, a number).

**How this ties to the GitHub learning log (roadmap Section 13a):** every phase's completion gate, skills-matrix update, and article list below has a home in `cloud-sec-learning-log/stages/phase-XX-<name>.md`. I'll write that file as I go through the phase, not retroactively — it's the honest, dated version of "what actually happened," separate from the polished project READMEs.

**The loop that runs through everything:** LEARN → LAB → BUILD → BREAK → SECURE → AUTOMATE → DOCUMENT → WRITE → PUBLISH → ASSESS → CERTIFY → REFLECT → ADVANCE.

**The mindset ladder that runs through every phase** (see roadmap Section 22 for the long version):
1. I know how it works → 2. I know how to deploy it → 3. I know how to configure it securely → 4. I know how to attack/test it → 5. I know how to detect attacks on it → 6. I know how to automate its security → 7. I can design secure systems using it → 8. I can audit someone else's implementation of it.

---

## Phase Map (18 phases, Phase 0–17)

| # | Phase | Merges/notes vs. your suggested structure |
|---|---|---|
| 0 | Orientation & Learning Environment | as suggested |
| 1 | Linux Fundamentals | as suggested |
| 2 | Networking Fundamentals | as suggested |
| 3 | Git, GitHub & Developer Workflows | as suggested |
| 4 | Bash/Python & Security Automation | as suggested |
| 5 | Web & Application Security | as suggested |
| 6 | Cloud Fundamentals | as suggested |
| 7 | Azure Administration & Security | as suggested |
| 8 | AWS Fundamentals & Security | as suggested |
| 9 | Docker & Container Security | as suggested |
| 10 | Infrastructure as Code (Terraform) | as suggested |
| 11 | CI/CD & DevSecOps Pipelines | **merged** your Phases 11+12 — a security gate can't be taught separately from the pipeline it gates |
| 12 | Kubernetes Fundamentals | your Phase 13 |
| 13 | Kubernetes Security | your Phase 14 — kept separate from 12 on purpose, see roadmap Stage 10 rationale on sequencing |
| 14 | Cloud Monitoring, Detection & Incident Response | **merged** your Phases 15+16 — detection without a response process is half a skill |
| 15 | Supply Chain Security & Policy as Code | **merged** your Phases 17+18 — SBOM/signing and OPA/Conftest are taught together in practice |
| 16 | Cloud Security Architecture | your Phase 19 |
| 17 | Capstone & Job Readiness | **merged** your Phases 20+21 — the capstone *is* the job-readiness proof |

---

# PHASE 0 — Orientation & Learning Environment

*Duration: 1 week (1hr/day) / 3–4 days (2–3hr/day). This phase is about setup, not mastery — move fast.*

## Module 0.1 — Career Orientation & Role Clarity

### 1. Purpose
You're about to spend a year or more building specific skills. Before writing any code, you need a clear, honest picture of what a Cloud Security/DevSecOps Engineer actually does day to day — so every later module has a "why" attached to it, not just a "what."

### 2. Learning Objectives
- Explain, in your own words, the difference between DevSecOps Engineer, Cloud Security Engineer, Application Security Engineer, and SOC Analyst.
- Identify which of these four roles best fits your current strengths (see roadmap Section 6).
- Write a one-page "career thesis" stating your target entry role and why.

### 3. Concepts to Learn
**Essential:** shared responsibility model (conceptually, not technically yet); how DevSecOps differs from traditional security; what "shift-left" means.
**Important:** typical team structures (platform team vs security team vs SRE); how a DevSecOps engineer's day differs from a SOC analyst's.
**Advanced/Optional:** organizational security maturity models — skip for now.

### 4. Technologies & Tools
None yet. This module is research and reflection only.

### 5. Learning Resources
- **Primary:** job postings — read 15–20 real "Cloud Security Engineer" / "DevSecOps Engineer" postings on LinkedIn to extract common requirements (this is your single best free resource for this module).
- **Secondary:** a handful of "day in the life" blog posts from working DevSecOps engineers (search current ones — don't rely on old posts).
- **Reference:** none needed yet.
- **Hands-on lab:** none — this module is 100% research/reflection.

### Sequence
1. **Learn** — read the job postings and 2–3 "day in the life" posts.
2. **Practice** — n/a.
3. **Break** — n/a.
4. **Fix** — n/a.
5. **Automate** — n/a.
6. **Document** — write your one-page career thesis (target role, why, current strengths, biggest gaps).
7. **Teach** — no article yet; save the thesis for your future "why I made this career switch" post.
8. **Test** — you can state your target entry role and defend it in two sentences without hesitation.

---

## Module 0.2 — Environment & Tooling Setup

### 1. Purpose
Every later module assumes a working lab environment. Get this right once, now, so you're never blocked by tooling in Phase 1 onward.

### 2. Learning Objectives
- Have a working Linux environment (VM or dedicated machine) ready for Phase 1.
- Have a dedicated "security work" GitHub account, password manager, and note-taking system configured.
- Have billing alerts configured on both Azure and AWS free tiers before you provision a single resource.

### 3. Concepts to Learn
**Essential:** what a hypervisor/VM is (just enough to install one); the difference between a free-tier resource and a pay-as-you-go resource.
**Important:** why you should never reuse your personal GitHub identity for security research repos that might later be linked publicly to sensitive findings.
**Advanced/Optional:** dual-booting Linux natively — nice to have later, not required now.

### 4. Technologies & Tools
| Tool | Why | Free? | Now or later |
|---|---|---|---|
| VirtualBox or a $5–6/mo VPS | Your Linux lab environment | Free (VirtualBox) | Now |
| GitHub account (dedicated) | Portfolio home | Free | Now |
| Password manager (Bitwarden) | Credential hygiene from day one | Free tier | Now |
| Note system (Obsidian) | Track progress, skills matrix | Free | Now |
| Azure free account + AWS free tier | Cloud labs (Phase 6+) | Free tier | Set up now, use from Phase 6 |

### 5. Learning Resources
- **Primary:** VirtualBox official quick-start guide.
- **Secondary:** your VPS provider's getting-started doc if you choose a VPS instead.
- **Official documentation:** virtualbox.org docs; docs.github.com.
- **Hands-on lab:** installing everything *is* the lab.

### Sequence
1. **Learn** — skim VirtualBox docs.
2. **Practice** — install VirtualBox, create an Ubuntu VM, boot it.
3. **Break** — n/a.
4. **Fix** — n/a.
5. **Automate** — n/a (you'll automate VM provisioning later with Vagrant/Terraform if you want, not now).
6. **Document** — a short `setup-notes.md` in your notes app: what you installed, versions, gotchas.
7. **Teach** — no article.
8. **Test** — you can SSH or console into your Ubuntu VM and run `uname -a` successfully.

---

## Module 0.3 — How You'll Track Progress

### 1. Purpose
This curriculum only works if you can see progress. Set up the tracking system now.

### 2. Learning Objectives
- Have a living skills matrix (Section 13 below) started with your Phase 0 baseline.
- Have a portfolio repo (`cloud-sec-portfolio` or similar) created as your central index.

### Sequence (compact)
Learn: skim Section 13 (Skills Matrix) below. Practice: create the tracking doc and the index repo. Document: baseline your current skill levels honestly (reuse roadmap Section 1's table as your starting point). Test: the tracker exists and is dated.

---

### Phase 0 — Project
No project — Phase 0 has no build deliverable, only setup.

### Phase 0 — Articles
None yet — you have nothing to write about. (Resist the urge to publish a "starting my cloud security journey" post; save your writing energy for evidence-backed content starting Phase 1.)

### Phase 0 — Certification Checkpoint
**Skip.** Nothing to certify yet.

### Phase 0 — Completion Gate
- [ ] Career thesis written
- [ ] Linux VM boots and is reachable
- [ ] Dedicated GitHub account + portfolio index repo created
- [ ] Billing alerts configured on Azure and AWS (even though you won't use them until Phase 6)
- [ ] Skills matrix baseline recorded

**Ready to move on** if all boxes are checked. **Needs more practice** only applies if your VM doesn't reliably boot — fix that before Phase 1, everything depends on it.

---

# PHASE 1 — Linux Fundamentals

*Duration: 3 weeks (2hrs/day) · 5–6 weeks (1hr/day) · 2 weeks (3–4hrs/day). Completion ≠ mastery — you'll keep using and re-hardening Linux in every phase from here on; expect to feel genuinely comfortable only after Phase 9 (Docker) forces you to use these skills again.*

## Module 1.1 — Linux Architecture

**Purpose:** Everything you'll deploy (containers, Kubernetes nodes, CI/CD runners) is Linux underneath. Understanding the kernel/shell/filesystem relationship now prevents "magic box" thinking later.
**Objectives:** Explain the kernel vs. shell vs. userspace relationship; identify your distro and kernel version from the CLI; explain what a process actually is at a conceptual level.
**Concepts — Essential:** kernel vs shell, distros (Ubuntu/Debian family, why it's the DevSecOps default), the boot process at a high level. **Important:** package managers (`apt`) as the OS's "npm." **Advanced/Optional:** kernel modules, custom kernel builds — skip.
**Tools:** just the CLI you already set up in Module 0.2 — nothing new yet.
**Resources — Primary:** Linux Journey (free, linuxjourney.com). **Secondary:** DigitalOcean's "Introduction to Linux Basics" tutorial. **Docs:** `man` pages themselves (`man bash`). **Lab:** your own VM.
**Sequence:** Learn (Linux Journey "Grasshopper" section) → Practice (`uname -a`, `lsb_release -a`, `apt list --installed | wc -l`) → Break/Fix: n/a this early → Document: one paragraph, in your own words, explaining kernel vs shell → Write: none yet → Test: explain the boot process out loud to an imaginary junior without notes.

## Module 1.2 — Filesystem

**Purpose:** File location conventions (`/etc`, `/var`, `/home`) are where security-relevant data lives (configs, logs, secrets) — you need this map before you can secure or audit anything.
**Objectives:** Navigate the FHS confidently; explain what lives in `/etc`, `/var/log`, `/home`, `/tmp`, `/root`; find a file by name or content across the filesystem.
**Concepts — Essential:** FHS layout, absolute vs relative paths, `find`/`locate`/`grep`. **Important:** mount points, disk usage (`df`, `du`). **Advanced:** filesystem types (ext4 vs xfs) — skip for now.
**Tools:** `find`, `grep`, `df`, `du` — all pre-installed.
**Resources — Primary:** Linux Journey "Filesystem" section. **Secondary:** the FHS spec itself (pathname.com/fhs) as a quick reference. **Lab:** your VM.
**Sequence:** Learn → Practice (`find / -name "*.conf" 2>/dev/null | head`, `du -sh /var/log`) → Break: fill `/tmp` intentionally with a large file and watch `df` react → Fix: clean it up, understand disk-full failure modes → Document: a one-page "where things live" cheat sheet → Test: given an unfamiliar Linux box, you can locate config files and logs for any given service within 2 minutes.

## Module 1.3 — Users & Groups

**Purpose:** IAM (Phase 6+) is just Linux users/groups at cloud scale. Master the local version first.
**Objectives:** Create users and groups; assign users to groups; explain UID/GID and why UID 0 is dangerous; audit `/etc/passwd` and `/etc/group` for anomalies.
**Concepts — Essential:** `useradd`/`usermod`/`groupadd`, `/etc/passwd`, `/etc/shadow`, `/etc/group`, `sudo` vs root. **Important:** `sudoers` file syntax for least-privilege sudo rules. **Advanced:** PAM modules — skip.
**Tools:** built-in user management commands.
**Resources — Primary:** Linux Journey "Grasshopper: Users." **Secondary:** DigitalOcean "Linux Users and Groups Explained." **Lab:** your VM.
**Sequence:** Learn → Practice (create a `deploy` user with a specific sudo rule limited to restarting one service, not full sudo) → Break: create a second admin-equivalent user and forget to document it (a classic real-world finding) → Fix: audit `/etc/passwd` for unexpected UID-0 accounts, remove the shadow admin → Automate: write a one-line script that lists all users with sudo rights → Document: your least-privilege sudoers pattern → Write idea: "Least-privilege sudo: a 10-minute Linux hardening habit" → Test: given a box, you can list every account with elevated privileges and justify (or flag) each one.

## Module 1.4 — Permissions

**Purpose:** File permission misconfigurations are one of the most common real-world findings (world-writable configs, secrets readable by any user).
**Objectives:** Read and set permissions using both symbolic and octal notation; explain SUID/SGID risk; audit a directory tree for world-writable or overly-permissive files.
**Concepts — Essential:** `chmod`, `chown`, `umask`, octal notation. **Important:** SUID/SGID bits and why they're a privilege-escalation vector. **Advanced:** ACLs (`setfacl`) — important later, optional now.
**Tools:** `chmod`, `chown`, `find -perm`.
**Resources — Primary:** Linux Journey "Permissions." **Secondary:** "Understanding Linux File Permissions" (RedHat blog). **Lab:** your VM.
**Sequence:** Learn → Practice (set 750/640-style least-privilege perms on a test directory) → Break: create a world-writable file containing a fake "password" string → Fix: find it (`find / -perm -o+w -type f 2>/dev/null`) and correct permissions → Automate: a script that scans for world-writable files and SUID binaries → Document: before/after permission audit output → Write idea: "I scanned my own server for world-writable files — here's what I found" → Test: given a directory tree, you correctly identify every overly-permissive file within 5 minutes.

## Module 1.5 — Processes

**Purpose:** Detecting a compromised or misbehaving service starts with understanding what's actually running.
**Objectives:** List, inspect, and kill processes; identify a process's owning user and listening ports; explain zombie/orphan processes conceptually.
**Concepts — Essential:** `ps`, `top`/`htop`, `kill`/`killall`, process states. **Important:** `lsof`, mapping a process to open files/ports. **Advanced:** cgroups/namespaces — save this, it becomes essential in Phase 9 (Docker).
**Tools:** `ps`, `htop`, `lsof`.
**Resources — Primary:** Linux Journey "Processes." **Secondary:** DigitalOcean "How To Use ps, kill, and nice." **Lab:** your VM.
**Sequence:** Learn → Practice (`ps aux`, `htop`, kill a runaway test process) → Break: start a fake "suspicious" background process bound to a port → Fix/Investigate: find it via `lsof -i` and `ps`, kill it → Document: your process-triage checklist → Test: given a box with an unfamiliar process running, you can identify what it is, what it's doing, and whether to kill it, in under 5 minutes.

## Module 1.6 — Networking (Linux side)

**Purpose:** Bridges directly into Phase 2. You need to see your own machine's network state before studying networking theory abstractly.
**Objectives:** List listening ports and their owning processes; use `curl`/`wget`/`ss` confidently; explain the difference between a listening and an established connection.
**Concepts — Essential:** `ss`/`netstat`, `curl`, `/etc/hosts`, `/etc/resolv.conf`. **Important:** basic `iptables`/`ufw` rules. **Advanced:** full iptables chains — deferred to Phase 2/hardening module.
**Tools:** `ss`, `curl`, `ufw`.
**Resources — Primary:** Linux Journey "Networking." **Lab:** your VM.
**Sequence:** Learn → Practice (`ss -tulpn`, identify every listening port and its process) → Break: stand up a throwaway `python3 -m http.server` on a random port → Investigate/Fix: find it with `ss`, decide if it should be closed, close it with `ufw` → Document: a "known good" baseline of what should be listening on a clean box → Test: you can baseline a box's listening ports and immediately flag anything unexpected.

## Module 1.7 — Services (systemd)

**Purpose:** Almost everything you'll secure later (web servers, agents, exporters) runs as a systemd service.
**Objectives:** Start/stop/enable/disable services; write a minimal custom systemd unit; check service status and logs.
**Concepts — Essential:** `systemctl`, unit files, enabled vs running. **Important:** running a service as a non-root dedicated user. **Advanced:** systemd sandboxing directives (`ProtectSystem=`, `NoNewPrivileges=`) — worth learning now, it's a genuinely strong hardening habit.
**Tools:** `systemctl`, `journalctl`.
**Resources — Primary:** DigitalOcean "Systemd Essentials." **Docs:** `man systemd.unit`. **Lab:** your VM.
**Sequence:** Learn → Practice (write a unit file for a simple script/app, running as a dedicated non-root user) → Break: run the same service as root first → Fix: convert it to a dedicated unprivileged user + add `NoNewPrivileges=true` → Document: your hardened unit-file template → Write idea: "Running services as non-root with systemd — a practical template" → Test: you can take any simple app and write a hardened systemd unit for it from memory.

## Module 1.8 — Logs

**Purpose:** Every later detection/IR skill (Phase 14) depends on reading logs fluently now.
**Objectives:** Read `journalctl` and `/var/log/auth.log`; filter logs by time/service/severity; identify a failed-login pattern in auth logs.
**Concepts — Essential:** `journalctl`, `/var/log/auth.log`, `/var/log/syslog`. **Important:** `grep`/`awk` for log filtering. **Advanced:** centralized logging — that's Phase 14.
**Tools:** `journalctl`, `grep`, `awk`.
**Resources — Primary:** Linux Journey/DigitalOcean log-reading guides. **Lab:** your VM.
**Sequence:** Learn → Practice (`journalctl -u ssh --since today`) → Break: attempt a few failed SSH logins against your own VM from another terminal → Investigate: find the failures in `auth.log` → Automate: a one-line `grep`/`awk` pipeline that counts failed logins per IP → Document: sample log excerpt + your one-liner → Test: given a raw auth log, you can identify a brute-force pattern within 2 minutes.

## Module 1.9 — SSH

**Purpose:** SSH is your primary access method for everything from here forward, and it's one of the most commonly misconfigured services in the real world.
**Objectives:** Configure key-only SSH auth; disable root login; change the default port; install and configure fail2ban; explain why each change matters.
**Concepts — Essential:** SSH key pairs, `sshd_config` hardening options, `fail2ban`. **Important:** SSH certificate authorities (enterprise-scale) — mention only, not needed yet. **Advanced:** bastion host patterns — save for Phase 7/8 cloud networking.
**Tools:** OpenSSH, fail2ban.
**Resources — Primary:** DigitalOcean "SSH Essentials." **Secondary:** a CIS-based SSH hardening checklist. **Lab:** your VM + a second attacker VM.
**Sequence:** Learn → Practice (generate a key pair, deploy it, confirm login works) → Break: leave password auth on temporarily and brute-force it from your second VM with a small wordlist, in your isolated lab only → Fix: disable password auth, disable root login, install fail2ban, confirm the brute-force now fails/gets banned → Automate: a Bash script that checks `sshd_config` against your hardening baseline → Document: before/after `nmap`/log evidence → Write idea: "Hardening SSH: the checklist, with real brute-force evidence" → Test: you can harden a fresh box's SSH config from memory in under 10 minutes.

## Module 1.10 — Linux Security Hardening (capstone module for this phase)

**Purpose:** Pull every prior module together into one repeatable hardening pass — this becomes your **Project 1** deliverable.
**Objectives:** Apply a full hardening checklist (users, permissions, services, SSH, firewall, auto-updates) to a fresh box unassisted; verify the result externally.
**Concepts — Essential:** CIS Benchmark for Linux (read the summary, don't try to implement all 300+ controls — pick the top 20 that matter most). **Important:** unattended-upgrades for automatic security patching. **Advanced:** AppArmor/SELinux — optional, mention only.
**Tools:** `ufw`, `unattended-upgrades`, `nmap` (from an external machine, to verify).
**Resources — Primary:** CIS Ubuntu Benchmark (free PDF, use the summary). **Secondary:** "Linux Server Hardening Checklist" community guides — cross-check, don't copy verbatim. **Lab:** a *fresh* VM (don't reuse the one you've been experimenting on all module — start clean to simulate a real deployment).

### Sequence
1. **Learn** — skim the CIS Benchmark summary, pick your top-20 controls.
2. **Practice** — provision a fresh VM and apply every prior module's lessons in order: users → permissions → services → SSH → firewall → auto-updates.
3. **Break** — from an external machine, run `nmap -sV` against the box before hardening; note every open port and banner.
4. **Fix** — apply the full checklist; re-run `nmap` and confirm the attack surface shrank to exactly what's needed.
5. **Automate** — turn your checklist into a single idempotent Bash script (`harden.sh`) that can re-apply itself safely.
6. **Document** — write the full hardening checklist as a standalone Markdown doc with before/after `nmap` evidence.
7. **Teach** — this is your flagship Phase 1 article (see below).
8. **Test** — see Phase 1 completion gate.

---

## Phase 1 — Project (Project 1 from the roadmap)

### Project Name: Hardened Linux Baseline Server

**Objective:** Provision and harden a Linux server to a documented, repeatable, evidence-backed baseline.
**Real-world scenario:** You've just joined a small startup as their first infrastructure-adjacent hire. There's no hardening standard. You're asked to stand up the first "golden image" baseline that every future server will be built from.
**Requirements:** functional — SSH-accessible, running a simple placeholder web service (even just Nginx's default page) to prove the box is usable. Security — key-only SSH, no root login, least-privilege sudo, firewall default-deny except SSH/HTTP, fail2ban active, automatic security updates enabled, no world-writable files, no unexpected listening services.
**Architecture:** single VM (local VirtualBox or a $5–6/mo cloud VPS), public/lab-accessible IP, one non-root admin user, one dedicated service user for the web server.
**Technologies:** Ubuntu 24.04 LTS, ufw, fail2ban, unattended-upgrades, Nginx (placeholder app).
**Implementation stages:** provision → baseline user/permission setup → SSH hardening → firewall setup → service hardening (Nginx as non-root-owned) → automatic updates → external verification scan → documentation.
**Security requirements:** listed above.
**Attack scenarios to try:** SSH brute-force from a second lab VM (before and after hardening); check for world-writable files; check for unexpected open ports via external `nmap`.
**Hardening:** apply Module 1.10's checklist in full.
**Testing:** external `nmap -sV` scan showing only intended ports open; `fail2ban-client status sshd` showing active bans from your simulated brute-force; a permissions audit script showing zero world-writable files.
**Documentation:** `README.md` (overview, architecture, how to reproduce), `hardening-checklist.md`, `harden.sh` (your automation script), `evidence/` folder with sanitized before/after scan output and screenshots.
**GitHub repository structure:**
```
cloud-sec-hardened-linux-server/
├── README.md
├── hardening-checklist.md
├── scripts/harden.sh
├── evidence/
│   ├── nmap-before.txt
│   ├── nmap-after.txt
│   └── fail2ban-ban-evidence.png
```
**Portfolio presentation:** lead your README with the before/after `nmap` diff — it's the single most convincing 10-second proof of skill a recruiter will see.
**Difficulty:** Beginner. **Estimated duration:** 1–2 weeks on top of the module work above (much of it overlaps).

---

## Phase 1 — Articles (pick 3–5, don't write all of them)

| Title | Type | Audience | Demonstrates | Evidence to include | Links to |
|---|---|---|---|---|---|
| "Hardening a fresh Ubuntu server: a checklist with real evidence" | Tutorial | Beginner/DevOps | End-to-end hardening competence | Before/after nmap, fail2ban logs | Project 1 repo |
| "Least-privilege sudo: a 10-minute habit that prevents real incidents" | Explainer | Developer | Deep understanding of privilege escalation risk | sudoers snippet, audit script | Module 1.3 |
| "I brute-forced my own SSH server (on purpose) — here's what fail2ban caught" | Security analysis | DevOps/Security | Attacker + defender mindset | Attack logs, ban evidence | Module 1.9 |
| "Where security-relevant files actually live on Linux" | Explainer | Beginner | FHS knowledge applied to security | Cheat sheet | Module 1.2 |
| "Running services as non-root with systemd" | Tutorial | Developer/DevOps | Practical hardening pattern | Unit file, before/after `ps aux` | Module 1.7 |

**How to turn Project 1 into multiple non-repetitive articles:** the hardening tutorial covers *how*; the brute-force article covers *what happens when it's attacked*; the sudo/systemd pieces are deep-dives on individual controls that stand alone for readers who found you via search. Each has a different entry point and a different piece of evidence — that's what keeps them from reading as the same post four times.

## Phase 1 — Certification Checkpoint

**Skip for now.** There is no standalone "Linux fundamentals" cert worth pursuing at this stage — CompTIA Linux+ exists but is redundant with what you'll prove through the project itself, and no cloud/K8s cert depends on it directly. Revisit only if a specific job listing requires it.

## Phase 1 — Skills Matrix Update

| Skill | Before Phase 1 | After Phase 1 | Evidence |
|---|---|---|---|
| Linux | 1 (Aware) | 3 (Independent) | Hardened server project, checklist, 2+ articles, fail2ban evidence |

## Phase 1 — Completion Gate

**Knowledge:** [ ] I can explain the Linux boot process, FHS layout, and the difference between users/groups/permissions. **Practical:** [ ] I can harden a fresh box from memory in under 30 minutes. **Security:** [ ] I can identify and remediate world-writable files, unexpected listening services, and weak SSH config. [ ] I've demonstrated a brute-force attempt against my own SSH in a controlled lab and shown fail2ban stopping it. **Project:** [ ] Project 1 completed with before/after evidence. **Documentation:** [ ] README + checklist complete. **Writing:** [ ] At least one article published. **Certification:** [ ] Consciously deferred (see above). **Interview:** [ ] I can answer "walk me through how you'd secure a fresh Linux server" without notes.

**Ready to move on** if every box is checked. **Needs more practice** if you can't reproduce the hardening checklist from memory — repeat Module 1.10 on a second fresh VM before moving to Phase 2.

---

# PHASE 2 — Networking Fundamentals

*Duration: 3–4 weeks (2hrs/day). This phase is conceptually dense — expect it to feel slower than Phase 1.*

**Modules (compact format from here forward):**

| Module | Purpose | Essential concepts | Primary resource + lab | Break/Fix | Write idea |
|---|---|---|---|---|---|
| 2.1 OSI/TCP-IP Model | Mental model for every later networking decision | 7-layer model, encapsulation | Cloudflare Learning Center "What is OSI Model" (free) + paper exercise | n/a (conceptual) | "OSI model explained the way I actually needed it explained" |
| 2.2 IP Addressing & Subnetting | You'll design VPC/VNet CIDR ranges from Phase 6 onward | CIDR notation, subnetting math, private vs public ranges | subnetting practice via `ipcalc` + Professor Messer subnetting videos (free) | Break: mis-subnet a /24 on paper, catch your own overlap error | "Subnetting without the headache: a worked example" |
| 2.3 Routing & NAT | Explains how your VM reaches the internet at all | Default gateway, static routing, NAT concept | `ip route`, `traceroute` on your Phase 1 VM | Break: misconfigure a route on a test VM, lose connectivity, fix it | — |
| 2.4 DNS | You'll debug DNS failures constantly in cloud work | Resolution chain, record types (A/AAAA/CNAME/MX/TXT), `dig`/`nslookup` | `dig` against real domains; freeCodeCamp DNS explainer | Break: point `/etc/hosts` somewhere wrong, observe resolution failure | "DNS explained by breaking it" |
| 2.5 HTTP/HTTPS & TLS | Every app you secure runs over this | Request/response lifecycle, status codes, TLS handshake, cert chain | `curl -v`, `openssl s_client -connect`; MDN HTTP docs (free, excellent) | Break: serve HTTP instead of HTTPS on a test app, intercept traffic with Wireshark to *see* the plaintext risk | "What actually happens during a TLS handshake" |
| 2.6 Firewalls & Ports | Direct bridge into every hardening task from here on | Stateful vs stateless filtering, default-deny | `ufw`/`iptables` on your Phase 1 VM, `nmap` from outside | Break: open every port, scan externally, close down to least-privilege | — |

### Phase 2 — Flagship Lab: "Map the Request"
**Objective:** fully trace and document one real HTTPS request from your laptop to your Phase 1 server, annotated at every layer. **Environment:** your laptop + Phase 1 VM. **Tasks:** capture the request with Wireshark, capture the TLS handshake separately with `openssl s_client`, run `dig` for the DNS step, run `traceroute` for the routing step. **Security challenge:** repeat the capture against a plain-HTTP version of the same app and screenshot the readable plaintext credentials/content. **Investigation:** compare the two captures side by side. **Remediation:** ensure the HTTPS version is what ships going forward; document why. **Verification:** a reviewer could follow your annotated diagram and understand every layer. **What it demonstrates:** you don't just know networking terms, you can trace and prove behavior — a skill directly tested in interviews.

### Phase 2 — Project (Project 2 continuation, ties into Project 1)
**Project Name:** Documented Request Path for the Hardened Server
Extend Project 1's repo with a `network-trace.md` containing your annotated diagram, DNS/TLS/routing captures, and the plaintext-vs-encrypted comparison. **Real-world scenario:** a new teammate joins and needs to understand your server's network path before their first on-call shift — you're writing their onboarding doc. **Difficulty:** Beginner–Intermediate. **Duration:** 1 week.

### Phase 2 — Articles
"What actually happens during a TLS handshake" (explainer, developer audience) · "DNS explained by breaking it" (tutorial) · "Subnetting without the headache" (explainer, beginner audience).

### Phase 2 — Certification Checkpoint
**Skip.** Networking certs (Network+, CCNA) are general IT credentials with weak ROI for a cloud-security-specific path — the hands-on labs above cover what you actually need, and later cloud certs (SC-500, AWS Security Specialty) test cloud-specific networking directly.

### Phase 2 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| Networking/TCP-IP/DNS/HTTP/TLS | 1 | 3 | Request-path trace doc, 3 articles, Wireshark captures |

### Phase 2 — Completion Gate
[ ] Can explain the OSI model and map a real request to it · [ ] Can subnet a /24 correctly on paper · [ ] Can read a `dig` and `openssl s_client` output and explain each field · [ ] Captured and compared plaintext vs TLS traffic · [ ] Project doc complete · [ ] 2+ articles published · [ ] Can answer "walk me through what happens when I type a URL" without notes.

---

# PHASE 3 — Git, GitHub & Developer Workflows

*Duration: 1–2 weeks. You already have Git skills (roadmap Section 1) — this phase is entirely about the security-relevant layer on top.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 3.1 Branch Protection & Review Workflow | Prevents unreviewed code reaching production | Branch protection rules, required reviews, CODEOWNERS | GitHub Docs (official, free) |
| 3.2 Commit Signing | Proves commit authenticity — increasingly expected in security-conscious teams | GPG/SSH commit signing, verified badge | GitHub Docs "Signing commits" |
| 3.3 Secret Scanning & Push Protection | Your first automated security gate | GitHub secret scanning, push protection | GitHub Docs "About secret scanning" |
| 3.4 Repository Security Hygiene | Sets the template every future repo will follow | SECURITY.md, dependabot alerts, least-privilege repo access | GitHub Docs "Securing your repository" |

### Phase 3 — Flagship Lab: "Catch Your Own Leak"
**Objective:** prove push protection actually works. **Tasks:** enable secret scanning + push protection on a private test repo; attempt to commit a fake AWS-format key; observe GitHub block the push. **Investigation:** review the scan alert. **Remediation:** rotate (in this case, delete) the fake key, document the workflow. **Verification:** screenshot the blocked push. **What it demonstrates:** hands-on proof of a control most candidates only describe in theory.

### Phase 3 — Project (folds into Project 1's repo as a template)
**Project Name:** Secure Repository Template
Turn `cloud-sec-hardened-linux-server` into your reference "secure repo" — branch protection, signed commits going forward, secret scanning + push protection, SECURITY.md, dependabot enabled. **Difficulty:** Beginner. **Duration:** 2–3 days.

### Phase 3 — Articles
"Locking down a GitHub repo in 30 minutes: branch protection, signing, and secret scanning" (tutorial).

### Phase 3 — Certification Checkpoint
**Skip.** No standalone cert needed; this is a workflow skill proven directly by your repo setup.

### Phase 3 — Completion Gate
[ ] Push protection demonstrably blocked a test secret · [ ] Commits are signed going forward · [ ] Reference repo template complete · [ ] Article published.

---

# PHASE 4 — Bash/Python & Security Automation

*Duration: 4–6 weeks (2hrs/day), and genuinely ongoing — you'll keep writing small scripts in every later phase.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 4.1 Bash Scripting Fundamentals | Glue for hardening/automation scripts you've already been writing | variables, conditionals, loops, exit codes | "Learn Shell" (free, interactive) |
| 4.2 Python Fundamentals for Automation | The language you'll use for anything Bash gets clumsy at | data types, functions, file I/O, `argparse` | Automate the Boring Stuff with Python (free online) |
| 4.3 Working with APIs in Python | Every cloud/security tool exposes an API you'll eventually script against | `requests`, JSON parsing, auth headers | Python `requests` docs (official) |
| 4.4 Log & Text Parsing | Directly reusable for detection work in Phase 14 | regex, `re` module, structured log parsing | Python `re` docs + your own Phase 1 auth logs as sample data |
| 4.5 Building a Real CLI Tool | Turns scripting into a portfolio artifact | `argparse`, packaging a script as a usable CLI | Official `argparse` tutorial |

### Phase 4 — Flagship Lab: "Secret Scanner"
**Objective:** build a Python CLI that scans a directory tree for hardcoded-secret patterns (AWS key format, generic API key patterns, private key headers). **Tasks:** implement regex-based detection, `argparse` for CLI options, exit codes suitable for CI use. **Security challenge:** seed a test directory with 5 fake secrets in different formats and confirm your tool catches all 5 with zero false positives on clean files. **Verification:** unit tests. **What it demonstrates:** this is a genuinely useful tool, a real SAST/secrets-scanning building block, and CI-ready — you'll actually plug a version of this into Phase 11's pipeline.

### Phase 4 — Project (Project continuation — automation layer for Project 1)
**Project Name:** Security Automation CLI ("mini security auditor")
Combine your Module 1.10 `harden.sh` logic with a Python front-end: SSH into a target (or run locally), report on open ports, running services, world-writable files, and now scan for hardcoded secrets in a given path. **Real-world scenario:** you're asked to build a lightweight internal tool a small team can run before every deploy, since there's no budget yet for a commercial scanner. **Requirements:** CLI tool, clear pass/fail exit codes, human-readable + JSON output modes. **Technologies:** Python, `argparse`, `paramiko` (for remote SSH checks) or local-only mode. **Testing:** run against both your hardened Phase-1 box and a deliberately unhardened test VM, confirm it correctly flags the difference. **Documentation:** README with usage examples, sample output. **GitHub structure:** `cloud-sec-security-auditor-cli/` with `src/`, `tests/`, `README.md`. **Portfolio presentation:** this is your strongest "I can build tools, not just use them" evidence — feature it prominently. **Difficulty:** Intermediate. **Duration:** 2–3 weeks.

### Phase 4 — Articles
"Building a mini security auditor in Python" (project walkthrough) · "Writing a secrets scanner from scratch — and why regex isn't enough" (honest lessons-learned piece covering false positives/negatives).

### Phase 4 — Certification Checkpoint
**Skip.** No Python/Bash cert has meaningful career value for this track — the CLI tool itself is stronger proof than any certificate.

### Phase 4 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| Bash | 1 | 3 | harden.sh automation |
| Python | 1 | 3 | Security auditor CLI, secrets scanner |

### Phase 4 — Completion Gate
[ ] CLI tool runs correctly against both a hardened and unhardened target · [ ] Unit tests pass · [ ] Published with README and usage examples · [ ] 2 articles published · [ ] Can write a working parser/automation script for a new log format within an hour, unaided.

---

# PHASE 5 — Web & Application Security

*Duration: 4–6 weeks (2hrs/day). This is your differentiator phase (roadmap Section 6) — invest extra time here, it will pay back the most given your React background.*

| Module | Purpose | Essential concepts | Important | Primary resource + lab |
|---|---|---|---|---|
| 5.1 OWASP Top 10 Overview | The shared vocabulary of the entire AppSec field | All 10 categories at a conceptual level | Historical Top 10 changes | OWASP Top 10 official page (free) |
| 5.2 Injection & SQLi | Still one of the most damaging vuln classes | Parameterized queries, input validation | ORM-level protections | PortSwigger Web Security Academy — SQLi path (free) |
| 5.3 XSS (Stored/Reflected/DOM) | Directly relevant to your React work | Output encoding, CSP as mitigation | DOM-based XSS specifics in SPAs | PortSwigger — XSS path |
| 5.4 CSRF & Session Security | Auth-adjacent, commonly misunderstood | SameSite cookies, CSRF tokens | Double-submit cookie pattern | PortSwigger — CSRF path |
| 5.5 Authentication & Authorization Deep Dive | The #1 real-world source of breaches | Session vs token auth, OAuth/OIDC flow, JWT pitfalls (storage, `alg:none`, expiry) | RBAC vs ABAC | OWASP Authentication Cheat Sheet + OAuth.net |
| 5.6 SSRF & API Security | Increasingly common in cloud-connected apps | SSRF mechanics, API auth patterns, rate limiting | GraphQL-specific risks | PortSwigger — SSRF path; OWASP API Security Top 10 |
| 5.7 Secure Headers & CSP | Directly actionable for any web app you ship | CSP, HSTS, X-Content-Type-Options | Report-only CSP rollout strategy | OWASP Secure Headers Project |

### Phase 5 — Flagship Lab: "Attack Your Own React App"
**Objective:** find and exploit real vulnerabilities in an app you control, then fix them. **Environment:** a small React + simple backend app you build specifically for this (a notes app or comment board is enough surface area). **Tasks:** deliberately implement 3 vulnerabilities — e.g., `dangerouslySetInnerHTML` with unsanitized user input (XSS), a fetch call missing CSRF protection on a state-changing endpoint, and a JWT stored in `localStorage` with no expiry check. **Security challenge:** exploit each one yourself — pop an alert via stored XSS, forge a CSRF request, replay an expired JWT. **Investigation:** document exactly how each exploit worked. **Remediation:** sanitize/encode output, add CSRF tokens or SameSite cookies, move the JWT to an httpOnly cookie with proper expiry handling, add a CSP. **Verification:** re-attempt each exploit post-fix and confirm it now fails. **What it demonstrates:** the single strongest artifact in your entire portfolio for AppSec/DevSecOps roles — most candidates can describe OWASP Top 10, very few can show their own working exploit-then-fix.

### Phase 5 — Project (Project 2 progression)
**Project Name:** Vulnerable-vs-Hardened React Application
**Objective:** ship two versions of the same app — clearly labeled `vulnerable/` (for learning only, never deployed live) and `hardened/` — demonstrating before/after security posture.
**Real-world scenario:** you're the new AppSec-minded developer on a team; you're asked to run an informal security review of an existing app and produce a remediation plan with evidence.
**Requirements:** functional — a working small app (notes/comments/simple auth). Security — the hardened version must have no XSS, working CSRF protection, secure JWT handling, and a working CSP.
**Architecture:** React frontend, minimal Node/Express backend, simple JWT-based auth.
**Technologies:** React, TypeScript, Express, JWT, CSP headers.
**Implementation stages:** build vulnerable v1 → exploit it and document → build hardened v2 → re-test → write comparison.
**Attack scenarios:** stored XSS, CSRF on a state-changing action, JWT replay/tampering, missing security headers (verify with securityheaders.com equivalent manual checks).
**Hardening:** output encoding/sanitization, CSRF tokens or SameSite=strict cookies, httpOnly+short-lived JWT with refresh pattern, full CSP.
**Testing:** re-run every exploit attempt against the hardened version, document pass/fail.
**Documentation:** README explaining both versions, a `SECURITY-FINDINGS.md` written like a real pentest report (finding, severity, evidence, remediation).
**GitHub structure:**
```
cloud-sec-vulnerable-vs-hardened-react/
├── README.md (clear warning: vulnerable/ is intentional, for learning only)
├── vulnerable/
├── hardened/
├── SECURITY-FINDINGS.md
└── evidence/
```
**Portfolio presentation:** this is your headline project for AppSec-flavored roles — lead your resume/portfolio with it, and write `SECURITY-FINDINGS.md` in the same format a real pentest report would use, since that format is exactly what an AppSec interviewer expects to see.
**Difficulty:** Intermediate. **Duration:** 3–4 weeks.

### Phase 5 — Articles
"I hacked my own React app — here's what I found" (security analysis, strongest piece) · "CSP the way I wish someone had explained it to me" (explainer) · "JWT storage: what can actually go wrong" (explainer) · "CSRF in a React SPA: a practical walkthrough" (tutorial) · "Writing a pentest-style findings report for your own project" (meta/process article — teaches other learners your documentation method).

### Phase 5 — Certification Checkpoint
**Optional, not urgent:** none of the standard AppSec certs (eWPT, GWAPT) are worth the cost at this stage — PortSwigger's own free "Burp Suite Certified Practitioner" badge is a legitimate, cheap (~$99) signal if you want one, but it's optional. **Learn now, postpone any paid cert** until you're closer to job applications and can see whether a specific listing values it.

### Phase 5 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| OWASP/AppSec | 2 | 4 | Vulnerable-vs-hardened app, findings report, PortSwigger labs completed |
| Authentication/Authorization | 2 | 4 | JWT/OAuth deep-dive module, hardened auth implementation |

### Phase 5 — Completion Gate
[ ] Completed PortSwigger XSS/SQLi/CSRF/SSRF paths · [ ] Vulnerable-vs-hardened project complete with a pentest-style findings doc · [ ] Every deliberate vulnerability was exploited *and* remediated *and* re-tested · [ ] 3+ articles published · [ ] Can explain, with your own example, at least 6 of the OWASP Top 10 categories unaided · [ ] Can answer "walk me through a JWT security review" in an interview-realistic way.

---

# PHASE 6 — Cloud Fundamentals

*Duration: 2–3 weeks. Short and conceptual — this phase exists to build a shared mental model before you specialize in Azure.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 6.1 Shared Responsibility Model | The single most-tested concept in every cloud security interview | What the provider secures vs what you secure, and how it shifts across IaaS/PaaS/SaaS | Microsoft Learn + AWS's own shared responsibility docs, compared side by side |
| 6.2 Core Service Categories Across Clouds | Lets you translate skills between Azure/AWS instantly | Compute, storage, networking, IAM equivalents | Build your own cheat sheet (this *is* the deliverable) |
| 6.3 Cloud Cost & Billing Basics | Prevents surprise bills starting now | Free tier limits, billing alerts, resource tagging | Azure/AWS billing docs |

### Phase 6 — Project
**Project Name:** Cross-Cloud Service Cheat Sheet
A one-page personal reference mapping Azure ↔ AWS ↔ GCP for compute, storage, IAM, networking, and logging — written by you, from docs, not copied. **Difficulty:** Beginner. **Duration:** 3–5 days. This becomes a genuinely reusable artifact you'll refer back to constantly in Phases 7–8.

### Phase 6 — Articles
None yet — save your cloud-writing energy for the hands-on Azure/AWS phases where you'll have real evidence.

### Phase 6 — Certification Checkpoint
**Skip.** Generic "cloud fundamentals" certs (AZ-900, CLF-C02) are low-signal on their own — you're about to go straight to the security-focused Azure track, which subsumes what these would teach.

### Phase 6 — Completion Gate
[ ] Can explain the shared responsibility model differently for IaaS vs PaaS vs SaaS · [ ] Cheat sheet complete · [ ] Billing alerts confirmed active on both Azure and AWS.

---

# PHASE 7 — Azure Administration & Security

*Duration: 6–8 weeks (2hrs/day). Your primary cloud (roadmap Section 7) — go deep here.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 7.1 Microsoft Entra ID (IAM) | The foundation everything else sits on | Users/groups, roles, RBAC vs Conditional Access | Microsoft Learn "Entra ID fundamentals" (free) |
| 7.2 Azure Networking (VNets, NSGs) | Direct continuation of Phase 2 at cloud scale | VNet design, NSGs, Azure Firewall basics | Microsoft Learn Azure networking modules |
| 7.3 Compute (VMs, App Service) | Where your app actually runs | VM security baseline (reuse Phase 1!), App Service basics | Microsoft Learn |
| 7.4 Storage Security | One of the most common real-world misconfig categories | Storage account access tiers, SAS tokens, private endpoints, public access blocking | Microsoft Learn "Azure Storage security guide" |
| 7.5 Key Vault & Secrets | Where credentials belong instead of code/CI variables | Key Vault access policies vs RBAC, secret versioning | Microsoft Learn Key Vault module |
| 7.6 Microsoft Defender for Cloud | Your first CSPM tool | Secure score, recommendations, regulatory compliance dashboard | Microsoft Learn + hands-on in your own subscription |
| 7.7 Azure Monitor & Logging | Feeds directly into Phase 14 | Log Analytics workspace, diagnostic settings | Microsoft Learn Azure Monitor module |

### Phase 7 — Flagship Lab: "Find and Fix the Public Blob"
**Objective:** experience a real-world misconfiguration class firsthand. **Tasks:** create a storage account, intentionally set a container to public access, upload a fake "sensitive" file. **Security challenge:** use a search tool or Azure's own resource explorer to demonstrate how such exposure would be discoverable. **Investigation:** review Defender for Cloud's recommendation about this exact misconfiguration. **Remediation:** disable public access, switch to private endpoints or SAS-token-based access. **Verification:** confirm the file is no longer publicly reachable; confirm Defender for Cloud's secure score improved. **What it demonstrates:** hands-on evidence of finding *and* fixing the single most common real-world cloud storage misconfiguration.

### Phase 7 — Project (Projects 5–6 from the roadmap, combined)
**Project Name:** Secure Azure Deployment of the Hardened App
**Objective:** deploy your Phase 5 hardened React/Express app to Azure with production-appropriate IAM, networking, secrets, and logging.
**Real-world scenario:** your team is moving off a single unmanaged VM (Phase 1) onto Azure, and you're responsible for making sure the migration doesn't regress security.
**Requirements:** app deployed and reachable; secrets in Key Vault, not in code/env files; least-privilege service principal (never a subscription-Owner-role credential) used for any deployment automation; NSGs restricting inbound traffic to only what's needed; Defender for Cloud enabled with a documented secure score.
**Architecture:** App Service or a hardened VM (reuse Phase 1 skills) behind an NSG, Key Vault for secrets, Log Analytics workspace for centralized logs.
**Technologies:** Azure App Service or VM, Entra ID, Key Vault, NSGs, Defender for Cloud, Azure Monitor.
**Implementation stages:** provision resource group → configure least-privilege IAM/service principal → deploy app → move secrets to Key Vault → configure NSGs → enable Defender for Cloud → wire up logging.
**Attack scenarios:** attempt access with an over-privileged vs least-privilege service principal and compare blast radius; attempt to reach a port that should be NSG-blocked from outside.
**Hardening:** iterate on every Defender for Cloud recommendation until secure score is meaningfully improved (document the before/after number).
**Testing:** external connectivity test confirming only intended ports reachable; confirm app functions correctly reading secrets from Key Vault instead of hardcoded values.
**Documentation:** architecture diagram (Mermaid or draw.io), IAM design rationale, before/after Defender secure score.
**GitHub structure:** `cloud-sec-azure-secure-deployment/` with `infra-notes/`, `README.md`, `evidence/`.
**Portfolio presentation:** the Defender for Cloud before/after score is your headline evidence here — concrete, numeric, easy for a recruiter to skim.
**Difficulty:** Intermediate–Advanced. **Duration:** 3–4 weeks.

### Phase 7 — Articles
"Deploying securely to Azure: IAM, networking, and logging from scratch" (tutorial) · "I found my own public blob storage misconfiguration — here's the fix" (security analysis) · "What Defender for Cloud actually caught in my project" (case study) · "Azure vs local hardening: what changes when you move to the cloud" (explainer, ties Phase 1 and Phase 7 together).

### Phase 7 — Certification Checkpoint

> **Correction:** I originally planned this checkpoint around AZ-500. It retires today, August 31, 2026, with no conversion path. Microsoft's replacement, live since July 21, 2026, is below — same price, same associate level, same core Azure security scope, plus a new AI-security domain (Entra Agent ID, Copilot risk, Defender for AI) that AZ-500 never covered.

| Certification | Category | Provider | Relevant Phase | Why | Prerequisites | Cost | Platform / link | Difficulty | Career Value |
|---|---|---|---|---|---|---|---|---|---|
| **SC-500** — Cloud and AI Security Engineer Associate *(replaces AZ-500)* | Premium | Microsoft | End of Phase 7 | Directly matches everything just practiced, plus the AI-security content is genuinely current for 2026 hiring | None formally required; comfort with Entra ID/Defender for Cloud/Sentinel expected | $165 | [Microsoft Learn — SC-500](https://learn.microsoft.com/credentials/certifications/exams/sc-500/) | Moderate | **High** |
| Azure security learning paths (study material) | Free | Microsoft | Throughout Phase 7 | Free prep feeding directly into SC-500 | None | Free | [Microsoft Learn](https://learn.microsoft.com/training/) | — | Feeds the paid exam above |

**Take the certification now** — this is one of the few points in the curriculum where "learn it, then immediately certify" is the right call, because the exam content maps closely onto Modules 7.1–7.7 and your project (plus the AI-security section, which nothing earlier in this curriculum directly covers — skim Microsoft's own SC-500 study guide for that domain specifically before sitting it).

### Phase 7 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| Azure | 2 | 4 | Secure deployment project, Defender score evidence, SC-500 |
| Cloud IAM | 1 | 4 | Least-privilege service principal design, Entra ID RBAC |

### Phase 7 — Completion Gate
[ ] App deployed to Azure with secrets in Key Vault, not code · [ ] NSGs verified via external scan · [ ] Defender for Cloud secure score improved and documented · [ ] Project + article(s) published (see note on article counts, Phase intro) · [ ] SC-500 taken or actively scheduled · [ ] Can write a least-privilege Azure RBAC assignment from a blank page for a given scenario.

---

# PHASE 8 — AWS Fundamentals & Security

*Duration: 4–6 weeks. Your secondary cloud (roadmap Section 7) — this phase is intentionally lighter than Phase 7 since patterns transfer.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 8.1 AWS IAM | The #1 AWS interview topic, bar none | Users/roles/policies, least privilege, policy JSON | AWS Skill Builder IAM module (free) |
| 8.2 VPC & Networking | Reuse your Phase 2/7 mental model | Security Groups vs NACLs, subnets, routing | AWS Skill Builder VPC module |
| 8.3 S3 Security | The single most common AWS misconfig class in the real world | Bucket policies, public access block, encryption | AWS Skill Builder S3 security module |
| 8.4 KMS & Secrets | AWS's Key Vault equivalent | Key management, Secrets Manager vs Parameter Store | AWS docs |
| 8.5 GuardDuty & Security Hub | AWS's CSPM/threat detection equivalent | Findings, severity triage | AWS Skill Builder |
| 8.6 CloudTrail | Feeds directly into Phase 14 IR work | API activity logging, event history | AWS docs |

### Phase 8 — Flagship Lab: "Public S3 Bucket, Again — But This Time You Write the IAM Policy"
**Objective:** the AWS-specific version of Phase 7's storage lab, plus the IAM-policy-writing skill that AWS interviews test most. **Tasks:** create an S3 bucket, misconfigure it public, find it, fix it with a proper bucket policy + public access block; separately, write a least-privilege IAM policy from scratch for a specific scenario ("this role may only read from this one bucket and nothing else") without copying a template. **Investigation:** review GuardDuty/Security Hub findings for the exposure. **Verification:** confirm the fixed bucket is unreachable publicly and that your custom IAM policy passes AWS's own policy simulator. **What it demonstrates:** the exact skill combination ("find the S3 misconfig" + "write the IAM policy from a blank page") that shows up almost verbatim in interviews.

### Phase 8 — Project (Project continuation — redeploy in AWS)
**Project Name:** AWS Redeployment with Least-Privilege IAM Focus
Redeploy a simplified version of your Phase 5/7 app to AWS (EC2 or a simple managed service), with the explicit goal of writing every IAM policy by hand rather than using AWS-managed policies. **Real-world scenario:** your company is going multi-cloud for redundancy, and you're asked to replicate the Azure deployment's security posture on AWS. **Requirements:** least-privilege IAM roles only (no `AdministratorAccess` anywhere), S3 bucket (if used) fully locked down, GuardDuty + CloudTrail enabled. **Difficulty:** Intermediate. **Duration:** 2–3 weeks.

### Phase 8 — Articles
"Azure vs AWS IAM: what actually differs when you've done both" (comparison, strong differentiator since most learners only know one) · "Writing an AWS IAM policy from a blank page" (tutorial) · "I misconfigured an S3 bucket on purpose — here's what GuardDuty caught" (security analysis).

### Phase 8 — Certification Checkpoint

| Certification | Provider | Relevant Phase | Why | Prerequisites | Cost | Difficulty | Career Value |
|---|---|---|---|---|---|---|---|
| AWS Certified Security – Specialty (SCS-C03) | AWS | After 6–12 months of real AWS project use | Highly respected, tests exactly this material | AWS recommends 5yrs security + 2yrs AWS experience | $300 | High | **High, but timing matters** |

**Learn this now, postpone the certification.** Unlike SC-500, this exam assumes real production-scale AWS exposure (multi-account setups, complex IAM at scale) that a solo learner's projects don't fully replicate yet. Sit it later, once I have real job or extended project experience layered on top of this phase — cold-studying it right now is the single most common reason people fail it.

### Phase 8 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| AWS | 1 | 3 | Redeployment project, custom IAM policies, GuardDuty findings addressed |

### Phase 8 — Completion Gate
[ ] App redeployed to AWS with zero AWS-managed broad-permission policies used · [ ] S3 misconfig found and fixed with evidence · [ ] GuardDuty/CloudTrail enabled and reviewed · [ ] 2+ articles published · [ ] Can write a least-privilege AWS IAM policy from a blank page for a novel scenario in an interview setting.

---

# PHASE 9 — Docker & Container Security

*Duration: 3–4 weeks.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 9.1 Docker Fundamentals | Reuses Phase 1's process/namespace knowledge directly | Images, layers, containers vs VMs | Docker's official "Get Started" (free) |
| 9.2 Dockerfile Best Practices | Where most container security problems originate | Multi-stage builds, minimal base images, non-root `USER` | Docker docs "Dockerfile best practices" |
| 9.3 Image Scanning | Your first SCA-adjacent tool | Trivy, CVE severity triage | Trivy official docs (free, open source) |
| 9.4 Registry & Supply Chain Basics | Foreshadows Phase 15 | Registry auth, image provenance basics | Docker Hub / GHCR docs |
| 9.5 Container Runtime Hardening | Where "how containers actually escape" lives | Capabilities, `--privileged` risk, socket mounting risk | Docker security docs + NIST container security guide summary |

### Phase 9 — Flagship Lab: "40 CVEs to 2"
**Objective:** experience the direct, measurable impact of image hardening. **Tasks:** containerize your Phase 5 app using a bloated root-user base image (e.g., full `node:latest`), scan with Trivy, note the CVE count. **Security challenge:** also run the container with `--privileged` and a mounted Docker socket in an isolated lab, and explain conceptually why that's dangerous (do not attempt a real escape — the conceptual understanding plus documentation is the point). **Remediation:** rebuild using a minimal/distroless base image, multi-stage build, non-root `USER`, no unnecessary capabilities. **Verification:** re-scan with Trivy, document the CVE count drop. **What it demonstrates:** a concrete, numeric before/after — extremely compelling portfolio evidence.

### Phase 9 — Project (Project 3 from the roadmap)
**Project Name:** Containerized & Hardened Application
Take your Phase 5/7 app, containerize it twice (bloated vs hardened), and publish both Dockerfiles side by side with Trivy scan evidence. **Real-world scenario:** you're asked to review why your team's container images have a growing CVE count in their scanning dashboard, and to fix it. **Requirements:** hardened image must run non-root, use a minimal base, and pass a defined CVE threshold (e.g., zero critical/high). **GitHub structure:** `cloud-sec-hardened-containers/` with `Dockerfile.bloated`, `Dockerfile.hardened`, `evidence/trivy-before.json`, `evidence/trivy-after.json`. **Difficulty:** Intermediate. **Duration:** 1–2 weeks.

### Phase 9 — Articles
"Cutting my container's CVE count from 40 to 2" (case study, strong evidence-based piece) · "Dockerfile mistakes I made on purpose (so you don't have to)" (lessons-learned) · "Why `--privileged` and Docker socket mounts are dangerous" (explainer).

### Phase 9 — Certification Checkpoint
**Skip a standalone Docker cert.** Docker Certified Associate exists but has limited current market pull compared to the Kubernetes-track certs coming in Phases 12–13, which subsume container security knowledge at a deeper level.

### Phase 9 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| Docker/Container Security | 1 | 3 | Hardened container project, Trivy before/after evidence |

### Phase 9 — Completion Gate
[ ] Bloated vs hardened image comparison complete with Trivy evidence · [ ] Can explain non-root/multi-stage/minimal-base rationale unaided · [ ] Article published · [ ] Can write a hardened Dockerfile from memory for a simple Node/Python app.

---

# PHASE 10 — Infrastructure as Code (Terraform)

*Duration: 4–5 weeks.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 10.1 Terraform Fundamentals | Declarative infra as a security control (repeatability = auditability) | Providers, resources, state | HashiCorp's official Terraform tutorials (free) |
| 10.2 State Management | The most common real-world Terraform failure mode | Remote state, locking, drift | HashiCorp docs |
| 10.3 Modules | How production Terraform actually scales | Reusable modules, variables/outputs | HashiCorp docs |
| 10.4 IaC Scanning | Your second SAST-adjacent tool, this time for infra | Checkov or tfsec, policy findings | Checkov docs (free, open source) |
| 10.5 Policy as Code (intro) | Foreshadows Phase 15's deeper treatment | OPA/Conftest basic concept | Conftest docs |

### Phase 10 — Flagship Lab: "Break the State, Recover the State"
**Objective:** experience — safely — what a real Terraform incident feels like. **Tasks:** provision a small resource set with local state; deliberately corrupt/delete the state file; practice recovery via `terraform import` or a state backup. **Security challenge:** run Checkov against your own Terraform before fixing anything, and note every finding. **Remediation:** move to remote state with locking (even a simple free-tier remote backend), fix every Checkov finding. **Verification:** re-run Checkov, confirm a clean scan. **What it demonstrates:** most learners never practice state recovery until it happens for real in production — you'll have already done it once safely.

### Phase 10 — Project (Project 6 from the roadmap)
**Project Name:** Terraform Rewrite of the Azure/AWS Deployment
Rewrite your Phase 7 (and optionally Phase 8) manual cloud deployment entirely in Terraform, remote state, modules, and a clean Checkov scan. **Real-world scenario:** your manager asks you to eliminate "console-driven" infrastructure changes ahead of a compliance audit — everything must be reproducible from code. **Requirements:** zero manual console changes going forward; `terraform plan` reviewable in a PR before `apply`; secrets never in `.tf` files (pull from Key Vault/Secrets Manager instead). **GitHub structure:** `cloud-sec-terraform-infra/` with `modules/`, `environments/`, `README.md`, Checkov scan evidence. **Difficulty:** Intermediate–Advanced. **Duration:** 3 weeks.

### Phase 10 — Articles
"Migrating my manual Azure setup to Terraform — what I got wrong first" (lessons-learned, very relatable to hiring managers) · "I broke my Terraform state on purpose — here's how I recovered it" (case study) · "Checkov caught these 8 issues in my 'secure' infrastructure" (security analysis).

### Phase 10 — Certification Checkpoint

| Certification | Provider | Relevant Phase | Why | Prerequisites | Cost | Difficulty | Career Value |
|---|---|---|---|---|---|---|---|
| HashiCorp Certified: Terraform Associate | HashiCorp | End of Phase 10 | Cheap, directly matches hands-on skill just built | None | ~$70.50 | Low–Moderate | High relative to cost |

**Take this certification now** — cheapest cert on the whole roadmap with a direct 1:1 skill match; there's no reason to defer it.

### Phase 10 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| Terraform/IaC | 0 | 3 | Full infra rewrite, Checkov clean scan, Terraform Associate |

### Phase 10 — Completion Gate
[ ] Manual infra fully replaced with Terraform · [ ] Remote state with locking configured · [ ] Checkov scan clean (or all findings consciously accepted and documented) · [ ] Terraform Associate taken · [ ] Can provision a secured environment from `terraform apply` with zero console clicks.

---

# PHASE 11 — CI/CD & DevSecOps Pipelines

*Duration: 5–6 weeks. This is the phase where everything you've built so far gets wired together and automated.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 11.1 CI/CD Fundamentals (GitHub Actions) | Reinforces and formalizes what you already knew from your frontend background | Workflows, jobs, runners, secrets in Actions | GitHub Actions official docs (free) |
| 11.2 SAST Integration | Automates Phase 5's manual review work | Semgrep rules, PR-blocking findings | Semgrep official docs (free, open source) |
| 11.3 SCA & Secrets Scanning in CI | Automates Phase 4's secrets scanner concept at scale | Trivy/Grype for dependencies, GitHub secret scanning in Actions | Trivy docs |
| 11.4 DAST Integration | Automates Phase 5's exploitation work against a staging deploy | OWASP ZAP baseline scan in CI | OWASP ZAP docs |
| 11.5 Container Scanning in CI | Automates Phase 9's Trivy work as a pipeline gate | Fail-the-build thresholds | Trivy Action (GitHub Marketplace) |
| 11.6 Pipeline Security & Least Privilege | Prevents the pipeline itself from becoming the vulnerability | Least-privilege `GITHUB_TOKEN` scopes, secrets never in logs, pinned action versions | GitHub Actions security hardening guide (official) |

### Phase 11 — Flagship Lab: "The Pipeline That Blocks Bad Code"
**Objective:** build a pipeline that actually stops a bad PR, not just reports on it after the fact. **Tasks:** wire SAST (Semgrep) + SCA (Trivy) + secrets scanning into a GitHub Actions workflow on every PR; configure severity thresholds that fail the build. **Security challenge:** open a deliberate PR reintroducing one of Phase 5's vulnerabilities and one vulnerable dependency; confirm the pipeline blocks the merge. **Investigation:** review the pipeline's findings output. **Remediation:** fix the code, confirm the pipeline goes green. **Verification:** the blocked-then-passed PR history is itself the evidence — screenshot it. **What it demonstrates:** this is the single most interview-relevant lab in the entire curriculum — "walk me through a pipeline you built that actually blocks vulnerable code" is a near-certain interview question, and you'll have a real screenshot to show, not a description.

### Phase 11 — Project (Projects 4 + capstone-DevSecOps-platform groundwork from the roadmap)
**Project Name:** DevSecOps Pipeline for the Vulnerable-vs-Hardened App
Apply the full pipeline (SAST + SCA + secrets scanning + container scanning + DAST against a staging deploy) to your Phase 5/9 app repos. **Real-world scenario:** your team has been shipping without any automated security gates; you're tasked with introducing them without breaking developer velocity — meaning you also have to tune thresholds to avoid alert fatigue, not just turn everything on at maximum strictness. **Requirements:** every gate runs on PR; critical/high findings block merge; medium/low findings report but don't block (documented rationale for the threshold choice). **Attack scenarios:** reintroduce a known vuln from Phase 5, a known-vulnerable dependency version, and a fake secret — confirm all three are caught. **GitHub structure:** `.github/workflows/security.yml` in your existing project repos, documented in a new `cloud-sec-devsecops-pipeline/` repo that explains the design decisions. **Portfolio presentation:** show the actual blocked-PR screenshot — it's your strongest single piece of evidence in the whole portfolio. **Difficulty:** Advanced. **Duration:** 3–4 weeks.

### Phase 11 — Articles
"Building a DevSecOps pipeline that actually blocks bad code (with real examples)" (flagship tutorial/case study) · "Tuning security gates to avoid alert fatigue: what I chose to block vs just report" (lessons-learned, shows mature judgment) · "Semgrep vs generic linting: what SAST actually catches" (tool explainer) · "Securing the pipeline itself: least-privilege GitHub Actions" (security analysis).

### Phase 11 — Certification Checkpoint
**Skip.** No single cert covers "DevSecOps pipeline engineering" well — this skill is proven entirely by the pipeline artifact itself, which is stronger evidence than any badge.

### Phase 11 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| CI/CD security, SAST, SCA, DAST | 0–2 | 4 | Working blocking pipeline, blocked-PR evidence, 4 articles |

### Phase 11 — Completion Gate
[ ] Pipeline demonstrably blocks a reintroduced vuln, vulnerable dependency, and fake secret · [ ] Thresholds documented and justified · [ ] 3+ articles published · [ ] Can explain the SAST/DAST/SCA distinction with a real example of each from your own pipeline, unaided.

---

# PHASE 12 — Kubernetes Fundamentals

*Duration: 4–5 weeks. Only start this phase once Phases 1–11 feel solid (roadmap Section 21 — don't touch K8s early).*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 12.1 Kubernetes Architecture | You can't secure what you don't understand structurally | Control plane, nodes, pods, the API server | Kubernetes official docs "Concepts" (free) |
| 12.2 Workloads | Deploying your app is the prerequisite to securing it | Deployments, Services, ConfigMaps | KodeKloud free content + Kubernetes docs |
| 12.3 Networking in Kubernetes | Bridges Phase 2's networking knowledge to cluster scale | ClusterIP/NodePort/Ingress, DNS inside the cluster | Kubernetes docs |
| 12.4 Storage & Volumes | Needed before secrets/security modules make sense | PersistentVolumes basics | Kubernetes docs |
| 12.5 kubectl Fluency | The daily-driver skill tested in every hands-on K8s exam | Imperative vs declarative usage, troubleshooting commands | `kubectl` cheat sheet (official) + practice on `kind` |
| 12.6 Local Cluster Operations | Your lab environment for the rest of Phase 12–13 | `kind` cluster setup/teardown | `kind` official docs |

### Phase 12 — Flagship Lab: "Deploy the Whole Stack Locally"
**Objective:** get your Phase 9 hardened container running on a real (local) Kubernetes cluster end to end. **Tasks:** stand up a `kind` cluster; deploy your hardened image via a Deployment + Service; expose it via Ingress or port-forward; troubleshoot at least one deliberately broken manifest (e.g., wrong image tag, missing env var) using `kubectl describe`/`kubectl logs`. **Verification:** app reachable and functioning on the cluster. **What it demonstrates:** baseline operational K8s competence — the prerequisite for everything in Phase 13.

### Phase 12 — Project (Project 9 from the roadmap, part 1)
**Project Name:** Application Deployed to Kubernetes
Deploy your hardened app (Phases 5+9) to a local `kind` cluster with proper Deployments, Services, ConfigMaps, and resource limits (CPU/memory requests+limits — a security-adjacent reliability control). **Real-world scenario:** your team is migrating off single-VM deployments to Kubernetes for scalability, and you're asked to produce the first working manifest set. **Difficulty:** Intermediate. **Duration:** 2 weeks.

### Phase 12 — Articles
"Kubernetes for a developer who's never touched infrastructure: what actually helped it click" (explainer, beginner-friendly, strong SEO potential) · "Deploying my hardened container to a local Kubernetes cluster" (tutorial).

### Phase 12 — Certification Checkpoint

| Certification | Provider | Relevant Phase | Why | Prerequisites | Cost | Difficulty | Career Value |
|---|---|---|---|---|---|---|---|
| KCNA (Kubernetes and Cloud Native Associate) | Linux Foundation/CNCF | End of Phase 12 | Cheap, foundational, no prerequisites, good pre-CKA checkpoint | None | $250 (includes 1 free retake) | Low–Moderate | Moderate — mainly useful as a stepping stone, not a destination |
| CKA (Certified Kubernetes Administrator) | Linux Foundation/CNCF | End of Phase 12/before 13 | Hands-on, respected, prerequisite for CKS | Hands-on cluster experience (this project) | $395 (includes 1 free retake) | High (hands-on exam) | **High** |

**KCNA: optional, not required** — take it only if you want a confidence checkpoint before committing to CKA's cost/difficulty; skip it if you're already comfortable from the project above. **CKA: take this now** (or immediately after finishing Phase 12/starting Phase 13's early modules) — it's a genuine prerequisite for CKS, so don't defer it the way you deferred AWS Security Specialty; the sequencing here is mandatory, not optional.

### Phase 12 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| Kubernetes | 0 | 3 | Working deployment, kubectl fluency, KCNA/CKA |

### Phase 12 — Completion Gate
[ ] App running correctly on a local cluster · [ ] Can troubleshoot a broken manifest using only `kubectl describe`/`logs` · [ ] CKA taken or scheduled · [ ] Project + 2 articles published.

---

# PHASE 13 — Kubernetes Security

*Duration: 4–5 weeks. Requires Phase 12 complete — RBAC and NetworkPolicy don't make sense without workload fundamentals first.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 13.1 RBAC | The #1 tested K8s security skill | Roles/ClusterRoles, RoleBindings, least privilege for ServiceAccounts | Kubernetes docs "Using RBAC Authorization" |
| 13.2 Network Policies | Cluster-internal segmentation | Default-deny, allow-list patterns | Kubernetes docs + Calico's free NetworkPolicy tutorial |
| 13.3 Secrets Management in K8s | Explains why raw K8s Secrets aren't enough on their own | Base64 ≠ encryption, encryption at rest, external secrets operators (mention) | Kubernetes docs "Secrets" |
| 13.4 Pod Security Standards & Admission Control | Prevents the privileged-pod risk conceptually covered in Phase 9 | Restricted/Baseline/Privileged profiles, admission controllers | Kubernetes docs "Pod Security Standards" |
| 13.5 Cluster Hardening & Benchmarking | Ties everything together into an auditable baseline | kube-bench, CIS Kubernetes Benchmark | kube-bench official docs (free, open source) |
| 13.6 Policy Enforcement (OPA/Kyverno intro) | Bridges directly into Phase 15's deeper Policy-as-Code work | Admission-time policy enforcement concept | Kyverno docs (free, open source — friendlier entry point than raw OPA) |

### Phase 13 — Flagship Lab: "Lock Down the Cluster"
**Objective:** take your Phase 12 cluster from wide-open to properly restricted. **Tasks:** write least-privilege RBAC for your app's ServiceAccount (read-only where possible); write a default-deny NetworkPolicy, then a specific allow rule for only the traffic your app actually needs; run kube-bench and address its top findings. **Security challenge:** deploy an intentionally over-privileged pod spec (`privileged: true`, hostPath mount) *first*, observe what a Pod Security Standard set to "Restricted" would reject, then fix it. **Investigation:** attempt a connection that the NetworkPolicy should now block, and confirm it fails. **Remediation:** the RBAC/NetworkPolicy/PSS changes above. **Verification:** kube-bench score improvement, blocked-connection proof, rejected-privileged-pod proof. **What it demonstrates:** this lab alone covers roughly half of what the CKS exam actually tests.

### Phase 13 — Project (Project 9/10 from the roadmap, completed)
**Project Name:** Secured Kubernetes Deployment
Extend Phase 12's deployment with full RBAC, NetworkPolicies, Pod Security Standards enforcement, and a documented kube-bench score improvement. **Real-world scenario:** a security review flagged your team's cluster as "wide open" — every workload runs with default (often cluster-admin-adjacent) permissions and no network segmentation; you're asked to remediate before the next audit. **Requirements:** least-privilege RBAC per workload, default-deny NetworkPolicy with explicit allows, Restricted Pod Security Standard enforced on the namespace, kube-bench run before and after. **GitHub structure:** extend `cloud-sec-kubernetes-app/` with `security/rbac.yaml`, `security/network-policies.yaml`, `security/pod-security.yaml`, `evidence/kube-bench-before.txt`, `evidence/kube-bench-after.txt`. **Portfolio presentation:** lead with the kube-bench score delta — concrete and skimmable. **Difficulty:** Advanced. **Duration:** 3 weeks.

### Phase 13 — Articles
"Kubernetes RBAC: the mental model that finally made it click" (explainer, high search value) · "I deployed a privileged pod on purpose — here's what should have stopped it" (security analysis) · "Default-deny NetworkPolicies: a practical walkthrough" (tutorial) · "kube-bench: what it actually checks and how I improved my score" (case study).

### Phase 13 — Certification Checkpoint

| Certification | Provider | Relevant Phase | Why | Prerequisites | Cost | Difficulty | Career Value |
|---|---|---|---|---|---|---|---|
| KCSA (Kubernetes and Cloud Native Security Associate) | Linux Foundation/CNCF | Start of Phase 13 | Conceptual security foundation before the hands-on CKS push | None (but pairs naturally after KCNA) | $250 (includes 1 free retake) | Low–Moderate | Moderate — same "stepping stone" role as KCNA |
| CKS (Certified Kubernetes Security Specialist) | Linux Foundation/CNCF | End of Phase 13 | One of the most respected hands-on security certs in the industry | **Must hold an active CKA** | $395 (includes 1 free retake) | Very High (hands-on) | **Very high** for DevSecOps/K8s-focused roles |

**KCSA: optional** — a reasonable warm-up if you want a conceptual gut-check before the CKS grind, but not required if the project/labs above already feel solid. **CKS: take this now, but only after CKA is actually in hand** — this is the one certification in the entire curriculum where the prerequisite is a hard technical requirement (you cannot register for CKS without an active CKA), not just a recommendation, so don't attempt to reorder this.

### Phase 13 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| Kubernetes Security | 0 | 4 | Secured cluster project, kube-bench evidence, CKS |

### Phase 13 — Completion Gate
[ ] RBAC, NetworkPolicy, and Pod Security Standards all implemented and verified with evidence · [ ] kube-bench score improvement documented · [ ] CKA held and CKS taken or scheduled · [ ] Project + 3 articles published · [ ] Can identify and fix at least 5 common K8s misconfigurations unaided, without a checklist in front of you.

---

# PHASE 14 — Cloud Monitoring, Detection & Incident Response

*Duration: 4–5 weeks.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 14.1 Log Aggregation | Centralizes everything you've been reading manually since Phase 1 | Shipping logs to Azure Monitor/Log Analytics or a self-hosted ELK stack | Microsoft Learn Azure Monitor, or Elastic's free ELK getting-started docs |
| 14.2 Detection Engineering Basics | Turns raw logs into actionable alerts | Threshold-based detections, false-positive tuning | SANS/community detection-engineering primers (free content exists — verify current links) |
| 14.3 Alerting | Closes the loop from detection to human action | Alert rules, severity, notification routing | Azure Monitor Alerts docs |
| 14.4 Incident Response Lifecycle | The framework every scenario-question answer should follow | Prepare/Detect/Contain/Eradicate/Recover/Lessons-learned (NIST SP 800-61 summary) | NIST SP 800-61 (free, official) — read the summary, not the full document |
| 14.5 Simulated Incident Practice | Where the IR lifecycle becomes muscle memory | Tabletop exercises, runbook writing | Build your own scenario based on your project history |

### Phase 14 — Flagship Lab: "The Leaked Key Incident"
**Objective:** simulate and fully respond to a realistic incident using your own infrastructure. **Tasks:** in an isolated lab, simulate an AWS access key "leak" (commit a fake-but-realistic key format to a scratch repo, as if it were real); using CloudTrail (Phase 8), identify what actions the key could have taken. **Investigation:** review CloudTrail for anomalous activity in your simulated window. **Remediation:** revoke/rotate the key, review IAM for unexpected persistence (new users/roles/policies), tighten the original permission scope that made the key over-privileged in the first place. **Documentation:** write a full incident report in professional IR format (timeline, impact, root cause, remediation, lessons learned). **Verification:** the report itself, reviewed against the NIST lifecycle for completeness. **What it demonstrates:** directly answers the "your production credentials were accidentally committed to GitHub — walk me through your response" interview question with real evidence instead of a rehearsed answer.

### Phase 14 — Project (Project 8 from the roadmap)
**Project Name:** Full Observability + Incident Response Runbook for the Capstone Environment
Add centralized logging/alerting to your Azure and/or AWS deployment, write 3 detection rules relevant to your actual architecture (e.g., failed-login spikes, unusual IAM activity, unexpected outbound traffic), and produce a written IR runbook for at least 2 realistic scenarios (leaked credentials, vulnerable container in production). **Real-world scenario:** your team just went through a near-miss and leadership wants a documented, repeatable incident response process before the next one becomes real. **Difficulty:** Advanced. **Duration:** 3 weeks.

### Phase 14 — Articles
"I simulated a leaked AWS key incident — here's my response runbook" (case study, flagship piece for this phase) · "Writing detection rules that don't drown you in false positives" (lessons-learned) · "The NIST incident response lifecycle, applied to a real (simulated) incident" (explainer).

### Phase 14 — Certification Checkpoint
**Skip formal IR certs (GCIH, etc.) for now** — SANS/GIAC IR certifications are excellent but expensive ($1,000+) and better pursued employer-funded once you're already in a role that touches IR regularly (roadmap Section 8).

### Phase 14 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| Logging/Monitoring/Incident Response | 1 | 3–4 | Observability setup, 3 detection rules, full IR runbook + simulated incident report |

### Phase 14 — Completion Gate
[ ] Logs centralized and searchable · [ ] 3 detection rules written and tested · [ ] Full simulated-incident report written in professional IR format · [ ] Article published · [ ] Can walk through first-10-actions for a leaked-key scenario in an interview setting without notes.

---

# PHASE 15 — Supply Chain Security & Policy as Code

*Duration: 3–4 weeks.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 15.1 SBOM Generation | Increasingly a compliance/procurement requirement | What an SBOM actually contains, SPDX/CycloneDX formats | Syft official docs (free, open source) |
| 15.2 Image Signing & Provenance | Directly answers "how do you know this image wasn't tampered with" | Cosign signing/verification, SLSA framework levels (conceptually) | Cosign docs, SLSA.dev overview |
| 15.3 Dependency & Supply Chain Risk | Ties Phase 4/11's SCA work into a broader framework | Dependency confusion, typosquatting, OpenSSF Scorecard | OpenSSF Scorecard docs (free, open source) |
| 15.4 Policy as Code at Scale | Deepens Phase 10/13's brief introductions | OPA/Conftest for Terraform, Kyverno for Kubernetes, policy testing | Open Policy Agent docs, Kyverno docs |

### Phase 15 — Flagship Lab: "Sign, Verify, Score"
**Objective:** apply the full supply-chain-security toolkit to your existing hardened container image. **Tasks:** generate an SBOM with Syft; sign the image with Cosign; verify the signature independently; run OpenSSF Scorecard against one of your public repos. **Remediation:** address at least 2 Scorecard findings (e.g., add branch protection if missing, pin GitHub Action versions to a SHA instead of a mutable tag). **Verification:** signature verification succeeds; Scorecard score improved and re-checked. **What it demonstrates:** genuinely current, high-relevance skills — supply chain security is one of the fastest-growing areas of the field right now.

### Phase 15 — Project (folds into the capstone)
**Project Name:** Signed, SBOM'd, Policy-Enforced Image Pipeline
Extend your Phase 11 CI/CD pipeline to generate an SBOM and sign every image on merge to main, and add an OPA/Conftest check to your Phase 10 Terraform pipeline plus a Kyverno policy to your Phase 13 cluster (e.g., "reject any pod that doesn't have resource limits set" or "reject any image that isn't signed"). **Real-world scenario:** a customer security questionnaire now requires proof of SBOM generation and image provenance before your company can close an enterprise deal — you're asked to make this real, not just a checkbox. **Difficulty:** Advanced. **Duration:** 2–3 weeks.

### Phase 15 — Articles
"What is an SBOM and why does anyone actually care (with a real example)" (explainer, strong evergreen search value) · "Signing and verifying container images with Cosign — a practical walkthrough" (tutorial) · "I ran OpenSSF Scorecard against my own repos — here's what it found" (case study).

### Phase 15 — Certification Checkpoint
**Skip.** No standalone supply-chain-security cert has meaningful market recognition yet at this stage of the field's maturity — the skill is proven by the pipeline artifact.

### Phase 15 — Skills Matrix Update
| Skill | Before | After | Evidence |
|---|---|---|---|
| SBOM/Supply Chain/Policy as Code | 0 | 3 | Signed+SBOM'd pipeline, Scorecard evidence, Kyverno/OPA policies enforced |

### Phase 15 — Completion Gate
[ ] SBOM generated automatically in CI · [ ] Images signed and verification demonstrably works · [ ] At least one OPA/Kyverno policy enforced and tested (both a passing and a rejected case) · [ ] Article published · [ ] Can explain a supply-chain attack scenario end to end and name the specific control that would stop it.

---

# PHASE 16 — Cloud Security Architecture

*Duration: 4+ weeks, and genuinely ongoing.*

| Module | Purpose | Essential concepts | Primary resource + lab |
|---|---|---|---|
| 16.1 Defense in Depth & Zero Trust | The organizing principle behind everything you've built so far | Layered controls, "never trust, always verify" | CISA Zero Trust Maturity Model (free, official) — read the summary |
| 16.2 Threat Modeling (STRIDE) | Turns architecture review from vague to systematic | STRIDE categories, data flow diagrams | OWASP Threat Modeling docs (free) |
| 16.3 Architecture Documentation | Makes your design thinking legible to others — a real career differentiator given your writing strength | ADRs (Architecture Decision Records), diagramming conventions | "Documenting Architecture Decisions" by Michael Nygard (free, the original ADR post) |

### Phase 16 — Flagship Lab: "Threat Model Your Own Capstone"
**Objective:** produce a full STRIDE-based threat model of the environment you've been building since Phase 7. **Tasks:** draw a data flow diagram of the full system; walk every trust boundary through each STRIDE category; identify at least 8 concrete risks; rank by severity; map each to an existing or missing control. **Documentation:** the threat model itself, plus 3–5 ADRs for your biggest architectural decisions (e.g., "why Azure over AWS as primary," "why we chose Kyverno over raw OPA"). **What it demonstrates:** this is the artifact that most clearly signals "architect-track thinking" rather than "tool operator," and it directly reuses nearly everything from every prior phase.

### Phase 16 — Project
This phase's project *is* the documentation layer added to your evolving capstone (see Section 23 below) — no new build, but a substantial new deliverable: full threat model + ADR set + a written defense-in-depth narrative explaining how each phase's controls compose into the whole system.

### Phase 16 — Articles
"Threat modeling my own cloud project with STRIDE" (case study, strong technical-depth signal) · "Architecture Decision Records: how I document infrastructure choices" (process article, plays directly to your documentation strength) · "Defense in depth, illustrated with my own project" (explainer).

### Phase 16 — Certification Checkpoint
**Skip for now.** Architecture-level certs (AWS Solutions Architect Professional, Azure Solutions Architect Expert, SABSA) explicitly require production-scale experience this roadmap alone can't fully replicate — revisit once employed and working at this level day to day (roadmap Section 8, "certifications to avoid initially").

### Phase 16 — Completion Gate
[ ] Full STRIDE threat model completed for the capstone · [ ] 3–5 ADRs written · [ ] Can look at an unfamiliar architecture diagram and identify the top 3 risks within 15 minutes · [ ] 2+ articles published.

---

# PHASE 17 — Capstone & Job Readiness

*Duration: 6–10 weeks for the capstone integration itself, ongoing for job-readiness activities.*

## Module 17.1 — Capstone Integration
Pull every prior phase's artifact into one coherent, documented, end-to-end platform (see Section 23 for the version-by-version build history this culminates). This is not new technical work — it's integration, polish, and documentation.

## Module 17.2 — Portfolio & GitHub Polish
Review every repo against roadmap Section 14's structure guidance; ensure a recruiter can understand your capability level from your pinned repos in under 5 minutes; write a portfolio-site or top-level README that ties the whole journey together as a narrative (roadmap Section 14's closing line: "started in frontend, progressively learned infrastructure, cloud, security, and DevSecOps by building increasingly complex systems").

## Module 17.3 — Interview Preparation
Work through roadmap Section 17's scenario questions using your *own* project evidence as the answer material, not generic theory. Do at least 2–3 mock interviews (peer, mentor, or structured self-recorded practice) before applying.

## Module 17.4 — Job Application Strategy
Target the entry points identified in roadmap Section 16 (Junior DevSecOps Engineer, Application Security Engineer junior) — apply broadly, but tailor your resume's top project bullet to match each posting's emphasis (AppSec-heavy postings → lead with Phase 5 project; cloud-heavy postings → lead with Phase 7/10 projects; pipeline-heavy postings → lead with Phase 11).

### Phase 17 — Certification Checkpoint
By now you should hold: Terraform Associate, SC-500, CKA, CKS, and (if timing allowed) be actively preparing for AWS Security Specialty. **Do not add a new certification in this phase** — this phase is about proving what you already have, not acquiring more.

### Phase 17 — Completion Gate (final gate of the whole curriculum)
[ ] Capstone repo complete, documented, and demonstrably functional end to end · [ ] Every pinned repo reviewed against the portfolio checklist · [ ] All target certifications from Phases 7/10/12/13 held · [ ] 2–3 mock interviews completed · [ ] Can answer every scenario question in roadmap Section 17 using real evidence from your own projects · [ ] Applications sent to at least 15–20 roles matching your target entry point.

**Ready for job applications** once every box above is checked — not before. **Needs more practice** if you find yourself describing controls you haven't actually implemented yourself; go back and close that specific gap rather than papering over it in an interview.

---

# The Evolving Capstone

One project, versioned across the whole curriculum, becomes your portfolio centerpiece.

| Version | Phase | What's added |
|---|---|---|
| v1 | Phase 5 | React app with deliberate vulnerabilities, then hardened |
| v2 | Phase 5 | Secure authentication (JWT/OAuth done right) |
| v3 | Phase 5/9 | Minimal backend API added |
| v4 | Phase 9 | Containerized, hardened, scanned |
| v5 | Phase 11 | CI/CD pipeline with security gates |
| v6 | Phase 11 | Full SAST/DAST/SCA/secrets scanning wired in |
| v7 | Phase 10 | Infrastructure rewritten in Terraform |
| v8 | Phase 7 | Deployed to Azure with IAM/networking/Key Vault |
| v9 | Phase 8 | Parallel AWS deployment for redundancy |
| v10 | Phase 14 | Cloud monitoring, detection rules, alerting added |
| v11 | Phase 12 | Deployed to Kubernetes |
| v12 | Phase 13 | Kubernetes RBAC, NetworkPolicy, Pod Security Standards |
| v13 | Phase 15 | SBOM, image signing, Policy as Code (OPA/Kyverno) |
| v14 | Phase 16 | Full threat model, ADRs, defense-in-depth documentation |
| **Final** | Phase 17 | Production-style DevSecOps platform: secure architecture, IaC, CI/CD, IAM, secrets management, SAST/DAST/SCA, SBOM, container scanning, image signing, Kubernetes security, logging/monitoring/alerting, threat model, incident response runbook, policy as code, full documentation |

Keep every version in Git history (don't squash/delete old versions) — the commit history itself becomes evidence of your progression, and a `CHANGELOG.md` narrating each version bump doubles as a ready-made article outline.

---

# Certification Strategy (consolidated)

> **Correction carried through this whole document:** every earlier "AZ-500" reference is now **SC-500** — AZ-500 retires today, August 31, 2026, with no conversion path to its replacement. See Phase 7's checkpoint above for the details.

**Definitely pursue, in this order:** Terraform Associate → SC-500 → CKA → CKS → AWS Security Specialty (once I have real production-adjacent experience, not immediately after Phase 8).

**Consider later, employer-funded if possible:** GIAC/SANS certs (GCLD, GCIH), AWS/Azure Professional/Expert-level architecture certs.

**Optional, low priority:** KCNA, KCSA (fine as confidence checkpoints, skip if the hands-on projects already feel solid), CompTIA Security+ (only if a specific US employer lists it as a hard requirement).

**Probably unnecessary for this track:** CISSP (experience-gated, GRC-heavy, wrong content for hands-on DevSecOps), OSCP/OffSec (pentesting-focused, not this career direction), ISC2 CC (now a $199 paid entry cert — redundant with what the projects already prove).

**Overlap to be aware of:** KCNA and CKA both cover foundational Kubernetes concepts — if Phase 12's project work already feels solid, skip KCNA and go straight to CKA rather than paying for both. Similarly, Security+ and ISC2 CC cover overlapping entry-level ground — never take both; pick at most one, and only if a specific employer requires it.

### Every certification in this curriculum, one table, with links

| Certification | Category | Cost | Platform / link |
|---|---|---|---|
| Microsoft Learn Azure paths | Free | Free | [learn.microsoft.com/training](https://learn.microsoft.com/training/) |
| AWS Skill Builder | Free | Free | [skillbuilder.aws](https://skillbuilder.aws/) |
| PortSwigger Web Security Academy | Free | Free | [portswigger.net/web-security](https://portswigger.net/web-security) |
| CNCF training material | Free | Free (paid exams below) | [cncf.io/training](https://www.cncf.io/training/) |
| HashiCorp Certified: Terraform Associate | Premium | ~$70.50 | [hashicorp.com/certification/terraform-associate](https://www.hashicorp.com/certification/terraform-associate) |
| KCNA | Premium | $250 | [cncf.io/training/certification/kcna](https://www.cncf.io/training/certification/kcna/) |
| KCSA | Premium | $250 | [cncf.io/training/certification/kcsa](https://www.cncf.io/training/certification/kcsa/) |
| CompTIA Security+ | Premium | ~$400 | [comptia.org/certifications/security](https://www.comptia.org/certifications/security) |
| ISC2 Certified in Cybersecurity (CC) | Premium | $199 + $50/yr | [isc2.org/certifications/cc](https://www.isc2.org/certifications/cc) |
| **SC-500** (replaces AZ-500) | Premium | $165 | [learn.microsoft.com/credentials/certifications/exams/sc-500](https://learn.microsoft.com/credentials/certifications/exams/sc-500/) |
| CKA | Premium | $395 | [cncf.io/training/certification/cka](https://www.cncf.io/training/certification/cka/) |
| CKS (requires active CKA) | Premium | $395 | [cncf.io/training/certification/cks](https://www.cncf.io/training/certification/cks/) |
| AWS Certified Security – Specialty | Premium | $300 | [aws.amazon.com/certification/certified-security-specialty](https://aws.amazon.com/certification/certified-security-specialty/) |
| GIAC (GCLD, GCIH, etc.) | Premium, employer-funded later | $1,000–2,500+ | [giac.org/certifications](https://www.giac.org/certifications/) |
| OffSec (OSCP) | Premium, not this track | $1,600+ | [offsec.com/courses-and-certifications](https://www.offsec.com/courses-and-certifications/) |

**The optimization this whole strategy is built around:** Skill (proven by projects) + Portfolio (proven by GitHub/articles) + a small number of well-timed certifications that close specific credibility gaps — never certification stacking as a substitute for the first two.

---

# Weekly Structure Templates

**Early phases (1–5), theory-heavy:**
Mon: theory · Tue: hands-on lab · Wed: theory + lab · Thu: security/break exercise · Fri: project work · Sat: project + documentation · Sun: review + article draft.

**Mid phases (6–13), build-heavy:**
Mon–Tue: build the module's lab · Wed: security/break exercise · Thu: fix + automate · Fri–Sat: phase project work · Sun: documentation + article + skills-matrix update.

**Late phases (14–17), integration-heavy:**
Mon–Wed: capstone integration work for the current phase's addition · Thu: security review/threat-model pass · Fri: documentation · Sat: article writing · Sun: review, mock-interview practice, or certification study.

---

# Monthly Review Template

Copy this into your notes at the end of every month:
**What I learned:** — **What I built:** — **What I published:** — **Certification progress:** — **What I can now explain that I couldn't last month:** — **What I can now demonstrate live (not just describe):** — **Weakest area to revisit:** — **Next month's objective:**

---

# Final Curriculum Map

| Phase | Modules | Duration | Main Skills | Project | Articles | Certification | Portfolio Evidence | Completion Gate |
|---|---|---|---|---|---|---|---|---|
| 0 | 3 | 1 wk | Setup | — | — | — | Tracking system | Env ready |
| 1 | 10 | 2–3 wks | Linux | Hardened server | 3–5 | Skip | Repo + evidence | See above |
| 2 | 6 | 3–4 wks | Networking | Request-path trace | 3 | Skip | Trace doc | See above |
| 3 | 4 | 1–2 wks | Git security | Secure repo template | 1 | Skip | Template repo | See above |
| 4 | 5 | 4–6 wks | Bash/Python | Security auditor CLI | 2 | Skip | CLI repo | See above |
| 5 | 7 | 4–6 wks | AppSec | Vulnerable-vs-hardened app | 3–5 | Optional (PortSwigger badge) | Findings report | See above |
| 6 | 3 | 2–3 wks | Cloud fundamentals | Cheat sheet | — | Skip | Cheat sheet | See above |
| 7 | 7 | 6–8 wks | Azure security | Secure Azure deployment | 3–4+ | **SC-500 — now** | Defender score evidence | See above |
| 8 | 6 | 4–6 wks | AWS security | AWS redeployment | 2–3 | AWS Security Specialty — later | IAM policies | See above |
| 9 | 5 | 3–4 wks | Container security | Hardened containers | 2–3 | Skip | Trivy evidence | See above |
| 10 | 5 | 4–5 wks | Terraform/IaC | Full IaC rewrite | 2–3 | **Terraform Associate — now** | Checkov evidence | See above |
| 11 | 6 | 5–6 wks | CI/CD security | Blocking pipeline | 3–4 | Skip | Blocked-PR evidence | See above |
| 12 | 6 | 4–5 wks | Kubernetes | K8s deployment | 2 | KCNA optional, **CKA — now** | Working cluster | See above |
| 13 | 6 | 4–5 wks | K8s security | Secured cluster | 3–4 | KCSA optional, **CKS — now** | kube-bench evidence | See above |
| 14 | 5 | 4–5 wks | Monitoring/IR | Observability + runbook | 3 | Skip | Incident report | See above |
| 15 | 4 | 3–4 wks | Supply chain/PaC | Signed+SBOM pipeline | 3 | Skip | Scorecard evidence | See above |
| 16 | 3 | 4+ wks | Architecture | Threat model + ADRs | 3 | Skip | Threat model doc | See above |
| 17 | 4 | 6–10 wks | Integration/job-readiness | **Capstone platform** | Case study series | None new | Full portfolio | Applications sent |

---

## My First 30 Days
Complete Phase 0 entirely (days 1–5), then move directly into Phase 1's Modules 1.1–1.6. Target: by day 30, your Linux VM is hardened through Module 1.7 and your career thesis + setup notes are written.

## My First 90 Days
Complete Phases 0–3 fully and be well into Phase 4. Target: Project 1 (hardened server) published with evidence, secure GitHub repo template in place, first 3–4 articles live, security auditor CLI in progress.

## 6-Month Target
Complete through Phase 7 (Azure). Target: SC-500 held, vulnerable-vs-hardened React app published, secure Azure deployment live with documented Defender score improvement, 10+ articles published. This is roughly the point where you're realistically ready to *start* applying for junior roles while continuing the curriculum in parallel (roadmap Section 16 — apply as soon as you're competitive, don't wait for "done").

## 12-Month Target
Complete through Phase 12–13 (Kubernetes + Kubernetes Security). Target: CKA and CKS held, full DevSecOps pipeline blocking real vulnerabilities, Terraform-managed multi-cloud-adjacent infrastructure, 20+ articles published. This is squarely "job-ready" territory for Junior DevSecOps/AppSec roles, and competitive for some mid-level postings depending on the employer's bar.

## Long-Term Target (18–24+ months and beyond)
Complete Phases 14–17, capstone fully integrated and documented, AWS Security Specialty held. From here, progression into Senior Cloud Security Engineer or Cloud Security Architect (roadmap Section 16) is a function of real job experience layered on top of this foundation — no curriculum, including this one, substitutes for time spent defending real production systems under real constraints (roadmap Section 22's expert-level progression). Keep publishing, keep building, and revisit this document's skills matrix (Section 13) every few months for the rest of your career — the ladder in roadmap Section 22 never really stops.

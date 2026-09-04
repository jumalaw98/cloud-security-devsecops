---
title: Roadmap
nav_order: 2
---

# Cloud Security & DevSecOps Roadmap — From React Developer to Cloud Security Engineer

*My own roadmap: a React/TypeScript developer with basic Linux/Azure/Git exposure and strong communication/writing skills, moving into Cloud Security / DevSecOps. Written as a document I'll actually reread — and, since I'm putting this on GitHub, as something useful to anyone else attempting the same path.*
*Certification pricing verified August 2026 — always re-check the vendor page before paying, prices do move (see the SC-500 correction in Section 8 — one already moved while I was writing this).*

---

## How I'm using this document

This is a reference, not a syllabus to read once. I'm bookmarking it, re-reading Section 4 every time I finish a stage, and updating the skills-gap table in Section 1 every 2–3 months as my real progress tracker — not the calendar.

**A note on "one project per stage" language below:** treat every project/article recommendation in this document as a floor, not a ceiling. Where a stage clearly benefits from a second smaller project, or a topic is rich enough for more than one article, I'll do more than one — the counts here are starting points, not limits.

---

## 1. Skills Gap Analysis

Levels: **0** None · **1** Aware · **2** Can do with guidance · **3** Can do independently · **4** Can design/architect · **5** Can teach/audit others

| Skill | Your Level | Required for Job-Ready | Gap | Priority |
|---|---|---|---|---|
| Linux (CLI, permissions, processes, systemd) | 1 | 3 | 2 | **Critical** |
| Networking fundamentals (OSI, subnets, routing) | 1 | 3 | 2 | **Critical** |
| TCP/IP | 1 | 3 | 2 | **Critical** |
| DNS | 1 | 3 | 2 | **Critical** |
| HTTP/HTTPS | 2 | 4 | 2 | **Critical** |
| TLS/certificates | 1 | 3 | 2 | **Critical** |
| Git/GitHub | 3 | 4 | 1 | Important |
| GitHub Actions | 1 | 3 | 2 | **Critical** |
| Bash scripting | 1 | 3 | 2 | **Critical** |
| Python | 1 | 3 | 2 | **Critical** |
| JavaScript/TypeScript | 4 | 3 | 0 | Already an asset |
| Web app architecture | 3 | 4 | 1 | Important |
| APIs (REST, auth) | 3 | 4 | 1 | Important |
| Databases (basic security) | 2 | 3 | 1 | Important |
| Authentication (sessions, OAuth, OIDC) | 2 | 4 | 2 | **Critical** |
| Authorization (RBAC/ABAC) | 1 | 4 | 3 | **Critical** |
| OWASP Top 10 | 2 | 4 | 2 | **Critical** |
| Application Security | 2 | 4 | 2 | **Critical** |
| Cloud fundamentals (shared responsibility) | 2 | 4 | 2 | **Critical** |
| Azure | 2 | 4 | 2 | **Critical** |
| AWS | 1 | 3 | 2 | Important |
| IAM (cloud) | 1 | 4 | 3 | **Critical** |
| Cloud networking (VPC/VNet, NSGs, firewalls) | 1 | 3 | 2 | **Critical** |
| Compute (VMs, serverless) | 2 | 3 | 1 | Important |
| Storage security | 1 | 3 | 2 | Important |
| Containers | 1 | 3 | 2 | **Critical** |
| Docker | 1 | 3 | 2 | **Critical** |
| Kubernetes | 0 | 3 | 3 | Important (not yet — see Stage 10) |
| Terraform / IaC | 0 | 3 | 3 | **Critical** |
| CI/CD | 2 | 4 | 2 | **Critical** |
| CI/CD security | 0 | 4 | 4 | **Critical** |
| SAST | 0 | 3 | 3 | **Critical** |
| DAST | 0 | 3 | 3 | Important |
| SCA (dependency scanning) | 1 | 3 | 2 | **Critical** |
| Secrets management | 0 | 3 | 3 | **Critical** |
| SBOM | 0 | 2 | 2 | Important |
| Container security | 0 | 3 | 3 | Important |
| Cloud security posture management (CSPM) | 0 | 3 | 3 | Important |
| Logging | 1 | 3 | 2 | **Critical** |
| Monitoring | 1 | 3 | 2 | **Critical** |
| SIEM | 0 | 2 | 2 | Useful |
| Incident response | 0 | 3 | 3 | Important |
| Threat modeling | 0 | 3 | 3 | Important |
| Zero Trust | 0 | 2 | 2 | Useful |
| Compliance (SOC2, ISO 27001, CIS) | 0 | 2 | 2 | Useful |
| Security architecture | 0 | 4 | 4 | Important (later stage) |
| Communication/writing/docs | 4 | 3 | 0 | **Already an asset — lean on this** |

**Reading the table:** your biggest, highest-priority gaps cluster around Linux, networking, IAM, IaC, and CI/CD security — the DevSecOps "plumbing." Application security and JS/TS are where you're already ahead of a typical beginner. Kubernetes is a real gap but is *deliberately* sequenced late (see Section 22 — don't touch it until Stage 10).

---

## 2. What "Critical vs Optional" Means for You Specifically

- **Critical (must be 3+ to get hired):** Linux, networking basics, IAM, cloud fundamentals on one primary cloud, Docker, Terraform, CI/CD security, SAST/SCA, secrets management, logging/monitoring, application security fundamentals.
- **Important (should be 2-3 by job-ready):** Kubernetes security, DAST, SBOM, container security, threat modeling, incident response, a second cloud at a basic level.
- **Useful (nice to have, deepen later):** SIEM, Zero Trust theory, formal compliance frameworks, GCP.
- **Optional (skip until senior-track):** Multi-cloud architecture, advanced compliance auditing, writing your own security tooling from scratch, GRC-heavy roles.

---

## 3. Learning Philosophy Applied

Every stage below follows: **Learn → Build → Break → Secure → Document → Teach → Repeat**, weighted ~70% hands-on / 20% reading / 10% certification prep. Don't skip the "Break" step — misconfiguring something on purpose and then finding it is where real skill comes from, not the tutorial.

---

## 4. The Staged Roadmap

Each stage below is intentionally compact (this document is already very long) — treat each as a checklist, and go deep using the resources in Sections 10–11.

### Stage 0 — Career Orientation & Environment (1–2 weeks)
- **Learn:** what Cloud Security/DevSecOps engineers actually do day to day; how the role differs from SOC analyst, pentester, or pure SRE.
- **Set up:** a dedicated GitHub account for security work, a password manager, a note-taking system (Obsidian or Notion), and your home lab base machine (Section 15).
- **Deliverable:** a one-page personal "career thesis" — why cloud security, why this order — pinned in your notes. You'll revisit it monthly.

### Stage 1 — Linux & Computing Fundamentals (3–5 weeks)
- **Concepts:** filesystem hierarchy, permissions (chmod/chown/umask), users/groups, processes, systemd services, package managers, SSH, cron, log files (`/var/log`), disk/partitions.
- **Tools:** Ubuntu Server (VM via VirtualBox or a $5–6/mo VPS), `tmux`, `htop`, `journalctl`.
- **Labs:** stand up an Ubuntu VM from scratch; create least-privilege users; harden SSH (key-only auth, disable root login, change port, fail2ban); read and interpret `auth.log`.
- **Project:** provision a hardened Linux server that will host your web app in later stages.
- **Break it:** intentionally misconfigure SSH (password auth + root login) and demonstrate a brute-force attempt against it in an isolated lab, then fix it.
- **Document:** a hardening checklist you wrote yourself (don't copy CIS verbatim — summarize it in your own words).
- **Blog ideas:** "Hardening a fresh Ubuntu server: a checklist"; "What SSH hardening actually protects against."
- **Mastery test:** you can SSH into a fresh box and get it to a CIS-lite baseline from memory in under 20 minutes.

### Stage 2 — Networking Fundamentals (3–4 weeks)
- **Concepts:** OSI/TCP-IP model, subnetting/CIDR, routing, NAT, DNS resolution chain, HTTP/HTTPS request lifecycle, TLS handshake, certificates/PKI basics, firewalls, ports.
- **Tools:** `tcpdump`, Wireshark, `dig`/`nslookup`, `curl -v`, `openssl s_client`.
- **Labs:** capture and read your own HTTPS handshake in Wireshark; set up a self-signed cert and explain why the browser distrusts it; subnet a /24 into four /26s on paper and verify with `ipcalc`.
- **Project:** document the full request path of your Stage-1 web app from browser to server, annotated with every protocol layer involved.
- **Break it:** intercept your own unencrypted HTTP traffic on a local test app to *see* why TLS matters.
- **Blog ideas:** "What actually happens during a TLS handshake"; "DNS explained by breaking it."
- **Mastery test:** you can explain, without notes, what happens between typing a URL and the page rendering — including DNS, TCP handshake, TLS, and HTTP.

### Stage 3 — Git, GitHub & Developer Workflows (1–2 weeks, mostly reinforcement)
You already know Git. The gap is **security-relevant** Git workflow: branch protection, signed commits, CODEOWNERS, secret scanning, GitHub Actions basics.
- **Labs:** enable GitHub secret scanning + push protection on a repo; set up branch protection rules; sign a commit with GPG/SSH.
- **Project:** convert one of your existing React repos into a "reference secure repo" (see Section 14).
- **Blog idea:** "Locking down a GitHub repo: branch protection, signing, and secret scanning in 30 minutes."
- **Mastery test:** you can explain the difference between a leaked secret being *blocked* vs *detected after the fact*, and you've configured both.

### Stage 4 — Programming & Automation: Python + Bash (4–6 weeks, ongoing)
- **Concepts:** Python for security automation (requests, argparse, file/log parsing), Bash for glue scripting, basic regex.
- **Labs:** write a Python script that scans a directory for hardcoded secrets using regex; write a Bash script that checks a server against your Stage-1 hardening checklist automatically.
- **Project:** a CLI tool ("mini security auditor") that SSHs into a target and reports on open ports, running services, and world-writable files.
- **Portfolio evidence:** publish the CLI tool with a README, tests, and usage examples.
- **Mastery test:** given a new API or log format, you can write a working parser/automation script within an hour without heavy Googling.

### Stage 5 — Web & Application Security (4–6 weeks) — **your differentiator stage**
- **Concepts:** OWASP Top 10 in depth, authentication vs authorization, session management, JWT pitfalls, CSRF, XSS (stored/reflected/DOM), SQLi, SSRF, CSP, secure headers, CORS misconfig, dependency vulnerabilities.
- **Tools:** Burp Suite Community, OWASP ZAP, PortSwigger Web Security Academy labs.
- **Labs:** complete PortSwigger's XSS, SQLi, CSRF, and SSRF learning paths (free, and genuinely excellent).
- **Project:** take one of your own React apps, deliberately introduce 3 OWASP Top 10 vulnerabilities, exploit them yourself, then fix them with secure headers/CSP/input validation and write up the before/after.
- **Break it:** the above — build vulnerable-on-purpose, then attack your own code.
- **Blog ideas:** "I hacked my own React app — here's what I found"; "CSP the way I wish someone had explained it to me"; "JWT: what can actually go wrong."
- **Portfolio evidence:** a "vulnerable-by-design" React app repo (clearly labeled as intentional, for learning) alongside a "hardened" version — a very strong differentiator for you specifically.
- **Mastery test:** given an unfamiliar web app, you can manually find at least 2–3 real OWASP-category issues without a scanner.

### Stage 6 — Cloud Fundamentals (2–3 weeks)
- **Concepts:** shared responsibility model, IAM basics, regions/availability zones, cloud networking basics, cost management, the "why" of cloud security differing from on-prem.
- **Labs:** compare the shared responsibility model across Azure/AWS/GCP side by side, in your own words.
- **Deliverable:** a one-page personal cheat sheet mapping equivalent services across the three major clouds (compute, storage, IAM, networking, logging).

### Stage 7 — Azure Security (Primary Cloud) (6–8 weeks)
See Section 8 for why Azure is your primary.
- **Concepts:** Microsoft Entra ID (IAM), RBAC, Conditional Access, Azure Policy, Key Vault, NSGs, Azure Firewall, Microsoft Defender for Cloud, Azure Monitor/Log Analytics, storage account security (SAS tokens, private endpoints).
- **Labs:** deploy a VM + web app to Azure free tier; lock it down with NSGs; put secrets in Key Vault instead of code; enable Defender for Cloud and fix its recommendations one by one.
- **Project:** deploy your Stage-5 hardened web app to Azure with proper IAM (least privilege service principals, not owner-role-everywhere), networking, and logging.
- **Break it:** create an intentionally public storage account/blob, find it using open-source tooling, then lock it down.
- **Blog ideas:** "Deploying securely to Azure: IAM, networking, and logging from scratch"; "What Defender for Cloud actually caught in my project."
- **Mastery test:** you can stand up a secured Azure environment for a small app without following a tutorial, using only docs.

### Stage 8 — AWS Security (Secondary Cloud) (4–6 weeks)
- **Concepts:** IAM (users/roles/policies — least privilege), VPC design, Security Groups vs NACLs, S3 bucket security, KMS, GuardDuty, Security Hub, CloudTrail.
- **Labs:** free-tier EC2 + S3 deployment with least-privilege IAM roles (never root/admin keys in code); enable GuardDuty and CloudTrail; deliberately misconfigure an S3 bucket to public, detect it, fix it.
- **Project:** redeploy a simplified version of your app to AWS, focused specifically on IAM policy writing (this is the #1 interview-tested AWS security skill).
- **Blog idea:** "Azure vs AWS IAM: what actually differs when you've done both."
- **Mastery test:** you can write a least-privilege IAM policy from a blank page for a given scenario.

### Stage 9 — Docker & Container Security (3–4 weeks)
- **Concepts:** image layers, Dockerfile best practices, non-root containers, multi-stage builds, image scanning, base image minimization (distroless/Alpine), container registries.
- **Tools:** Docker, Trivy, Hadolint, Docker Scout.
- **Labs:** containerize your app with a bloated root-user image, scan it with Trivy, then rebuild it minimal/non-root and rescan.
- **Project:** Project 2 from Section 6 (containerize + secure).
- **Break it:** run a container as root with a mounted Docker socket, demonstrate why that's dangerous (in an isolated lab only).
- **Blog idea:** "Cutting my container's CVE count from 40 to 2."
- **Mastery test:** you can explain and demonstrate why `USER root` + Docker socket mounting is dangerous, and you write non-root Dockerfiles by default.

### Stage 10 — Kubernetes & Kubernetes Security (6–8 weeks) — *only start after Stages 1–9 are solid*
- **Concepts:** pods/deployments/services, RBAC, network policies, secrets (and why raw K8s Secrets aren't enough), pod security standards/admission control, service accounts.
- **Tools:** kind or minikube locally, kubectl, Trivy for images, OPA/Gatekeeper or Kyverno for policy, kube-bench.
- **Labs:** deploy your containerized app to a local kind cluster; run kube-bench against it; write a NetworkPolicy that actually restricts traffic and prove it with a failed connection test; implement RBAC least privilege for a service account.
- **Project:** Project 8 from Section 6.
- **Break it:** deploy an overly-permissive pod (privileged: true, hostPath mount) and demonstrate the escape risk conceptually/in an isolated lab, then remediate with a Pod Security Standard.
- **Blog idea:** "Kubernetes RBAC: the mental model that finally made it click."
- **Mastery test:** given a cluster, you can identify and fix at least 5 common misconfigurations without a checklist in front of you.

### Stage 11 — Infrastructure as Code (Terraform) (4–5 weeks)
- **Concepts:** declarative IaC, state management, modules, drift detection, policy as code.
- **Tools:** Terraform, tflint, Checkov or tfsec (IaC scanning), OPA/Conftest.
- **Labs:** rewrite your Stage 7/8 manual cloud deployments as Terraform; run Checkov against your own IaC and fix every finding; break the state file intentionally and practice recovering.
- **Project:** Project 7 from Section 6.
- **Blog idea:** "Migrating my manual Azure setup to Terraform — what I got wrong first."
- **Mastery test:** you can provision a secured environment from `terraform apply` with zero manual console clicks.

### Stage 12 — CI/CD & DevSecOps (5–6 weeks)
- **Concepts:** pipeline security, shift-left, security gates (fail the build on critical findings), SAST/DAST/SCA integration, secrets in CI, least-privilege pipeline permissions.
- **Tools:** GitHub Actions, Semgrep (SAST), OWASP ZAP (DAST), Trivy/Grype (SCA + container), GitHub secret scanning, HashiCorp Vault or cloud-native secret managers.
- **Labs:** build a pipeline that runs SAST + SCA + container scan on every PR and blocks merge on critical/high findings; integrate DAST against a staging deployment.
- **Project:** Projects 3–4 from Section 6.
- **Blog idea:** "Building a DevSecOps pipeline that actually blocks bad code (with real examples)."
- **Mastery test:** you can add a security gate to an existing pipeline and correctly tune it to avoid both false-negative blindness and alert fatigue.

### Stage 13 — Software Supply Chain Security (3 weeks)
- **Concepts:** SBOM, dependency confusion, image signing/provenance, SLSA framework, OpenSSF Scorecard.
- **Tools:** Syft (SBOM), Cosign (image signing), OpenSSF Scorecard.
- **Labs:** generate an SBOM for your app; sign and verify a container image with Cosign; run Scorecard against one of your public repos and fix findings.
- **Blog idea:** "What is an SBOM and why does anyone care (with a real example)."
- **Mastery test:** you can explain a supply-chain attack scenario (e.g., a compromised dependency) end to end and name the specific control that would have stopped it.

### Stage 14 — Cloud Detection, Monitoring & Incident Response (4–5 weeks)
- **Concepts:** log aggregation, alerting, detection engineering basics, incident response lifecycle (prepare/detect/contain/eradicate/recover/lessons-learned).
- **Tools:** Azure Monitor/Sentinel free-tier trial or the ELK stack self-hosted, GuardDuty (from Stage 8).
- **Labs:** ship your app's logs to a central location; write 3 detection rules (e.g., failed-login spikes, unusual IAM activity); simulate an incident (e.g., a leaked key) and run a written incident response.
- **Project:** add full observability + a documented IR runbook to your capstone environment.
- **Blog idea:** "I simulated a leaked AWS key incident — here's my response runbook."
- **Mastery test:** given a simulated alert, you can walk through containment and remediation steps within minutes, not hours.

### Stage 15 — Cloud Security Architecture (ongoing, 4+ weeks)
- **Concepts:** defense in depth, Zero Trust principles, secure-by-design, threat modeling (STRIDE), architecture documentation (ADRs, diagrams).
- **Labs:** produce a full threat model for your capstone using STRIDE; document architectural decisions as ADRs.
- **Mastery test:** you can look at an unfamiliar architecture diagram and identify the top 3 risks in 15 minutes.

### Stage 16 — Advanced Security Engineering (ongoing)
Policy as Code at scale, custom security tooling, multi-account/multi-subscription governance, cost-aware security. This is where you specialize based on what the job market pulls you toward.

### Stage 17 — Expert/Architect Level (career-long)
See Section 23 for what actually distinguishes this level — it's not a stage you "finish," it's a way of working.

---

## 5. Realistic Progressive Projects

| # | Project | Core Skill | Difficulty | Est. Duration |
|---|---|---|---|---|
| 1 | Secure a Linux server hosting a web app | Linux hardening | Beginner | 1–2 weeks |
| 2 | Containerize + secure with Docker | Container security | Beginner–Int | 2 weeks |
| 3 | CI/CD pipeline with security gates | Pipeline security | Intermediate | 2–3 weeks |
| 4 | Add SAST/DAST/SCA/secrets scanning | AppSec automation | Intermediate | 2 weeks |
| 5 | Deploy to Azure | Cloud deployment | Intermediate | 2 weeks |
| 6 | Azure IAM, networking, logging | Cloud security | Intermediate | 2–3 weeks |
| 7 | Rebuild infra in Terraform | IaC | Intermediate–Adv | 3 weeks |
| 8 | Deploy to Kubernetes, secure cluster | K8s security | Advanced | 4 weeks |
| 9 | Full DevSecOps platform (tie 1–8 together) | Integration | Advanced | 4–6 weeks |
| C | **Capstone**: production-style secure cloud environment | Everything above | Expert | 6–10 weeks |

**Example spec — Project 1 (fully worked, use this template for the rest):**
- **Objective:** stand up and harden a Linux VM that will host a real app.
- **Architecture:** single Azure/AWS free-tier VM, public IP, SSH key auth only.
- **Technologies:** Ubuntu 22.04/24.04, ufw or cloud-native firewall, fail2ban.
- **Skills learned:** Linux hardening, SSH security, basic firewalling, log reading.
- **Phases:** provision → baseline hardening → app deploy → monitoring → documented hardening report.
- **Security requirements:** no password SSH, no root login, firewall default-deny, automatic security updates.
- **Attack scenario:** simulate an SSH brute-force from a second VM in the same lab network; observe in logs; confirm fail2ban blocks it.
- **Hardening tasks:** listed in Stage 1 above.
- **Testing:** `nmap` scan from outside to confirm only intended ports are open.
- **Documentation:** hardening checklist + before/after `nmap`/log evidence.
- **Blog topics:** "Hardening a Linux server: a real checklist with evidence, not just theory."
- **GitHub structure:** `README.md`, `hardening-checklist.md`, `scripts/`, `evidence/` (screenshots/logs, sanitized).
- **Portfolio presentation:** pin this repo; lead with the before/after `nmap` output.

**Capstone (tie it all together)** should demonstrate, end to end: secure architecture diagram, Terraform-provisioned infra, CI/CD with SAST/DAST/SCA gates, secrets in a vault (not env files), signed + scanned container images with an SBOM, a Kubernetes deployment with RBAC + network policies, centralized logging/alerting, a written threat model, and an incident-response runbook exercised against a simulated incident. This single repo becomes the centerpiece of your portfolio and your primary interview talking point.

---

## 6. Turning Your React/TypeScript Background Into a Differentiator

Most people entering cloud security come from either networking/sysadmin or generalist IT — very few come from frontend development with strong AppSec instincts. That combination (build the app *and* secure it *and* explain it clearly) is rare and valuable, especially for **Application Security Engineer** and **DevSecOps Engineer** roles where you need to talk to developers in their own language.

Concretely, lean into: secure React patterns (avoiding `dangerouslySetInnerHTML`, sanitizing rendered content, CSP-compatible builds), OAuth/OIDC implemented from the frontend perspective, JWT storage pitfalls (localStorage vs httpOnly cookies), dependency security for `npm`/`package-lock.json`, and secure CI/CD for a JS/TS codebase specifically. Nobody explains SAST/DAST findings to a React team better than someone who's shipped React in production. Your writing and explaining strength (Section 13) is what turns this technical edge into visible reputation — most engineers with equal skills don't publish, so you'll stand out just by documenting well.

---

## 7. Cloud Strategy: Azure → AWS → (GCP optional)

| Factor | Azure | AWS | GCP |
|---|---|---|---|
| Your existing exposure | Yes | No | No |
| Global market demand | Very high (enterprise) | Highest overall | Lower, niche (data/ML-heavy shops) |
| Cloud security job volume | High, esp. enterprise/finance/healthcare | Highest | Lowest of the three |
| Free tier for learning | Good (student/free credits) | Good (12-month free tier + always-free) | Good ($300 credit) |
| Learning difficulty | Moderate (Microsoft-ecosystem heavy) | Moderate–High (huge service surface) | Moderate |
| Remote job availability | High globally | Highest globally | Moderate |

**Recommendation: Primary = Azure, Secondary = AWS, Optional = GCP.**
Azure because you already have exposure and it dominates enterprise environments (finance, healthcare, government, and most large African/Kenyan enterprises running Microsoft 365 also run Azure) — this compounds your existing knowledge fastest. AWS second because it has the single largest global job volume and is treated as the "lingua franca" of cloud security interviews — most scenario questions assume AWS unless stated otherwise. GCP is optional: learn it only if a specific job requires it, since the incremental job-market value for a generalist cloud security engineer is lower than deepening Azure+AWS.

**The trap to avoid:** don't try to reach depth on all three simultaneously. Get Azure to a "can secure and deploy independently" level first, then AWS to the same level, before ever touching GCP.

---

## 8. Certification Roadmap

> Prices verified via web search, August 2026. Always confirm on the vendor page before paying — these change, and one already changed mid-writing this: see the correction box below.

> **Correction I need to remember:** AZ-500 (Azure Security Engineer Associate) retires today, August 31, 2026 — I originally scoped this roadmap around it before checking. Microsoft's replacement is **SC-500: Implementing End-to-End Security Controls for Cloud and AI Workloads**, leading to the **Microsoft Certified: Cloud and AI Security Engineer Associate** credential. SC-500 reached general availability July 21, 2026. It keeps roughly 80% of AZ-500's content (identity, networking, Defender for Cloud, Sentinel) and adds a new AI-security domain (Entra Agent ID, Copilot risk, Defender for AI). There is **no conversion path** — AZ-500 holders don't automatically get SC-500, and since I'm starting from zero today, AZ-500 isn't obtainable anymore anyway. Every "AZ-500" reference below is now SC-500.

### Free
| Certification / Credential | Provider | Cost | Platform / link | When to take it |
|---|---|---|---|---|
| Azure fundamentals + security learning paths | Microsoft | Free | [Microsoft Learn](https://learn.microsoft.com/training/) | Throughout Stage 6–7 |
| AWS Skill Builder free digital courses | AWS | Free | [AWS Skill Builder](https://skillbuilder.aws/) | Alongside Stage 8 |
| PortSwigger Web Security Academy + Burp Suite Certified Practitioner prep material | PortSwigger | Free content | [PortSwigger Academy](https://portswigger.net/web-security) | Stage 5 |
| CNCF cloud-native security whitepaper + KCNA/KCSA free curriculum | CNCF | Free study material, paid exam | [CNCF Training](https://www.cncf.io/training/) | Before Stage 10 |

### Low-cost / premium (worth self-funding)
| Certification | Provider | Cost | Platform / link | Prerequisites | When to take it |
|---|---|---|---|---|---|
| HashiCorp Certified: Terraform Associate | HashiCorp | ~$70.50 | [HashiCorp Certifications](https://www.hashicorp.com/certification/terraform-associate) | None | After Stage 11 |
| KCNA (Kubernetes and Cloud Native Associate) | Linux Foundation/CNCF | $250 (incl. 1 retake) | [CNCF KCNA](https://www.cncf.io/training/certification/kcna/) | None | Optional, before Stage 10 |
| KCSA (Kubernetes and Cloud Native Security Associate) | Linux Foundation/CNCF | $250 (incl. 1 retake) | [CNCF KCSA](https://www.cncf.io/training/certification/kcsa/) | None | Optional, before/alongside CKS prep |
| CompTIA Security+ | CompTIA | ~$400 (often discounted via vouchers) | [CompTIA Security+](https://www.comptia.org/certifications/security) | None | Only if a specific employer lists it as a hard requirement |
| ISC2 Certified in Cybersecurity (CC) | ISC2 | $199 + $50/yr maintenance — the free-voucher program closed to new participants May 20, 2026 | [ISC2 CC](https://www.isc2.org/certifications/cc) | None | Optional, redundant with Security+ — pick at most one |

### Professional / paid, high value for the roles I'm targeting
| Certification | Provider | Cost | Platform / link | Prerequisites | When to take it |
|---|---|---|---|---|---|
| **SC-500: Cloud and AI Security Engineer Associate** *(replaces AZ-500)* | Microsoft | $165 | [Microsoft Learn — SC-500](https://learn.microsoft.com/credentials/certifications/exams/sc-500/) | None formally required; comfort with Entra ID, Defender for Cloud, Sentinel expected | After Stage 7 |
| Certified Kubernetes Administrator (CKA) | Linux Foundation/CNCF | $395 (incl. 1 retake) | [CNCF CKA](https://www.cncf.io/training/certification/cka/) | Hands-on K8s experience | After Stage 10 |
| Certified Kubernetes Security Specialist (CKS) | Linux Foundation/CNCF | $395 (incl. 1 retake) | [CNCF CKS](https://www.cncf.io/training/certification/cks/) | **Requires an active CKA** | After CKA + hands-on cluster hardening |
| AWS Certified Security – Specialty (SCS-C03) | AWS | $300 | [AWS Certification — Security Specialty](https://aws.amazon.com/certification/certified-security-specialty/) | AWS recommends 5yrs security + 2yrs AWS experience | After Stage 8, once I have real project experience, not right after the theory |
| GIAC certifications (e.g., GCLD, GCSA) | GIAC/SANS | $1,000–2,500+ | [GIAC Certifications](https://www.giac.org/certifications/) | Varies | Only once employed and employer-funded |
| OffSec (OSCP etc.) | OffSec | $1,600+ | [OffSec](https://www.offsec.com/courses-and-certifications/) | Strong offensive security background | Skip unless pivoting to pentesting |

### Certifications to avoid initially
- **CISSP** — requires 5 years of experience to even claim, and its content (broad GRC/management) doesn't match hands-on DevSecOps work at this stage.
- **AWS Solutions Architect Professional / Azure Solutions Architect Expert** — too advanced and too broad before real production-style project experience.
- **GIAC/SANS certs self-funded** — excellent content, but $1,000+ each is poor ROI before employment (get an employer to fund these later).
- **Any "bootcamp certificate of completion"** — a learning artifact, not a credential; don't let it substitute for a real cert or a portfolio project.
- **Both Security+ and ISC2 CC** — they overlap heavily; take at most one, and only if a specific posting requires it.

**Sequencing that matches this roadmap:** Terraform Associate (cheap, reinforces Stage 11) → SC-500 (my primary cloud, Stage 7) → CKA then CKS (Stage 10, in that order — CKS requires CKA) → AWS Security Specialty (once I have 6–12 months of real AWS project work, not right after Stage 8 theory).

---

## 9. Learning Platforms

| Platform | Best for | Level | Free content | Hands-on labs | Certificates matter? |
|---|---|---|---|---|---|
| Microsoft Learn | Azure fundamentals through SC-500 | Beg–Int | Extensive, free | Yes (sandbox) | Low alone, feeds SC-500 |
| AWS Skill Builder | AWS fundamentals through Security Specialty | Beg–Int | Extensive, free | Some paid labs | Low alone, feeds AWS certs |
| PortSwigger Web Security Academy | Application security, hands-on exploitation | Beg–Adv | 100% free | Yes, excellent | No cert, but the skill is the credential |
| TryHackMe | General security fundamentals, guided | Beg–Int | Some free rooms | Yes | Low, learning value high |
| KodeKloud | Kubernetes, Docker, DevOps hands-on labs | Beg–Adv | Some free content | Yes, excellent for K8s/CKA/CKS prep | Low, but labs are the point |
| CNCF / Linux Foundation Training | Kubernetes, cloud native | Int–Adv | Some free | Yes | High (feeds CKA/CKS directly) |
| Udemy (Stephane Maarek, Adrian Cantrill via cantrill.io) | Deep cert-focused courses (AWS/Azure) | Beg–Adv | No (cheap, $10–20 on sale / ~$40 flat) | Some | Low, content quality is the value |
| OverTheWire / CyberDefenders / LetsDefend | Blue-team/IR practice | Int | Mostly free | Yes | No |

Prioritize **PortSwigger, Microsoft Learn, AWS Skill Builder, and KodeKloud** first — genuinely high-quality and mostly free. Add Udemy/Cantrill only when prepping for a specific paid certification exam.

---

## 10. Books, Documentation & Standards — when to use each

- **OWASP (Top 10, Cheat Sheet Series, ASVS)** — use throughout Stage 5, and again anytime you review app code.
- **NIST (SP 800-53, CSF)** — reference during Stage 15 (architecture) and 16, not before — too abstract without hands-on context first.
- **CIS Benchmarks** — use as your hardening reference during Stage 1 (Linux), Stage 9 (Docker), Stage 10 (Kubernetes via kube-bench).
- **MITRE ATT&CK** — use during Stage 14 (detection/IR) to structure what you're detecting for.
- **Kubernetes docs (kubernetes.io) + CNCF security whitepaper** — Stage 10, primary source, better than most paid courses.
- **Terraform docs (developer.hashicorp.com)** — Stage 11, primary source.
- **SLSA framework + OpenSSF docs** — Stage 13.
- **Cloud Security Alliance (CSA) guidance** — Stage 15, for architecture patterns.

---

## 11. Continuous Portfolio Table

| Project | Skills Demonstrated | Security Skills | Cloud Skills | DevSecOps Skills | Blog Opportunities |
|---|---|---|---|---|---|
| Hardened Linux server | Sysadmin | Hardening, SSH security | — | — | Hardening checklist |
| Vulnerable-vs-hardened React app | AppSec | OWASP Top 10, CSP | — | — | "I hacked my own app" |
| Containerized + scanned app | Docker | Container security | — | Image scanning | CVE reduction story |
| Azure secured deployment | Cloud deploy | IAM, networking | Azure | — | IAM walkthrough |
| Terraform infra | IaC | Policy as code | Azure/AWS | IaC scanning | Migration story |
| CI/CD with gates | Pipeline eng. | SAST/DAST/SCA | — | Full DevSecOps | Pipeline build log |
| K8s secured cluster | Container orchestration | RBAC, NetworkPolicy | — | K8s security | RBAC mental model |
| Capstone platform | Everything | Everything | Multi-service | Full lifecycle | Case study series |

---

## 12. Blogging & Technical Writing Strategy

Turn every project into a content pipeline: **Project → Problem → Research → Implementation → Security issue found → Attack demonstrated → Fix applied → Testing/evidence → Lessons learned → Article.** That's typically 2–4 articles per project, not one.

Article types to rotate through: hands-on tutorials, "how I secured X" narratives, vulnerability walkthroughs (on your own deliberately-vulnerable apps only), architecture explainers with diagrams, tool comparisons, and honest "what I got wrong" retrospectives — the last category is underused and reads as far more credible than polished tutorials. Avoid shallow "I completed a course" posts entirely; if an article doesn't include your own evidence (a screenshot, a scan result, a diff, a metric), don't publish it as a portfolio piece.

**First 10 article ideas** (mapped to early stages): hardening checklist with evidence; TLS handshake explained; "I hacked my own React app"; CSP explained the hard way; JWT storage pitfalls; deploying securely to Azure; cutting a container's CVE count; migrating manual cloud setup to Terraform; building a DevSecOps pipeline that blocks bad code; what an SBOM actually is.

---

## 13. GitHub Portfolio Strategy

**Repo naming:** `cloud-sec-<topic>` (e.g., `cloud-sec-hardened-linux-server`, `cloud-sec-azure-devsecops-pipeline`) — consistent prefixing makes your profile scannable in seconds.

**Every repo README should open with:** a one-paragraph summary, an architecture diagram (even simple ones — use Mermaid or draw.io), a "what this demonstrates" bullet list, and a link to the related blog post. Follow with: setup instructions, security controls implemented, threat model or ADRs where relevant, CI/CD badge, and (for later-stage repos) SBOM and scan results.

**A recruiter should understand your capability level from your pinned repos alone in under 5 minutes** — pin your capstone first, then 3–4 of the strongest individual projects, prioritizing recency and the vulnerable-vs-hardened AppSec repo since it's your most differentiated piece.

### 13a. Documenting the learning itself, not just the projects

I want to use GitHub as my actual learning log, not just as a place project code ends up after the fact. Two things live side by side, on purpose:

- **Project repos** (`cloud-sec-<topic>`) — the polished, recruiter-facing artifacts above.
- **One dedicated `cloud-sec-learning-log` repo** — the messier, honest, dated record of the journey itself, meant for me to look back on and for anyone else attempting this same path to actually learn from. This is where "writing to myself and anyone who intended this learning" lives structurally, not just in tone.

Suggested structure for the log repo:
```
cloud-sec-learning-log/
├── README.md              (the pitch: what this is, where I started, where I'm headed)
├── skills-matrix.md        (the living table from Section 1 — updated every 2–3 months, with dated history kept, not overwritten)
├── stages/
│   ├── stage-01-linux.md   (what I actually did, what confused me, what clicked, links to the real project repo + article)
│   ├── stage-02-networking.md
│   └── ...
├── weekly-notes/
│   └── 2026-W36.md         (short, honest, dated — a paragraph is enough some weeks)
└── monthly-reviews/
    └── 2026-09.md
```
Commit to this repo often and don't clean it up after the fact — the unpolished commit history (including the weeks that stalled) is itself useful evidence, both to future-me checking progress and to anyone following the same roadmap who wants to see what the messy middle actually looks like, not just the highlight reel.

---

## 14. Home Lab

**Local:** a laptop/desktop with 16GB+ RAM running Ubuntu (dual-boot or primary), Docker Desktop or Docker Engine, `kind` for local Kubernetes (much lighter than minikube for security labs), Terraform CLI, GitHub Actions (runs against your own repos for free).

**Cloud:** use Azure's free account (12 months of popular services + always-free tier + student credits if eligible) and AWS's free tier (12 months + always-free services) for hands-on labs only — **never leave resources running**. Set a billing alert at $5 on day one in both clouds, tag every resource you create with your name/date so nothing is orphaned, and destroy everything (`terraform destroy`) at the end of every lab session. This single habit prevents almost all surprise bills.

**Labs to run locally-first before touching real cloud spend:** IAM policy writing (JSON, no deploy needed to practice), Terraform plans (`terraform plan` doesn't cost anything), Kubernetes RBAC/NetworkPolicy on `kind`, log parsing on sample datasets. Save real cloud time for deployment, networking, and IAM *enforcement* testing specifically.

---

## 15. Priority Tools — the 5–10 that matter most right now

Don't tool-hop. Master these first, in roughly this order: **Docker, Terraform, Trivy (SCA + container scanning), Semgrep (SAST), GitHub Actions, kubectl + kind, Checkov or tfsec (IaC scanning), and OWASP ZAP (DAST).** Everything else in Section 16-style tool lists (Grafana, Sentinel, Vault, OPA, Cosign, Syft) can wait until the stage that specifically calls for it.

---

## 16. Career Roadmap

**Current skills → Entry point → Mid → Senior → Architect**

Given your background, the most realistic entry point is **Junior DevSecOps Engineer** or **Application Security Engineer (junior)** — not straight into "Cloud Security Engineer," which typically wants 1–2 years of cloud-specific experience first. Your frontend background is a direct asset for AppSec-adjacent roles specifically.

| Level | Role | Required skills | Typical responsibilities | Portfolio expectation |
|---|---|---|---|---|
| Entry | Junior DevSecOps / AppSec Engineer | Stages 1–9 solid | Pipeline security, AppSec triage, basic cloud IAM | Capstone in progress, 3–4 solid projects |
| Mid | Cloud Security Engineer / DevSecOps Engineer | Stages 1–13 solid, 1 cert (SC-500 or Terraform Associate) | Own cloud security posture, build detection rules, harden pipelines | Full capstone, published articles, 1 cert |
| Senior | Senior Cloud Security Engineer | Stages 1–16, multiple certs, K8s security depth | Design controls, lead incident response, mentor juniors | Multiple production-style projects, CKS/AWS Security Specialty |
| Architect | Cloud Security Architect | All stages, deep multi-domain expertise, org-level judgment | Design org-wide security architecture, govern multi-cloud | Years of production experience, thought leadership writing |

**Common interview topics at entry/mid level:** IAM least privilege scenarios, "a secret got committed to Git — walk me through your response," container/K8s misconfig identification, SAST vs DAST vs SCA differences, OWASP Top 10 explanation with real examples from your own projects.

---

## 17. Interview Preparation — sample scenario questions with labs behind them

- *"Your production credentials were accidentally committed to GitHub. What do you do?"* → practice this for real: commit a fake credential to a private test repo, then walk through revoke → rotate → audit access logs → root-cause → prevent (push protection).
- *"A container image in production has a critical vulnerability. How do you respond?"* → practice against your Stage 9 Trivy-scanned images: triage severity/exploitability → patch/rebuild → redeploy → verify.
- *"An attacker obtained an AWS access key. What are your first 10 actions?"* → practice against your Stage 8 CloudTrail setup: disable key → review CloudTrail for actions taken → rotate all related credentials → check for persistence (new IAM users/roles) → notify → document.

Build a written runbook for each of these three scenarios from your own lab evidence — this is far stronger in an interview than reciting theory.

---

## 18. Using AI Responsibly in This Journey

Use AI (including tools like this one) for: explaining unfamiliar docs, debugging error messages, reviewing your Terraform/Dockerfiles/K8s manifests for obvious misconfigurations, brainstorming lab scenarios and blog topics, and mock interview practice. **Do not** paste AI-generated IAM policies, Terraform, or Kubernetes manifests straight into a lab or (especially) production without reading every line and understanding why each permission/rule exists — the entire point of this roadmap is that *you* can explain and defend every control, not that a tool generated something that happened to work.

---

## 19. Learning Schedules & Realistic Timelines

| Pace | Hours/week | Beginner → Competent | → Job-ready | → Advanced |
|---|---|---|---|---|
| A — 1 hr/day | ~7 | 6–8 months | 14–18 months | 3+ years |
| B — 2 hrs/day | ~14 | 3–4 months | 8–10 months | 20–24 months |
| C — 3–4 hrs/day | ~24 | 2–3 months | 6–7 months | 14–18 months |
| D — Weekend-focused (~8hrs on weekends) | ~8 | 5–7 months | 12–15 months | 30+ months |

These are honest estimates, not marketing timelines — "expert" (Section 23) realistically takes several years of actual job experience layered on top of this roadmap, not a fixed course length. Don't be discouraged if you land closer to Option A pace; consistency matters more than speed.

---

## 20. Monthly Milestones (first 6 months, Option B pace ~14 hrs/week)

- **Month 1:** Stage 0 + Stage 1 (Linux). Deliverable: hardened Linux server + checklist blog post.
- **Month 2:** Stage 2 (Networking) + Stage 3 (Git/GitHub security). Deliverable: TLS/DNS explainer post + secured reference repo.
- **Month 3:** Stage 4 (Python/Bash) + start Stage 5 (AppSec). Deliverable: mini security-auditor CLI tool published.
- **Month 4:** Finish Stage 5 (AppSec). Deliverable: vulnerable-vs-hardened React app + "I hacked my own app" post.
- **Month 5:** Stage 6 + Stage 7 (Azure). Deliverable: app deployed securely to Azure with IAM/networking/logging.
- **Month 6:** Finish Stage 7, begin Terraform Associate cert prep. Deliverable: Azure IAM/Defender writeup; sit Terraform Associate exam if ready.

Continue this cadence: Months 7–9 → Stage 8 (AWS) + Stage 9 (Docker); Months 10–13 → Stage 10 (Kubernetes) + CKA prep; Months 14–16 → Stage 11–12 (Terraform + CI/CD security) + SC-500; Months 17–20 → Stage 13–14 (supply chain + IR) + CKS; Months 21+ → capstone, AWS Security Specialty, Stage 15–17 ongoing.

---

## 21. "Do Not Learn Yet" List

- **Kubernetes before Docker and cloud fundamentals are solid** — you'll cargo-cult YAML without understanding what it's protecting.
- **All three clouds at once** — pick Azure, go deep, then AWS. GCP only if a job requires it.
- **CISSP or other experience-gated management certs** — you don't have the years to even claim them yet, and the content doesn't match hands-on work.
- **Building elaborate custom security tools from scratch** before you understand the manual process the tool would automate.
- **Chasing every new tool you see on X/LinkedIn** — the 5–10 tools in Section 15 cover 90% of what you need for a long time.
- **Collecting certifications without matching hands-on project evidence** — a cert with no portfolio behind it is a weak signal in this field specifically, because interviews are heavily scenario-based.
- **Advanced compliance/GRC frameworks (SOC2 audit prep, ISO 27001 lead auditor)** — valuable later, not now; it's org-process knowledge, not hands-on engineering skill.

---

## 22. Expert-Level Progression — what actually changes

Applied across domains, the same ladder holds:

| Domain | Beginner | Intermediate | Advanced | Expert |
|---|---|---|---|---|
| IAM | "I know what IAM is" | Can configure IAM securely | Can design secure IAM architecture | Can design, implement, audit, automate, and defend IAM across complex multi-account environments |
| Cloud | Knows service names | Can deploy securely on one cloud | Can design multi-service secure architectures | Can architect and govern security across multi-cloud, multi-team orgs |
| Kubernetes | Can deploy a pod | Can secure RBAC/NetworkPolicy for one cluster | Can design cluster security for multi-tenant environments | Can define org-wide K8s security standards and audit compliance at scale |
| DevSecOps | Knows the term "shift-left" | Can add scanning to a pipeline | Can design pipeline security gates org-wide | Can build a security engineering culture and tooling platform that scales across teams |
| AppSec | Knows OWASP Top 10 names | Can find and fix common vulns | Can threat-model an app before it's built | Can define secure-by-design standards adopted org-wide |
| Incident Response | Knows the IR lifecycle | Can execute a runbook | Can write runbooks and lead a response | Can build detection/response capability and post-incident process improvement at org scale |

The through-line: expertise isn't "knows more facts," it's **the ability to design, implement, automate, audit, and defend — under real constraints, at increasing scale.** Certifications and courses can validate knowledge; only sustained hands-on work and time in a real job builds the "design and defend at scale" layer.

---

## 23. Final Roadmap Dashboard

| Phase | Skills | Project | Certification | Labs | Blog | Portfolio Evidence | Job Readiness |
|---|---|---|---|---|---|---|---|
| 1 (Mo 1–4) | Linux, networking, Git, Python/Bash, AppSec | Hardened server, secured repo, vulnerable-app | — | Ongoing | 4–5 posts | 3 repos | Not yet |
| 2 (Mo 5–9) | Azure, AWS, Docker | Cloud deployment, containerized app | Terraform Associate | Ongoing | 3–4 posts | +2 repos | Junior-adjacent |
| 3 (Mo 10–16) | Kubernetes, Terraform, CI/CD security | K8s cluster, IaC rebuild, secured pipeline | SC-500, CKA | Ongoing | 3–4 posts | +3 repos | **Entry-level job ready** |
| 4 (Mo 17–20+) | Supply chain, IR, architecture | Capstone platform | CKS, AWS Security Specialty | Ongoing | Case study series | Capstone + full portfolio | **Mid-level competitive** |

**Top 10 skills to prioritize:** Linux hardening, cloud IAM, networking fundamentals, Docker/container security, Terraform, CI/CD security gates, application security (OWASP), Kubernetes security, logging/monitoring, secrets management.

**Top 10 tools:** Docker, Terraform, Trivy, Semgrep, GitHub Actions, kubectl/kind, Checkov, OWASP ZAP, Cosign, Syft.

**Top 10 free resources:** Microsoft Learn, AWS Skill Builder, PortSwigger Web Security Academy, Kubernetes official docs, Terraform official docs, OWASP Cheat Sheet Series, CNCF security whitepaper, KodeKloud free content, GitHub Docs (Actions/security features), CIS Benchmarks.

**Top 5 paid resources worth considering:** Adrian Cantrill's AWS/cloud courses (cantrill.io), KodeKloud full subscription (for K8s/CKA/CKS labs), Stephane Maarek's cert-prep Udemy courses, Semgrep/Trivy premium tiers only once you're employed and need enterprise features, a paid Burp Suite Pro license only if pursuing deeper AppSec work.

**Top certifications (in order):** Terraform Associate → SC-500 → CKA → CKS → AWS Security Specialty.

**First 3 projects:** hardened Linux server, containerized+scanned app, vulnerable-vs-hardened React app.

**First 10 blog articles:** listed in Section 12.

**First GitHub repos:** `cloud-sec-hardened-linux-server`, `cloud-sec-vulnerable-vs-hardened-react`, `cloud-sec-security-auditor-cli`.

**First job roles to target:** Junior DevSecOps Engineer, Application Security Engineer (junior), Cloud Support/Security Analyst — roles that value your AppSec+cloud+writing combination even without 2 years of pure cloud infra experience.

**Biggest mistakes to avoid:** collecting certs without matching hands-on evidence; jumping to Kubernetes before fundamentals are solid; trying to master three clouds simultaneously; treating this as a course-completion checklist instead of a build-break-secure-document loop; going quiet instead of publishing your work.

---

*Revisit Section 1's skills table every 2–3 months and update your levels honestly — that's your real progress tracker, not the calendar.*

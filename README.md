<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Aman%20Vishwakarma&fontSize=48&fontColor=fff&animation=twinkling&fontAlignY=36&desc=Full-Stack%20Product%20Engineer%20%E2%80%94%20Fintech%20%C2%B7%20EdTech%20%C2%B7%20Cloud%20%C2%B7%20Mobile&descAlignY=56&descAlign=50" />

[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=600&size=20&duration=3000&pause=1000&color=6AD3F7&center=true&vCenter=true&multiline=false&repeat=true&width=800&lines=I+design+the+product.+I+architect+the+system.+I+ship+the+code.;Full-stack+across+API+%C2%B7+Web+%C2%B7+Mobile+%C2%B7+Cloud;PostgreSQL+%C2%B7+MongoDB+%C2%B7+Redis+%C2%B7+BullMQ+%C2%B7+AWS)](https://git.io/typing-svg)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/aman-vishwakarma/)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aman.vishwakarma.dev@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/amankumar430206)
[![Location](https://img.shields.io/badge/Bangalore%2C%20India-FF5722?style=for-the-badge&logo=googlemaps&logoColor=white)](#)

</div>

<br/>

## Who I Am

<img align="right" width="400" src="https://github-readme-stats.vercel.app/api?username=amankumar430206&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=6AD3F7&icon_color=6AD3F7&text_color=ffffff&rank_icon=github" />

I'm a **Sr. Full-Stack Engineer** who builds products end-to-end — from data model to API, from web dashboard to mobile app, from local Docker to AWS production.

I don't just implement features. I **design the domain**, **architect the system**, **write the API**, **build the UI**, and **ship to production**. Every project I take on has a complete thought behind it.

My work spans **fintech** (cross-border payments, neobanking, maker-checker compliance), **edtech** (student assessment platforms, cognitive skill tracking), and **career tech** (mentorship networks, AI-driven guidance).

```yaml
currently_building:
  remitx:        Multi-tenant white-label cross-border payment platform
  campus_mentor: Mentorship-driven career acceleration platform
  ngn_360seel:   Student mental health & skill assessment platform

at_work:
  company: Flipkart(VC) SDE 2
```

<br clear="right"/>

<br/>

## Projects I've Built

> Platforms I designed, architected, and built from scratch — PRD to production.

<br/>

### RemitX — Multi-Tenant Cross-Border Payment Platform

> White-label fintech infrastructure. Businesses onboard → get branded portal → send international payments → manage sub-clients. Built for compliance, scale, and zero-trust.

```
Stack: Node.js · Express · PostgreSQL · Knex · Redis · BullMQ · React Native · React · Vite · Tailwind
Auth:  RS256 JWT · bcrypt · TOTP MFA
Infra: Docker · Modular Monolith (microservice-extractable)
```

- **Maker-Checker enforcement** — DB constraint + app-level: maker ≠ checker, no self-approval, ever
- **Append-only ledger** — `REVOKE UPDATE/DELETE` at DB level; ledger and audit logs are immutable
- **Idempotent payments** — every write requires `X-Idempotency-Key`; duplicate requests are safe
- **Pluggable provider adapters** — switch from `manual` → `ZoQQ` → `CloudCurrency` via DB config, zero redeploy
- **Multi-tenant row isolation** — every query carries `tenant_id`; cross-tenant data leaks are structurally impossible
- **KYC/KYB flow** — document upload, admin review queue, 2-year expiry, adapter-ready for Sumsub/Onfido
- **Big.js arithmetic** — zero native float used anywhere money is calculated
- **Approval thresholds** — auto ≤ $1k, single checker ≤ $50k, dual checker > $50k

Roles: Super Admin · Client Admin · Maker · Checker · Sub-Client Admin · Sub-Client User

<br/>

### Campus Mentor — Career Acceleration & Mentorship Platform

> The complete career OS for students. Discover mentors → Get guidance → Build projects → Get reviewed → Get endorsed → Get referred → Get hired.

```
Stack: Node.js · Express · PostgreSQL · Prisma · Redis · BullMQ · OpenAI · Razorpay
       React Native (Expo) · TypeScript · Next.js · Tailwind · AWS S3
Auth:  JWT · bcrypt
Arch:  Modular Monolith · DDD · Event-Driven · AI-Ready
```

- **Domain-Driven Design** — each module (`auth`, `students`, `mentors`, `bookings`) is a bounded context, independently extractable
- **AI-powered guidance** — OpenAI integration for career path recommendations and mentor matching
- **Booking & session management** — mentor calendars, session states (`PENDING → CONFIRMED → COMPLETED`), waitlist support
- **Payments** — Razorpay integration for mentor session billing
- **Waitlist system** — role-based (`STUDENT | MENTOR`) with admin-controlled approvals
- **Institution registry** — `COLLEGE | UNIVERSITY | BOOTCAMP` with student-institution linking

Actors: Students · Mentors · Colleges · Recruiters · Admins

<br/>

### NGN 360SEEL — Student Mental Health & Skill Assessment Platform

> Multi-role assessment platform tracking cognitive, emotional, and social skills across school terms. Dual-respondent scoring and PDF reporting on mobile.

```
Stack: Node.js · Express · MongoDB · Mongoose · AWS S3 · Nodemailer
       React Native (Expo) · TypeScript · Redux Toolkit · NativeWind · Formik
Auth:  JWT · bcrypt · OTP email
Infra: Docker (Node 20 Alpine) · Cluster multi-worker
```

- **Multi-survey architecture** — per-grade versioned surveys (`Q1, Q2, Q3...`), `pre/post` types, bidirectional linking, window-based auto-activation/expiry
- **Dual-respondent scoring** — parent and teacher independently respond; engine computes category scores, badges, and `overallAverage`
- **Survey lifecycle** — `upcoming → active → expired` with `windowStatus`, `responseStatus`, and `isLocked` annotations per student
- **Aggregate reports** — yearly cross-survey trend reports with per-category averages and grade progression
- **PDF generation** — branded reports with both NGN and school logos, delivered in-app
- **Bulk operations** — teachers upload student rosters via Excel (`xlsx`); validated, parsed, enrolled
- **Role-based access** — `SUPER | ADMIN | CLIENT (school) | TEACHER | PARENT`; each with scoped data access

<br/>

## Tech Stack

<div align="center">

**Languages & Runtimes**

![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)

**Frontend & Mobile**

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vue.js](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D)
![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

**Backend & Databases**

![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white)

**Cloud & DevOps**

![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0089D6?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

**Integrations**

![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Razorpay](https://img.shields.io/badge/Razorpay-0C2451?style=for-the-badge&logo=razorpay&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)

</div>

<br/>

## Architecture Patterns

```
Modular Monolith → Microservice-extractable design
Domain-Driven Design (bounded contexts, clean public APIs per module)
Event-driven internal communication via BullMQ
Multi-tenant row-level data isolation
Maker-Checker compliance enforcement (DB + app level)
Append-only audit ledgers (REVOKE UPDATE/DELETE)
Pluggable provider adapters (swap logic via DB config, zero redeploy)
JWT (RS256) · bcrypt · TOTP MFA · OTP email auth
Idempotent APIs with deduplication keys
Cluster-mode Node.js for multi-worker concurrency
```

<br/>

## Impact

<div align="center">

| What | Result |
|------|--------|
| Deployment time cut | **80%** |
| Critical prod bugs reduced | **35%** |
| Legacy system perf improvement | **90%** |
| Code reviews done | **250+** |
| Daily transactions handled | **100,000+** |
| Regions shipped | **UAE · KSA · Egypt · India** |

</div>

<br/>

## Certifications

<div align="center">

[![Oracle](https://img.shields.io/badge/Oracle_Certified_Architect_Associate_2025-F80000?style=for-the-badge&logo=oracle&logoColor=white)](#)
[![Oracle](https://img.shields.io/badge/Oracle_Certified_Developer_Professional_2025-F80000?style=for-the-badge&logo=oracle&logoColor=white)](#)

</div>

<br/>

## GitHub Activity

<div align="center">

<img height="160em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=amankumar430206&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=6AD3F7&text_color=ffffff"/>

<img src="https://github-readme-streak-stats.herokuapp.com?user=amankumar430206&theme=tokyonight&hide_border=true&background=0D1117&ring=6AD3F7&fire=FF6B6B&currStreakLabel=6AD3F7" />

</div>

<br/>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&text=Open%20to%20interesting%20problems&fontSize=22&fontColor=fff&animation=twinkling&fontAlignY=65" />

**aman.vishwakarma.dev@gmail.com · +91 9979850588 · Bangalore, India**

*"I don't just write code. I build systems that are worth building."*

⭐ From [amankumar430206](https://github.com/amankumar430206)

</div>

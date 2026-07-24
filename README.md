<div align="center">
  <img src="assets/banner.svg" alt="Khristopher Ben Manilla — Full-Stack Software Engineer" width="100%" />
</div>

<div align="center">
  <sub>Fourth-Year BS Computer Science · Project Coordinator · Cavite, Philippines</sub>
</div>

<br />

I build secure, documented, and testable full-stack applications with **React, TypeScript, Next.js, NestJS, Laravel, Python, and PostgreSQL**. My strongest work combines product requirements, role-based security, automated validation, offline-first workflows, and practical AI/ML.

<div align="center">
  <img src="assets/project-coordinator.svg" height="28" alt="Project Coordinator" />
  <img src="https://img.shields.io/badge/Project_Coordinator-F7F8FA?style=for-the-badge&logoColor=040609" height="28" alt="Project Coordinator" />
  <a href="https://kbmanilla06.vercel.app"><img src="https://img.shields.io/badge/Portfolio-090C11?style=for-the-badge&logo=vercel&logoColor=F7F8FA" alt="Portfolio" /></a>
  <a href="https://github.com/kbmanilla06"><img src="https://img.shields.io/badge/GitHub-090C11?style=for-the-badge&logo=github&logoColor=F7F8FA" alt="GitHub" /></a>
  <a href="https://www.linkedin.com/in/khristopher-ben-manilla-b875181b6/"><img src="assets/linkedin-button.svg" height="28" alt="LinkedIn" /></a>
  <a href="https://kbmanilla06.vercel.app/Khristopher_Ben_Manilla_Resume.pdf"><img src="https://img.shields.io/badge/Résumé-090C11?style=for-the-badge&logo=readthedocs&logoColor=F7F8FA" alt="Résumé" /></a>
  <a href="mailto:kbmanilla06@gmail.com"><img src="https://img.shields.io/badge/Email-090C11?style=for-the-badge&logo=gmail&logoColor=F7F8FA" alt="Email" /></a>
</div>

<img src="assets/divider.svg" width="100%" alt="" />

## Engineering Profile

| | |
|---|---|
| **Primary focus** | Full-stack software engineering |
| **Supporting strengths** | Application security · Applied AI/ML |
| **Current role** | **Project Coordinator** at StartupLab Business Center & AI Consulting Services OPC |
| **Education** | BS Computer Science, Lyceum of the Philippines University–Cavite |
| **Academic standing** | Dean’s List awardee for three consecutive academic years |

I translate requirements into maintainable systems and use AI-assisted development as an engineering tool—not a substitute for architecture, review, testing, or ownership.

<img src="assets/divider.svg" width="100%" alt="" />

## Flagship Projects

### [RESPONDA](https://github.com/kbmanilla06/Responda) — Offline-First Disaster Response Platform

An emergency reporting and relief-coordination platform for residents, LGUs, responders, shelters, relief organizations, and volunteers. Reports remain usable through poor or absent connectivity, then synchronize automatically when the device reconnects.

| Engineering evidence | Verified result |
|---|---|
| Automated validation | **398+ tests** — 177 API e2e, 96 API unit, 67 web unit, and 58+ browser e2e |
| Access control | **8 account types** with capability-based, organization-scoped authorization |
| Offline reliability | IndexedDB outbox, idempotent sync, conflict resolution, retry policy, and multi-tab locking |
| Operational scope | Incident verification, rescue dispatch, shelters, relief inventory, volunteers, notifications, and reports |
| Geospatial architecture | PostgreSQL + PostGIS with MapLibre-based maps and jurisdiction-aware workflows |
| Delivery integrity | 17 documented sprints, CI quality gates, threat model, runbooks, backup/restore, and release evidence |

<details>
<summary><b>Architecture, safety, and release status</b></summary>
<br />

RESPONDA is a pnpm/Turborepo monorepo pairing a Next.js PWA with a NestJS modular-monolith API. PostgreSQL/PostGIS stores operational and geographic data; Redis and BullMQ support background work; WebSockets provide real-time coordination; and S3-compatible object storage handles incident evidence.

The repository documents its boundaries explicitly: the application preview is available, but production infrastructure, real notification providers, human UAT, and manual accessibility testing remain release gates. Automated accessibility checks cover 12 critical pages with zero reported axe-core violations.

</details>

<p>
  <img src="https://img.shields.io/badge/Next.js-090C11?style=flat-square&logo=nextdotjs&logoColor=F7F8FA" alt="Next.js" />
  <img src="https://img.shields.io/badge/NestJS-090C11?style=flat-square&logo=nestjs&logoColor=F7F8FA" alt="NestJS" />
  <img src="https://img.shields.io/badge/TypeScript-090C11?style=flat-square&logo=typescript&logoColor=F7F8FA" alt="TypeScript" />
  <img src="https://img.shields.io/badge/PostgreSQL-090C11?style=flat-square&logo=postgresql&logoColor=F7F8FA" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/PostGIS-090C11?style=flat-square&logo=postgresql&logoColor=F7F8FA" alt="PostGIS" />
  <img src="https://img.shields.io/badge/Redis-090C11?style=flat-square&logo=redis&logoColor=F7F8FA" alt="Redis" />
  <img src="https://img.shields.io/badge/Docker-090C11?style=flat-square&logo=docker&logoColor=F7F8FA" alt="Docker" />
  <img src="https://img.shields.io/badge/Playwright-090C11?style=flat-square&logo=playwright&logoColor=F7F8FA" alt="Playwright" />
</p>

<a href="https://github.com/kbmanilla06/Responda"><img src="https://img.shields.io/badge/Source_Code-090C11?style=for-the-badge&logo=github&logoColor=F7F8FA" alt="RESPONDA source code" /></a>
<a href="https://responda-web.vercel.app"><img src="https://img.shields.io/badge/Live_Preview-F7F8FA?style=for-the-badge&logo=vercel&logoColor=040609" alt="RESPONDA live application preview" /></a>

<br />

### [All in Time](https://github.com/kbmanilla06/All-in-Time) — Workforce Operations Platform

A full-stack workforce performance system covering time tracking, approval workflows, KPIs, payroll preparation, reporting, onboarding, protected attachments, and auditable workforce insights.

| Engineering evidence | Verified result |
|---|---|
| Automated validation | **717 tests** — 370 backend + 347 frontend |
| Authorization | **4 roles** enforced server-side through policies and middleware |
| Delivery | Stakeholder-led implementation with documented sprint history |
| Operations | Docker, GitHub Actions, setup, QA, deployment, backup, and user guides |
| Insight architecture | **7 deterministic capabilities** with no external model calls |

<details>
<summary><b>Architecture, security, and tradeoffs</b></summary>
<br />

The React and TypeScript SPA communicates with a Laravel REST API backed by PostgreSQL and protected file storage. Interface-level role awareness improves usability, while server-side policies and middleware remain the authorization source of truth.

The current insight engine is deterministic and local. This keeps sensitive workforce data out of third-party model calls while preserving an upgrade path to a future provider. Deliberate MVP boundaries—including single-organization scope, synchronous mail, and deferred malware scanning—are documented instead of hidden.

</details>

<p>
  <img src="https://img.shields.io/badge/React-090C11?style=flat-square&logo=react&logoColor=F7F8FA" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-090C11?style=flat-square&logo=typescript&logoColor=F7F8FA" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Laravel-090C11?style=flat-square&logo=laravel&logoColor=F7F8FA" alt="Laravel" />
  <img src="https://img.shields.io/badge/PHP-090C11?style=flat-square&logo=php&logoColor=F7F8FA" alt="PHP" />
  <img src="https://img.shields.io/badge/PostgreSQL-090C11?style=flat-square&logo=postgresql&logoColor=F7F8FA" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Docker-090C11?style=flat-square&logo=docker&logoColor=F7F8FA" alt="Docker" />
  <img src="https://img.shields.io/badge/GitHub_Actions-090C11?style=flat-square&logo=githubactions&logoColor=F7F8FA" alt="GitHub Actions" />
</p>

<a href="https://github.com/kbmanilla06/All-in-Time"><img src="https://img.shields.io/badge/Source_Code-090C11?style=for-the-badge&logo=github&logoColor=F7F8FA" alt="All in Time source code" /></a>
<a href="https://kbmanilla06.vercel.app/projects/all-in-time"><img src="https://img.shields.io/badge/Case_Study-F7F8FA?style=for-the-badge&logo=vercel&logoColor=040609" alt="All in Time engineering case study" /></a>

<br />

### [Customer Churn Prediction](https://github.com/kbmanilla06/customer-churn-prediction)

An end-to-end machine-learning pipeline and Streamlit dashboard for identifying telecom customers at risk of churn. SMOTE is applied inside stratified cross-validation to avoid data leakage, with Logistic Regression, Random Forest, and XGBoost compared using F1 and ROC-AUC.

<p>
  <img src="https://img.shields.io/badge/Python-090C11?style=flat-square&logo=python&logoColor=F7F8FA" alt="Python" />
  <img src="https://img.shields.io/badge/Scikit--learn-090C11?style=flat-square&logo=scikitlearn&logoColor=F7F8FA" alt="Scikit-learn" />
  <img src="https://img.shields.io/badge/XGBoost-090C11?style=flat-square&logoColor=F7F8FA" alt="XGBoost" />
  <img src="https://img.shields.io/badge/Streamlit-090C11?style=flat-square&logo=streamlit&logoColor=F7F8FA" alt="Streamlit" />
</p>

<a href="https://github.com/kbmanilla06/customer-churn-prediction"><img src="https://img.shields.io/badge/Repository-090C11?style=flat-square&logo=github&logoColor=F7F8FA" alt="Customer Churn Prediction repository" /></a>

<br />

### [NLTKBot](https://github.com/Jassim3nidad/NLTKBot)

A four-person academic NLP project combining preprocessing, fuzzy matching, sentiment analysis, keyword extraction, and a Flask API across web and command-line interfaces.

<p>
  <img src="https://img.shields.io/badge/Python-090C11?style=flat-square&logo=python&logoColor=F7F8FA" alt="Python" />
  <img src="https://img.shields.io/badge/NLTK-090C11?style=flat-square&logoColor=F7F8FA" alt="NLTK" />
  <img src="https://img.shields.io/badge/Flask-090C11?style=flat-square&logo=flask&logoColor=F7F8FA" alt="Flask" />
  <img src="https://img.shields.io/badge/Natural_Language_Processing-090C11?style=flat-square&logoColor=F7F8FA" alt="Natural Language Processing" />
</p>

<a href="https://github.com/Jassim3nidad/NLTKBot"><img src="https://img.shields.io/badge/Repository-090C11?style=flat-square&logo=github&logoColor=F7F8FA" alt="NLTKBot repository" /></a>

<img src="assets/divider.svg" width="100%" alt="" />

## Technical Toolkit

<div align="center">
  <img src="https://skillicons.dev/icons?i=react,ts,nextjs,vite,laravel,php,python,postgres,docker,git,github,vercel&theme=dark&perline=12" alt="React, TypeScript, Next.js, Vite, Laravel, PHP, Python, PostgreSQL, Docker, Git, GitHub, and Vercel" />
</div>

<br />

| Area | Tools and evidence |
|---|---|
| **Frontend** | React, TypeScript, Next.js, Vite, PWAs, offline sync, responsive UI, component testing |
| **Backend** | NestJS, Laravel, PHP, REST APIs, WebSockets, policies, middleware, validation |
| **Data** | PostgreSQL, PostGIS, Redis, IndexedDB, SQL, schema design, migrations, reporting queries |
| **Security** | Capability-based authorization, server-enforced RBAC, rate limiting, protected files, auditability |
| **AI / ML** | Python, Scikit-learn, XGBoost, NLTK, reproducible evaluation |
| **Delivery** | Git, Docker Compose, GitHub Actions, Vercel, operational documentation |

<img src="assets/divider.svg" width="100%" alt="" />

## Certifications & Development

- **Networking Basics** — Cisco Networking Academy, May 2026
- **Introduction to Modern AI** — Cisco Networking Academy, February 2026
- **Python Essentials 1 & 2** — Cisco Networking Academy, January & June 2024
- **IoT Bootcamp** — ACube Technologies Inc.

<img src="assets/divider.svg" width="100%" alt="" />

## Engineering Principles

<img src="assets/principles.svg" width="100%" alt="Architecture: requirements before implementation. Security: enforced at system boundaries. Validation: tests and documentation are delivery work." />

<img src="assets/divider.svg" width="100%" alt="" />

## Contact

<div align="center">
  <a href="mailto:kbmanilla06@gmail.com"><img src="https://img.shields.io/badge/-090C11?style=for-the-badge&logo=gmail&logoColor=F7F8FA" alt="Email" /></a>
  <a href="https://www.linkedin.com/in/khristopher-ben-manilla-b875181b6/"><img src="assets/linkedin-icon.svg" height="28" alt="LinkedIn" /></a>
  <a href="https://kbmanilla06.vercel.app"><img src="https://img.shields.io/badge/-090C11?style=for-the-badge&logo=vercel&logoColor=F7F8FA" alt="Portfolio" /></a>
  <a href="https://github.com/kbmanilla06"><img src="https://img.shields.io/badge/-090C11?style=for-the-badge&logo=github&logoColor=F7F8FA" alt="GitHub" /></a>
  <a href="https://kbmanilla06.vercel.app/Khristopher_Ben_Manilla_Resume.pdf"><img src="https://img.shields.io/badge/-090C11?style=for-the-badge&logo=readthedocs&logoColor=F7F8FA" alt="Résumé" /></a>

<br /><br />
<sub>Open to software engineering, full-stack, AI/ML, and application-security opportunities.</sub>

<br /><br />
<sub>Visual system: <a href="https://github.com/kbmanilla06/WashDish-Design-Language">WashDish Design Language</a> · monochrome baseline</sub>

</div>

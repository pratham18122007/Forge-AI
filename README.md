# FORGE

### AI-Powered Startup Creation & Venture Operating Platform

Developed during a 3-month Prompt & Research Engineering internship at **Algo Force AI**.

🌐 **Live Demo:** [forge26.netlify.app](https://forge26.netlify.app/)

---

## Project Information

| | |
|---|---|
| **Project** | FORGE |
| **Organization** | Algo Force AI |
| **Engagement** | 3-Month Internship |
| **Role** | Prompt & Research Engineering |
| **Project Type** | AI-Powered SaaS Platform |
| **Deployment** | Cloud / Web Application |

> This repository is a public project showcase, not internal engineering documentation. Credentials, datasets, infrastructure configuration, proprietary business logic, and other organization-specific details are intentionally excluded.

---

## Overview

FORGE unifies the major startup-building workflows into a single platform, connecting founders, builders, and investors across the full venture lifecycle:

**Idea → Validation → Team Building → Startup Creation → Funding → Growth → Scale**

It provides role-specific workspaces for **founders**, **builders**, and **investors**.

---

## Platform Users

**Founders** create and validate ideas, build startup teams, recruit builders, launch projects, and explore funding opportunities.

**Builders** discover startup projects, apply to opportunities, manage their skills and profile, and collaborate with startup teams.

**Investors** discover and evaluate startups, access startup intelligence, shortlist opportunities, and track investment workflows.

---

## Core Capabilities

- **Idea Exchange** — Idea discovery, validation, voting, and AI-assisted refinement
- **Founder & Builder Matching** — Profiles, project discovery, applications, and collaboration
- **Startup Creation** — Startup formation, team building, projects, and execution workflows
- **Builder Marketplace** — Opportunities, skill-based matching, and project collaboration
- **Investor Workflows** — Startup discovery, evaluation, shortlisting, and funding workflows
- **Startup Intelligence** — AI-assisted market, risk, competitor, and readiness analysis

---

## AI Intelligence Layer

FORGE's AI supports idea validation, market and competitor analysis, business model evaluation, experiment generation, pitch improvement, investor readiness scoring, and roadmap generation.

The application uses a provider abstraction layer so AI workflows aren't tightly coupled to a single provider:

```text
              AI Request
                  │
                  ▼
           Provider Router
                  │
          ┌───────┴───────┐
          ▼               ▼
       Primary          Fallback
       Provider         Provider
          │               │
          └───────┬───────┘
                  ▼
             AI Response
```

*API keys, private endpoints, internal prompts, and provider configuration values are intentionally not disclosed.*

---

## System Architecture

```text
                         FORGE PLATFORM
                              │
                              ▼
                    ┌──────────────────┐
                    │   Next.js Web    │
                    │ React / TypeScript│
                    └────────┬─────────┘
                             │
                ┌────────────┴────────────┐
                ▼                         ▼
       ┌─────────────────┐       ┌─────────────────┐
       │    Supabase     │       │  FastAPI AI     │
       │                 │       │    Service      │
       │ Authentication  │       │                 │
       │ PostgreSQL      │       │ LangGraph       │
       │ Realtime        │       │ AI Workflows    │
       │ RLS             │       │ Provider Layer  │
       └─────────────────┘       └────────┬────────┘
                                          │
                                          ▼
                                  ┌───────────────┐
                                  │ AI Providers  │
                                  │ Primary +     │
                                  │ Fallback      │
                                  └───────────────┘

                 Infrastructure & Observability
                       Docker · Prometheus · Grafana
```

This diagram is intentionally high-level. Internal service URLs, network topology, database hostnames, project IDs, and connection strings are not included.

---

## Technology Stack

**Frontend** — Next.js, React, TypeScript, Tailwind CSS

**Backend** — FastAPI, Python, REST APIs

**Database & Authentication** — Supabase, PostgreSQL, Supabase Auth, Row Level Security, Supabase Realtime, OAuth

**AI** — LangGraph, Google Gemini, Groq, AI Provider Abstraction (Primary / Fallback Architecture)

**Infrastructure** — Docker, Docker Compose, Cloud Deployment

**Observability** — Prometheus, Grafana

**Development** — Git, GitHub, npm, Python

---

## Authentication & Data

FORGE uses Supabase for authentication and data persistence, including OAuth-based sign-in, session management, and role-based access control. PostgreSQL (via Supabase) backs the application's persistent data, with Row Level Security enforcing access boundaries and Supabase Realtime powering live updates across role-based workspaces.

*Schema details, table structures, and connection configuration are not published in this repository.*

---

## My Contribution

FORGE was a collaborative, organization-built platform. Over the course of the internship, I contributed across:

- **Frontend Engineering** — Built and refined Next.js/TypeScript interfaces, dashboards, onboarding flows, and responsive role-based experiences
- **Backend Engineering** — Worked with FastAPI services, API workflows, and backend integration
- **Database Engineering** — Integrated Supabase/PostgreSQL for persistent application data, authentication, and realtime workflows
- **Authentication & Authorization** — Built authentication flows, OAuth, sessions, protected routes, and role-based access
- **AI Engineering** — Worked with LangGraph-based AI workflows and contributed to the AI provider abstraction/fallback mechanism powering startup intelligence features
- **Infrastructure** — Worked with Docker-based development and cloud deployment configuration
- **Observability** — Integrated Prometheus and Grafana for application monitoring and visualization
- **Testing & Debugging** — Investigated issues in authentication persistence, database integration, role routing, responsive behavior, realtime functionality, and deployment

*This section reflects my individual contribution within a larger, organization-owned project — not sole authorship of the platform.*

---

## Engineering Highlights

- Role-based SaaS architecture with persistent cloud database
- Authentication and OAuth with realtime application workflows
- AI-assisted startup intelligence with provider abstraction and fallback
- Modular frontend architecture and API-driven backend services
- Containerized development, application observability, and cloud deployment

---

## Security & Confidentiality

This repository is a public portfolio and project showcase, not internal engineering documentation. It intentionally excludes API keys and secrets, service-role credentials, database credentials and connection strings, private environment variable values, proprietary datasets, internal prompts, private API endpoints, organization-specific infrastructure details, confidential business logic, and internal monitoring configuration or URLs.

Environment variables must be supplied through local or deployment configuration and are never committed to version control.

---

## Live Project

🌐 **Live Application:** [forge26.netlify.app](https://forge26.netlify.app/)

---

## Project Status

This repository is a curated public showcase of a real, internally-deployed platform, maintained as a portfolio reference. It is not the organization's production codebase.

# TryTami (formerly bILTup)

## Role: Co-Founder / Developer then CTO
## Dates: 8/2024 - Present
## Location: Denver, CO

---

## Company Overview

TryTami is a B2B training marketplace SaaS platform that connects corporate customers with training companies and individual trainers. The platform enables customers to discover courses, request proposals, book training sessions, and manage billing -- all facilitated by an AI-powered chat assistant.

---

## Scale of Contribution

- **4,026 total commits** across the project (~20 months)
- **2,840 commits by Dean Hiller (70.5% of all commits)** across two accounts
- **190+ branches** managed
- **2,166+ PRs merged**
- Primary architect and tech lead of the entire platform

---

## Technology Stack

### Frontend
- Angular 19 with Angular Material and Angular Google Maps
- TypeScript 5.7
- Tailwind CSS with Prettier plugin
- SCSS
- Service Workers (PWA-style offline/upgrade behavior)

### Backend
- Node.js 22.4 with Express 4
- TypeScript
- Prisma 7.3 ORM with PostgreSQL
- Google Cloud Firestore (real-time chat)
- esbuild (bundling)

### AI / ML
- OpenAI/ChatGPT integration (streaming chat with tool calls)
- Anthropic Claude Agent SDK
- AI-powered course creation, trainer matching, and proposal generation
- Vector search / auto-suggest for skills
- Prompt versioning and management system (dedicated microservice)

### Payments
- Stripe (3D Secure, webhooks, saved payment methods, billing/invoicing)

### Infrastructure
- Google Cloud Platform (Cloud Run, Cloud Tasks, Cloud Scheduler, Cloud Storage)
- Terraform (12 modules: Cloud Run, Postgres, Firestore Storage, GitHub Actions SA, IAM, Public Secrets, etc.)
- Docker (containerized deployments)
- Cloudflare Workers (proxy / multi-subdomain routing)
- Firebase/Firestore (real-time chat, authentication)

### DevOps / Build
- Nx 21.6 monorepo with custom plugins and guardrails
- GitHub Actions CI/CD
- Sentry (error monitoring, client and server)
- Brevo (email/marketing integration)
- Playwright (E2E testing) and Jest (unit testing)
- Custom AI-powered code review workflow

---

## Architecture

### Monorepo Structure
- **3 services:** `website` (client + server), `prompt-svc`, `cloudflare-proxy`
- **10 shared libraries:** `agents`, `api-prompt`, `apis`, `firestore-schema`, `lib-express`, `lib-firestore`, `lib-website-util`, `prisma-schema`, `root-api-util`, `root-svr-util`
- **2 tools:** `eslint-rules`, `test-generator`

### Multi-Role System
- Customer, Trainer, Training Company Admin, Tami Admin, Student

### Multi-Tenant
- Each training company gets its own subdomain via Cloudflare Workers proxy

---

## Major Features Built

### Phase 1: Foundation (Aug 2024 - Sep 2024)
- Initial project setup and architecture design
- Google OAuth sign-in (trainer + customer)
- User registration, settings, profile photo upload/crop
- PostgreSQL schema with Prisma, UUID primary keys
- Role-based authorization (JWT tokens)
- Trainer profiles with skills autocomplete
- Customer dashboard with sortable/filterable tables
- Admin pages for course management
- Real-time chat with Firestore (chat groups, members, messages)
- Firebase authentication with custom token service
- Error handling framework (global handlers, 404/500 pages)

### Phase 2: AI Integration & Core Platform (Aug 2025 - Oct 2025)
- Prompt microservice (dedicated service for AI prompt management)
- Dynamic prompt versioning system with tagging (dev/demo/prod)
- ChatGPT streaming integration with custom tool calls
- AI tools: displayContent, displayForm, todoList, queryEstimates, nextInstructions, updateProposal, createThread, displayCourse
- Content panel for rich AI responses
- Subprompts and dynamic menu system
- Service Worker for automatic client upgrades
- Firestore-based real-time messaging with multi-tab support
- Email system (Brevo integration, email filtering per environment)
- Cloud Tasks integration for async processing
- Rebranding from "Biltup" to "TryTami"
- Stripe payments: buy now, 3D Secure, billing pages, webhooks
- Sentry error monitoring (client and server)

### Phase 3: Training Company Features (Dec 2025 - Jan 2026)
- Multi-role system expansion (Training Company Admin, Student)
- Training company onboarding and management pages
- Training company billing and invoicing
- Trainer billing and rate management
- Booking flow (Airbnb-inspired UX)
- Proposal lifecycle management
- Course catalog for training companies

### Phase 4: Multi-Tenant & Advanced Features (Jan 2026 - Mar 2026)
- Multi-subdomain architecture (Cloudflare Workers proxy)
- Per-company subdomain routing and login
- Terraform infrastructure upgrades
- Customer billing consolidation
- Trainer matching and scoring algorithms
- Skills CRUD with vector auto-suggest
- Google Maps integration for trainer locations
- Resource calendar and booking for training companies
- Purchase order management with expiration dates
- Course detail redesign
- Batch delivery checklists
- Authentication cutover and security patches
- RAM savings with idle watchdog

---

## Custom Developer Tooling Built

1. **AI-powered PR review system** -- automated code review using Claude
2. **Custom ESLint rules** for architecture enforcement:
   - File size limits (902 lines max)
   - Method size limits (80 lines max)
   - Return type requirements on all methods
   - No inline type literals
   - Import cycle detection (madge)
   - Prisma schema validation (no uppercase columns)
   - JSON property primitive type linting
3. **Architecture validation framework** with dependency graph visualization
4. **Git workflow automation scripts** (push, review, merge, conflict resolution)
5. **Test generator tool** for automated test scaffolding
6. **Deployment chunking system** for tracking what gets deployed
7. **Bootstrap/seed data system** for development environments
8. **Custom Nx plugins** for build validation

---

## Key Architecture Decisions

- **Monorepo with Nx** for code sharing across services
- **Prisma ORM** with strict schema validation and migration guardrails
- **Firestore for real-time chat** (separate from Postgres for CRUD)
- **Separate prompt microservice** for AI prompt management and versioning
- **DTO pattern** throughout (dedicated DTO types for API contracts, separate from DB objects)
- **Converter pattern** for all Prisma-to-DTO transformations
- **Zod validation** for API input validation
- **Multi-subdomain architecture** for white-labeling per training company

---

## Server Controller Domains

- **Customer:** AI chat (ChatGPT streaming), booking, billing, trainer lookup/matching/scoring
- **Trainer:** Profile, calendar, revenue
- **Training Company:** Booking, resources, resource calendars, resource types, trainer booking, trainer calendar, workflow, company management
- **Admin (TamiAdmin):** User management, company approval, system configuration
- **Student:** Class registration, evaluations
- **Prompt:** Dynamic prompt management, versioning, tagging

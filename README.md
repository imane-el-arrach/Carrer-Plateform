# CareerPlatform — AI-Powered Employability Platform for Tech Students

> 🍴 This is my personal fork of a team end-of-year project built at **ENSA Safi** (Génie Informatique et Intelligence Artificielle). My individual work lives primarily on the [`imane` branch](https://github.com/imane-el-arrach/Carrer-Plateform/tree/imane); `main` holds the team's merged, final version.

## About

CareerPlatform is an intelligent platform that helps tech students:

- Analyze their **Career Gap** (their CV vs. the real job market)
- Get a personalized **employability score**
- Generate a **week-by-week learning roadmap**
- Optimize their **CV for ATS** (Applicant Tracking Systems)
- Practice with an **AI-powered mock technical interview**

### Context

Many students master technical skills but are unaware of what the market actually expects. This gap leads to rejected CVs, failed interviews, and a sense of mismatch. CareerPlatform addresses this by combining CV analysis, job-market monitoring, and actionable recommendations.

## Technical Architecture

- **Backend:** FastAPI (Python) REST API, JWT authentication, PostgreSQL + SQLAlchemy
- **ML micro-service:** 3-tier skill extraction — spaCy NER, fine-tuned BERT (F1 = 0.70), regex-based taxonomy
- **RAG:** ChromaDB + Sentence Transformers to enrich recommendations with real market data
- **LLM:** Gemini 2.5 Flash for roadmap generation and a multi-turn mock interview simulator
- **Scraper:** collects real job postings (RemoteOK, Jobicy, Adzuna)
- **Frontend:** React 19, TypeScript, TanStack Router, Tailwind CSS, shadcn/ui
- **Deployment:** Render + Supabase

## My Contribution (Imane El Arrach)

On this project I worked mainly on the **roadmap generation engine, the RAG/knowledge-base pipeline, parts of the backend, and the frontend–backend integration**:

- Set up the core application configuration, main entry point, and authentication route
- Built the job scraper integrating external job-board APIs (RemoteOK, Jobicy, Adzuna)
- Designed and implemented the **RAG module** (ChromaDB + Sentence Transformers) for semantic retrieval over real job-market data
- Connected the `/roadmap` API endpoints to the RAG pipeline
- Built the **hybrid recommendation pipeline** combining a Rule-Based Engine, RAG retrieval, and Gemini for roadmap and tip generation
- Fixed backend CORS configuration to support the frontend
- Integrated the React frontend with the backend API
- General maintenance: dependency updates, `.gitignore` configuration, merging `main` into my feature branch

Full commit history for my work is available [here](https://github.com/imane-el-arrach/Carrer-Plateform/commits?author=imane-el-arrach) and on the [`imane` branch](https://github.com/imane-el-arrach/Carrer-Plateform/tree/imane).

## Team & Credits

This was a group project — full credit to my teammates for their work on the other parts of the platform:

- [Wiame Erraoui](https://github.com/Werraoui)
- [Zineb EL ARBAOUI](https://github.com/zineb-elarbaoui)
- [Abdelhaq Lahlali](https://github.com/abdelhaq94))

Supervised by **M. Harzalla Driss**.

**Institution:** ENSA Safi — Génie Informatique et Intelligence Artificielle

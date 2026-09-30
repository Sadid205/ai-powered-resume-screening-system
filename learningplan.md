# 🎯 AI-Powered Resume Screening System - Complete Study Roadmap

> **Project Goal:** Build a production-grade AI Recruitment Platform with FastAPI, React, LangChain, RAG, Kafka, Celery, Docker, AWS, and Terraform.

---

## 📑 Table of Contents

1. [Project Overview](#-project-overview)
2. [Feature List](#-feature-list)
3. [Tech Stack](#-tech-stack)
4. [Phase-wise Study Roadmap](#-phase-wise-study-roadmap)
5. [Feature-wise Tech Mapping](#-feature-wise-tech-mapping)
6. [Study Priority Order](#-study-priority-order)
7. [Recommended Resources](#-recommended-resources)
8. [Project Structure](#-project-structure)
9. [Pro Tips](#-pro-tips)
10. [Milestones & Timeline](#-milestones--timeline)

---

## 🎯 Project Overview

এটা একটা **AI-Powered Recruitment Platform** যেখানে recruiter:
- Login করে dashboard দেখবে
- Resume upload করবে (PDF/DOCX)
- AI দিয়ে candidate summary generate করবে
- Job description এর সাথে resume match করবে
- Candidate rank করবে
- Analytics দেখবে

**Final Goal:** Production-grade, scalable, deployed on AWS with CI/CD.

---

## ✨ Feature List

| # | Feature | Description |
|---|---------|-------------|
| 1 | Recruiter Login | JWT-based authentication |
| 2 | Dashboard | Overview of candidates, jobs, stats |
| 3 | Upload Resume | PDF/DOCX upload + parsing |
| 4 | Candidate Search | Semantic + keyword search |
| 5 | AI Candidate Summary | LLM-generated summary |
| 6 | Candidate Ranking | Score-based ranking |
| 7 | Job Management | CRUD for job posts |
| 8 | Resume Matching | RAG-based matching |
| 9 | Analytics Dashboard | Charts, stats, insights |

---

## 🛠️ Tech Stack

### Backend
- **FastAPI** + REST APIs
- **PostgreSQL** + **SQLAlchemy 2.0** + **Alembic**
- **Redis** (cache, broker)
- **Celery** (background jobs)
- **Kafka** (event streaming)
- **pgvector** / **ChromaDB** (vector store)

### AI/ML
- **LangChain** + **LangSmith**
- **RAG** pipeline
- **OpenAI / Anthropic / Llama** (LLM)
- **sentence-transformers** (embeddings)
- **Pandas + NumPy + Matplotlib**
- **PyTorch** (optional)

### Frontend
- **React** + **TypeScript**
- **React Router**
- **Tailwind CSS** + **shadcn/ui**
- **Axios** + **TanStack Query**
- **React Hook Form** + **Zod**

### DevOps
- **Docker** + **docker-compose**
- **AWS** (EC2, S3, RDS, ElastiCache, ECR, ECS)
- **Terraform**
- **GitHub Actions** (CI/CD)

### Testing
- **Pytest** + **pytest-asyncio**
- **React Testing Library**

---

## 📚 Phase-wise Study Roadmap

---

### 🔹 Phase 1: Foundation (Week 1-2)

#### 1. Python Advanced + Async Programming
- `asyncio`, `await`, `async def`, event loop
- `httpx` (async HTTP), `aiofiles`
- **Parallelism vs Concurrency**
  - `threading` (I/O bound)
  - `multiprocessing` (CPU bound)
  - `concurrent.futures`, `asyncio.gather`
- **কেন লাগবে?** Resume parsing, AI calls, DB queries parallel এ চালাতে

#### 2. FastAPI Deep Dive
- Routing, Dependency Injection, Pydantic v2
- Background Tasks, Middleware, CORS
- OAuth2 + JWT authentication
- WebSockets (real-time analytics)
- File upload (`UploadFile`, streaming)

#### 3. Database Layer
- **PostgreSQL**: indexes, joins, JSONB, full-text search
- **SQLAlchemy 2.0**: ORM, async engine, relationships
- **Alembic**: migrations
- **Redis**: caching, session, rate-limiting
- **pgvector**: vector similarity search

---

### 🔹 Phase 2: Frontend (Week 3-4)

#### 4. React Fundamentals + TypeScript
- Components, hooks (`useState`, `useEffect`, `useMemo`)
- TypeScript: interfaces, generics, utility types
- Custom hooks

#### 5. React Router
- Nested routes
- Protected routes (auth guard)
- Lazy loading

#### 6. Tailwind CSS + shadcn/ui
- Utility classes, responsive design
- shadcn components: Table, Dialog, Form, Card, Chart

#### 7. Axios + TanStack Query
- Axios interceptors (JWT attach, error handling)
- TanStack Query: `useQuery`, `useMutation`, caching, invalidation, optimistic updates

#### 8. React Hook Form + Zod
- Form validation schema
- Zod + TypeScript type inference

---

### 🔹 Phase 3: AI/ML Core (Week 5-7) ⭐

#### 9. CV Parsing (PDF/DOCX)
- `pypdf`, `pdfplumber`, `python-docx`
- Regex, NLP for extracting:
  - Name, email, phone
  - Skills, experience, education
- **spaCy** বা **LayoutLM** (advanced)

#### 10. Generative AI + LLM APIs
- OpenAI / Anthropic / open-source (Llama)
- Prompt engineering
- Structured output (function calling, JSON mode)

#### 11. LangChain
- Chains, PromptTemplates, OutputParsers
- LCEL (LangChain Expression Language)
- Agents, Tools
- Memory management

#### 12. RAG (Retrieval Augmented Generation)
- Pipeline: Load → Chunk → Embed → Store → Retrieve → LLM
- Embeddings: `text-embedding-3-small`, `sentence-transformers`
- Chunking strategies (semantic, recursive)

#### 13. Vector Database
- **ChromaDB** (easy start) বা **pgvector** (Postgres integrated)
- Similarity search: cosine, L2, inner product
- Metadata filtering

#### 14. LangSmith
- Tracing, debugging LLM calls
- Evaluation, datasets
- Production monitoring

#### 15. Candidate Ranking
- Embedding similarity score
- Re-ranking (cross-encoder)
- Weighted scoring (skills + experience + education)

---

### 🔹 Phase 4: Background Jobs & Messaging (Week 8-9)

#### 16. Celery + Redis
- Task queues, workers, beat scheduler
- **কেন?** Resume parsing (slow), bulk email, analytics computation

#### 17. Kafka
- Producer/Consumer, topics, partitions
- **কেন?** Event-driven pipeline: upload → parse → embed → rank
- `aiokafka` for async

#### 18. Async Programming Recap
- Celery + async FastAPI integration
- Task chaining, groups, chords

---

### 🔹 Phase 5: Data & Analytics (Week 10)

#### 19. Pandas + NumPy
- DataFrame operations, groupby, merge
- Statistical analysis

#### 20. Matplotlib
- Charts for Analytics Dashboard
- (Frontend এ Recharts / shadcn charts)

#### 21. PyTorch (Optional)
- Custom embedding model fine-tuning
- Classification (resume category)
- BERT fine-tuning for NER

---

### 🔹 Phase 6: Testing (Week 11)

#### 22. Pytest
- Fixtures, parametrize, mocking (`pytest-mock`)
- Async tests (`pytest-asyncio`)
- Coverage

#### 23. React Testing Library
- `render`, `screen`, `userEvent`
- Mocking API (MSW)
- Vitest / Jest

---

### 🔹 Phase 7: DevOps & Cloud (Week 12-13)

#### 24. Docker
- Dockerfile (multi-stage build)
- docker-compose (FastAPI + Postgres + Redis + Kafka + Celery)
- Volumes, networks

#### 25. AWS
- EC2, S3 (resume storage), RDS (Postgres), ElastiCache (Redis)
- ECR (Docker images), ECS/EKS (deploy)
- Lambda (optional)
- CloudWatch (logs)

#### 26. Terraform
- IaC basics: providers, resources, variables, state
- AWS resource provisioning
- Modules

#### 27. CI/CD (GitHub Actions)
- Workflows: lint → test → build → push → deploy
- Secrets management
- Matrix builds

---

## 🗺️ Feature-wise Tech Mapping

| Feature | Required Tech |
|---|---|
| Recruiter Login | FastAPI + JWT + PostgreSQL + RHF + Zod |
| Dashboard | React + TanStack Query + shadcn/ui |
| Upload Resume | FastAPI `UploadFile` + S3 + Celery + Kafka + pdfplumber |
| Candidate Search | pgvector/ChromaDB + RAG + Embeddings |
| AI Candidate Summary | LangChain + LLM + LangSmith |
| Candidate Ranking | Embeddings + Re-ranker + NumPy |
| Job Management | CRUD API + SQLAlchemy + React forms |
| Resume Matching | RAG + Vector similarity + LangChain |
| Analytics Dashboard | Pandas + Matplotlib (backend) + Recharts (frontend) |

---

## 🎓 Study Priority Order

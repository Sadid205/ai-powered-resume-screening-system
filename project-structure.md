## 📁 Project Structure
ai-recruitment-platform/
├── backend/
│ ├── app/
│ │ ├── api/
│ │ │ ├── v1/
│ │ │ │ ├── auth.py
│ │ │ │ ├── candidates.py
│ │ │ │ ├── jobs.py
│ │ │ │ ├── resumes.py
│ │ │ │ └── analytics.py
│ │ ├── core/
│ │ │ ├── config.py
│ │ │ ├── security.py
│ │ │ └── celery_app.py
│ │ ├── db/
│ │ │ ├── base.py
│ │ │ ├── session.py
│ │ │ └── models/
│ │ ├── schemas/
│ │ ├── services/
│ │ │ ├── resume_parser.py
│ │ │ ├── ai_summary.py
│ │ │ ├── matching.py
│ │ │ └── ranking.py
│ │ ├── ai/
│ │ │ ├── llm.py
│ │ │ ├── embeddings.py
│ │ │ ├── rag_pipeline.py
│ │ │ └── vector_store.py
│ │ ├── workers/
│ │ │ └── tasks.py
│ │ └── main.py
│ ├── alembic/
│ ├── tests/
│ ├── Dockerfile
│ └── requirements.txt
│
├── frontend/
│ ├── src/
│ │ ├── components/
│ │ │ └── ui/ # shadcn components
│ │ ├── pages/
│ │ │ ├── Login.tsx
│ │ │ ├── Dashboard.tsx
│ │ │ ├── Candidates.tsx
│ │ │ ├── Jobs.tsx
│ │ │ └── Analytics.tsx
│ │ ├── hooks/
│ │ ├── lib/
│ │ │ ├── axios.ts
│ │ │ └── queryClient.ts
│ │ ├── schemas/ # Zod schemas
│ │ ├── routes/
│ │ └── App.tsx
│ ├── Dockerfile
│ └── package.json
│
├── infra/
│ ├── terraform/
│ │ ├── main.tf
│ │ ├── variables.tf
│ │ └── modules/
│ └── docker-compose.yml
│
├── .github/
│ └── workflows/
│ ├── backend-ci.yml
│ ├── frontend-ci.yml
│ └── deploy.yml
│
└── README.md
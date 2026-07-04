---
layout: default
title: Anagha Ramadas Mulloth
---

## 👋 About Me

I'm **Anagha Ramadas Mulloth**, an AI Enthusiast and Full Stack Developer based in Dubai, UAE. I hold an **MSc in Artificial Intelligence and Machine Learning** from the University of Birmingham, UK (2024) and a **B.Tech in Computer Science and Engineering**.

I'm passionate about building intelligent systems, exploring LLMs, AI Agents, and creating meaningful applications with cutting-edge technology.

📍 Dubai, UAE &nbsp;|&nbsp; 🌐 [anaghamulloth.com](https://anaghamulloth.com) &nbsp;|&nbsp; 💼 [LinkedIn](https://linkedin.com/in/anagharamadas) &nbsp;|&nbsp; 🐙 [GitHub](https://github.com/anagharamadas)

---

## 🛠️ Skills

| Category | Technologies |
|----------|-------------|
| **AI / ML** | Python, TensorFlow, Keras, Scikit-learn, PyTorch |
| **LLMs & Agents** | LangChain, LangGraph, LlamaIndex, Generative AI |
| **Data** | Pandas, NumPy, Matplotlib |
| **Backend** | FastAPI, Spring Boot, Java |
| **Frontend** | Next.js, React, TypeScript, Tailwind CSS, HTML, CSS, JavaScript |
| **Data & Infra** | Supabase (PostgreSQL), SQLAlchemy, Row-Level Security |
| **Deployment & Ops** | Render, Vercel, Sentry, MLflow, Apache Airflow, Git, Jupyter |

---

## 🚀 Projects

### 📚 Trial Reads

**Full-stack AI reading companion — FastAPI · Next.js · Supabase · LangGraph · LlamaIndex**

A ground-up rebuild of Trial Reads into a production-grade, full-stack AI application deployed as a monorepo. A **FastAPI** backend (deployed on **Render**) exposes a modular REST API and orchestrates the LLM features, while a **Next.js 14 / TypeScript / React** frontend (deployed on **Vercel**, styled with Tailwind CSS) delivers a responsive library manager, shelves view, and conversational chat. Authentication and data are handled by **Supabase** — users sign in with Supabase Auth, and the backend verifies **Supabase JWTs** to scope every request to the signed-in user. There is **no vector store / ChromaDB**; retrieval is done with governed SQL over Postgres.

**What it does**

- **Book summarization** — chapter-by-chapter summaries generated with OpenAI \`gpt-4o-mini\`.
- **Library management** — full CRUD over a personal collection, with automatic cover art via the Google Books and Apple Books APIs.
- **Natural-language Q&A over your library** — questions are translated to SQL using **LlamaIndex's NLSQLTableQueryEngine** and executed against Supabase Postgres.
- **Smart recommendations** — similar-title suggestions with purchase links.
- **AI shelf curation** — a **LangGraph** agent builds an ordered, books-only reading list toward a stated goal (e.g. "learn to start a consulting firm").
- **Conversational chat** — a unified ReAct-style interface tying summaries, recommendations, and library Q&A together.

**Engineering highlights**

- **Defense-in-depth multi-user isolation** for the text-to-SQL feature: the LLM only ever sees a self-filtering \`my_library\` view, queries run on a non-pooled engine that stamps each connection with the caller's JWT claims and \`SET ROLE authenticated\` so **Postgres Row-Level Security** physically restricts every statement to the user's own rows, and \`NullPool\` guarantees no connection state is reused across users.
- **LLM orchestration** with LangChain / LangGraph and LlamaIndex; JWT auth verified via JWKS.
- **Production hardening**: per-user daily rate limiting on AI endpoints, CORS allow-listing for the Vercel domain, and Sentry error monitoring (backend and frontend).

<div class="project-shots">
  <img src="{{ '/assets/images/trialreads/library.png' | relative_url }}" alt="TrialReads library view with reading-status badges" />
  <img src="{{ '/assets/images/trialreads/book-detail.png' | relative_url }}" alt="TrialReads book detail with summarise and recommendations" />
  <img src="{{ '/assets/images/trialreads/chat.png' | relative_url }}" alt="TrialReads chat answering a natural-language library question" />
</div>

[View on GitHub →](https://github.com/anagharamadas/trialreads){: .gh-link}

### 🔬 Fluorescence Image Microscopy

**Predicting missing channels using fluorescence microscopy images**

Used deep learning to predict missing fluorescence channels in microscopy images.

[View on GitHub →](https://github.com/anagharamadas){: .gh-link}

### 🌿 Weed Classification using Deep Learning

**Deep learning model for weed species classification**

Applied CNN architectures to classify weed species from field images with high accuracy.

[View on GitHub →](https://github.com/anagharamadas){: .gh-link}

### 💬 PDF Querying Bot

**Intelligent chatbot to query PDF documents using LangChain and LLMs**

Built natural language querying over custom PDF documents using LangChain.

[View on GitHub →](https://github.com/anagharamadas){: .gh-link}

### 🤖 Chatbot — LangChain & LLMs

**Personal project to learn LangChain and LLMs**

An AI-powered chatbot exploring prompt engineering, chains, and memory management.

[View on GitHub →](https://github.com/anagharamadas){: .gh-link}

### 📊 LangGraph Learning Projects

**Experiments with LangGraph for agentic workflows**

Explored stateful, multi-actor agentic workflows using LangGraph.

[View on GitHub →](https://github.com/anagharamadas){: .gh-link}

---

## 🎓 Education

**MSc Artificial Intelligence and Machine Learning**
University of Birmingham, United Kingdom — 2024

**B.Tech Computer Science and Engineering**
India

---

## 📫 Get in Touch

Feel free to reach out for collaborations, opportunities, or just to chat about AI and tech!

🌐 [anaghamulloth.com](https://anaghamulloth.com)
💼 [LinkedIn](https://linkedin.com/in/anagharamadas)
🐙 [GitHub](https://github.com/anagharamadas)

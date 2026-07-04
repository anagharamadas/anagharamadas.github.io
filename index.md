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
| **Deep Learning** | GANs, Pix2Pix, CNNs, Vision Transformers, Transfer Learning, Image-to-Image Translation |
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

**Generative AI for medical imaging — Pix2Pix conditional GAN (TensorFlow/Keras)**

MSc dissertation project applying **generative AI to fluorescence microscopy** to tackle the scarcity of labelled medical imaging data. Using the **Berkeley Single-Cell Computational Microscopy (BSCCM)** dataset, a **Pix2Pix conditional GAN** (built in **TensorFlow/Keras**) performs image-to-image translation to synthesise realistic multi-channel fluorescence images — reducing the need for costly, confidentiality-restricted lab captures.

**Two input strategies were designed and compared**

- **Brightfield → fluorescence** — predict all six fluorescence channels directly from a single brightfield image.
- **Masked-channel reconstruction** — randomly mask five of the six channels, and train the model to reconstruct the full six-channel fluorescence image (a novel input formulation).

**Engineering highlights**

- **U-Net-style generator** and a **PatchGAN discriminator**, trained with a combined **adversarial (BCE) + L1** objective and the Adam optimizer.
- **Quantitative evaluation** using **SSIM** and **PSNR** against ground-truth fluorescence, plus qualitative visual comparison.
- Validated the reliability of a newly published white-blood-cell microscopy dataset for supervised learning, demonstrating that GAN-based augmentation can expand medical datasets without compromising patient confidentiality.

[View on GitHub →](https://github.com/anagharamadas/Fluorescence_Image_Microscopy){: .gh-link}

### 🌿 Weed Classification using Deep Learning

**Vision Transformer vs CNN benchmark for precision agriculture (TensorFlow/Keras)**

A comparative deep-learning study on classifying weeds from crop imagery to enable targeted herbicide spraying — cutting chemical waste and environmental impact. Trained and evaluated on a dataset of **17,509 labelled images of Australian weed species** (DeepWeeds), distinguishing **grass vs broadleaf** weeds, the project benchmarks a **Vision Transformer (ViT)** against four state-of-the-art CNN backbones using **transfer learning** in **TensorFlow/Keras**.

**Models compared and results**

- **Vision Transformer (ViT)** — best performer at **96.41%** accuracy.
- **ResNet-50** — 95.70%.
- **Xception** — 95.04%.
- **Inception V3** — 94.70%.
- **Inception-ResNet V2** — 94.15%.

**Engineering highlights**

- **Transfer learning** from ImageNet-pretrained backbones with fine-tuning and data augmentation, wrapped in a modular training/evaluation pipeline.
- Explored **attention-based transformers as an alternative to CNNs**, showing ViT can outperform established convolutional architectures on this task.
- Results and analysis documented in an accompanying technical report.

[View on GitHub →](https://github.com/anagharamadas/Weed-Classification-using-Deep-Learning){: .gh-link}

---

## ✍️ Writing

I write about AI, machine learning, and LLMs on Medium — sharing tutorials, project deep-dives, and notes on the tools and ideas I'm exploring.

[Read my blog on Medium →](https://medium.com/@anagharamdas2000){: .gh-link}

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
✍️ [Medium](https://medium.com/@anagharamdas2000)

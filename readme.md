# Samarth MN

**AI Engineer | LLM Engineer | Senior Full-Stack Engineer**

Generative AI, RAG, AI Agents, LLM Evaluation, Python, TypeScript, React, Next.js, Rust

[Portfolio](https://www.samarthmn.com) | [LinkedIn](https://www.linkedin.com/in/samarthmn/) | [GitHub](https://github.com/samarthmn) | [Blogs](https://www.samarthmn.com/blogs)

## Summary

I am an AI engineer and LLM engineer with a product engineering background. Before working on LLM applications I worked as a senior frontend engineer, product engineer, full-stack engineer, React Native engineer, founder, and CTO, so most of my work has been about taking an idea and turning it into a product that someone can actually use. Now I do the same thing with generative AI: RAG pipelines, AI agents, tool calling, model evaluation, multimodal apps, and local LLMs.

I think the model is only one part of an AI product. For example, if the retrieval brings back the wrong context then even a very good model gives a wrong answer, and if the interface is slow or confusing then the user does not trust the answer even when it is right. So I work on retrieval quality, evals, latency, error handling, and the UI together, because all of these decide if an AI feature is useful or not.

**Looking for:** Forward Deployed Engineer (FDE), Forward Deployed AI Engineer, Applied AI Engineer, AI Engineer, LLM Engineer, Generative AI Engineer, Solutions Engineer, and Senior Full-Stack Engineer roles, where I can work directly with customers and take an AI use case from a rough requirement to a deployed product they actually use.

## Skills

**Generative AI and LLM Engineering:** Large Language Models (LLMs), Generative AI, Retrieval-Augmented Generation (RAG), AI Agents, Multi-Agent Systems, Tool Calling, Function Calling, Prompt Engineering, Structured Outputs, LLM Evaluation, Evals, LLM-as-a-Judge, Fine-Tuning, QLoRA, Multimodal AI, Speech-to-Text, Text-to-Speech, Local LLMs, Open-Source Models

**RAG and Retrieval:** Embeddings, Vector Databases, Vector Search, Chroma, Chunking, Query Rewriting, Reranking, Cross-Encoders, Small-to-Big Retrieval, Document Enrichment, Retrieval Evaluation

**AI Frameworks and APIs:** OpenAI API, Anthropic Claude, OpenRouter, Hugging Face, Ollama, llama.cpp, Whisper, LangChain, LlamaIndex, Gradio

**Languages:** Python, TypeScript, JavaScript, Rust, SQL, HTML, CSS, Solidity

**Frontend:** React, Next.js, React Native, Expo, Tailwind CSS, Radix UI, Chat Interfaces, Responsive UI, Frontend Architecture

**Backend and Data:** Node.js, Express, FastAPI, Pydantic, GraphQL, Hasura, Supabase, PostgreSQL, REST APIs, Stripe, Jupyter Notebook, Data Analysis

**Systems and Infrastructure:** WebAssembly (WASM), Docker, Vercel, Cloudflare R2, Amazon S3 APIs, GitHub Actions, CI/CD, npm Package Publishing, Sentry

**Testing and Quality:** Playwright, End-to-End Testing, Unit Testing, ESLint, TypeScript Migration

**Web3:** Ethereum, Solidity, Web3.js, Smart Contracts

## Experience

**Founder and CTO, DocKosha** (secure document sharing and virtual data room SaaS)

- Founded DocKosha and built it end to end: product, architecture, frontend, backend, billing, deployment, and the document engine
- Built the web app with Next.js, TypeScript, Supabase, PostgreSQL, Cloudflare R2, and Stripe, with Playwright end-to-end tests and Sentry monitoring
- Built DocYantra, a Rust and WebAssembly document engine that replaced an earlier NestJS and Gotenberg HTTP service
- Released both DocKosha and DocYantra as open source under the AGPL-3.0 license

**Senior Frontend Engineer, Product Engineer, Full-Stack Engineer, React Native Engineer**

- Led frontend architecture and TypeScript adoption for production web applications
- Migrated production JavaScript and React Native codebases to TypeScript so the code was easier to change
- Built React Native mobile apps for iOS and Android from scratch
- Built healthcare, education, SaaS, Web3, and AI-adjacent products across React, Next.js, Node.js, GraphQL, and PostgreSQL

**AI Engineer, independent LLM projects**

- Built RAG benchmarks, multimodal AI apps, synthetic data tools, and full-stack AI chat apps with Python, Ollama, Hugging Face, OpenAI, and OpenRouter
- Currently building with AI agents, fine-tuning, local models, and evals

## Featured Projects

### [DocKosha](https://github.com/samarthmn/doc-kosha)

Secure document sharing and virtual data room (VDR) SaaS, powered by DocYantra, its own Rust and WebAssembly document engine.

DocKosha is the product I founded and built. People share sensitive documents like pitch decks, contracts, and due diligence files, and they need to control who opens them and see what happened after sharing, so every link in DocKosha can sit behind a password, an email OTP, an allowlist, or an NDA, and the owner can watch the viewer analytics and audit trail. DocYantra is the engine underneath it. The earlier version was an HTTP service built on NestJS and Gotenberg, and I rewrote it in Rust and compiled it to WebAssembly, so now the same engine runs inside the app as an npm package and does PDF processing, redaction, watermarking, and Office to PDF conversion without LibreOffice or Chromium.

- **Product:** password and email OTP gates, allowlists and blocklists, NDA gates, link expiry and revocation, server-side watermarking, redaction, document versioning, viewer analytics, comments, Q&A, and audit trails
- **DocYantra:** PDF merge, split, watermark, and redaction in pure Rust; DOCX, PPTX, and XLSX to PDF conversion; redaction that fails closed if the engine cannot prove the result is safe
- **DocYantra packaging:** four npm packages released in lockstep through GitHub Actions and GitHub Packages, with a TypeScript adapter for DocKosha

[Website](https://www.dockosha.com) | [DocYantra engine](https://github.com/samarthmn/doc-yantra)

**Tech:** Next.js, TypeScript, React, Supabase, PostgreSQL, Rust, WebAssembly, Cloudflare R2, Stripe, Playwright, Sentry, Vercel, GitHub Actions

### [RAGnosis](https://github.com/samarthmn/RAGnosis)

Applied research project benchmarking Retrieval-Augmented Generation (RAG) over a synthetic healthcare clinic database.

The question I wanted to answer was simple: which retrieval techniques make a healthcare-style database easier for an LLM to answer from? So I started with a plain vector search baseline and kept adding one technique at a time, query rewriting, reranking, document enrichment, Small-to-Big retrieval, and aggregate rollup documents, and then scored every run on retrieval quality and answer quality. Most of it ran on local resources, so I think of the results as a practical study on limited hardware rather than a search over every possible model.

- Compared a baseline RAG pipeline against an advanced pipeline with dual retrieval, reranking, and parent document expansion
- Ran reranker ablations with jina-reranker-v3 and BAAI bge-reranker-v2-m3
- Tracked every experiment with its config, metadata, and eval scores, and published an interactive benchmark report with a sortable leaderboard

[Benchmark](https://ragnosis.samarthmn.com) | [Research doc](https://ragnosis.samarthmn.com/#paper)

**Tech:** Python, RAG, Chroma, Ollama, Hugging Face, Embeddings, Vector Search, Reranking, LLM Evaluation, OpenAI API

### [Zyra](https://github.com/samarthmn/zyra)

Multimodal AI app for plant identification and plant care questions.

You can upload a photo, type a question, or just speak, and Zyra answers back in text and voice. The plant reasoning runs on a local vision-language model, and when the model finds a botanical match it calls the Trefle API to check the plant data, because a model can sound confident about a plant and still be wrong.

- Runs quantized Gemma 4 GGUF models locally through llama.cpp, with a choice between the 12B model for better answers and the E4B model for faster responses
- Uses Whisper Large v3 Turbo for speech-to-text and Kokoro for text-to-speech
- Uses tool calling with the Trefle API for verified plant data

**Tech:** Python, Gradio, llama.cpp, Gemma, Whisper, Kokoro, Multimodal AI, Tool Calling, Local LLMs

### [Pretendo](https://github.com/samarthmn/pretendo)

Full-stack AI chat app that replies with a chosen character, mood, and model.

Pretendo is small on purpose, but it has the parts a real product needs: an API boundary, model validation, persistence, tests, deployment, and a UI that feels finished. For AI apps I think this product layer matters even more, because a bad interface can make a good model feel useless.

- Built a monorepo with a Next.js client and a Python FastAPI service, deployed together on Vercel
- Integrated OpenRouter with validated model selection, and the reply always shows the exact model used
- Added local-first chat history with browser SQLite, plus CORS allowlists, request limits, provider timeouts, and focused tests

[Live demo](https://pretendo.samarthmn.com)

**Tech:** Next.js, React, TypeScript, Tailwind CSS, FastAPI, Python, OpenRouter, SQLite, Vercel

### [DataAlchemy](https://github.com/samarthmn/data-alchemy)

Synthetic dataset generator powered by a local LLM.

You describe the dataset you want and pick the complexity, format, and row count. Then a local Ollama model designs the related tables, and Faker fills in the actual rows, so names, addresses, and dates stay realistic instead of the model making up every value.

- Generates related tables and exports them as CSV, JSON, and Markdown in one ZIP download
- Uses Ollama through its OpenAI-compatible API

**Tech:** Python, Gradio, Ollama, Faker, Synthetic Data, Prompt Engineering, Jupyter Notebook

## Certifications

- AI Engineer Core Track: LLM Engineering, RAG, QLoRA, and AI Agents

The course was project-heavy and that suits me, because I learn best by building the thing, breaking it, fixing it, and then turning it into something someone can try.

## What I Am Building Next

I am working through LLM projects where the outcome is something a person can use:

- A multimodal airline support agent with a UI, tool use, and function calling
- A RAG knowledge worker for company-specific questions
- A meeting minutes tool that turns audio into summaries and action items
- A price prediction system that compares frontier models with fine-tuned open-source models
- A multi-agent deal spotting system that evaluates options and notifies the user
- A Python to C++ code optimizer

## How I Work

- I like clear product behavior more than vague scope
- I ship small working releases instead of long speculative builds
- I care about frontend quality, because users judge software through the interface
- I use TypeScript to make product code easier to change
- I am comfortable moving between product conversations and implementation details

## Links

- Portfolio: [samarthmn.com](https://www.samarthmn.com)
- Blogs: [samarthmn.com/blogs](https://www.samarthmn.com/blogs)
- LinkedIn: [linkedin.com/in/samarthmn](https://www.linkedin.com/in/samarthmn/)
- X: [x.com/samarth_mn](https://x.com/samarth_mn)
- Medium: [samarthmn.medium.com](https://samarthmn.medium.com/)

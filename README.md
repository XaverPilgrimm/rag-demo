# RAG Pipeline Demo

A minimal Retrieval-Augmented Generation (RAG) pipeline that extracts and queries knowledge from a research paper using Python, OpenAI, ChromaDB, and Docling.

## Paper

[DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning](https://arxiv.org/abs/2501.12948) — Guo et al., 2025

## Stack

- **Docling** — PDF to Markdown extraction
- **OpenAI API** — Embeddings + LLM (GPT-4o-mini)
- **ChromaDB** — Vector store
- **LangChain Text Splitters** — Chunking

## Workflow

PDF → Markdown (Docling) → Chunks → Embeddings (OpenAI) → Vector Store (ChromaDB) → LLM Query

## Setup

1. Clone the repo
2. Install dependencies: `pip install -r requirements.txt`
3. Copy `.env.example` to `.env` and add your OpenAI API key
4. Start Docling: see `docker-compose.yml` in the repo
5. Run `notebook.ipynb` top to bottom

## Notes

- `data/raw/` is gitignored — the PDF is downloaded automatically by the notebook
- `data/processed/deepseek_r1.md` is included for convenience so the notebook runs without Docling

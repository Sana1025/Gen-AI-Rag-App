
# GenAI RAG App (Docs + Code)

GenAI Retrieval-Augmented Generation (RAG) application that supports both **documents** and **source code** for semantic search, understanding, and analysis.



## Features

### Document RAG
- Summarization
- Bullet point extraction
- Keyword extraction
- Semantic contextual search

### Code RAG
- Explain what code does
- Debug code
- Refactor code
- Fix code
- Add comments
- Complexity analysis

### Full-Stack Integration
- FastAPI backend (RAG + Vector DB)
- Streamlit frontend (UI)
- FAISS vector store (retrieval)
- HuggingFace LLM (generation)

---

## Tech Stack

| Layer | Tools |
|-------|-------|
| Frontend | Streamlit |
| Backend | FastAPI |
| Embeddings | SentenceTransformers (HF) |
| Vector Store | FAISS |
| LLM | FLAN-T5 / Code LLM |
| Deployment | Local / HF Spaces |
| Language | Python |

---

## Project Structure

```

.
├── backend/
│   ├── main.py
│   ├── rag_pipeline.py
│   ├── vector_store.py
│   ├── llm_loader.py
│   ├── doc_loader.py
│   └── code_loader.py
├── app.py             # Streamlit UI
├── requirements.txt
└── README.md

````

---

## How It Works

1. User uploads PDF/TXT or `.py` source code
2. Text/code is chunked + embedded
3. Embeddings stored in FAISS vector store
4. Query retrieves top matching chunks
5. LLM generates final answer based on context

---

## Supported Modes

| Domain | Modes |
|-------|-------|
| Document | summarize, keywords, bullet-points |
| Code | explain, debug, fix, refactor, add-comments, complexity |

---

## Run Locally

Clone the repo:

```bash
git clone https://github.com/Sana1025/Gen-AI-Rag-App.git
cd <repo>
````

Install requirements:

```bash
pip install -r requirements.txt
```

Start backend:

```bash
uvicorn backend.main:app --reload
```

Start UI:

```bash
streamlit run app.py
```

---


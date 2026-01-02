# Medical-RAG-Assistant

This repository contains my **M.Tech (CSE) Second Semester Seminar Project**:  
a **Medical Report Assistant** built using **Retrieval-Augmented Generation (RAG)**.

The system allows users to upload medical documents (PDF/TXT) and ask questions that
are answered using retrieved document context along with a large language model.

---

## Overview

Medical documents often contain large amounts of unstructured text. This project
demonstrates how **RAG (Retrieval-Augmented Generation)** can be used to ground
LLM responses in domain-specific documents, improving reliability and relevance.

---

## Features

- Streamlit-based interactive user interface  
- Upload and process medical PDF and TXT files  
- Semantic document retrieval using vector embeddings  
- Context-aware question answering  
- Fallback to general medical knowledge when no relevant context is found  

---

## Architecture

- **Frontend:** Streamlit  
- **LLM:** LLaMA 3 (via Ollama)  
- **Embeddings:** mxbai-embed-large  
- **Vector Database:** ChromaDB  
- **Framework:** LangChain  

---

## Project Structure

```

Medical-RAG-Assistant/
│
├── medical_app.py
├── rag_engine.py
├── requirements.txt
├── README.md
│
├── medical_docs/          # Uploaded documents (ignored in Git)
└── medical_chroma_db/     # Vector database (auto-generated, ignored in Git)

```

yaml
Copy code

---

## How to Run

### Step 1: Install Ollama
Download and install Ollama from:  
https://ollama.com

Pull the required models:
```bash
ollama pull llama3.2
ollama pull mxbai-embed-large

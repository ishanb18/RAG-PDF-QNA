# 📘 RAG-PDF-QnA — Retrieval-Augmented Generation for Intelligent PDF Question Answering

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline that enables users to upload PDF documents and interactively ask context-aware questions.  
The system retrieves relevant sections from the document using **vector embeddings** and generates accurate, human-like answers using **LLMs (Large Language Models)**.

---

## 🚀 Features

- 📄 Upload any PDF and ask natural-language questions.  
- 🧠 Combines **retrieval-based search** with **generative AI** for precise answers.  
- 🔍 Uses **FAISS** vector database for semantic search.  
- 🧩 Built with **LangChain**, **OpenAI embeddings**, and **FastAPI** for modular, real-time interaction.  
- 💬 Supports both CLI and web API usage.  

---

## 🏗️ Tech Stack & Architecture

| Layer | Technology | Purpose |
|-------|-------------|----------|
| **Frontend / Interface** | Streamlit or FastAPI UI | File upload, question input |
| **Backend Framework** | FastAPI | Manages routes, queries, and response handling |
| **Document Processing** | PyPDF2 / LangChain | Extracts and chunks text from PDFs |
| **Vector Storage** | FAISS | Stores document embeddings for semantic retrieval |
| **Embeddings Model** | OpenAI `text-embedding-ada-002` | Converts document chunks into dense vectors |
| **LLM for Generation** | GPT-3.5 / GPT-4 (via OpenAI API) | Generates context-based answers |
| **Pipeline Control** | LangChain | Orchestrates retrieval + generation workflow |

---

## 🔄 Workflow Overview

```text
📁 PDF Upload
   ↓
📄 Text Extraction → Chunking → Embedding Generation
   ↓
🧮 Embeddings stored in FAISS Vector DB
   ↓
❓ User Question
   ↓
🔍 Retrieve top relevant chunks (semantic search)
   ↓
💬 Combine retrieved context + user query
   ↓
🤖 Generate final answer using OpenAI LLM
   ↓
📤 Return answer to user

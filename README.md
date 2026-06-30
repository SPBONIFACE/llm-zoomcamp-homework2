# LLM Zoomcamp - Homework 2: Vector Search 🔍

This repository contains my solution for Homework 2 of the [LLM Zoomcamp](https://github.com/DataTalksClub/llm-zoomcamp). 

In this module, we explore the fundamentals of vector search, embedding generation, and hybrid search (combining keyword and vector search) without relying on heavy frameworks. We use the lightweight ONNX runtime to generate embeddings and `minsearch` for indexing and retrieval.

## 🛠️ Tech Stack & Tools
* **Language:** Python 3
* **Package Manager:** [uv](https://github.com/astral-sh/uv) (Extremely fast Python package installer and resolver)
* **Embeddings:** ONNX Runtime (`all-MiniLM-L6-v2`)
* **Vector & Text Search:** `minsearch`

---

## 🚀 How to Run this Project

Follow these steps to perfectly recreate the environment and run the Jupyter notebook on your own machine.

### 1. Initialize the Project
First, create a new directory and initialize it with `uv`:
```bash
mkdir llm-zoomcamp-hw2
cd llm-zoomcamp-hw2
uv init --no-workspace

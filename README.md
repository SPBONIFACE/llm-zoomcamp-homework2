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

2. Install Dependencies
Install the required packages for the vector search pipeline and the development tools needed to run the notebook:

bash


# Core dependencies
uv add onnxruntime tokenizers numpy tqdm minsearch gitsource
# Development dependencies (for downloading models and running notebooks)
uv add --dev huggingface-hub jupyter
3. Download the Embedder Scripts & Model
We use a custom, lightweight ONNX embedder rather than the heavy PyTorch sentence-transformers library. Download the helper scripts from the main course repository:

bash


PREFIX="https://raw.githubusercontent.com/DataTalksClub/llm-zoomcamp/main/02-vector-search/embed"
wget $PREFIX/download.py
wget $PREFIX/embedder.py
Next, run the download script to fetch the Xenova/all-MiniLM-L6-v2 ONNX model:

bash


uv run python download.py
4. Run the Jupyter Notebook
With the environment fully configured and the model downloaded, launch Jupyter to view and run the homework notebook:

bash


uv run jupyter lab
Open llmzoomcamp-hw2.ipynb to see the complete implementation of vector search, cosine similarity scoring, and Reciprocal Rank Fusion (RRF).

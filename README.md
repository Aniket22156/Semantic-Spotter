
# Semantic Spotter

This project implements a **Retrieval-Augmented Generation (RAG)** system for the **insurance domain** using **LangChain**. It aims to provide a robust generative search system capable of answering queries from a comprehensive set of policy documents.

## 📌 Problem Statement

Construct a system that can accurately and effectively answer user inquiries by extracting relevant information from a collection of insurance policy documents.

## 🛠️ Approach

The project leverages **LangChain**, an open-source framework for building applications with large language models (LLMs). Key features include:

- **Interfacing with LLMs** like OpenAI, Cohere, Hugging Face
- **Modular architecture** with components like Chains, Agents, Retrievers, and Callbacks
- **Python/JavaScript** support for application development

### LangChain Components Used

- **Model I/O**: LLM interfaces, prompts, and output parsers
- **Retrieval**: Document loaders, transformers, embedding models, vector stores
- **Chains**: Sequences of LLM calls
- **Memory**: Application state persistence
- **Agents**: Tool selection for high-level tasks
- **Callbacks**: Logging and streaming

## 🧱 System Architecture

1. **PDF Processing**: Using `PyPDFDirectoryLoader` to read files
2. **Document Chunking**: RecursiveCharacterTextSplitter for smart segmentation
3. **Embeddings**: `OpenAIEmbeddings` to convert text to vectors
4. **Vector Storage**: Embeddings stored in `ChromaDB` with `CacheBackedEmbeddings`
5. **Retrievers**: Query-response document retrieval using `VectorStoreRetriever`
6. **Re-ranking**: Using Hugging Face Cross-Encoder `BAAI/bge-reranker-base`
7. **Chains**: Creating RAG pipelines with prompt templates

## 📦 Requirements

- Python 3.7+
- `langchain==0.3.13`
- OpenAI API key for embeddings and LLM queries

## 🚀 Getting Started

1. Clone this repo
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Add your OpenAI API key:
   ```bash
   export OPENAI_API_KEY='your-api-key-here'
   ```
4. Run the application

---

Built with ❤️ using LangChain

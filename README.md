# Multi-PDF RAG Question Answering System
A Retrieval-Augmented Generation (RAG) system that allows users to ask questions over multiple PDF documents.
The project processes PDF files, splits their text into manageable chunks, converts the chunks into semantic embeddings, 
stores them in a persistent ChromaDB vector database, retrieves the most relevant content for a query, and uses a 
Groq-hosted LLM to generate a context-grounded answer.

# Project Overview
This project implements an end-to-end RAG pipeline:
<img width="1774" height="887" alt="ChromaDB-Groq RAG Architecture Flowchart" src="https://github.com/user-attachments/assets/6d974603-dcd5-4f3a-8b96-142110696c85" />
The notebook processes 8 PDF study guides covering Python Programming, Machine Learning, Data Structures & Algorithms, SQL,
Pandas, Git, Statistics, and NLP. The processed documents produced 122 text chunks, which were embedded and stored in ChromaDB.

# Features
- Process multiple PDF documents from a data directory.
- Extract PDF content using LangChain's PyPDFLoader.
- Split documents using RecursiveCharacterTextSplitter.
- Generate semantic embeddings with all-MiniLM-L6-v2.
- Persist embeddings and document metadata using ChromaDB.
- Perform top-k semantic retrieval for user queries.
- Integrate retrieved context with a Groq LLM.
- Generate answers using retrieved document context rather than
- relying only on the model's general knowledge.
- Preserve document metadata such as source, page, title, and subject.

# Tech Stack
- Python
- LangChain
- PyPDFLoader
- RecursiveCharacterTextSplitter
- Sentence Transformers
- all-MiniLM-L6-v2
- ChromaDB
- Groq API
- LangChain Groq
- python-dotenv
- NumPy
- Jupyter Notebook

# Assignment-GenAI
# FastAPI Server for Retrieval-Augmented Generation (RAG)

This project implements a lightweight FastAPI server that utilizes ChromaDB for ingesting and querying documents. It leverages the `sentence-transformers/all-MiniLM-L6-v2` model from Hugging Face for generating embeddings. The server supports PDF, DOCX, and TXT file formats.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
  - [Running the Server](#running-the-server)
  - [API Endpoints](#api-endpoints)
- [Testing the API](#testing-the-api)
- [Contributing](#contributing)
- [License](#license)

## Features

- Upload documents in PDF, DOCX, and TXT formats.
- Query documents using natural language.
- Efficient document embedding and retrieval using ChromaDB.
- Non-blocking API endpoints for concurrent requests.

## Requirements

- Python 3.7 or higher
- FastAPI
- Uvicorn
- python-multipart
- Pydantic
- ChromaDB
- Sentence Transformers
- Aiofiles
- PyPDF2
- python-docx
- pyngrok

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/fastapi-chromadb-rag.git
   cd fastapi-chromadb-rag

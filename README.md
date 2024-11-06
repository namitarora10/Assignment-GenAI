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

## Usage
**Running the Server**
To start the FastAPI server, run the following command:
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
main refers to the Python file (without the .py extension) where your FastAPI app is defined.
--reload enables auto-reloading of the server when code changes are detected.

**API Endpoints**
Upload Document
Endpoint: /upload/
Method: POST
Description: Upload a document (PDF, DOCX, TXT) for embedding.
Request:
Form-data: file (the document to upload)
Response:
Success: {"message": "File uploaded successfully."}
Error: {"error": "Unsupported file type."}
Query Documents

Endpoint: /query/
Method: GET
Description: Query the documents using natural language.
Request:
Query parameter: query (the search term)
Response:
Returns the top 5 results matching the query.
## Testing the API
You can test the API using tools like Postman or cURL.

Example cURL Commands
Upload a Document:

curl -X POST "http://localhost:8000/upload/" -F "file=@/path/to/your/file.pdf"
Query Documents:
curl -X GET "http://localhost:8000/query/?query=your_search_term"

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

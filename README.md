# RAG Backend (FastAPI)

This backend provides an API for Question Answering using RAG (Retrieval Augmented Generation).

## Tech Stack

* FastAPI
* LangChain
* FAISS Vector Store
* HuggingFace Transformers
* TinyLlama / GPT2 (text-generation)

## Features

* Load PDF / documents
* Create embeddings
* Store in FAISS
* Retrieve using similarity search
* Generate answers using LLM
* API endpoint for asking questions

## Installation

```bash
pip install fastapi uvicorn langchain faiss-cpu transformers sentence-transformers
```

## Run Backend

```bash
uvicorn app:app --reload
```

Server runs at:

```
http://127.0.0.1:8000
```

## API Endpoint

Ask question:

```
GET /ask?question=your_question
```

Example:

```
http://127.0.0.1:8000/ask?question=college name
```

Response:

```json
{
  "answer": "KONGU ENGINEERING COLLEGE"
}
```

## Project Structure

```
backend/
 ├── app.py
 ├── rag.py
 ├── embeddings/
 ├── README.md
```

## Notes

* Uses similarity retriever
* Uses FAISS vector database
* Uses text-generation model
* Designed for RAG experiments

## Future Improvements

* Chat API
* MultiQuery Retriever
* ParentDocumentRetriever
* Frontend UI
* Deployment

```
```

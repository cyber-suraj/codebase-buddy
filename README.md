# codebase-buddy

Codebase Buddy is an AI-powered onboarding and debugging assistant that helps students and developers quickly understand and work with unfamiliar codebases. It indexes a public GitHub repository (or uploaded ZIP) and enables natural-language question answering over the repository using Retrieval-Augmented Generation (RAG) with file-level citations.

Track: Student Track – AI for Learning & Developer Productivity  
Hackathon: AI for Bharat

---

## Problem

Onboarding to a new codebase is slow and frustrating. Developers must search through documentation, scan folders, and trace errors manually. Traditional keyword search or rule-based tools cannot answer high-level questions like:

- How do I run this project?
- Where is authentication implemented?
- Explain the architecture of this repository
- Why am I getting this error?

---

## Solution

Codebase Buddy uses Large Language Models with Retrieval-Augmented Generation (RAG) to:

1. Ingest repository files (code + docs)  
2. Convert content into embeddings and store in a vector index  
3. Retrieve relevant context for a user question  
4. Generate grounded answers with citations to source files  

The system answers only from retrieved repository content and clearly indicates when information is not found.

---

## Key Features

- Public GitHub URL or ZIP upload  
- Semantic search over code and documentation  
- Natural-language Q&A with file citations  
- Stack trace explanation with relevant file pointers  
- Hallucination prevention using strict grounding  
- Responsible AI guardrails and disclaimers  

---

## Why AI

Understanding codebases requires semantic reasoning, summarization, and multi-file context synthesis. These capabilities cannot be reliably achieved with rule-based systems or keyword search alone. AI enables natural-language understanding and explanation of complex repositories.

---

## Tech Stack

- Amazon Bedrock (LLM + Embeddings)  
- FAISS Vector Index  
- Python  
- FastAPI (backend, optional)  
- Streamlit (UI, optional)  

---

## Responsible Design

- Uses only public repositories or user-provided files  
- No private repository access  
- No code execution or modification  
- Mandatory citations for every answer  
- "Not found in repository context" response when information is unavailable  

---

## Project Structure

codebase-buddy/  
 ├ requirements.md  
 ├ design.md  
 └ README.md  

---

## Future Enhancements

- IDE plugin integration  
- Hybrid search (vector + keyword)  
- Support for large repositories via incremental indexing  
- Team workspaces and collaboration  

---

## Team

Suraj Khanase (Team Lead)  
Pranay Khodade  
Nandkishor Tamkhade  

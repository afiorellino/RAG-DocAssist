# Project Name
RAG-DocAssist - (Building AI course project)

## Summary  
RAG-DocAssist is a lightweight RAG (Retrieval-Augmented Generation) application that allows project team (project managers, technical staff, ...) to quickly query and retrieve information from large amounts of documents such as: contract, customer specifications, company standards, local laws, ..., typically stored in PDF format. This is the final project for the Building AI course

## The problem  
In large industrial sectors like Oil & Gas and Energy, technical teams frequently work with massive amounts of documentation (often thousands of pages of specifications and technical standards).  
Finding a single piece of relevant information manually can take hours or even days, especially when dealing with PDFs or scanned/raster documents.

## Motivation  
As often happens in large projects (where deadlines are strict) many people are busy wasting precious time scrolling through PDFs or sending emails to colleagues to ask for clarifications already hidden somewhere in the documentation.

## Why it matters  
A tool that allows natural language querying over internal documents, powered by AI, can lead to faster decision-making, reduced errors, and better project performance.

## Data sources
- Internal project documentation in PDF format (both text-based and raster/scanned)
- Document types: contract, technical manuals, datasheets,  project specifications, local low, etc.

## Data processing workflow
- OCR (Optical Character Recognition) for raster PDFs (using Tesseract OCR)
- Chunking and preprocessing using LangChain and Unstructured.io
- Embedding generation using open-source models from Hugging Face (e.g., all-MiniLM-L6-v2)
- Vector storage in ChromaDB (embedded, local)

## AI techniques used
- Semantic search / Vector similarity retrieval
- Prompt engineering
- LLMs (Large Language Models) for generation (using Mistral 7B Instruct via Ollama running locally)

## Demo (optional for implementation)
- Simple Streamlit web interface for submitting questions and viewing generated answers.

## Who uses it
- Project engineers
- Document controllers
- Project managers
- QA/QC inspectors
- Technical consultants

## Where
- Within Company offices and construction sites

## Usage context
- During Design phases
- During design reviews
- During procurement clarifications
- While preparing technical reports
- In response to vendor or client queries
- Other

## What the project does not solve
- Accuracy limits: The AI may provide hallucinated or incomplete answers if source documents lack clarity.
- OCR errors: Poor quality scans may result in missing or misinterpreted text.
- Document coverage: If a document hasn’t been ingested into the system, it won’t appear in search results.
- Limited model size (for local deployment): Running larger models requires more powerful hardware.

## Possible Future improvements
- Add support for multi-language querying and document sets
- Integrate a web-based document upload tool
- Support real-time document ingestion
- Implement user feedback and response ranking
- Explore fine-tuning a custom LLM on company-specific vocabulary
- Deploy the solution on a local company server or cloud VM

## Acknowledgments

- LangChain: https://www.langchain.com/
- LlamaIndex: https://www.llamaindex.ai/
- ChromaDB: https://www.trychroma.com/
- Hugging Face Transformers & SentenceTransformers: https://huggingface.co/
- Ollama: https://ollama.com/
- Unstructured.io: https://unstructured.io/
- Tesseract OCR: https://github.com/tesseract-ocr/tesseract
- Inspiration from numerous AI/RAG tutorials and open-source contributors in the LangChain and Hugging Face communities.



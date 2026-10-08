---
layout: page
title: Development of CV Analyzer and Text2SQL AI Agents
description: Engineered AI agents leveraging LangChain and Langflow to automate data processing and hiring workflows.
img: assets/img/Orbislabs.png
importance: 2
category: Internship
---

**TL;DR:** Developed and deployed RAG-based and multi-agent AI solutions at Orbislabs to automate CV screening for Human Resources and translate natural language into SQL for enterprise databases.

![OrbisFlow Agent Architecture](/assets/img/SQL Agent.png)

### Technologies & Methodology
* **Software & Frameworks:** Python, PyMuPDF, FAISS vector database, LangChain, OrbisFlow (modified Langflow), and Vanna AI.
* **Models:** SBERT, Cohere Embedding, Cohere Rerank, Cohere LLM, and local LLMs.
* **Databases:** PostgreSQL.

### Key Contributions & Results
* Developed an RAG-based CV Analyzer that utilizes PyMuPDF for text extraction, Cohere embeddings, and an FAISS vector database to automatically rank candidates against job descriptions.
* Integrated a Cohere LLM with a memory component to allow users to interactively chat with the CV database, extracting missing or matching candidate qualities while reducing human hiring biases.
* Engineered a Text2SQL multi-agent architecture using LangChain for an insurance company, enabling non-technical managers to query a PostgreSQL database using natural language.
* Implemented a complex LangChain routing system containing table-specific agents, fuzzy filter checks, and query validation layers to generate and refine SQL queries.
* Evaluated and iterated through multiple architectural frameworks (such as SBERT and Vanna AI) and applied prompt engineering to resolve LLM output format errors and reduce hallucination issues.

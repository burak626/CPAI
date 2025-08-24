---

# AI Career Path Advisor (CPAI)

## Overview

The **AI Career Path Advisor Project (CPAI)** is an **n8n-orchestrated workflow** that analyzes real-time AI job market data (starting March 2025) to uncover **high-value opportunities with low competition**.
It integrates multiple AI tools and services to provide **data-driven insights** into emerging skills, industry demands, and tailored career growth recommendations.

---

## Workflow Architecture

The workflow is composed of the following components:

1. **Trigger: Chat Message**

   * Starts whenever a user sends a message to the system.

2. **AI Agent (Tools Agent)**

   * The core orchestrator.
   * Routes messages to the right tools (memory, vector search, calculator).

3. **Groq Chat Model**

   * Main LLM reasoning engine for fast and optimized responses.

4. **Simple Memory**

   * Keeps track of previous conversations for context continuity.

5. **Vector Store Query**

   * Handles knowledge retrieval.
   * Connects to **Pinecone Vector Store** for semantic search.

6. **Pinecone Vector Store**

   * Stores embeddings of AI job market data.
   * Ensures queries return the most relevant results.

7. **Embeddings (OpenAI)**

   * Transforms job market text into vector embeddings.
   * Powers semantic search inside Pinecone.

8. **OpenAI Chat Model (Secondary)**

   * Generates contextual answers from retrieved documents.

9. **Calculator Tool**

   * Provides numerical reasoning (salary projections, trend comparisons, etc.).

---

## Features

* **Real-time AI job market analysis** (March 2025 dataset).
* **Context-aware chat agent** with memory.
* **Semantic search** over job market insights using Pinecone.
* **Multi-tool integration**: LLM, memory, vector store, and calculator.
* **Career recommendations** tailored to skills, demand, and growth potential.

---

## Tech Stack

* **n8n** (workflow orchestration)
* **Groq LLM** (chat model)
* **Pinecone** (vector database)
* **OpenAI Embeddings** (text-to-vector)
* **n8n Simple Memory** (conversation history)

---

## How to Use

1. Clone this repository.
2. Import the provided `.json` workflow into your **n8n instance**.
3. Configure credentials for:

   * Pinecone API
   * OpenAI API (for embeddings)
   * Groq API (for chat model)
4. Run the workflow and interact with it via chat trigger.

---

## License

This project is licensed under the **MIT License** — free to use, modify, and distribute with attribution.

---

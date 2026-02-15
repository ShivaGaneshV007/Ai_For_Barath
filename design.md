# Design.md

## System Architecture & Technical Design

------------------------------------------------------------------------

## 1. Architectural Overview

The platform follows a **layered AI‑native architecture**:

1.  Capture Layer\
2.  Intelligence Processing Layer\
3.  Memory & Storage Layer\
4.  Collaboration Layer\
5.  Security & Governance Layer

This separation ensures scalability, modularity, and maintainability.

------------------------------------------------------------------------

## 2. Component‑Level Design

### 2.1 Capture Layer

Handles multimodal ingestion:

-   Voice input → Speech‑to‑Text pipeline
-   Text notes → Direct semantic parsing
-   Screenshots → OCR + embedding generation

Outputs structured events to the processing layer.

------------------------------------------------------------------------

### 2.2 Intelligence Processing Layer

Core AI reasoning components:

-   Intent classification models
-   Task & decision extraction
-   Semantic embedding generation
-   Context linking across historical knowledge
-   Summarization and explanation generation

Implements Human‑in‑the‑Loop validation before committing critical
actions.

------------------------------------------------------------------------

### 2.3 Memory & Storage Layer

Hybrid storage architecture:

**Relational Storage (PostgreSQL)** - Users - Rooms - Tasks - Meetings -
Permissions

**Vector Storage (ChromaDB / FAISS)** - Semantic embeddings - Context
retrieval - Cross‑knowledge similarity search

**Cache & Queue (Redis)** - Realtime notifications - Background job
triggers - Session state

------------------------------------------------------------------------

### 2.4 Collaboration Layer

Provides shared intelligence:

-   Realtime updates via WebSockets
-   Shared Room knowledge graph
-   Automatic task propagation
-   Meeting knowledge persistence
-   Onboarding context generation

------------------------------------------------------------------------

### 2.5 Meet Mode Engine

Pipeline:

1.  Audio capture\
2.  Transcription (Whisper)\
3.  Speaker segmentation\
4.  Decision & task extraction\
5.  MoM generation via LLM\
6.  Storage in Room context

Ensures meetings become persistent, actionable knowledge.

------------------------------------------------------------------------

## 3. Security Architecture

### Identity & Access

-   JWT‑based authentication
-   Role‑based permissions per Room

### Data Isolation

-   Context‑scoped retrieval
-   No cross‑room inference without permission

### Encryption

-   TLS for transport
-   Encrypted storage for sensitive artifacts

------------------------------------------------------------------------

## 4. Deployment Architecture

### Services

-   API service (FastAPI)
-   Worker service (Celery/RQ)
-   Vector DB service
-   Relational DB service
-   Redis realtime service

### Scalability

-   Containerized deployment
-   Horizontal scaling of workers
-   Load‑balanced API gateway

------------------------------------------------------------------------

## 5. Future Extensions

-   On‑device transcription for privacy
-   Multi‑modal video understanding
-   Predictive task recommendations
-   Organization‑wide knowledge graphs

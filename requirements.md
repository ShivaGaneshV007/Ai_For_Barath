# Requirements.md

## MIND VAULT


## AI-Powered Personal & Collective Knowledge System

------------------------------------------------------------------------

## 1. Product Overview

The system is an AI-driven cognitive workspace designed to function
as: - A **personal memory layer** for individuals - A **shared project
intelligence layer** for collaborative teams

It enables continuous capture, contextual understanding, structured
recall, and secure collaboration across learning and development
workflows.

------------------------------------------------------------------------

## 2. Functional Requirements

### 2.1 Personal Knowledge Capture

-   Voice-first capture of ideas, fixes, explanations, and reminders
-   Text and screenshot ingestion
-   Automatic intent classification:
    -   Idea
    -   Task
    -   Decision
    -   Learning note
-   Contextual linking across time and topics
-   Conversational recall of stored knowledge

### 2.2 Collaborative Rooms (Shared Memory)

-   Project‑scoped shared knowledge environments
-   Natural language responsibility detection (e.g., @mentions → tasks)
-   Real‑time synchronization of updates across members
-   Persistent project state tracking:
    -   Completed features
    -   Pending work
    -   Dependencies
    -   Decisions

### 2.3 Meet Mode

-   Live speech transcription (in‑person & online)
-   Automatic Minutes of Meeting generation
-   Decision extraction and task assignment
-   Follow‑up scheduling and reminders
-   Storage of meeting knowledge inside the relevant Room

### 2.4 Knowledge Recall & Intelligence

-   Context‑aware summaries
-   Cross‑room semantic linking (permission‑based)
-   Onboarding snapshot for new members
-   Knowledge drift detection for outdated information

### 2.5 Alerts & Productivity Automation

-   Due detection and reminders
-   Stalled task identification
-   Overload‑aware notification throttling
-   Passive learning resurfacing

------------------------------------------------------------------------

## 3. Non‑Functional Requirements

### Security

-   Room‑level data isolation
-   Role‑based access control
-   Encryption in transit and at rest
-   Consent‑based voice recording

### Scalability

-   Horizontal scaling of services
-   Vector search optimization for large knowledge graphs
-   Event‑driven background processing

### Performance

-   Near real‑time transcription and recall
-   Sub‑second knowledge retrieval for queries
-   Efficient memory indexing

### Reliability

-   Fault‑tolerant background workers
-   Graceful degradation for AI failures
-   Data backup and recovery

------------------------------------------------------------------------

## 4. Technical Stack

### Backend

-   FastAPI (async API framework)
-   WebSockets for realtime collaboration
-   Celery/RQ for background processing

### AI & NLP

-   OpenAI models for reasoning and summarization
-   Whisper/Faster‑Whisper for transcription
-   Sentence‑Transformers for embeddings
-   LangChain/LlamaIndex for orchestration

### Data Layer

-   PostgreSQL for structured storage
-   Redis for caching, queues, and realtime alerts
-   ChromaDB/FAISS for vector memory retrieval

### Security

-   JWT authentication
-   Passlib hashing
-   Cryptographic encryption utilities

------------------------------------------------------------------------

## 5. Deliverables

-   Functional backend API
-   Voice capture and meeting transcription pipeline
-   Collaborative Rooms with realtime sync
-   Contextual knowledge retrieval engine
-   Secure authentication and authorization
-   Demonstration UI prototype

------------------------------------------------------------------------


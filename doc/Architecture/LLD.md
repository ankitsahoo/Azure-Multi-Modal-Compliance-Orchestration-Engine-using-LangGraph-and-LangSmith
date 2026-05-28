# Low Level Design (LLD)

# 1. Backend Modules

| Module        | Responsibility           |
| ------------- | ------------------------ |
| routes/       | API endpoints            |
| services/     | Business logic           |
| orchestrator/ | LangGraph workflows      |
| rag/          | Retrieval pipelines      |
| models/       | Request/response schemas |
| monitoring/   | Telemetry                |
| utils/        | Helper functions         |

---

# 2. LangGraph Nodes

| Node                 | Function                |
| -------------------- | ----------------------- |
| video_ingestion_node | Download/upload video   |
| transcript_node      | Extract transcript      |
| ocr_node             | OCR extraction          |
| chunking_node        | Split text chunks       |
| embedding_node       | Generate embeddings     |
| retrieval_node       | Retrieve policies       |
| audit_node           | GPT-4o compliance audit |
| report_node          | Generate JSON report    |
| monitoring_node      | Push telemetry          |

---

# 3. Database Design

## Vector Store

Azure AI Search stores:

* compliance policies
* embeddings
* metadata

## Blob Storage

Stores:

* uploaded videos
* intermediate JSON files
* audit reports

---

# 4. API Layer

FastAPI handles:

* authentication
* validation
* orchestration trigger
* report retrieval

---

# 5. Prompt Engineering Design

Prompts include:

* compliance policies
* transcript chunks
* OCR text
* timestamps
* evidence instructions

---

# 6. Failure Handling

| Failure             | Strategy           |
| ------------------- | ------------------ |
| OCR failure         | Retry              |
| LLM timeout         | Fallback execution |
| Retrieval miss      | Re-query           |
| Blob upload failure | Queue retry        |

---

# 7. Observability Integration

Integrated with:

* LangSmith tracing
* Azure App Insights
* structured logs
* token monitoring

# Workflow Architecture

# End-to-End Workflow

```text
User Uploads Video
        ↓
FastAPI Receives Request
        ↓
LangGraph Workflow Starts
        ↓
Video Download/Ingestion
        ↓
Azure Blob Storage Upload
        ↓
Azure Video Indexer Processing
        ↓
Transcript Extraction
        ↓
OCR Extraction
        ↓
Chunking Pipeline
        ↓
Embedding Generation
        ↓
Azure AI Search Retrieval
        ↓
Compliance Policy Matching
        ↓
GPT-4o Compliance Reasoning
        ↓
Violation Detection
        ↓
Severity Classification
        ↓
JSON Report Generation
        ↓
Storage + Dashboard Update
        ↓
Monitoring + Telemetry
```

# Workflow Objectives

* Fully automated compliance auditing
* Explainable AI reasoning
* Enterprise observability
* Scalable orchestration
* Structured outputs

# Workflow Benefits

* Reduced manual effort
* Faster approvals
* Improved governance
* Enterprise traceability

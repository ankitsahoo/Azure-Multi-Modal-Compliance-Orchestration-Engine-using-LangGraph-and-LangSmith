# Azure-Multi-Modal-Compliance-Orchestration-Engine-using-LangGraph-and-LangSmith

# Architetcture Diagram
<img width="1402" height="817" alt="Project2_Langgraph_Architecture" src="https://github.com/user-attachments/assets/59ad198b-37d1-479d-b35b-700fbb1213f0" />

- **LangGraph** for orchestration
- **Microsoft Azure services** for video processing and storage
- **Azure OpenAI Service** for reasoning and compliance checking
- **Azure AI Search** for RAG retrieval
- **LangSmith** for debugging and tracing

# End-to-End Architecture Flow

User Uploads Video
        ↓
FastAPI Receives Request
        ↓
LangGraph Starts Workflow
        ↓
Video Downloaded
        ↓
Stored in Azure Blob
        ↓
Azure Video Indexer
   → Transcript
   → OCR
        ↓
Embeddings Generated
        ↓
Stored/Searched in Azure AI Search
        ↓
RAG Retrieves Compliance Rules
        ↓
GPT-4o Audits Video
        ↓
Violations Detected
        ↓
JSON Compliance Report Generated
        ↓
Logs + Traces Sent to Monitoring

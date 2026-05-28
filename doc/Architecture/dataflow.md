# Data Flow Architecture

# Data Flow Overview

## Step 1 — Video Input
Source:
- YouTube URL
- MP4 upload
- Enterprise storage

↓

## Step 2 — Blob Storage
Video stored temporarily in Azure Blob Storage.

↓

## Step 3 — Azure Video Indexer
Extracts:
- transcript
- OCR text
- timestamps

↓

## Step 4 — Text Processing
Data cleaned and chunked.

↓

## Step 5 — Embedding Generation
Azure OpenAI converts chunks into embeddings.

↓

## Step 6 — Vector Search
Azure AI Search retrieves relevant compliance policies.

↓

## Step 7 — GPT-4o Reasoning
LLM compares:
- transcript
- OCR text
- compliance policies

↓

## Step 8 — Compliance Report
Structured JSON output generated.

↓

## Step 9 — Monitoring
Telemetry sent to:
- LangSmith
- Azure App Insights

# Data Stores

| Store | Data |
|---|---|
| Blob Storage | Videos + reports |
| AI Search | Embeddings + policies |
| Logs | Monitoring data |
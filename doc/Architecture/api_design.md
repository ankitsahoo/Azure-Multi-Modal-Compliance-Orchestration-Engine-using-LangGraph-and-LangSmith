# API Design

# Base URL

/api/v1

# Endpoints

## 1. Upload Video

POST /audit-video

Request:
{
  "video_url": "string"
}

Response:
{
  "audit_id": "123",
  "status": "processing"
}

---

## 2. Get Audit Status

GET /audit-status/{audit_id}

Response:
{
  "status": "completed"
}

---

## 3. Fetch Report

GET /report/{audit_id}

Response:
{
  "violations": []
}

---

## 4. Upload Policies

POST /policies

---

# Authentication

- JWT token
- OAuth2

# Response Standards

- JSON responses
- Standard error handling
- Correlation IDs
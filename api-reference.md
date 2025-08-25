---
description: 'Complete API reference for VerifyWise integrations and automation'
---

# 🔌 API Reference

The VerifyWise API enables programmatic access to all platform features, allowing integration with existing systems and automation of governance workflows.

## 🚀 Quick Start

### Authentication
All API requests require authentication using Bearer tokens.

```bash
# Get authentication token
curl -X POST https://your-verifywise-domain.com/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{
    "email": "your-email@domain.com",
    "password": "your-password"
  }'
```

### Basic Request Example
```bash
# Get projects list
curl -H "Authorization: Bearer YOUR_TOKEN" \
  https://your-verifywise-domain.com/api/projects
```

> **Screenshot Location:** *Postman or API client showing successful authentication response*

---

## 🔑 Authentication

### Login
```http
POST /api/users/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "password123"
}
```

**Response:**
```json
{
  "message": "Login successful",
  "data": {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "refreshToken": "refresh_token_string",
    "user": {
      "id": 1,
      "email": "user@example.com",
      "name": "John",
      "surname": "Doe",
      "role": {
        "id": 1,
        "name": "Admin"
      }
    }
  }
}
```

### Refresh Token
```http
POST /api/users/refresh-token
Cookie: refreshToken=refresh_token_string
```

### Logout
```http
POST /api/users/logout
Authorization: Bearer YOUR_TOKEN
```

---

## 📊 Projects API

### List All Projects
```http
GET /api/projects
Authorization: Bearer YOUR_TOKEN
```

**Query Parameters:**
- `limit`: Number of results (default: 50, max: 100)
- `offset`: Pagination offset (default: 0)
- `search`: Search term for project names
- `status`: Filter by project status
- `risk_level`: Filter by risk classification

**Response:**
```json
{
  "data": [
    {
      "id": 1,
      "project_title": "AI Chatbot System",
      "ai_risk_classification": "High Risk",
      "goal": "Customer service automation",
      "start_date": "2024-01-15",
      "last_updated": "2024-08-20",
      "owner": {
        "id": 1,
        "name": "John Doe"
      }
    }
  ],
  "pagination": {
    "total": 25,
    "limit": 50,
    "offset": 0
  }
}
```

### Get Project Details
```http
GET /api/projects/{project_id}
Authorization: Bearer YOUR_TOKEN
```

### Create New Project
```http
POST /api/projects
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "project_title": "New AI Project",
  "ai_risk_classification": "High Risk",
  "type_of_high_risk_role": "Provider",
  "goal": "Automate customer support",
  "start_date": "2024-09-01"
}
```

### Update Project
```http
PUT /api/projects/{project_id}
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "project_title": "Updated Project Name",
  "goal": "Updated project goals"
}
```

### Delete Project
```http
DELETE /api/projects/{project_id}
Authorization: Bearer YOUR_TOKEN
```

---

## 📋 Assessment API

### Get Assessment Progress
```http
GET /api/eu/assessment-progress
Authorization: Bearer YOUR_TOKEN
```

**Query Parameters:**
- `project_id`: Specific project ID (optional)

### Get Assessment Topics
```http
GET /api/topics/{project_id}
Authorization: Bearer YOUR_TOKEN
```

### Get Subtopics
```http
GET /api/subtopics/{topic_id}
Authorization: Bearer YOUR_TOKEN
```

### Get Questions
```http
GET /api/questions/{subtopic_id}
Authorization: Bearer YOUR_TOKEN
```

### Update Question Answer
```http
PUT /api/questions/{question_id}
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "answer": "Detailed answer to the assessment question",
  "evidence_files": ["file1.pdf", "file2.docx"],
  "status": "completed"
}
```

---

## ✅ Compliance API

### Get Compliance Progress
```http
GET /api/eu/compliance-progress
Authorization: Bearer YOUR_TOKEN
```

### Get Control Categories
```http
GET /api/control-categories/{project_id}
Authorization: Bearer YOUR_TOKEN
```

### Get Controls
```http
GET /api/controls/{control_category_id}
Authorization: Bearer YOUR_TOKEN
```

### Update Control Status
```http
PUT /api/controls/{control_id}
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "status": "implemented",
  "implementation_details": "Control has been fully implemented",
  "evidence_description": "Evidence of implementation",
  "evidence_files": ["evidence1.pdf"]
}
```

### Get Subcontrols
```http
GET /api/subcontrols/{control_id}
Authorization: Bearer YOUR_TOKEN
```

---

## ⚠️ Risk Management API

### List Project Risks
```http
GET /api/project-risks/{project_id}
Authorization: Bearer YOUR_TOKEN
```

### Create New Risk
```http
POST /api/project-risks
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "project_id": 1,
  "risk_name": "Data Privacy Risk",
  "risk_description": "Potential unauthorized access to personal data",
  "risk_category": "Privacy",
  "impact": "High",
  "likelihood": "Medium",
  "ai_lifecycle_phase": "Development"
}
```

### Update Risk Assessment
```http
PUT /api/project-risks/{risk_id}
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "current_risk_level": "Medium",
  "mitigation_plan": "Implement additional encryption",
  "mitigation_status": "In Progress"
}
```

---

## 👥 Vendor Management API

### List Vendors
```http
GET /api/vendors
Authorization: Bearer YOUR_TOKEN
```

### Create New Vendor
```http
POST /api/vendors
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "vendor_name": "AI Solutions Inc",
  "vendor_provides": "Machine Learning APIs",
  "website": "https://aisolutions.com",
  "vendor_contact_person": "Jane Smith"
}
```

### Get Vendor Risks
```http
GET /api/vendor-risks/{vendor_id}
Authorization: Bearer YOUR_TOKEN
```

### Link Vendor to Project
```http
POST /api/vendors/{vendor_id}/projects
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "project_id": 1
}
```

---

## 👤 User Management API

### List Users
```http
GET /api/users
Authorization: Bearer YOUR_TOKEN
```

### Get User Details
```http
GET /api/users/{user_id}
Authorization: Bearer YOUR_TOKEN
```

### Update User Profile
```http
PUT /api/users/{user_id}
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "name": "Updated Name",
  "surname": "Updated Surname"
}
```

### Get User Roles
```http
GET /api/roles
Authorization: Bearer YOUR_TOKEN
```

---

## 📁 File Management API

### Upload File
```http
POST /api/files/upload
Authorization: Bearer YOUR_TOKEN
Content-Type: multipart/form-data

FormData:
- file: [file content]
- project_id: 1
- file_type: "evidence"
```

### List User Files
```http
GET /api/files/metadata/{user_id}
Authorization: Bearer YOUR_TOKEN
```

### Download File
```http
GET /api/files/{file_id}
Authorization: Bearer YOUR_TOKEN
```

---

## 📊 Dashboard API

### Get Dashboard Data
```http
GET /api/dashboard
Authorization: Bearer YOUR_TOKEN
```

**Response:**
```json
{
  "data": {
    "totalProjects": 15,
    "highRiskProjects": 5,
    "completedAssessments": 8,
    "pendingRisks": 12,
    "recentActivity": [
      {
        "type": "project_created",
        "description": "New project: AI Chatbot",
        "timestamp": "2024-08-20T10:30:00Z"
      }
    ]
  }
}
```

---

## 📈 Reporting API

### Generate Report
```http
POST /api/reporting/generate
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "project_id": 1,
  "report_type": "compliance",
  "format": "pdf",
  "sections": ["assessment", "risks", "compliance"]
}
```

### Get Report Status
```http
GET /api/reporting/status/{report_id}
Authorization: Bearer YOUR_TOKEN
```

### Download Report
```http
GET /api/reporting/download/{report_id}
Authorization: Bearer YOUR_TOKEN
```

---

## 🔍 Search API

### Global Search
```http
GET /api/search?q={search_term}&type={content_type}
Authorization: Bearer YOUR_TOKEN
```

**Parameters:**
- `q`: Search query
- `type`: Content type (projects, risks, vendors, users)
- `limit`: Results limit
- `project_id`: Limit search to specific project

---

## 🎯 AI Trust Center API

### Get Public Trust Center
```http
GET /api/ai-trust-centre/public/{organization_id}
```

### Update Trust Center Settings
```http
PUT /api/ai-trust-centre/overview
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "intro_visible": true,
  "purpose_text": "Our commitment to AI ethics",
  "our_statement_visible": true,
  "our_statement_text": "We believe in responsible AI"
}
```

---

## 📊 Analytics API

### Get Project Analytics
```http
GET /api/analytics/projects/{project_id}
Authorization: Bearer YOUR_TOKEN
```

### Get Organization Metrics
```http
GET /api/analytics/organization
Authorization: Bearer YOUR_TOKEN
```

---

## 🔧 Webhooks

### Configure Webhook
```http
POST /api/webhooks
Authorization: Bearer YOUR_TOKEN
Content-Type: application/json

{
  "url": "https://your-system.com/webhook",
  "events": ["project.created", "risk.updated", "assessment.completed"],
  "secret": "your-webhook-secret"
}
```

### Webhook Events
- `project.created`
- `project.updated`
- `project.deleted`
- `risk.created`
- `risk.updated`
- `assessment.completed`
- `compliance.updated`
- `user.invited`

**Webhook Payload Example:**
```json
{
  "event": "project.created",
  "timestamp": "2024-08-20T10:30:00Z",
  "data": {
    "project_id": 1,
    "project_title": "New AI Project",
    "created_by": 1
  },
  "signature": "sha256=signature_hash"
}
```

---

## 🔒 Security Considerations

### Rate Limiting
- **Authentication**: 10 requests per minute
- **Standard APIs**: 1000 requests per hour per user
- **File Uploads**: 50 requests per hour

### API Security Best Practices

1. **Token Management**
   ```bash
   # Store tokens securely
   export VERIFYWISE_TOKEN="your_token_here"
   
   # Use environment variables, not hardcoded tokens
   curl -H "Authorization: Bearer $VERIFYWISE_TOKEN"
   ```

2. **Request Validation**
   - Validate all input data
   - Use HTTPS for all requests
   - Implement proper error handling

3. **Error Handling**
   ```json
   {
     "error": true,
     "message": "Invalid project ID",
     "code": "INVALID_PROJECT_ID",
     "details": {
       "project_id": "Must be a valid integer"
     }
   }
   ```

---

## 🔄 Error Codes

| HTTP Status | Error Code | Description |
|-------------|------------|-------------|
| 400 | BAD_REQUEST | Invalid request format |
| 401 | UNAUTHORIZED | Invalid or missing token |
| 403 | FORBIDDEN | Insufficient permissions |
| 404 | NOT_FOUND | Resource not found |
| 409 | CONFLICT | Resource already exists |
| 422 | VALIDATION_ERROR | Input validation failed |
| 429 | RATE_LIMITED | Too many requests |
| 500 | INTERNAL_ERROR | Server error |

---

## 📚 SDK and Libraries

### JavaScript/TypeScript
```bash
npm install @verifywise/sdk
```

```javascript
import { VerifyWiseClient } from '@verifywise/sdk';

const client = new VerifyWiseClient({
  baseUrl: 'https://your-domain.com/api',
  token: 'your-auth-token'
});

// Get projects
const projects = await client.projects.list();

// Create project
const newProject = await client.projects.create({
  project_title: 'My AI Project',
  ai_risk_classification: 'High Risk'
});
```

### Python
```bash
pip install verifywise-python
```

```python
from verifywise import VerifyWiseClient

client = VerifyWiseClient(
    base_url='https://your-domain.com/api',
    token='your-auth-token'
)

# Get projects
projects = client.projects.list()

# Create project
new_project = client.projects.create({
    'project_title': 'My AI Project',
    'ai_risk_classification': 'High Risk'
})
```

---

## 🧪 Testing and Development

### Sandbox Environment
```bash
# Use sandbox for testing
export VERIFYWISE_BASE_URL="https://sandbox.verifywise.com/api"
export VERIFYWISE_TOKEN="sandbox_token"
```

### API Testing Tools
- **Postman Collection**: Available for download
- **OpenAPI Specification**: Full API documentation
- **Swagger UI**: Interactive API explorer

---

## 📞 API Support

### Getting Help
- **Documentation Issues**: Report unclear or missing information
- **Integration Support**: Get help with API integration
- **Rate Limit Increases**: Request higher limits for production use

### Best Practices for API Requests
1. Include descriptive error handling
2. Implement exponential backoff for retries
3. Use appropriate pagination for large datasets
4. Cache responses when appropriate
5. Monitor API usage and performance

**Related Documentation:**
- [Authentication Setup](settings.md#authentication)
- [File Upload Guide](troubleshooting.md#file-upload-issues)
- [Webhook Configuration](settings.md#webhooks)
# TravelFollower - Quy Tắc Thiết Kế API

## Luồng xử lý API Development

### 1. Design Phase
- Định nghĩa endpoints theo RESTful standards
- Thiết kế request/response format
- Xác định authentication requirements

### 2. Implementation Phase
- Implement với Go + Fiber framework
- Thêm Swagger annotations
- Validate input data

### 3. Documentation Phase
- Generate OpenAPI spec
- Auto-generate TypeScript client
- Update API documentation

## Quy định bắt buộc

### URL Structure
```
Base URL: /api/v1
Resources: /locations, /users, /visits
Actions: GET, POST, PUT, DELETE
```

### Response Format
```json
{
  "success": true,
  "data": {},
  "message": "Operation successful",
  "timestamp": "2024-01-01T00:00:00.000Z"
}
```

### Error Handling
```json
{
  "success": false,
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid input data"
  },
  "timestamp": "2024-01-01T00:00:00.000Z"
}
```

## Workflow

### Backend → Frontend Flow
1. **Backend**: Design API → Add Swagger → Generate spec
2. **Frontend**: Generate client → Implement integration
3. **Testing**: Test API → Test integration → E2E testing

### Version Management
- Use URL versioning: `/api/v1/`, `/api/v2/`
- Maintain backward compatibility for 6 months
- Include deprecation warnings

## Security Requirements
- JWT authentication cho protected endpoints
- Rate limiting: 100 requests/minute
- Input validation cho tất cả parameters
- HTTPS only trong production

---

*AI Agent phải tuân thủ quy định này khi tạo API mới.*
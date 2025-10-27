# [ProjectName] - Quy Tắc Phát Triển

## Tổng quan
Thư mục `rules/` chứa các quy định bắt buộc AI Agent phải tuân thủ trước khi thực hiện chức năng.

## Luồng xử lý phát triển

### 1. Backend Development Flow
```
API Design → Database Design → Implementation → Testing → Deployment
```

**Bắt buộc:**
1. Đọc [`api-design.md`](./api-design.md) trước khi tạo API mới
2. Đọc [`database-design.md`](./database-design.md) trước khi thay đổi schema
3. Tuân thủ [`coding-standards.md`](./coding-standards.md) khi viết code

### 2. Frontend Development Flow
```
UI/UX Design → Component Development → API Integration → Testing → Build
```

**Bắt buộc:**
1. Tham khảo UI/UX guidelines trong `reference/`
2. Sử dụng API client được generate từ backend
3. Tuân thủ coding standards cho framework

### 3. API Development Workflow
```
1. Design API → 2. Generate OpenAPI → 3. Implement Backend → 4. Generate Client → 5. Implement Frontend
```

**Quy định:**
- Backend phải generate OpenAPI spec trước
- Frontend chỉ sử dụng API client được generate
- Không được hard-code API calls

### 4. Database Change Workflow
```
1. Design Schema → 2. Create Migration → 3. Update Models → 4. Test Migration → 5. Deploy
```

**Quy định:**
- Mọi thay đổi schema phải qua migration
- Migration phải có rollback script
- Test migration trên development trước

## Các quy định quan trọng

### Security Rules
- Mọi API phải có authentication
- Input validation là bắt buộc
- Không bao giờ expose sensitive data

### Performance Rules
- API response time < 200ms
- Database queries phải có index
- Frontend bundle size < 1MB

### Code Quality Rules
- Test coverage > 80%
- Code review là bắt buộc
- Tuân thủ coding standards

## Trình tự thực hiện task

1. **Đọc rules liên quan** trước khi bắt đầu
2. **Kiểm tra reference** nếu cần thông tin chi tiết
3. **Tham khảo plan** để hiểu thứ tự ưu tiên
4. **Implement** theo quy định
5. **Test** theo testing guidelines
6. **Deploy** theo deployment guidelines

---

*Lưu ý: AI Agent phải đọc các quy định này trước khi thực hiện bất kỳ task nào.*
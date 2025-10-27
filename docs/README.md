# [ProjectName] - Documentation

## Tổng quan

Thư mục này chứa toàn bộ tài liệu kỹ thuật và hướng dẫn phát triển cho dự án [ProjectName]. Tài liệu được tổ chức theo 5 thư mục chính để AI Agent dễ dàng theo dõi và thực hiện.

## Cấu trúc Documentation

```
docs/
├── old/                          # Tài liệu cũ đã xử lý xong
├── plan/                         # Kế hoạch thực hiện (AI Agent bám vào đây)
├── plan-detail/                  # Chi tiết kế hoạch thực hiện
├── rules/                         # Quy định bắt buộc (AI Agent phải tuân thủ)
└── reference/                     # Tài liệu tham khảo (chi tiết khi cần)
```

## Cách sử dụng Documentation

1. **Đọc plan trước**: Kiểm tra `plan/README.md` để hiểu công việc tiếp theo
2. **Tuân thủ rules**: Đọc `rules/README.md` trước khi thực hiện chức năng
3. **Tham khảo reference**: Chỉ sử dụng `reference/` khi cần thông tin chi tiết
4. **Kiểm tra old**: Tránh sử dụng tài liệu trong `old/` vì đã lỗi thời

## Rules vs Reference

### Rules (docs/rules/)
- **Bắt buộc**: AI Agent phải tuân thủ các quy định này
- **Luồng xử lý**: Định nghĩa workflow cho development
- **Ngắn gọn**: Tập trung vào quy định và luồng xử lý
- **Trước khi thực hiện**: Phải đọc rules trước khi bắt đầu task

### Reference (docs/reference/)
- **Tham khảo**: Hướng dẫn và thông tin chi tiết
- **Khi cần thiết**: Chỉ sử dụng khi cần thông tin chi tiết
- **Chi tiết**: Có thể chứa code examples và best practices
- **Sau khi đọc rules**: Tham khảo sau khi đã hiểu quy định

## Quy trình làm việc cho AI Agent

1. **Đọc plan**: Kiểm tra `plan/README.md` để hiểu task tiếp theo
2. **Đọc rules**: Đọc các quy định liên quan trong `rules/`
3. **Tham khảo reference**: Chỉ khi cần thông tin chi tiết
4. **Thực hiện**: Theo đúng luồng xử lý đã định nghĩa
5. **Cập nhật**: Cập nhật progress trong plan khi hoàn thành

## Maintenance

### Regular Updates
- Plan được cập nhật từng phase
- Rules được cập nhật khi có thay đổi quy trình
- Reference được cập nhật khi có thay đổi kỹ thuật

### Quality Assurance
- Đảm bảo tài liệu nhất quán và dễ đọc
- Kiểm tra broken links và references
- Giữ tài liệu đồng bộ với code hiện tại

# Contributing to OSSVN

Bạn không cần join group hay xin membership trước khi bắt đầu.

## Quy tắc chung

- PR nhỏ, rõ scope.
- Task nằm trong repo nơi thay đổi xảy ra.
- Không commit secret hoặc dữ liệu nhạy cảm.
- Nói rõ phần bạn chưa chắc.

## Trước khi mở PR

### 1. Kiểm tra diff

Từ root của repository:

```bash
git status --short
git diff --check
git diff
```

Đọc toàn bộ diff và bỏ thay đổi ngoài scope.

### 2. Chạy automated checks

**Automated check: không có.**

### 3. Kiểm tra thủ công

- Preview các file Markdown đã sửa và kiểm tra heading, list, code block render đúng.
- Mở các internal Markdown link đã thêm hoặc sửa và xác nhận target tồn tại.
- Nếu sửa `SECURITY.md` hoặc `CODE_OF_CONDUCT.md`, kiểm tra email/contact hiển thị đúng và nhất quán.
- Nếu sửa `CONTRIBUTING.md`, `REVIEW_POLICY.md` hoặc `.github/pull_request_template.md`, preview PR template và kiểm tra contribution flow vẫn khớp với tài liệu.

### 4. Kết quả mong đợi

- `git diff --check` không in lỗi và exit code bằng `0`.
- Markdown render đúng, không có internal link hỏng.
- Contact và contribution flow không mâu thuẫn giữa các tài liệu liên quan.

## AI

AI-assisted và vibecoding contributions được welcome.

Nếu submit PR, bạn chịu trách nhiệm về output:

- Đọc diff.
- Thực hiện đúng phần `Trước khi mở PR` của repository đang sửa.
- Không bịa test đã chạy.
- Không đưa secret hoặc dữ liệu không được phép vào AI.
- Không dùng AI làm nguồn kỹ thuật.
- Nói rõ phần bạn chưa chắc.

Khai báo công cụ AI là optional.

## Review

Reviewer xem [REVIEW_POLICY.md](REVIEW_POLICY.md).

Repo riêng có thể có `CONTRIBUTING.md` bổ sung command và manual check cho workflow của repo đó.

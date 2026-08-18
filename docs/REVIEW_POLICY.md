# Review Policy

OSSVN dùng community review làm mặc định.

Review level dựa trên [Risk Levels](RISK_LEVELS.md).

## Nguyên tắc

> **Low barrier to contribute. High standard to merge.**

Không phân biệt code do AI, vibecoder hay senior viết.

Không dùng seniority làm cổng.

Reviewer được chọn theo domain, contribution và chất lượng review trước đó.

## Review Levels

### L0 - Light

Dùng cho thay đổi trivial.

Yêu cầu:

- PR.
- Required automation nếu có.
- Không bắt buộc human approval.

Maintainer vẫn có thể review.

### L1 - Normal

Dùng cho thay đổi thông thường.

Yêu cầu:

- 1 reviewer.
- Relevant CI pass.
- Smoke test nếu user-facing.

### L2 - Strict

Dùng cho production hoặc sensitive change.

Yêu cầu:

- 1 domain reviewer hoặc Code Owner.
- Full relevant CI.
- Manual test critical cases.

### L3 - Critical

Dùng cho security-critical change.

Yêu cầu:

- 2 approvals khi có đủ reviewer.
- Ít nhất một domain reviewer hoặc Code Owner.
- Security checks.
- Critical manual tests.
- Failure hoặc rollback evidence khi phù hợp.

Nếu community chưa có đủ 2 reviewer, không giả approval.

Maintainer phải ghi rõ exception trước merge.

## Content review

### Docs đơn giản

- L0 hoặc L1.

### Concept kỹ thuật

- 1 editor review.
- 1 domain review.

Một người có thể làm cả hai khi thay đổi nhỏ và đủ năng lực.

### Nội dung còn tranh cãi

- 2 domain reviewers nếu có thể.
- Hoặc giữ `draft`.
- Ghi rõ điểm chưa thống nhất.

Fact được quyết định bằng bằng chứng và nguồn tốt hơn, không bằng số đông.

## CODEOWNERS

Dùng CODEOWNERS cho critical paths khi team đã sẵn sàng.

Không bắt mọi file cần Code Owner review ở repo beginner.

## Khi reviewer không đồng ý

1. Tách fact khỏi opinion.
2. Đưa nguồn gốc lên trước.
3. Xác định factual conflict.
4. Ghi uncertainty nếu chưa giải quyết.

Maintainer không dùng quyền merge để thay thế bằng chứng.

## Review định kỳ

Concept ổn định nên kiểm tra lại tối thiểu mỗi 12 tháng.

Nội dung thay đổi nhanh có thể cần 3 đến 6 tháng.

AI có thể hỗ trợ review. AI không được tính là reviewer bắt buộc.

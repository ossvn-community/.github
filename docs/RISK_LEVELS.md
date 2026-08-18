# Risk Levels

OSSVN review theo risk, không theo người viết code.

Công thức:

```text
Repo Risk + Change Risk -> Review Level
```

Dùng mức cao hơn.

## Repo Risk

| Level | Loại repo | Ví dụ |
| --- | --- | --- |
| R0 | Content hoặc data | docs, translation, project index |
| R1 | Low-risk software | demo, learning app, static site |
| R2 | Production software | app, CLI, library, API |
| R3 | Critical software | auth, payment, security, infrastructure |

Risk không phải điểm chất lượng.

R0 vẫn có thể là repo rất chuyên nghiệp.

## Change Risk

### C0 - Trivial

Ví dụ:

- Typo.
- Comment.
- Text.
- Broken link.
- Metadata nhỏ.

### C1 - Normal

Ví dụ:

- Feature nhỏ.
- UI.
- Bug fix.
- Refactor có phạm vi rõ.

### C2 - Sensitive

Ví dụ:

- Dependency.
- CI/CD.
- Data migration.
- Persistence.
- Public API behavior.

### C3 - Critical

Ví dụ:

- Authentication.
- Authorization.
- Secrets.
- Payment.
- Security boundary.
- Release hoặc deployment critical.

Nếu chưa chắc, chọn mức cao hơn và để reviewer hạ xuống.

## Mapping

| Risk | Review |
| --- | --- |
| R0 hoặc C0 | L0 |
| R1 hoặc C1 | L1 |
| R2 hoặc C2 | L2 |
| R3 hoặc C3 | L3 |

Maintainer có thể tăng review level.

Không giảm review level chỉ để merge nhanh.

## Critical paths

Mỗi repo nên xác định file nhạy cảm.

Ví dụ:

```text
.github/workflows/**
auth/**
security/**
migrations/**
deploy/**
release/**
```

Thay đổi critical path có thể tăng Change Risk.

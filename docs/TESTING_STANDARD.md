# Testing Standard

Test phải phù hợp với risk.

Không bắt contributor viết test report dài nếu thay đổi nhỏ.

## Nguyên tắc

> **Machines check repeatable rules. Humans check important behavior.**

Automation nên kiểm tra phần có thể lặp lại.

Manual test tập trung vào user flow và risk khó tự động hóa.

## Status check names

OSSVN dùng tên chuẩn khi áp dụng:

```text
validate
links
test
build
security
```

Không phải repo nào cũng cần tất cả.

Chỉ require check sau khi check đó đã chạy thành công ít nhất một lần.

## Theo Repo Risk

### R0

Tối thiểu:

- `validate`
- `links` nếu repo chứa link

Manual test thường không cần.

### R1

Tối thiểu khi phù hợp:

- `validate`
- `test`
- `build`

User-facing change cần smoke test.

### R2

Tối thiểu:

- Relevant automated tests.
- Build.
- Critical user flow manual test.
- Dependency hoặc security check khi phù hợp.

### R3

Tối thiểu:

- Full relevant CI.
- Security check.
- Critical path manual test.
- Failure case.
- Rollback hoặc recovery test nếu thay đổi hỗ trợ rollback.

## Manual test theo repo

| Repo | Manual test chính |
| --- | --- |
| Docs | Preview và link quan trọng |
| Website | Critical UI flow |
| App | Main user flow |
| CLI | Success và invalid input |
| API | Success và error path |
| Library | Example và compatibility |
| Migration | Migrate và rollback |
| Auth | Success, failure và permission boundary |

## Evidence trong PR

Chỉ cần ngắn:

```text
Automated:
- test
- build

Manual:
- Login
- Create note
- Logout
```

Hoặc:

```text
Manual: Not required - docs only.
```

Không ghi test đã chạy nếu bạn chưa chạy.

## Coverage

OSSVN không đặt một % coverage chung cho mọi repo.

Coverage là signal, không phải mục tiêu duy nhất.

Critical behavior quan trọng hơn số đẹp.

# Review Policy

Reviewer kiểm tra ba việc: thay đổi có đúng không, có đúng scope không, và evidence kiểm tra có đủ không.

Contributor không cần tự tính risk level.

## Ba loại thay đổi

| Loại | Ví dụ | Yêu cầu |
| --- | --- | --- |
| Small | typo, link, wording, metadata | Làm đầy đủ section `Trước khi mở PR` trong `CONTRIBUTING.md` của repo. Human approval có thể không bắt buộc. |
| Normal | feature, bug fix, refactor nhỏ, technical content | Làm đầy đủ `Trước khi mở PR` + 1 reviewer. |
| Sensitive | auth, payment, secrets, security, deploy, migration, critical workflow | Làm đầy đủ `Trước khi mở PR` + Domain/Code Owner + kiểm tra critical path và failure case bị ảnh hưởng. 2 approvals khi project có đủ reviewer. |

Nếu chưa chắc, reviewer chọn mức cao hơn.

## Reviewer kiểm tra

1. Correctness - thay đổi có đúng không?
2. Scope - PR có làm thêm việc không liên quan không?
3. Verification - contributor có ghi đúng command và manual step đã thực hiện không?
4. Security/license - kiểm tra khi thay đổi liên quan.

Command bắt buộc và manual step của từng repo nằm trong `CONTRIBUTING.md` của chính repo đó.

Không yêu cầu test report dài. PR chỉ cần ghi ngắn dưới `Automated:` và `Manual:`.

## Reviewer assignment

Repo có thể dùng `.github/CODEOWNERS` để GitHub tự request reviewer phù hợp khi Pull Request sẵn sàng để review.

Risk ruleset quyết định Code Owner approval có bắt buộc hay không. `CODEOWNERS` chỉ xác định ai phù hợp để review phần code hoặc nội dung tương ứng.

## Technical content

Reviewer kiểm tra:

1. Claim có đúng không?
2. Nguồn có support claim không?
3. Người mới có hiểu không?
4. Có thể viết ngắn hơn mà không đổi nghĩa không?

Fact được quyết định bằng bằng chứng và nguồn tốt hơn, không bằng seniority hay số vote.

## Repo risk - dành cho maintainer

`risk_level` là GitHub Custom Property của repository, dùng để chọn ruleset mặc định:

| Level | Repo |
| --- | --- |
| R0 | Content/data |
| R1 | Low-risk software, demo, static site |
| R2 | Production app, CLI, library, API |
| R3 | Auth, payment, security, infrastructure |

Contributor không cần tự phân loại PR theo R0-R3.

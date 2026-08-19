# Micro-task Standard

Micro-task phải giúp contributor biết chính xác cần làm gì.

Task nhỏ không có nghĩa là task mơ hồ.

## Task nằm ở đâu?

Task phải là GitHub Issue trong **repository nơi thay đổi thực sự xảy ra**.

Ví dụ:

```text
it-in-plain-vietnamese
└── Issues
    └── [5-min] Sửa ví dụ trong concept Git
```

Không duy trì một central task database bằng tay nếu chưa có nhu cầu aggregate thật.

## Labels

Thời gian:

- `5-min`
- `15-min`
- `30-min`

Loại:

- `docs`
- `code`
- `translation`
- `review`
- `design`
- `data`

Onboarding:

- `first-pr`
- `good first issue`
- `mentor-ready`
- `no-setup`

Không cần repo nào cũng phải dùng đủ label.

## Tiêu chuẩn `5-min`

Một task chỉ được gắn `5-min` khi:

1. Chỉ có một outcome.
2. Vị trí cần sửa được chỉ rõ.
3. Không cần hiểu architecture.
4. Không cần local setup nếu có thể.
5. Acceptance criteria có tối đa 3 ý.
6. Phạm vi thường là một file hoặc thay đổi nhỏ tương đương.
7. Contributor có thể bỏ task mà không block project.

`5-min` tính từ lúc contributor hiểu task và bắt đầu làm, không tính thời gian tạo GitHub account.

## Issue nên có

```text
Goal
File / location
Done when
Required checks
Manual test nếu có
Risk / review level nếu cần
AI: Welcome / Restricted + lý do
Help / context
```

Ví dụ:

```text
Fix typo trong concept Git

File: concepts/git-github/git.md

Done when:
- Sửa đúng typo.
- Không thay đổi nội dung khác.

Checks:
- links

AI: Welcome
```

## AI-friendly task

Nếu AI không phù hợp do dữ liệu nhạy cảm hoặc constraint khác, nói rõ lý do.

Không cấm AI chỉ vì maintainer thích code thủ công.

## Review contract

Issue nên nói trước:

- Required automation.
- Manual test.
- Review level nếu khác mặc định.
- Critical file nếu có.

Không đợi contributor làm xong mới thêm yêu cầu lớn.

## Không được gọi là `5-min`

Không gắn label nếu task cần:

- Setup phức tạp.
- Đọc nhiều file để hiểu context.
- Tự thiết kế solution.
- Debug lỗi chưa rõ nguyên nhân.
- Chờ maintainer cung cấp thông tin.

## Kiểm tra task

Trước khi publish một beginner task, đọc lại như người chưa biết project.

Nếu người đó không biết phải bắt đầu ở file nào và done khi nào, viết lại task.

# Track1 — Day 17 — Finding and Validating Pain Points

**Repo:** `Track1_Day17_2A202601721_CaoNhatMinh`
**Case được giao:** Case B — AI Notes: Personal Learning Notes

---

## 1. Đề bài

### Đọc trước khi bắt đầu

Nhóm nhận một **solution directive AI** đã được mô tả khá cụ thể. Nhiệm vụ **không phải chứng minh solution đó đúng**, mà đi ngược để hình thành giả thuyết về **user, situation, job và pain**; sau đó thiết kế và luyện một **problem interview** không làm lộ solution.

### Bài này đang nói về điều gì?

- Reverse-engineering **không tìm ra pain point**; nó chỉ tạo ra **giả thuyết** để đi kiểm chứng.
- Trong problem interview, **hành vi đã xảy ra** đáng tin hơn ý kiến, lời khen và dự đoán về tương lai.
- Buổi luyện giúp **phát hiện lỗi trong cách hỏi và sửa guide**; **không đủ** để tuyên bố pain đã được validated.

### Luồng làm việc

```
Problem Hypothesis  ->  Conversation Guide  ->  Interview Practice  ->  Guide Revision
```

Nhóm nhận một solution directive: một tính năng AI đã được mô tả tương đối cụ thể. **Đừng bắt đầu bằng việc hoàn thiện tính năng đó.** Hãy đi ngược để trả lời:

> Solution này đang dựa trên **giả định nào** về user, tình huống, job và pain — và **bằng chứng thực tế** có ủng hộ giả định đó không?

### Luật của bài lab

1. **Không cho interviewee xem solution directive.** Đây là problem interview, không phải concept interview.
2. **Hỏi về quá khứ cụ thể.** Ưu tiên "lần gần nhất" hơn "thường thì" hoặc "bạn có muốn".
3. **Mỗi người phỏng vấn một người ngoài nhóm.** Không dùng câu trả lời của thành viên cùng nhóm làm evidence.
4. **Ghi facts trước, diễn giải sau.** Lời nói, hành vi và workaround của user phải được tách khỏi kết luận của nhóm.
5. **Không bảo vệ giả thuyết.** Evidence làm giả thuyết yếu đi cũng là evidence có giá trị.
6. **Không tuyên bố validated.** Chặng 3 là phần luyện kỹ năng, không phải một vòng field research chính thức.

### Sử dụng AI trong bài lab

**Được phép:** dùng AI để gợi ý cách diễn đạt hoặc rà soát câu hỏi dẫn dắt.

**Không được phép:** dùng AI để tạo interview data, bịa quote, suy diễn chi tiết user chưa nói, hoặc viết reflection thay cho việc tự nghe lại cuộc phỏng vấn.

Mọi cách dùng AI **phải được khai báo trong README này** (xem mục 4).

---

## 2. Solution Directive — Case B: AI Notes (Personal Learning Notes)

Trong khi học, học viên có thể **highlight** một đoạn nội dung, đánh dấu **"Chưa hiểu"**, hoặc viết một **câu hỏi** hay **ghi chú ngắn**.

Khi bài học kết thúc, **AI Notes** kết hợp những dấu vết này với nội dung bài để tạo một **bản ghi chú có cấu trúc**. Học viên có thể **chỉnh sửa và xác nhận trước khi lưu**.

| Thành phần | Solution đã mô tả |
|---|---|
| **Trigger** | Học viên hoàn thành bài học |
| **Input** | Nội dung bài, highlights, điểm "Chưa hiểu", câu hỏi và ghi chú cá nhân |
| **AI action** | Chọn lọc, nhóm và tổ chức thông tin |
| **Output** | Bản ghi chú cá nhân có cấu trúc |
| **User control** | Học viên chỉnh sửa và xác nhận trước khi lưu |

### Tiêu chí chọn người phỏng vấn

Người phù hợp để phỏng vấn: **trong bảy ngày gần đây đã ghi chú, highlight hoặc lưu lại nội dung để xem sau.**

> Lưu ý: tiêu chí này mô tả **hành vi đã xảy ra trong quá khứ gần**, không phải thái độ hay ý định. Dùng đúng tiêu chí này để screening, không nới lỏng thành "người có hứng thú với việc ghi chú".

---

## 3. Cấu trúc repo

| File / thư mục | Nội dung | Trạng thái |
|---|---|---|
| `README.md` | Đề bài, solution directive, khai báo AI | Đã có |
| `01-problem-hypothesis.md` | Solution → Change → Actor → Situation & Job → Pain → Evidence, chốt problem hypothesis + Solution Parking Lot | Khung đã dựng, đang điền |
| `02-conversation-guide-v1.md` | Big 3 → tiêu chí tuyển người → lời mở đầu → story opener → Big 3 Questions → probe bank → rà soát & phân công | Khung đã dựng, đang điền |
| `03-interview-notes/example-interview-record.md` | **Bản mẫu** Interview Record để mỗi thành viên copy ra bản của mình | Đã có |
| `03-interview-notes/interview-record-*.md` | Facts thô từng buổi phỏng vấn (ghi tách riêng khỏi diễn giải) — mỗi thành viên một file | Chưa làm |
| `04-conversation-guide-v2.md` | Guide sau khi sửa + ghi rõ đã đổi gì và vì sao | Chưa làm |
| `05-reflection.md` | Reflection cá nhân sau khi tự nghe lại phỏng vấn | Chưa làm |

---

## 3b. Chặng 3 — Cách các thành viên dùng `03-interview-notes/`

**Yêu cầu:** mỗi thành viên hoàn thành **một lượt làm interviewer**, có **Interview Record** và **bản ghi đã được người tham gia đồng ý**.

**Ba bước:**

1. Copy `03-interview-notes/example-interview-record.md`
2. Đổi tên thành `03-interview-notes/interview-record-<tên-bạn>.md`
3. Điền vào bản copy của mình. **Không sửa file mẫu.**

| Thành viên | File của mình | Mã người tham gia | Đúng tiêu chí tuyển | Đã có consent | Đã nộp |
|---|---|---|---|---|---|
| _(điền tên)_ | `interview-record-....md` | | ☐ | ☐ | ☐ |
| _(điền tên)_ | `interview-record-....md` | | ☐ | ☐ | ☐ |
| _(điền tên)_ | `interview-record-....md` | | ☐ | ☐ | ☐ |

**Ba luật không được vi phạm ở chặng này:**

- Người tham gia phải là **người ngoài nhóm**. Câu trả lời của thành viên cùng nhóm không tính là evidence.
- Bản ghi phải **được người tham gia đồng ý**. Trong repo chỉ dùng **mã người tham gia**, không có tên thật.
- **Lời khen** hoặc **"mình sẽ dùng"** **không được coi là bằng chứng về pain** — đẩy xuống mục *Bãi đỗ* trong Interview Record.

**Nhắc lại:** ghi **facts trước, diễn giải sau**. Trong mỗi Interview Record, phần trên là những gì user nói và làm; phần dưới mới là suy luận của người phỏng vấn. Hết chặng 3 vẫn **không tuyên bố validated**.

---

## 4. Khai báo sử dụng AI

> Mục này bắt buộc theo luật của bài lab. Cập nhật mỗi khi có thêm một lần dùng AI.

| # | Công cụ | Dùng vào việc gì | Phạm vi output của AI | Người chịu trách nhiệm nội dung cuối |
|---|---|---|---|---|
| 1 | Claude (Cowork) | Đọc hiểu đề bài và soạn README.md từ nội dung đề bài + solution directive Case B do nhóm cung cấp | Chỉ định dạng và sắp xếp lại nội dung đề bài; không thêm giả thuyết, dữ liệu hay kết luận mới | _(điền tên)_ |
| 2 | Claude (Cowork) | Dựng khung file `01-problem-hypothesis.md` theo đúng template 6 bước của bài lab | Chỉ tạo cấu trúc file, chép lại directive nguyên văn và bộ câu hỏi dẫn dắt; **toàn bộ ô phân tích để trống cho nhóm tự điền** | _(điền tên)_ |
| 3 | Claude (Cowork) | Dựng khung file `02-conversation-guide-v1.md` theo đúng template của bài lab | Chỉ tạo cấu trúc file, chép lại probe bank, bảng ba phản xạ và checklist rà soát; **Big 3, tiêu chí tuyển, lời mở đầu và toàn bộ câu hỏi phỏng vấn để trống cho nhóm tự viết** | _(điền tên)_ |

| 4 | Claude (Cowork) | Dựng **bản mẫu trống** `03-interview-notes/example-interview-record.md` và mục hướng dẫn 3b trong README | Chỉ tạo cấu trúc bảng ghi chép và checklist quy trình; **không có nội dung phỏng vấn, quote hay diễn giải nào** — toàn bộ do thành viên tự điền sau khi phỏng vấn | _(điền tên)_ |

**Cam kết:** không có interview data, quote, chi tiết user hay reflection nào trong repo này được sinh ra bởi AI.

---

## 5. Ghi chú tiến độ

- [x] Đọc hiểu đề bài và dựng README
- [ ] Chặng 1 — Problem Hypothesis
- [ ] Chặng 2 — Conversation Guide
- [ ] Chặng 3 — Interview Practice (mỗi người 1 người ngoài nhóm)
- [ ] Chặng 4 — Guide Revision + Reflection

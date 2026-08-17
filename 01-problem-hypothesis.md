# Chặng 1 — Problem Hypothesis

**Case đã chọn:** Case B — AI Notes: Personal Learning Notes

> **Nguyên tắc xuyên suốt chặng này:** reverse-engineering **không tìm ra pain point**, nó chỉ tạo ra **giả thuyết** để mang đi kiểm chứng. Không ô nào dưới đây được điền bằng kết luận; tất cả đều là thứ cần đem đi hỏi.

---

## 1. Solution — Gỡ solution khỏi hình thức cụ thể

Ghi lại directive nguyên văn, sau đó diễn đạt lại dưới dạng một **capability trung tính**.

**Câu hỏi dẫn dắt:**

- Câu nào trong directive đang mô tả giao diện, tên feature hoặc công nghệ?
- Nếu bỏ tên nút, màn hình và AI action, khả năng cần tạo ra là gì?
- Nhóm có đang mặc định cách triển khai được giao là cách duy nhất không?
- Capability có thể được mô tả mà không dùng tên feature không?

### Solution directive (nguyên văn)

> Trong khi học, học viên có thể highlight một đoạn nội dung, đánh dấu "Chưa hiểu", hoặc viết một câu hỏi hay ghi chú ngắn.
>
> Khi bài học kết thúc, AI Notes kết hợp những dấu vết này với nội dung bài để tạo một bản ghi chú có cấu trúc. Học viên có thể chỉnh sửa và xác nhận trước khi lưu.

| Thành phần | Solution đã mô tả                                                              |
| ------------ | ---------------------------------------------------------------------------------- |
| Trigger      | Học viên hoàn thành bài học                                                  |
| Input        | Nội dung bài, highlights, điểm "Chưa hiểu", câu hỏi và ghi chú cá nhân |
| AI action    | Chọn lọc, nhóm và tổ chức thông tin                                         |
| Output       | Bản ghi chú cá nhân có cấu trúc                                             |
| User control | Học viên chỉnh sửa và xác nhận trước khi lưu                             |

### Bóc tách: phần nào là hình thức triển khai?

| Chi tiết trong directive                        | Đây là gì? (giao diện / tên feature / công nghệ / khả năng) | Có bắt buộc không? |
| ------------------------------------------------ | --------------------------------------------------------------------- | ---------------------- |
| "AI Notes"                                       | Tên feature / thương hiệu                                            | Không — có thể gọi tên khác mà không đổi bản chất |
| Nút highlight                                   | Giao diện cụ thể                                                     | Không — khả năng cốt lõi là "đánh dấu một đoạn nội dung là quan trọng ngay lúc đang học"; có thể làm bằng thao tác khác |
| Nhãn "Chưa hiểu"                              | Giao diện cụ thể (label)                                             | Không — khả năng cốt lõi là "gắn cờ một điểm không hiểu ngay lúc phát sinh, để khỏi phải nhớ lại sau" |
| Ô ghi chú / câu hỏi ngắn                    | Giao diện cụ thể                                                     | Không — khả năng cốt lõi là "ghi lại một suy nghĩ/câu hỏi ngắn ngay tại thời điểm nó xuất hiện" |
| "AI kết hợp và tổ chức"                     | Công nghệ / cách triển khai cụ thể                                    | Không bắt buộc phải là AI — khả năng cốt lõi là "biến các dấu vết rời rạc thành một bản tổng hợp có cấu trúc mà user không phải tự làm thủ công" |
| Bước chỉnh sửa & xác nhận trước khi lưu | Một phần giao diện, nhưng phần "được kiểm soát đầu ra" có thể là khả năng cần thiết | Hình thức (nút xác nhận) thì không bắt buộc; nhưng ở mức khái niệm, việc user giữ quyền kiểm soát nội dung cuối có thể là điều cần giữ |
| Thời điểm chạy: khi bài học kết thúc     | Hình thức triển khai (thời điểm trigger)                              | Không — có thể tổng hợp theo yêu cầu, theo phiên, hoặc định kỳ |

### Capability trung tính

_(Mô tả khả năng cần tạo ra, không dùng tên feature, không nhắc AI, không nhắc màn hình.)_
```
Khả năng giúp người học gom lại những dấu vết rời rạc phát sinh trong lúc học (điểm quan trọng, điểm chưa hiểu, câu hỏi/ghi chú) thành một bản tổng hợp có cấu trúc mà không cần tự làm thủ công, đồng thời vẫn giữ cho người học quyền kiểm soát nội dung cuối cùng trước khi lưu lại.
```

---

## 2. Change — Làm lộ chuỗi thay đổi được kỳ vọng

Đừng nhảy thẳng từ feature tới outcome. Viết các **mắt xích** mà team đang ngầm tin sẽ xảy ra.

**Câu hỏi dẫn dắt:**

- User sẽ biết hoặc làm được điều gì khác?
- Hành vi nào phải thay đổi để outcome xảy ra?
- Trạng thái hoặc kết quả nào được kỳ vọng thay đổi?
- Đâu là **output** team tạo ra, đâu là **outcome** team chỉ có thể ảnh hưởng?
- Nếu user không thay đổi hành vi, solution còn tạo được outcome không?


```text
Solution → User tin tưởng & quay lại mở bản ghi chú → User dùng bản ghi chú để ôn tập/tra cứu → Outcome: User nắm/nhớ nội dung bài học tốt hơn theo thời gian
```

### Các thay đổi được kỳ vọng

1. `User tin tưởng và mở lại bản ghi chú do AI tạo ra, thay vì đọc lại toàn bộ bài học từ đầu.`
2. `User dùng các dấu vết (highlight, "chưa hiểu", câu hỏi) trong lúc học nhiều/thật hơn, vì biết chúng sẽ được tổng hợp thành thứ hữu ích.`
3. `User chủ động quay lại xem bản ghi chú ở một thời điểm sau (ôn tập, trước khi làm bài), thay vì tạo ra rồi bỏ quên.`

### Tách output và outcome


|                                            | Nội dung | Team kiểm soát được đến đâu? |
| ------------------------------------------ | --------- | ------------------------------------- |
| **Output** (team tạo ra)            | Một bản ghi chú cá nhân có cấu trúc, được tạo và lưu lại sau mỗi bài học | Kiểm soát hoàn toàn — team quyết định nội dung và hình thức bản ghi chú |
| **Outcome** (team chỉ ảnh hưởng) | User có quay lại dùng bản ghi chú để ôn tập hay không; user có nắm/nhớ nội dung bài học tốt hơn hay không | Chỉ ảnh hưởng — phụ thuộc vào việc user có tin tưởng và thực sự dùng bản ghi chú sau khi nó được tạo ra |

**Mắt xích yếu nhất trong chuỗi (nếu gãy thì outcome không xảy ra):**

```
User có thực sự quay lại mở và dùng bản ghi chú sau khi nó được tạo ra hay không. Nếu bước này không xảy ra, toàn bộ chuỗi outcome sụp đổ, bất kể bản ghi chú được tổ chức tốt đến đâu.
```

---

## 3. Actor — Xác định các nhóm người có liên quan

Một solution có thể liên quan đến nhiều nhóm user hoặc stakeholder khác nhau. **Người trực tiếp sử dụng feature chưa chắc là người đang gặp pain chính**, phải thay đổi hành vi hoặc chịu hậu quả.

> Ví dụ với AI Support Radar trên VLearn: *learner* là người có hành vi học tập được phân tích; *instructor* là người xem Support Queue và quyết định can thiệp; *coach* là người có thể trực tiếp hỗ trợ learner. Cả ba đều là actor liên quan nhưng có job, pain và lợi ích khác nhau.

**Câu hỏi dẫn dắt:**

- Ai trực tiếp sử dụng solution?
- Ai trực tiếp trải nghiệm pain?
- Ai phải thay đổi hành vi để outcome xảy ra?
- Ai chịu hậu quả nếu problem không được giải quyết?
- Ai hưởng lợi gián tiếp?
- Người nhận feature có chắc là người sở hữu pain chính không?


| Actor | Họ đang làm gì? | Pain hoặc hậu quả có thể có | Họ hưởng lợi thế nào? |
| ----- | ------------------- | --------------------------------- | --------------------------- |
| Học viên — lúc đang học | Nghe/đọc bài, tranh thủ đánh dấu nhanh điều thấy quan trọng hoặc chưa hiểu | Có thể không đủ thời gian/sự tập trung để đánh dấu đầy đủ; sợ đánh dấu làm gián đoạn mạch học | Ghi chú nhanh mà không phải dừng lại viết dài |
| Học viên — lúc ôn tập sau đó | Cố nhớ lại nội dung đã học để chuẩn bị làm bài / áp dụng | Quên nội dung, không tìm lại được ý quan trọng, phải đọc lại toàn bộ bài học tốn thời gian | Có bản tổng hợp sẵn để tra cứu nhanh, tiết kiệm thời gian ôn tập |
| Instructor / người tạo khoá học | Theo dõi tiến độ, thiết kế nội dung bài học | Không biết học viên có thực sự ôn tập lại hay không; khó biết điểm nào học viên phổ biến "chưa hiểu" | Nếu học viên ôn tập tốt hơn → kết quả học tập / tỉ lệ hoàn thành khoá cao hơn |
| Đội vận hành sản phẩm / nền tảng học | Theo dõi retention, completion rate | Nếu học viên không quay lại nền tảng để ôn tập, engagement giảm | Feature có thể giữ chân user quay lại nền tảng nhiều hơn |

**Actor nhóm chọn để điều tra trước:**

```
Học viên — lúc ôn tập sau đó
```

**Vì sao chọn nhánh này thay vì actor khác:**

```
Đây là actor có khả năng cao nhất đang trải nghiệm pain rõ ràng và cụ thể (khó tìm lại ý
quan trọng, phải đọc lại toàn bộ bài, quên nội dung), trong khi "học viên lúc đang học" thì
pain (nếu có) thường ẩn và khó gợi ra bằng phỏng vấn — họ có thể đang học bình thường mà
không tự nhận ra vướng mắc. Chọn "lúc ôn tập" cũng giúp hỏi về một hành vi cụ thể, gần đây,
dễ kể lại (ví dụ: "lần gần nhất bạn cố nhớ lại nội dung một bài đã học, chuyện gì đã xảy
ra?"), thay vì hỏi về một trạng thái mơ hồ.
```

---

## 4. Situation & Job — User đang cố làm gì trong tình huống nào?

Chọn **một khoảnh khắc cụ thể** mà actor có thể đã trải qua. Mô tả hoàn cảnh và việc họ đang cố hoàn thành, **chưa kết luận pain nằm ở đâu**. Job phải **còn tồn tại ngay cả khi bỏ AI và feature khỏi bối cảnh**.

**Câu hỏi dẫn dắt:**

- Tình huống bắt đầu khi chuyện gì xảy ra?
- Lúc đó user đang cố hoàn thành việc gì?
- Vì sao việc đó quan trọng với họ?
- Hiện tại họ đang thực hiện việc đó như thế nào?
- Họ bắt đầu gặp vướng mắc ở điểm nào?

```text
Tình huống bắt đầu
→ User muốn hoàn thành việc gì
→ Hiện tại họ làm như thế nào
→ Điểm bắt đầu gặp vướng mắc
```

### Mô tả Situation & Job

> Khi **[tình huống/trigger]**, **[actor]** đang cố **[việc cần hoàn thành]** bằng cách **[cách họ đang làm hiện tại]**.

```
..........................................................................................
..........................................................................................
```

### JTBD Hypothesis

> Khi **[situation]**, tôi muốn **[progress]**, để có thể **[desired outcome]**.

```
..........................................................................................
..........................................................................................
```

**Kiểm tra:** bỏ hết AI và feature ra khỏi câu trên — job này còn tồn tại không?  ☐ Có  ☐ Không

---

## 5. Pain — Viết các cách giải thích cạnh tranh

Pain là **barrier cản actor hoàn thành job** và **consequence** đi kèm; **không phải sự vắng mặt của feature**.

**Câu hỏi dẫn dắt:**

- Barrier cụ thể nào đang cản actor hoàn thành job?
- Actor thiếu thông tin, kỹ năng, thời gian hay sự hỗ trợ?
- Họ có nhận ra mình đang gặp pain không?
- Nếu không xử lý, hậu quả thực tế là gì?
- Actor có thể sống chung với sự bất tiện này không?
- Có cách giải thích nào khác cho cùng hành vi?
- Pain có còn tồn tại nếu solution directive biến mất khỏi đầu nhóm không?

### Pain Hypothesis A

> Khi **[situation]**, **[actor]** gặp khó khăn trong việc **[job]** vì **[barrier]**, dẫn đến **[consequence]**.

```
..........................................................................................
..........................................................................................
```

### Pain Hypothesis B — cách giải thích cạnh tranh

> Khi **[situation]**, **[actor]** gặp khó khăn trong việc **[job]** vì **[barrier]**, dẫn đến **[consequence]**.

```
..........................................................................................
..........................................................................................
```

**Giả thuyết nhóm chọn để điều tra trước:**  ☐ A  ☐ B

**Lý do chọn:**

```
..........................................................................................
```

---

## 6. Evidence — Xác định điều cần tìm trước khi viết câu hỏi

Evidence phải đến từ **sự kiện, hành vi, workaround và hậu quả đã xảy ra**; một problem statement nghe hợp lý **chưa phải** evidence.

**Câu hỏi dẫn dắt:**

- User có kể được một sự kiện gần đây với trình tự cụ thể không?
- Trong sự kiện đó, họ thực sự đã làm gì?
- Họ đã dùng workaround nào và bỏ ra bao nhiêu công sức?
- Tình huống có lặp lại không?
- Hậu quả quan sát được là gì?
- Họ đã chủ động tìm cách xử lý chưa?
- Điều gì cho thấy pain **không** đủ quan trọng?
- Evidence nào sẽ khiến nhóm **sửa hoặc bác bỏ** hypothesis?

| Cần kiểm tra        | Evidence làm nhóm tin hơn | Evidence làm nhóm nghi ngờ hoặc bác bỏ |
| --------------------- | ---------------------------- | -------------------------------------------- |
| Situation có thật   |                              |                                              |
| Pain có ý nghĩa    |                              |                                              |
| Workaround tồn tại  |                              |                                              |
| Consequence tồn tại |                              |                                              |
| Pattern có lặp      |                              |                                              |

---

## Chốt Problem Hypothesis và park solution

**Problem Hypothesis nhóm mang sang Chặng 2:**

```
..........................................................................................
..........................................................................................
```

**Điều gì phải đúng để giả thuyết đứng vững:**

```
..........................................................................................
..........................................................................................
```

**Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:**

```
..........................................................................................
..........................................................................................
```

### Solution Parking Lot

Brainstorm **ít nhất năm hướng**, trong đó **ít nhất một hướng không sử dụng AI**.

| # | Hướng giải quyết có thể có | AI / Không sử dụng AI |
| - | --------------------------------- | ------------------------ |
| 1 |                                   |                          |
| 2 |                                   |                          |
| 3 |                                   |                          |
| 4 |                                   |                          |
| 5 |                                   |                          |

> Sau khi điền xong bảng này, **cất toàn bộ solution lại**. Chặng 2 không được để bất kỳ hướng nào ở trên lọt vào câu hỏi phỏng vấn.

---

## Tiêu chí tự kiểm trước khi sang Chặng 2

- [ ] Capability trung tính viết được mà không dùng tên feature, không nhắc AI
- [ ] Chuỗi Change có ít nhất một mắt xích là **hành vi user phải thay đổi**
- [ ] Đã liệt kê ≥ 3 actor và nói rõ vì sao chọn actor này
- [ ] Job còn tồn tại khi bỏ AI và feature ra khỏi bối cảnh
- [ ] Pain viết dưới dạng **barrier + consequence**, không phải "thiếu tính năng X"
- [ ] Có Pain Hypothesis B thật sự cạnh tranh, không phải bản diễn đạt lại của A
- [ ] Mỗi dòng Evidence đều có cột **bác bỏ** được điền
- [ ] Parking Lot có ≥ 5 hướng và ≥ 1 hướng không dùng AI
- [ ] Không có chỗ nào trong file này dùng chữ "validated"

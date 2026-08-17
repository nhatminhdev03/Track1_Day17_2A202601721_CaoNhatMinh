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

| Chi tiết trong directive                        | Đây là gì? (giao diện / tên feature / công nghệ / khả năng)                                  | Có bắt buộc không?                                                                                                                                                           |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "AI Notes"                                       | Tên feature / thương hiệu                                                                          | Không — có thể gọi tên khác mà không đổi bản chất                                                                                                                   |
| Nút highlight                                   | Giao diện cụ thể                                                                                    | Không — khả năng cốt lõi là "đánh dấu một đoạn nội dung là quan trọng ngay lúc đang học"; có thể làm bằng thao tác khác                                 |
| Nhãn "Chưa hiểu"                              | Giao diện cụ thể (label)                                                                            | Không — khả năng cốt lõi là "gắn cờ một điểm không hiểu ngay lúc phát sinh, để khỏi phải nhớ lại sau"                                                      |
| Ô ghi chú / câu hỏi ngắn                    | Giao diện cụ thể                                                                                    | Không — khả năng cốt lõi là "ghi lại một suy nghĩ/câu hỏi ngắn ngay tại thời điểm nó xuất hiện"                                                              |
| "AI kết hợp và tổ chức"                     | Công nghệ / cách triển khai cụ thể                                                               | Không bắt buộc phải là AI — khả năng cốt lõi là "biến các dấu vết rời rạc thành một bản tổng hợp có cấu trúc mà user không phải tự làm thủ công" |
| Bước chỉnh sửa & xác nhận trước khi lưu | Một phần giao diện, nhưng phần "được kiểm soát đầu ra" có thể là khả năng cần thiết | Hình thức (nút xác nhận) thì không bắt buộc; nhưng ở mức khái niệm, việc user giữ quyền kiểm soát nội dung cuối có thể là điều cần giữ               |
| Thời điểm chạy: khi bài học kết thúc     | Hình thức triển khai (thời điểm trigger)                                                         | Không — có thể tổng hợp theo yêu cầu, theo phiên, hoặc định kỳ                                                                                                      |

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
Solution
→ [HÀNH VI 1 — trong lúc học] User thực sự dừng lại để đánh dấu điều quan trọng
  hoặc chỗ chưa hiểu, đủ nhiều và đủ đúng chỗ để có cái mà tổng hợp
→ [Output] Hệ thống tạo ra một bản tổng hợp có cấu trúc từ những dấu vết đó
→ [HÀNH VI 2 — vài ngày sau] Khi có việc buộc phải dùng lại nội dung, user mở
  bản tổng hợp đó, thay vì mở lại bài học và tua tìm như trước
→ Outcome: user lấy lại được thứ mình cần nhanh hơn, ít phải bỏ dở việc đang làm
```

> **Chuỗi này đòi HAI hành vi phải đổi, không phải một.** Hành vi 1 xảy ra trong lúc học, hành vi 2 xảy ra vài ngày sau ở một bối cảnh hoàn toàn khác. Chỉ cần một trong hai không xảy ra là outcome không tới. Bản vẽ ban đầu chỉ có hành vi 2 nên đã che mất rủi ro của hành vi 1.

### Các thay đổi được kỳ vọng

1. `Trong lúc học, user dừng lại đánh dấu / ghi lại điều quan trọng hoặc chỗ chưa hiểu — thay vì học một mạch rồi thôi.`
2. `Khi cần dùng lại nội dung sau đó, user mở bản tổng hợp — thay vì mở lại bài học từ đầu và tua tìm.`
3. `User coi bản tổng hợp là chỗ đáng tin để tra cứu — biểu hiện là quay lại nó nhiều lần chứ không chỉ mở đúng một lần rồi bỏ.`

_(Thay đổi 3 là **trạng thái tin tưởng**, không quan sát trực tiếp được — nên viết lại theo dấu hiệu hành vi: mở lại bao nhiêu lần.)_

### Tách output và outcome

|                                            | Nội dung                                                                                                                    | Team kiểm soát được đến đâu?                                                                                          |
| ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Output** (team tạo ra)            | Một bản ghi chú cá nhân có cấu trúc, được tạo và lưu lại sau mỗi bài học                                   | Kiểm soát hoàn toàn — team quyết định nội dung và hình thức bản ghi chú                                          |
| **Outcome** (team chỉ ảnh hưởng) | User có quay lại dùng bản ghi chú để ôn tập hay không; user có nắm/nhớ nội dung bài học tốt hơn hay không | Chỉ ảnh hưởng — phụ thuộc vào việc user có tin tưởng và thực sự dùng bản ghi chú sau khi nó được tạo ra |

**Mắt xích yếu nhất trong chuỗi (nếu gãy thì outcome không xảy ra):**

```
Hành vi 2: user có thực sự quay lại mở và dùng bản tổng hợp hay không. Nếu bước
này không xảy ra thì toàn bộ chuỗi sụp, bất kể bản tổng hợp được tổ chức tốt
đến đâu.

Nhưng hành vi 1 mới là mắt xích ĐI TRƯỚC và ít được để ý: nếu trong lúc học
user không để lại dấu vết nào (hoặc để lại rất thưa, hoặc ghi ở chỗ khác ngoài
nền tảng), thì không có gì để tổng hợp và chuỗi đứt ngay từ mắt xích đầu —
lúc đó hành vi 2 không bao giờ có cơ hội được kiểm chứng.

→ Chặng 2 phải hỏi được CẢ HAI: lần gần nhất họ ghi lại gì trong lúc học, và
  lần gần nhất họ mở lại thứ đã ghi.
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

| Actor                                         | Họ đang làm gì?                                                                      | Pain hoặc hậu quả có thể có                                                                                          | Họ hưởng lợi thế nào?                                                                     |
| --------------------------------------------- | ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Học viên — lúc đang học                 | Nghe/đọc bài, tranh thủ đánh dấu nhanh điều thấy quan trọng hoặc chưa hiểu | Có thể không đủ thời gian/sự tập trung để đánh dấu đầy đủ; sợ đánh dấu làm gián đoạn mạch học   | Ghi chú nhanh mà không phải dừng lại viết dài                                           |
| Học viên — lúc ôn tập sau đó          | Cố nhớ lại nội dung đã học để chuẩn bị làm bài / áp dụng                  | Quên nội dung, không tìm lại được ý quan trọng, phải đọc lại toàn bộ bài học tốn thời gian             | Có bản tổng hợp sẵn để tra cứu nhanh, tiết kiệm thời gian ôn tập                   |
| Instructor / người tạo khoá học          | Theo dõi tiến độ, thiết kế nội dung bài học                                     | Không biết học viên có thực sự ôn tập lại hay không; khó biết điểm nào học viên phổ biến "chưa hiểu" | Nếu học viên ôn tập tốt hơn → kết quả học tập / tỉ lệ hoàn thành khoá cao hơn |
| Đội vận hành sản phẩm / nền tảng học | Theo dõi retention, completion rate                                                     | Nếu học viên không quay lại nền tảng để ôn tập, engagement giảm                                                | Feature có thể giữ chân user quay lại nền tảng nhiều hơn                               |

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

> **Neo theo actor đã chọn ở mục 3:** *Học viên — lúc ôn tập sau đó.* Vì vậy tình huống **không** bắt đầu lúc học xong (đó là trigger của solution), mà bắt đầu lúc học viên **có việc buộc phải dùng lại nội dung đã học**.

```text
Có việc buộc phải dùng lại nội dung của một bài đã học cách đó vài ngày
(làm bài tập, chuẩn bị kiểm tra, áp dụng vào việc thật, hoặc học bài kế tiếp
cần kiến thức bài trước)
→ Học viên muốn lấy lại đúng phần mình cần, đủ nhanh để làm tiếp việc đang dở
→ Hiện tại họ mở lại bài học và tua tới đoạn nhớ mang máng, lục lại những gì
  đã lưu ở nhiều nơi khác nhau, hỏi người khác, hoặc tra lại từ đầu
→ Bắt đầu vướng khi không nhớ nội dung đó nằm ở đâu, hoặc thứ tìm lại được
  không đủ để hiểu lại, nên phải xem lại nhiều hơn dự tính
```

### Mô tả Situation & Job

> Khi **[tình huống/trigger]**, **[actor]** đang cố **[việc cần hoàn thành]** bằng cách **[cách họ đang làm hiện tại]**.

```
Khi có việc buộc phải dùng lại nội dung của một bài đã học cách đó vài ngày —
làm bài tập, chuẩn bị kiểm tra, hoặc áp dụng vào việc thật — học viên đang cố
lấy lại đúng phần mình cần, đủ nhanh để làm tiếp việc đang dở, bằng cách mở lại
bài học và tua tìm, lục lại những gì mình đã lưu, hoặc hỏi người khác.
```

### JTBD Hypothesis

> Khi **[situation]**, tôi muốn **[progress]**, để có thể **[desired outcome]**.

```
Khi tôi cần dùng lại nội dung của một bài đã học nhưng không còn nhớ rõ, tôi
muốn lấy lại đúng phần mình cần đủ nhanh để không phải dừng việc đang làm, để
có thể hoàn thành việc đó đúng hạn mà không phải học lại bài từ đầu.
```

**Kiểm tra:** bỏ hết AI và feature ra khỏi câu trên — job này còn tồn tại không?  ☑ Có  ☐ Không

_Lý do: câu mô tả không dùng từ nào gắn với nền tảng (highlight, ghi chú trong bài, bản tổng hợp). Người đọc sách giấy hay xem một video bất kỳ vẫn gặp đúng tình huống này._

**Lưu ý mang sang chặng 2:** situation này xảy ra **vài ngày sau** buổi học, nên tiêu chí tuyển "7 ngày gần đây đã ghi chú / highlight / lưu lại" chưa chắc chạm tới nó. Recruitment check cần thêm một vế về **lần gần nhất phải dùng lại nội dung đã học**, nếu không sẽ tuyển đúng người nhưng hỏi trượt khoảnh khắc.

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

> **Cả ba cách giải thích dưới đây cùng giải thích một hành vi quan sát được:** học viên phải xem lại nhiều hơn dự tính khi cần dùng lại nội dung của một bài đã học. Chúng khác nhau ở **barrier**, nên dẫn tới hướng giải quyết khác hẳn nhau.

### Pain Hypothesis A — vấn đề nằm ở việc tìm lại

> Khi **[situation]**, **[actor]** gặp khó khăn trong việc **[job]** vì **[barrier]**, dẫn đến **[consequence]**.

```
Khi cần dùng lại nội dung của một bài đã học cách đó vài ngày, học viên gặp khó
khăn trong việc lấy lại đúng phần mình cần vì nội dung nằm rải ở nhiều nơi (bài
học gốc, chỗ họ tự ghi lại, trí nhớ) và không có điểm vào rõ ràng để biết cần
mở chỗ nào trước; dẫn đến họ phải tua và đọc lại nhiều hơn dự tính, hoặc bỏ
cuộc giữa chừng và làm tiếp việc đang dở với hiểu biết mơ hồ.
```

### Pain Hypothesis B — cách giải thích cạnh tranh: vấn đề nằm ở việc hiểu lại

> Khi **[situation]**, **[actor]** gặp khó khăn trong việc **[job]** vì **[barrier]**, dẫn đến **[consequence]**.

```
Khi cần dùng lại nội dung của một bài đã học cách đó vài ngày, học viên gặp khó
khăn trong việc lấy lại đúng phần mình cần vì thứ họ tìm lại được không giúp họ
hiểu ra — chỗ đó vốn đã không hiểu ngay từ lúc học, nên đọc lại vẫn tắc; cái họ
thiếu là một người giải thích chứ không phải thêm thông tin; dẫn đến họ bỏ qua
phần đó, đi hỏi người khác hoặc tra nguồn ngoài, hoặc làm sai mà không biết.
```

### Cách giải thích C — không có pain đáng giải

> _(Không có trong template gốc. Nhóm có thể xoá nếu thấy thừa — nhưng đây là cách giải thích duy nhất khiến nhóm phải dừng hướng hiện tại, nên nên giữ để đi kiểm chứng.)_

```
Khi cần dùng lại nội dung của một bài đã học, học viên mở lại bài, tua tới đoạn
cần tìm và xong việc trong vài phút. Họ coi đây là chi phí bình thường của việc
học, không có hậu quả nào đáng kể và cũng chưa từng tìm cách xử lý nó; barrier
mà nhóm hình dung không tồn tại ở mức đủ để họ bận tâm.
```

**Giả thuyết nhóm chọn để điều tra trước:**  ☑ A  ☐ B  ☐ C

**Lý do chọn:**

```
Chọn A KHÔNG phải vì nó nghe hợp lý hay vì nó khớp với solution directive — nhóm
ý thức rằng A chính là cách giải thích mà directive đang giả định sẵn, nên nó là
giả thuyết dễ được bênh nhất và cần bị kiểm chứng gắt nhất.

Chọn A vì một lý do về mặt kiểm chứng: A dự đoán những thứ quan sát được trong
CÙNG một câu chuyện — người học phải mở bao nhiêu chỗ, mất bao lâu, kết cục ra
sao — và chính những dữ kiện đó cũng đồng thời trả lời cho C. Hỏi về A thì tự
động thu được evidence cho hoặc chống C mà không tốn thêm câu hỏi nào. B cần một
hướng đào khác (họ có hiểu ra không, có phải đi hỏi ai không), nên để làm nhánh
rẽ khi câu chuyện dẫn tới đó.

Nhóm KHÔNG dựa vào lập luận "học viên đã chủ động highlight/ghi chú nên hẳn là
dấu vết bị phân tán" — đó là dùng chính giả định đang cần kiểm chứng làm căn cứ.
```

**Evidence cụ thể sẽ khiến nhóm chuyển sang B hoặc C:**

| Nghe thấy điều này trong phỏng vấn | Nhóm chuyển sang |
|---|---|
| Người học tìm lại được đúng chỗ khá nhanh, nhưng đọc lại rồi vẫn tắc — họ phải đi hỏi người khác, tra nguồn ngoài, hoặc bỏ qua và làm đại | **B** |
| Người học kể việc mở lại bài mất vài phút, họ không thấy phiền, không nhớ có hậu quả gì và chưa từng thử làm gì để việc đó dễ hơn | **C** |
| Người học không tự tạo dấu vết nào trong lúc học, và khi cần dùng lại thì đơn giản là xem lại từ đầu | **C** — và capability ở mục 1 phải viết lại |

> **Cảnh báo khi chọn:** A là cách giải thích khớp nhất với solution directive đã được giao — chọn A vì nó "hợp lý" chính là cách giả thuyết tự bảo vệ mình. Nếu chọn A, nhóm phải nêu được **một evidence cụ thể sẽ khiến nhóm chuyển sang B hoặc C**. Nếu không nêu được, đó là dấu hiệu nhóm đang chọn theo directive chứ không theo lý lẽ.
>
> Lý do chọn **không được** dựa vào "học viên đã chủ động highlight/ghi chú" — chính điều đó là giả định đang cần kiểm chứng, dùng nó làm căn cứ là lập luận vòng.

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

| Cần kiểm tra        | Evidence làm nhóm tin hơn                                                                                                                                        | Evidence làm nhóm nghi ngờ hoặc bác bỏ                                                                      |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Situation có thật   | Học viên kể được **một lần cụ thể, gần đây** phải dùng lại nội dung của một bài đã học cách đó vài ngày (làm bài tập, ôn kiểm tra, áp dụng vào việc thật) — nói được hôm đó là bài gì, cần dùng để làm gì, và họ đã mở những đâu. | Không nhớ nổi lần nào phải dùng lại nội dung cũ; chỉ nói chung chung "thỉnh thoảng cũng có"; hoặc mọi lần xem lại đều diễn ra ngay trong lúc học chứ không phải vài ngày sau. |
| Pain có ý nghĩa    | Học viên **mô tả được hành vi đã xảy ra**: mở bao nhiêu chỗ, tua đi tua lại mấy lần, mất khoảng bao lâu, có phải dừng việc đang làm không — và kể được lần đó kết thúc ra sao.                                | Chỉ đưa ra **ý kiến** ("cũng hơi bất tiện") mà không kể được lần nào; hoặc kể ra thì thấy chỉ mất vài phút, làm xong rồi thôi, không ảnh hưởng gì tới việc đang dở.                        |
| Workaround tồn tại  | Học viên kể được cách họ **đã tự xoay** để lần sau tìm lại dễ hơn: chụp màn hình, chép sang vở / Notion / Google Docs, lưu link kèm mốc thời gian trong video, đặt tên file theo buổi học, nhắn hỏi bạn cùng lớp — và nói được **đã bỏ ra bao nhiêu công**: làm mất bao lâu, làm mấy lần, có duy trì không. | Không làm gì cả, cứ mở lại bài rồi tua; hoặc từng thử một cách nào đó đúng **một lần** rồi bỏ vì thấy không cần. Workaround bị bỏ giữa chừng là dấu hiệu pain chưa đủ lớn. |
| Consequence tồn tại | Học viên kể được lần đó **ảnh hưởng cụ thể tới việc đang làm dở**: nộp muộn, làm sai phải sửa lại, bỏ qua phần đó rồi tắc ở bước sau, phải nhờ người khác, hoặc phải xem lại gần như cả bài.                      | Tìm hơi lâu nhưng cuối cùng vẫn xong đúng hạn; không nhớ có hậu quả gì; hoặc coi đó là chuyện bình thường của việc học và không định làm gì khác đi.           |
| Pattern có lặp      | Kể được **lần trước đó nữa** với chi tiết riêng, hoặc gắn tần suất vào một mốc có thật ("cứ tới hạn nộp bài tập là lại phải mở lại"), chứ không phải nói "thường xuyên" chung chung.                                      | Chỉ có đúng một lần kể được; lần trước đó đã lâu hoặc không nhớ; hoặc mỗi khoá học lại một kiểu, không thành nếp.                 |

---

## Chốt Problem Hypothesis và park solution

**Problem Hypothesis nhóm mang sang Chặng 2:**

```
Khi có việc buộc phải dùng lại nội dung của một bài đã học cách đó vài ngày,
học viên có thể gặp khó khăn trong việc lấy lại đúng phần mình cần vì nội dung
nằm rải ở nhiều nơi và không có điểm vào rõ ràng; điều này có thể khiến họ phải
tua và đọc lại nhiều hơn dự tính, hoặc bỏ cuộc giữa chừng và làm tiếp việc đang
dở với hiểu biết mơ hồ.
```

**Điều gì phải đúng để giả thuyết đứng vững:**

```
1. Tình huống "buộc phải dùng lại nội dung của một bài đã học" thực sự xảy ra
   và lặp lại, chứ không phải chuyện hiếm.
2. Khi tình huống đó xảy ra, việc lấy lại đúng phần cần tìm mất công đủ để
   học viên nhớ được — chứ không phải xong trong vài phút rồi quên luôn.
3. Barrier nằm ở chỗ TÌM (không biết mở đâu, phải lục nhiều nơi), chứ không
   phải ở chỗ HIỂU (tìm thấy rồi vẫn tắc).
4. Việc đó kéo theo một hậu quả quan sát được lên việc học viên đang làm dở.
```

**Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:**

```
- Học viên không nhớ nổi một lần cụ thể nào phải dùng lại nội dung cũ
  → situation không có thật, phải chọn lại actor/situation ở mục 3 và 4.
- Học viên tìm lại nhanh gọn, không thấy phiền, chưa từng làm gì để việc đó
  dễ hơn → nghiêng về cách giải thích C, pain không đủ để giải.
- Học viên tìm được đúng chỗ nhưng đọc lại vẫn không hiểu, phải đi hỏi người
  khác → nghiêng về cách giải thích B, barrier là hiểu chứ không phải tìm.
- Học viên không tạo dấu vết nào trong lúc học và vẫn xoay xở bình thường
  → capability ở mục 1 đang giả định sai ngay từ đầu, phải viết lại.
```

### Solution Parking Lot

Brainstorm **ít nhất năm hướng**, trong đó **ít nhất một hướng không sử dụng AI**.

| # | Hướng giải quyết có thể có                                                                               | AI / Không sử dụng AI |
| - | --------------------------------------------------------------------------------------------------------------- | ------------------------ |
| 1 | Tự động tổng hợp highlight, ghi chú và câu hỏi thành bản ghi chú theo chủ đề sau bài học       | AI                       |
| 2 | Gợi ý các ý chính, phần chưa hiểu và câu hỏi cần xem lại để học viên chọn đưa vào ghi chú | AI                       |
| 3 | Tạo flashcard hoặc câu hỏi ôn tập từ nội dung học và ghi chú cá nhân                               | AI                       |
| 4 | Cung cấp mẫu ghi chú có sẵn để học viên tự kéo thả, phân nhóm và hoàn thiện sau bài học      | Không sử dụng AI      |
| 5 | Lưu highlight và ghi chú theo từng bài, kèm danh sách nhắc xem lại theo thời gian                     | Không sử dụng AI      |

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

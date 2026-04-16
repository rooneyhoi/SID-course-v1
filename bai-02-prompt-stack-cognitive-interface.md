# Buổi 2 — Prompt như Giao Diện Nhận Thức & Prompt Stack

Thiết kế giao diện ngôn ngữ để điều khiển suy luận của AI

---

## 0. Chuẩn bị trước Buổi 2

Trước khi bắt đầu nội dung Buổi 2, cần có sẵn:

- **Framing Brief** cho một chủ đề/domain thật (từ Buổi 1), gồm:
  - Topic (chủ đề)
  - Problem (bài toán)
  - Audience (đối tượng)
  - Scope (phạm vi: in-scope / out-of-scope)
  - Output & Task type (đầu ra & kiểu nhiệm vụ)
  - Rủi ro nếu framing sai

- 2–3 prompt cũ có độ dài tương đối nhưng kết quả không như mong đợi, đúng với chủ đề trong Framing Brief.

Nếu chưa có Framing Brief, cần hoàn thành assignment của Buổi 1 trước.

---

## 1. Mục tiêu của Buổi 2

Kết thúc Buổi 2, người học có thể:

- Nhìn nhận prompt như **giao diện điều khiển nhận thức** (cognitive interface), thay vì chỉ là “câu hỏi ngẫu hứng”.
- Phân tích cấu trúc một prompt tốt bằng khung **RTC-COE**:
  - Role – Task – Context – Constraints – Output – Evaluation.
- Nhận diện lý do tại sao **một master prompt duy nhất** là ý tưởng kém hiệu quả cho bài toán phức tạp.
- Thiết kế một **Prompt Stack** (chuỗi prompt nhiều bước) gồm 3–6 bước cho domain thực tế, bám sát Framing Brief.
- Tự phân tích lại 2–3 prompt cũ và viết lại chúng thành một stack có các phase rõ ràng.

---

## 2. Vấn đề của “master prompt” và nhu cầu Prompt Stack

### 2.1. Vấn đề của “master prompt 1000 chữ”

Nhiều người dùng AI (1–3 năm kinh nghiệm) có xu hướng:

- Sao chép một “master prompt” rất dài trên mạng, hoặc
- Tự viết một prompt cực dài với cấu trúc tương tự:

> “Hãy đóng vai một chuyên gia hàng đầu, trả lời cực kỳ chi tiết, có ví dụ, cho framework, checklist, lộ trình, cách dạy lại, các sai lầm, rủi ro, trường hợp thay thế, và mọi thứ cần biết về [TOPIC]…”

và kỳ vọng rằng:

> “Mô hình sẽ xử lý toàn bộ bài toán chỉ với một lần hỏi”.

**Hệ quả thường gặp:**

- Output:
  - rất dài,
  - có vẻ “đầy đủ”,
  - nhưng thiếu chiều sâu để sử dụng trong thực tế,
  - hoặc “chạm nhẹ” nhiều ý nhưng không điểm nào đủ sâu.

**Nguyên nhân:**

- Có quá nhiều task (5–7 loại) được nhét vào **một prompt duy nhất**.
- Thiếu phân chia phase:
  - không tách rõ giai đoạn bóc tách, suy luận, phản biện, đóng gói.
- Mô hình được sử dụng theo hình thức:
  - “1 lệnh → 1 câu trả lời”,
  - thay vì một **chuỗi tương tác nhiều bước**.

#### Ví dụ một master prompt “dài lê thê” (đời thường)

```text
Hãy đóng vai chuyên gia hàng đầu về quản lý thời gian và năng suất, 
giải thích tất cả những gì quan trọng về việc quản lý thời gian hiệu quả, 
gồm các khái niệm, mô hình nổi tiếng, cách áp dụng vào đời sống của nhân viên văn phòng bận rộn, 
các sai lầm phổ biến, công cụ cần dùng, checklist từng ngày, 
và cuối cùng hãy thiết kế một lộ trình chi tiết 30 ngày để trở nên siêu hiệu quả trong công việc, 
giảm stress, cân bằng cuộc sống, có thêm thời gian cho gia đình và sở thích cá nhân.
```

Phân tích nhanh:

- Role: “chuyên gia quản lý thời gian và năng suất” – chấp nhận được.
- Task: trộn lẫn nhiều nhiệm vụ:
  - giải thích khái niệm,
  - liệt kê mô hình,
  - áp dụng thực tế,
  - chỉ ra sai lầm,
  - gợi ý công cụ,
  - làm checklist từng ngày,
  - thiết kế lộ trình 30 ngày.
- Context: mơ hồ (nhân viên văn phòng, nhưng không rõ ngành, mức độ áp lực, giới hạn thời gian…).
- Constraints: gần như không có; cụm “tất cả những gì quan trọng” không phải ràng buộc có nghĩa.
- Output: không xác định artifact trung tâm; “lộ trình 30 ngày” chỉ là một phần nhỏ.
- Evaluation: không có tiêu chí đánh giá thế nào là kết quả “tốt”.

Đây là loại prompt điển hình gây ra output dài nhưng khó sử dụng.

---

### 2.2. Prompt như giao diện điều khiển mô hình

Thay vì coi prompt đơn thuần là câu hỏi, có thể coi prompt như:

> Một **giao diện điều khiển** để:
> - xác định **Role** (vai trò),
> - giao **Task** (nhiệm vụ),
> - cung cấp **Context** (bối cảnh),
> - quy định **Constraints** (ràng buộc),
> - chỉ rõ **Output** (dạng đầu ra),
> - kèm theo **Evaluation** (tiêu chí đánh giá).

Thay vì một master prompt duy nhất, chiến lược hiệu quả hơn là:

> Sử dụng **Prompt Stack**:  
> một chuỗi 3–6 prompt,  
> mỗi prompt phục vụ một phase riêng,  
> kết nối với nhau: output bước trước → input bước sau.

---

## 3. Khung RTC-COE — “xương sống” của 1 prompt tốt

### 3.1. Thành phần RTC-COE

**RTC-COE** là viết tắt của:

- **R – T – C – C – O – E**
  - Role – Task – Context – Constraints – Output – Evaluation

Giải nghĩa:

- **Role (vai trò)**  
  Vai trò mô hình được yêu cầu “đóng”.  
  Ví dụ: chuyên gia nghiên cứu UX, nhà thiết kế chương trình đào tạo, trưởng phòng nhân sự, cố vấn chiến lược.

- **Task (nhiệm vụ)**  
  Hành động chính cần mô hình thực hiện.  
  Ví dụ: explain (giải thích), compare (so sánh), design (thiết kế), critique (phê bình), teach (giảng giải), diagnose (chẩn đoán), summarize (tóm tắt), brainstorm (đề xuất ý tưởng)…

- **Context (bối cảnh)**  
  Miêu tả môi trường thực tế, đối tượng, phạm vi, ràng buộc sẵn có.  
  Ví dụ: domain, loại đối tượng, thời lượng, nguồn lực, tình huống sử dụng…

- **Constraints (ràng buộc cụ thể)**  
  Những “luật chơi” rõ ràng:  
  - giới hạn độ dài,  
  - nội dung không được đụng tới,  
  - mức độ chi tiết,  
  - phong cách trình bày,  
  - những điều bắt buộc phải có hoặc phải tránh.

- **Output (dạng đầu ra)**  
  Artifact/kết quả mong muốn, không chỉ là “trả lời bằng chữ”.  
  Ví dụ: bảng, danh sách, framework, checklist, outline, memo, email mẫu, kế hoạch 30 ngày…

- **Evaluation (tiêu chí đánh giá)**  
  Tiêu chí để phân biệt output tốt/kém.  
  Ví dụ:  
  - “tốt nếu có ví dụ cụ thể”,  
  - “kém nếu chỉ liệt kê chung chung”,  
  - “tránh các buzzword mơ hồ”.

### 3.2. So sánh prompt “ngây thơ” và prompt có RTC-COE

**Prompt ngây thơ:**

```text
Hãy giải thích thật chi tiết về AI literacy, đưa ví dụ, framework, các sai lầm phổ biến và cách dạy lại cho người khác.
```

Hạn chế:

- Role: không rõ.
- Task: explain + design + teach + liệt kê sai lầm – trộn lẫn.
- Context: không có thông tin về đối tượng, ngành, trình độ.
- Constraints: không rõ (chỉ có “thật chi tiết”).
- Output: không xác định artifact cụ thể.
- Evaluation: không có chuẩn tốt/xấu.

**Prompt theo RTC-COE (minh họa):**

```text
[Role] Đóng vai chuyên gia về AI literacy và giáo dục đại học.

[Task] Thiết kế một bản mô tả khung năng lực AI literacy phù hợp cho giảng viên đại học đã dùng AI 1–2 năm 
(dùng chủ yếu để soạn bài, chấm bài, soạn câu hỏi).

[Context]
- Không yêu cầu viết code hay triển khai mô hình.
- Mục tiêu: hiểu để dạy lại và thiết kế hoạt động học tập.
- Thời lượng khóa học dự kiến: 4 buổi x 2 giờ.

[Constraints]
- Không đi vào chi tiết kỹ thuật model training.
- Tránh buzzword mơ hồ; mỗi khái niệm phải có ví dụ classroom cụ thể.
- Ưu tiên các năng lực có thể quan sát/đánh giá được trong giảng dạy.

[Output]
- Một bảng khung năng lực với các cột:
  (1) Năng lực
  (2) Mô tả
  (3) Hành vi quan sát được
  (4) Ví dụ hoạt động lớp học

[Evaluation]
Output tốt khi:
- Phân biệt rõ AI literacy với “chỉ biết dùng một công cụ chat AI”.
- Mỗi năng lực có ít nhất một hành vi cụ thể.
- Bảng có thể dùng làm xương sống cho rubric đánh giá sau này.
```

---

## 4. Hai tầng “stack”: RTC‑COE (bên trong 1 prompt) và Prompt Stack (giữa các prompt)

Khái niệm “stack” xuất hiện ở hai tầng khác nhau:

### 4.1. Tầng 1 – Stack bên trong từng prompt: RTC‑COE

Bên trong **một** prompt tốt, các thành phần thường được sắp xếp như một “mini‑stack”:

> Role → Task → Context → Constraints → Output → Evaluation

Tầng này:

- Là **cấu trúc nội bộ** của một prompt.
- Đảm bảo mỗi prompt có đầy đủ “xương sống”: vai, nhiệm vụ, bối cảnh, ràng buộc, đầu ra, tiêu chí.

### 4.2. Tầng 2 – Stack giữa các prompt: Prompt Stack

Ở cấp cao hơn, nhiều prompt được sắp xếp theo **trình tự phase**:

> Prompt 1 → Prompt 2 → Prompt 3 → Prompt 4 → …

Mỗi prompt:

- Dùng RTC‑COE bên trong,
- Thuộc **một phase khác nhau** của bài toán:
  - Prompt 1: Clarify (làm rõ bài toán),
  - Prompt 2: Structure (bóc tách & cấu trúc),
  - Prompt 3: Refine (rút gọn & thiết kế khung),
  - Prompt 4: Critique (phản biện & chỉnh sửa), v.v.

Tổng thể:

- **RTC‑COE** = “stack vi mô” bên trong một prompt.
- **Prompt Stack** = “stack vĩ mô” giữa các prompt, qua các phase.

Cảm giác “tất cả đều là stack” là đúng, nhưng cần phân biệt:

- Stack **thành phần** (RTC‑COE) trong 1 prompt.
- Stack **prompt** (Prompt Stack) trong toàn bộ quy trình giải bài toán.

---

## 5. Prompt Stack – từ “1 lệnh” sang “chuỗi phase”

### 5.1. Định nghĩa Prompt Stack

**Prompt Stack** trong phạm vi tài liệu này được hiểu là:

> **Chuỗi 3–6 prompt có cấu trúc**,  
> mỗi prompt:
> - sử dụng khung RTC-COE (ít nhất Role, Task, Context, Constraints, Output),
> - giải quyết **một phase/nhiệm vụ cụ thể** trong toàn bộ bài toán,
> - nhận **đầu vào** từ bước trước,  
> - tạo **đầu ra** cho bước sau.

Điểm quan trọng:

- Các prompt trong stack **không phải** là 3 phiên bản sửa đi sửa lại của cùng một master prompt.
- Mỗi prompt trong stack thực hiện **một nhiệm vụ khác nhau**:
  - clarify (làm rõ),
  - structure (bóc tách/cấu trúc),
  - refine (tinh chỉnh),
  - reason (suy luận sâu),
  - critique (phản biện),
  - synthesize (đóng gói).

### 5.2. Lợi ích của Prompt Stack so với master prompt

Prompt Stack tạo ra:

- **Checkpoints**: có điểm dừng trung gian để xem mô hình đang đi đúng hướng hay không.
- **Khả năng chỉnh hướng**: có thể sửa, bổ sung, thay đổi từ giữa quy trình thay vì phải viết lại toàn bộ prompt.
- **Tính tái sử dụng**: từng bước trong stack có thể dùng lại cho các chủ đề khác cùng domain, với ít sửa đổi.
- **Khả năng tự động hóa**: từng bước dễ được embed vào một Gem/GPT/assistant hoặc workflow tự động sau này.

---

## 6. Từ master prompt đến Prompt Stack (ví dụ refactor)

### 6.1. Master prompt ban đầu (quản lý thời gian)

Nhắc lại master prompt:

```text
Hãy đóng vai chuyên gia hàng đầu về quản lý thời gian và năng suất, 
giải thích tất cả những gì quan trọng về việc quản lý thời gian hiệu quả, 
gồm các khái niệm, mô hình nổi tiếng, cách áp dụng vào đời sống của nhân viên văn phòng bận rộn, 
các sai lầm phổ biến, công cụ cần dùng, checklist từng ngày, 
và cuối cùng hãy thiết kế một lộ trình chi tiết 30 ngày để trở nên siêu hiệu quả trong công việc, 
giảm stress, cân bằng cuộc sống, có thêm thời gian cho gia đình và sở thích cá nhân.
```

Bài toán thực chất cần:

- Khung kỹ năng/nội dung về quản lý thời gian.
- Phiên bản áp dụng cho nhân viên văn phòng bận rộn.
- Lộ trình 30 ngày cụ thể.

### 6.2. Framing Brief (giả định) cho ví dụ này

- Topic: Quản lý thời gian cho nhân viên văn phòng bận rộn.
- Problem: Thiết kế một lộ trình 30 ngày, khả thi, giúp cải thiện quản lý thời gian, giảm stress và tạo thêm thời gian cho cuộc sống cá nhân.
- Audience: Nhân viên văn phòng 25–35 tuổi, làm full-time, thời gian hạn chế, hay bị ngắt quãng công việc.
- Output ưu tiên:
  - Khung kỹ năng/năng lực quản lý thời gian,
  - Kế hoạch 30 ngày theo tuần, mỗi ngày 1–2 hành động nhỏ.

### 6.3. Refactor thành Prompt Stack

Ví dụ một Prompt Stack (rút gọn):

1. Prompt 1: Clarify – làm rõ bài toán, đối tượng, phạm vi.
2. Prompt 2: Structure – liệt kê các kỹ năng/thành phần liên quan quản lý thời gian.
3. Prompt 3: Refine – gom lại thành khung kỹ năng cốt lõi (5–7 kỹ năng).
4. Prompt 4: Design – thiết kế lộ trình 30 ngày dựa trên khung kỹ năng.
5. Prompt 5: Critique – tự phản biện lộ trình, đề xuất phiên bản nhanh/sâu.

Cấu trúc chi tiết của Prompt 1–4 trong tài liệu sẽ áp dụng lại cách viết RTC‑COE tương tự phần AI literacy.

---

## 7. Thiết kế Prompt Stack cho domain thực tế

### 7.1. Bước nền tảng: cung cấp Framing Brief cho mô hình

Bước này tạo “nền tảng bối cảnh” cho toàn bộ session làm việc:

```text
Sắp gửi một Framing Brief mô tả chủ đề, bài toán, đối tượng, phạm vi và output mong muốn.

Yêu cầu:
- Chỉ sử dụng brief này làm nguồn thông tin chính về bối cảnh.
- Nếu các prompt sau có nội dung mâu thuẫn với brief, cần báo lại để kiểm tra.

Đây là Framing Brief:

[FRAMING BRIEF]

Nhiệm vụ:
- Xác nhận đã hiểu bối cảnh.
- Tóm tắt lại ngắn gọn theo cách diễn đạt của mô hình để kiểm tra mức độ hiểu framing.
Chưa cần giải bài toán chính.
```

Bước này:

- Thiết lập grounding cho toàn bộ stack.
- Giúp phát hiện sớm những điểm mơ hồ hoặc mâu thuẫn trong Framing Brief.

---

### 7.2. Prompt 1 – Clarify Prompt (task: làm rõ bài toán)

**Mục tiêu:**  
Làm rõ yêu cầu, đối tượng, phạm vi và giả định trước khi thiết kế bất kỳ khung hay lộ trình nào.

```text
[Role] Đóng vai business analyst, chuyên làm rõ yêu cầu trước khi thiết kế giải pháp.

[Task]
1. Tóm tắt lại bài toán, đối tượng, phạm vi và output mong muốn trong Framing Brief bằng ngôn ngữ đơn giản.
2. Liệt kê 5–7 giả định đang được ngầm hiểu về người học và bối cảnh.
3. Đề xuất 5 câu hỏi cần được trả lời thêm để làm rõ brief (nếu còn điểm mơ hồ hoặc thiếu).

[Context]
- Đây là bước làm rõ yêu cầu, chưa bước vào thiết kế khung hay lộ trình.

[Constraints]
- Không đề xuất giải pháp, khung năng lực hay lộ trình cụ thể.
- Trình bày ngắn gọn, tránh thuật ngữ không cần thiết.

[Output]
- Đoạn tóm tắt ngắn (5–7 câu).
- Danh sách “Giả định hiện tại”.
- Danh sách “Câu hỏi cần làm rõ”.

[Evaluation]
Output tốt khi:
- Thể hiện việc nắm đúng bài toán.
- Các câu hỏi giúp phát hiện điểm mơ hồ trong Framing Brief.
```

---

### 7.3. Prompt 2 – Structure Prompt (task: extract/structure – bóc mảnh)

**Mục tiêu:**  
Từ Framing Brief (đã được làm rõ), bóc tách chủ đề thành các thành phần hoặc kỹ năng, tạo một “bản đồ nội dung” sơ bộ.

```text
[Role] Đóng vai knowledge organizer, chuyên tổ chức và phân loại kiến thức.

[Task]
Dựa trên Framing Brief và phần làm rõ từ Prompt 1:
- Liệt kê các "thành phần" hoặc "kỹ năng" quan trọng trong [TOPIC],
- Nhóm các thành phần này thành 3–5 nhóm lớn (category), phục vụ cho việc xây dựng khung năng lực/khung nội dung ở bước sau.

[Context]
- Audience: [AUDIENCE trong Framing Brief].
- Scope: [in-scope / out-of-scope trong Framing Brief].
- Mục tiêu: tạo một bản đồ thô (mindmap dạng chữ) của toàn bộ chủ đề.

[Constraints]
- Mỗi nhóm lớn có thể chứa nhiều thành phần con.
- Mỗi thành phần cần có mô tả ngắn, dễ hiểu, ưu tiên ví dụ gần với bối cảnh thực tế.
- Không thêm nội dung đã được ghi rõ là out-of-scope.

[Output]
- Danh sách dạng:
  - Nhóm A:
    - Thành phần 1: mô tả ngắn
    - Thành phần 2: mô tả ngắn
  - Nhóm B:
    - ...

[Evaluation]
Output tốt khi:
- Thể hiện được bức tranh đầy đủ các mảnh ghép có thể dạy hoặc huấn luyện.
- Không bị lan man sang nội dung ngoài phạm vi.
```

---

### 7.4. Prompt 3 – Refine Prompt (task: refine + design khung)

**Mục tiêu:**  
Dựa trên danh sách thành phần/thành tố ở Prompt 2, rút gọn và gom nhóm thành khung năng lực hoặc khung nội dung có thể triển khai thành chương trình.

```text
[Role] Đóng vai program designer phụ trách thiết kế chương trình/khóa học cho [TOPIC].

[Task]
1. Từ danh sách thành phần ở bước trước, gộp và cấu trúc lại thành 5–7 năng lực hoặc cụm nội dung cốt lõi.
2. Gán cho mỗi năng lực/cụm nội dung:
   - tên ngắn gọn (2–4 từ),
   - mô tả 1–2 câu,
   - 1–2 hành vi hoặc ví dụ cụ thể gắn với bối cảnh thực tế.

[Context]
- Audience: [AUDIENCE trong Framing Brief].
- Thời lượng: [ví dụ: 4 buổi x 2 giờ].
- Mục tiêu: dùng khung này làm xương sống cho khóa học và hệ thống đánh giá.

[Constraints]
- Tối đa 7 năng lực/cụm nội dung.
- Mỗi năng lực:
  - không trùng lặp về ý với năng lực khác,
  - liên hệ trực tiếp đến tình huống thực tế (ví dụ: dạy học, làm việc văn phòng, ra quyết định, v.v.).
- Không bổ sung nội dung hoàn toàn mới; chỉ được:
  - chọn lọc,
  - gộp nhóm,
  - đổi tên các thành phần có sẵn.

[Output]
- Một bảng với các cột:
  1. Năng lực/cụm nội dung
  2. Mô tả
  3. Hành vi quan sát được / Ví dụ cụ thể
  4. Gợi ý một hoạt động học tập/minh họa ngắn (5–15 phút)

[Evaluation]
Output tốt khi:
- Mỗi năng lực có thể trở thành một buổi hoặc một module.
- Không có hai năng lực quá giống nhau về nội dung.
- Có thể dễ dàng dùng bảng này để thiết kế khung khóa học chi tiết.
```

---

### 7.5. Prompt 4 – Critique Prompt (task: self-critique)

**Mục tiêu:**  
Giúp mô hình (và người thiết kế) tự phản biện khung đã tạo, chuẩn bị cho việc cải tiến và sử dụng ở các bối cảnh khác nhau.

```text
[Role] Đóng vai reviewer khó tính trong domain [TOPIC].

[Task]
Đánh giá và phản biện khung năng lực/khung nội dung đã tạo ở bước trước.

[Output]
1. Ba điểm mạnh lớn nhất của khung hiện tại (theo góc nhìn ứng dụng thực tế).
2. Ít nhất năm điểm yếu hoặc lỗ hổng, bao gồm:
   - các năng lực hoặc cụm nội dung có dấu hiệu trùng lặp,
   - các khía cạnh quan trọng của [TOPIC] còn thiếu,
   - rủi ro khi áp dụng khung này cho các nhóm đối tượng khác nhau.
3. Đề xuất hai hướng chỉnh sửa:
   - Phiên bản A: rút gọn để phù hợp chương trình ngắn (ví dụ: 1–2 buổi).
   - Phiên bản B: mở rộng để phù hợp chương trình sâu (ví dụ: 6–8 buổi).

[Constraints]
- Trình bày ngắn gọn, tập trung vào tính khả thi và tính dùng được của khung.
- Không cần viết lại toàn bộ khung, chỉ nêu rõ hướng chỉnh sửa.

[Evaluation]
Output tốt khi:
- Chỉ ra được điểm yếu một cách cụ thể, không chung chung.
- Đưa ra gợi ý chỉnh sửa rõ ràng, có thể triển khai ở bước tiếp theo.
```

---

## 8. Bài tập thực hành — RTC-COE & Prompt Stack V1

### 8.1. Bài tập 1 — RTC-COE Lab: “Mổ xẻ & viết lại 2 prompt dài-sai”

**Mục tiêu**  
Luyện thói quen nhìn prompt theo cấu trúc, không viết theo cảm tính.

**Bước 1:** Chọn 2 prompt dài-sai từ lịch sử sử dụng.

**Bước 2:** Với mỗi prompt, tạo bảng:

| Thành phần | Có/Không | Nhận xét ngắn                                         |
|-----------|----------|-------------------------------------------------------|
| Role      |          | Vai trò rõ hay mơ hồ?                                 |
| Task      |          | Có trộn bao nhiêu loại task?                          |
| Context   |          | Bối cảnh, audience, thời gian, domain có rõ không?    |
| Constraints |        | Có ràng buộc cụ thể, hữu ích không?                   |
| Output    |          | Output là artifact cụ thể hay chỉ “trả lời kỹ”?       |
| Evaluation|          | Có tiêu chí "tốt/kém" không?                          |

**Bước 3:** Viết lại một phiên bản prompt mới cho mỗi prompt, bảo đảm:

- Chỉ nhắm **một nhiệm vụ chính**.
- Bối cảnh (Context) rõ ràng.
- Có ràng buộc (Constraints) cụ thể.
- Chỉ định output dưới dạng artifact.

---

### 8.2. Bài tập 2 — Thiết kế Prompt Stack V1 cho domain trong Framing Brief

**Mục tiêu**  
Xây dựng một Prompt Stack 3–6 bước phục vụ đúng domain và bài toán đã xác định trong Framing Brief.

**Yêu cầu:**

- Sử dụng Framing Brief từ Buổi 1.
- Thiết kế stack gồm tối thiểu 3 prompt:
  - Một prompt để **làm rõ** (clarify).
  - Một prompt để **bóc tách/cấu trúc** (structure).
  - Một prompt để **rút gọn/tinh chỉnh** (refine).
  - (Tùy chọn) Một prompt để **phản biện** (critique).

Mỗi prompt cần:

- Ghi rõ: Role – Task – Context – Constraints – Output (và Evaluation nếu cần).
- Đánh dấu **Task type chính** (ví dụ: explain, design, critique, teach…).

**Gợi ý format nộp (Markdown):**

```markdown
Prompt Stack V1 — [Tên domain]

Context
Tóm tắt Framing Brief trong 3–5 câu 
(Topic, Problem, Audience, Scope, Output ưu tiên…)

Prompt 1 — [Tên ngắn, ví dụ: "Làm rõ bài toán"]
Task type chính: [ví dụ: explain + diagnose]

Prompt:
[Role: ...]
[Task: ...]
[Context: ...]
[Constraints: ...]
[Output: ...]
[Evaluation: ...]


Prompt 2 — [Tên ngắn, ví dụ: "Bóc cấu trúc chủ đề"]
Task type chính: [ví dụ: design, extract]

Prompt:
...


Prompt 3 — [Tên ngắn, ví dụ: "Rút gọn & thêm ví dụ"]
Task type chính: [ví dụ: refine + design]

Prompt:
...


Prompt 4 — [Tên ngắn, ví dụ: "Tự phản biện khung"]
Task type chính: [ví dụ: critique]

Prompt:
...
```

---

## 9. Assignment Buổi 2 – Prompt Stack V1 cho domain riêng

### 9.1. Đề bài

Dựa trên Framing Brief đã có, thiết kế một Prompt Stack V1 gồm 3–6 prompt để:

- Bóc tách chủ đề,
- Chuẩn hóa thành khung năng lực/khung nội dung,
- Tự critique sơ bộ khung đó.

### 9.2. Tiêu chí tự chấm (rubric gợi ý)

| Tiêu chí                 | Mô tả                                                                                          | Điểm (0–5) |
|--------------------------|------------------------------------------------------------------------------------------------|-----------|
| Alignment với Brief      | Stack bám sát problem, audience, scope, output trong Framing Brief                           | /5        |
| Cấu trúc RTC-COE         | Mỗi prompt có Role, Task, Context, Constraints, Output rõ ràng                               | /5        |
| Tách phase hợp lý        | Các prompt thực sự xử lý các nhiệm vụ khác nhau, không lặp lại cùng một task                 | /5        |
| Tính tái sử dụng         | Stack có thể áp dụng lại cho chủ đề khác trong cùng domain với ít chỉnh sửa                  | /5        |
| Chuẩn bị cho Buổi 3–4    | Output của stack có thể dùng làm input cho Decomposition & Information Architecture (IA)      | /5        |
| Clarity                  | Văn bản rõ ràng, dễ hiểu, tránh mơ hồ                                                         | /5        |

---

## 10. Kết quả sau Buổi 2

Khi hoàn thành:

- **Framing Brief** (Buổi 1).
- **Prompt Stack V1** (Buổi 2).

Hệ thống đầu vào cho Buổi 3–4 bao gồm:

- Mô tả bài toán rõ ràng, nhất quán.
- Bộ prompt có cấu trúc, có các phase (clarify → structure → refine → critique) có thể:
  - được tích hợp vào Gem/GPT/assistant,
  - sử dụng như pipeline tri thức khi nghiên cứu và thiết kế nội dung cho một chủ đề.

Buổi 3 và Buổi 4 sẽ:

- Sử dụng output của Prompt Stack (đặc biệt là bảng/khung đã tạo),
- Để thực hiện:
  - **Decomposition** (bóc tách vấn đề thành các phần nhỏ hơn),
  - **Information Architecture – IA** (kiến trúc thông tin: taxonomy, hierarchy, bảng/matrix).

---

## 11. Gợi ý Prompt Stack mẫu — AI literacy cho giảng viên đại học

### 11.1. Context (tóm tắt Framing Brief mẫu)

Chủ đề: AI literacy cho giảng viên đại học.  
Bài toán: Thiết kế một khung năng lực AI literacy dành cho giảng viên đã sử dụng AI 1–2 năm (không viết code, chủ yếu dùng AI để soạn bài, chấm bài, thiết kế câu hỏi).  
Mục tiêu: Dùng khung năng lực làm xương sống cho khóa học nội bộ 4 buổi và cho hệ thống đánh giá năng lực.  
Phạm vi: Không đi vào training model hoặc hạ tầng kỹ thuật; tập trung vào khai thác AI an toàn, có đạo đức, hiệu quả trong dạy và học.

### 11.2. Prompt 1 — Làm rõ bài toán

*Task type chính: explain + diagnose*

```text
[Role] Đóng vai business analyst trong môi trường giáo dục đại học.

[Task]
1. Tóm tắt lại bài toán, đối tượng, phạm vi và output từ Framing Brief này.
2. Liệt kê 5–7 giả định về giảng viên và bối cảnh dạy học với AI.
3. Đề xuất 5 câu hỏi cần được trả lời thêm trước khi thiết kế khung năng lực.

[Constraints]
- Không thiết kế khung năng lực hay nội dung khóa học ở bước này.
- Trình bày rõ ràng, tránh thuật ngữ không cần thiết.

[Output]
- Đoạn tóm tắt.
- Danh sách giả định.
- Danh sách câu hỏi.

[Evaluation]
Output được xem là tốt nếu phản ánh chính xác bài toán và nêu được các câu hỏi làm rõ quan trọng.
```

### 11.3. Prompt 2 — Bóc khung năng lực sơ bộ

*Task type chính: design (extract & structure)*

```text
[Role] Đóng vai knowledge architect chuyên thiết kế khung năng lực cho giáo dục đại học.

[Task]
Dựa trên bối cảnh AI literacy cho giảng viên và các thông tin đã làm rõ:
- Bóc tách chủ đề AI literacy thành một danh sách năng lực/thành phần sơ bộ phù hợp để dạy trong 4 buổi nội bộ.

[Context]
- Audience: giảng viên đại học đã sử dụng AI 1–2 năm, không viết code.
- Mục tiêu: sử dụng AI như công cụ hỗ trợ thiết kế bài giảng, đánh giá và phản tư.
- Scope: không đi sâu vào training/fine-tuning/hạ tầng; tập trung vào khai thác, đánh giá, đạo đức, sư phạm.

[Constraints]
- Số năng lực chính: từ 5 đến 8.
- Mỗi năng lực:
  - có mô tả ngắn, rõ ràng,
  - gắn trực tiếp với tình huống dạy và học thực tế,
  - tránh các cụm từ mơ hồ như "hiểu sâu", "nâng cao" trừ khi được gắn với ví dụ cụ thể.
- Không đưa nội dung đã được xác định là out-of-scope.

[Output]
- Bảng với các cột:
  1. Năng lực
  2. Mô tả ngắn
  3. Hành vi quan sát được trong lớp học hoặc khi chuẩn bị bài
  4. Ví dụ hoạt động minh họa 5–10 phút

[Evaluation]
Output tốt khi:
- Tập trung vào khung năng lực (không biến thành giáo trình chi tiết).
- Mỗi năng lực có thể trở thành một buổi hoặc một module.
- Hành vi quan sát được rõ ràng, gắn với thực hành của giảng viên.
```

### 11.4. Prompt 3 — Rút gọn & tinh luyện khung năng lực

*Task type chính: refine + design*

```text
[Role] Đóng vai program director phụ trách khóa AI literacy cho giảng viên.

[Task]
Dựa trên bảng khung năng lực sơ bộ:
1. Gộp hoặc loại bỏ những năng lực trùng ý hoặc quá chi tiết.
2. Rút lại còn 5–7 năng lực cốt lõi, mỗi năng lực:
   - có tên ngắn gọn (2–4 từ),
   - có mô tả 1–2 câu,
   - có 1–2 hành vi quan sát được.

[Constraints]
- Không vượt quá 7 năng lực.
- Không bổ sung nội dung mới ngoài phạm vi đã nêu; chỉ tái cấu trúc và tinh luyện.
- Mỗi năng lực đủ “lớn” để trở thành một buổi học 2 giờ.

[Output]
- Bảng rút gọn với các cột:
  1. Tên năng lực
  2. Mô tả
  3. Hành vi quan sát được
  4. Gợi ý một hoạt động học tập 10–15 phút

[Evaluation]
Output tốt khi:
- Có thể dễ dàng đặt tên 4 buổi học dựa trên các năng lực cốt lõi.
- Mỗi năng lực mang ý nghĩa riêng, không trùng lặp với các năng lực còn lại.
```

### 11.5. Prompt 4 — Tự phản biện khung năng lực

*Task type chính: critique*

```text
[Role] Đóng vai reviewer khó tính trong bối cảnh giáo dục đại học.

[Task]
Đánh giá và phản biện khung năng lực rút gọn ở trên.

[Output]
1. Ba điểm mạnh lớn nhất của khung này.
2. Ít nhất năm điểm yếu hoặc lỗ hổng, bao gồm:
   - năng lực có thể trùng lặp hoặc chồng lấn,
   - các khía cạnh quan trọng của AI literacy (đặc biệt về đạo đức, đánh giá, tri thức luận) còn thiếu,
   - rủi ro khi áp dụng khung này cho các khoa khác nhau (khoa kỹ thuật so với khoa xã hội, v.v.).
3. Hai phiên bản chỉnh sửa:
   - Phiên bản A: ưu tiên dạy nhanh trong 2 buổi (rút bớt).
   - Phiên bản B: ưu tiên dạy sâu trong 6–8 buổi (mở rộng).

[Constraints]
- Trả lời ngắn gọn, rõ ràng, tập trung vào tính khả dụng trong thiết kế khóa học.

[Evaluation]
Output tốt khi:
- Chỉ ra được điểm mạnh và điểm yếu cụ thể, có dẫn chứng từ khung.
- Đề xuất hai phiên bản chỉnh sửa có thể triển khai trong thực tế.
```

Ghi chú: Ví dụ này chỉ mang tính minh họa. Khi áp dụng cho domain riêng, toàn bộ nội dung cần được điều chỉnh theo Framing Brief tương ứng.


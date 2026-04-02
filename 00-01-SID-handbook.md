# Structured Intelligence Design (SID) — Course Handbook

> A Complete Program for AI Information Mastery, Knowledge Architecture, and Natural-Language Cognitive Design

Từ “dùng AI để hỏi” sang “dùng AI để kiến trúc và chuyển giao tri thức”

Để khai thác AI (vốn vận hành dựa trên xác suất ngôn ngữ và không gian vector) đạt đến mức "đúng nhất, đủ nhất và sâu nhất", chúng ta cần nâng cấp từ tư duy "Truy vấn thông tin" (**Information Retrieval** – truy xuất thông tin) sang "Kiến trúc tri thức" (**Knowledge Architecting** – kiến trúc hóa tri thức).

---

## 0. Mục đích của tài liệu này

Handbook này là lớp kiến thức nền cho toàn bộ khóa SID:

- Giải thích SID là gì và khác gì so với “prompt engineering” (kỹ thuật viết prompt).
- Định nghĩa năng lực cốt lõi và 6 level trưởng thành.
- Chuẩn hóa 8 nhóm kỹ thuật và cách chúng móc nối với nhau.
- Đưa ra quy trình chuẩn để nghiên cứu bất kỳ chủ đề nào với AI.
- Chuẩn hóa rubric (bảng tiêu chí đánh giá) đánh giá năng lực và chuẩn đầu ra cuối khóa.

Handbook không làm nhiệm vụ:

- Dạy chi tiết từng buổi học.
- Liệt kê toàn bộ prompt mẫu.
- Thiết kế project cụ thể.

Những phần đó sẽ nằm trong: Syllabus (đề cương khóa học) và Lesson Notes (ghi chú/bài giảng từng buổi).

---

## 1. Vấn đề khóa học này giải quyết

### 1.1. Vấn đề thực tế của người dùng AI 1–3 năm

Phần lớn người dùng AI (kể cả “dùng hàng ngày 1–3 năm”) đang mắc các lỗi:

- Hỏi prompt dài nhưng lệch gốc:
  - lẫn lộn mục tiêu, audience (đối tượng), output (đầu ra), scope (phạm vi), task (nhiệm vụ).
- Dùng AI chủ yếu để:
  - “giải thích giúp”, “tóm tắt giúp”, “viết hộ”.
- Không có bản đồ chủ đề, không bóc tách, không kiến trúc thông tin.
- Tin output đầu tiên hoặc “thấy hợp lý là dùng”, thiếu validation (kiểm định).
- Không biết biến output AI thành:
  - framework (khung 5–7 bước), checklist (bảng kiểm), workflow (quy trình), syllabus (đề cương), rubric (bảng tiêu chí), playbook (cẩm nang).
- Không dám (hoặc không biết cách) xây:
  - Gems, Custom GPTs, AI tutor, RAG assistant,… từ kiến thức mình có.

Nói cách khác: AI được dùng như “máy trả lời thông minh”, không phải như:  
- môi trường khai thác tri thức,  
- công cụ tổ chức hiểu biết,  
- hay nền tảng để xây hệ thống tri thức.

### 1.2. Insight trung tâm

Prompt tốt chỉ giải quyết lớp bề mặt.

Lớp gốc là: khả năng định khung vấn đề, bóc tách, tổ chức, suy luận, kiểm định và chuyển giao tri thức bằng ngôn ngữ tự nhiên.

---

## 2. SID là gì?

### 2.1. Định nghĩa

**Structured Intelligence Design (SID – Thiết kế trí tuệ có cấu trúc)** là phương pháp dùng ngôn ngữ tự nhiên để:

- định khung vấn đề (**framing** – định khung),
- kiến trúc hóa thông tin (**information architecture** – kiến trúc thông tin),
- điều khiển suy luận (**reasoning design** – thiết kế suy luận),
- kiểm định tri thức (**epistemic validation** – kiểm định tri thức theo lớp “biết/không chắc/giả định”),
- tổng hợp (**synthesis** – tổng hợp),
- và chuyển giao (**transfer** – chuyển giao/ứng dụng)

với sự hỗ trợ của AI, như một **hệ thống** chứ không chỉ là chuỗi câu hỏi lẻ tẻ.

### 2.2. SID không phải (chỉ là) prompt engineering

**Prompt engineering (kỹ thuật viết prompt)** tập trung vào:

- viết câu lệnh,
- chọn từ khóa,
- dùng role/context/examples (vai trò/bối cảnh/ví dụ),
- chỉnh nhiệt độ, style (phong cách).

SID đi xa hơn:

- bắt đầu từ bài toán nhận thức chứ không từ câu lệnh;
- thiết kế chuỗi tương tác (**prompt stack** – chuỗi prompt nhiều bước),
- kiến trúc hóa tri thức thành:
  - framework (khung), workflow (quy trình), syllabus (đề cương), rubric (bảng tiêu chí), playbook (cẩm nang);
- biết kiểm định và phản biện output;
- dùng AI để xây hệ tri thức (knowledge system – hệ thống tri thức, AI assistant – trợ lý AI, mini-course – khóa học nhỏ,…).

### 2.3. Câu chốt định vị

- Beginner (người mới) dùng AI để lấy câu trả lời.
- Intermediate (trung cấp) dùng AI để lấy cấu trúc.
- Advanced (nâng cao) dùng AI để điều khiển bóc tách, suy luận, kiểm định, tổng hợp tri thức.
- Expert (chuyên gia) dùng AI để thiết kế hệ tri thức, workflow, chương trình đào tạo cho người khác.

SID nhắm tới **hai nấc trên cùng**.

---

## 3. Chuỗi chuyển hóa: từ dữ liệu đến hành động

### 3.1. Tầng tri thức

Trong mọi công việc tri thức (kể cả với AI) luôn có chuỗi:

> **Data → Signal → Information → Knowledge → Insight → Decision → Action → Feedback → Refined Knowledge**

Ý nghĩa nhanh:

- **Data (dữ liệu)**: mảnh vụn (log, số liệu, đoạn text,…).
- **Signal (tín hiệu)**: phần dữ liệu liên quan đến mục tiêu.
- **Information (thông tin)**: data đã có ngữ cảnh, quan hệ.
- **Knowledge (tri thức)**: information + cấu trúc + mô hình giải thích.
- **Insight (ngộ nhận thức / khám phá giá trị)**: phát hiện có giá trị (đòn bẩy, pattern, trade-off).
- **Decision (quyết định)**: chọn hướng đi.
- **Action (hành động)**: làm thật.
- **Feedback (phản hồi)**: kết quả, phản ứng.
- **Refined Knowledge (tri thức đã tinh chỉnh)**: tri thức sau khi va chạm thực tế.

### 3.2. Sai lầm phổ biến với AI

Nhiều người coi:

- text mà AI spit ra = knowledge.

Thực tế, phần lớn output AI chỉ ở mức:

- paraphrase (diễn đạt lại),
- tóm tắt,
- tổng hợp bề mặt.

Để lên tầng **knowledge** và **insight**, cần:

- decomposition (bóc tách),
- information architecture (kiến trúc thông tin),
- reasoning (suy luận),
- validation (kiểm định),
- synthesis (tổng hợp).

SID chính là bộ kỹ thuật để đi từ **output AI → knowledge → insight → hành động**.

---

## 4. Khung SID 7 bước

Đây là framework (khung) lõi của toàn khóa. Mọi buổi học, mọi project đều móc vào đây.

**SID Framework**  
1. Frame (định khung)  
2. Architect (kiến trúc hóa)  
3. Explore (khám phá/mở rộng)  
4. Reason (suy luận)  
5. Validate (kiểm định)  
6. Synthesize (tổng hợp)  
7. Transfer (chuyển giao/ứng dụng)

### 4.1. Frame — Định khung bài toán

Trả lời:

- Thực sự đang muốn làm gì với chủ đề này?
- Mục tiêu cuối là gì (hiểu, so sánh, thiết kế, dạy, quyết định…)?
- Audience (đối tượng) là ai?
- Phạm vi nào in-scope / out-of-scope (trong/ngoài phạm vi)?
- Output cần là gì (bảng, framework, syllabus, playbook, memo…)?

Nếu Frame sai:

- prompt có đẹp đến đâu cũng có khả năng vô dụng.

### 4.2. Architect — Kiến trúc hóa thông tin

Trả lời:

- Chủ đề gồm những phần nào?
- Quan hệ giữa các phần?
- Thiếu mảng nào?
- Nên biểu diễn bằng:
  - outline (dàn ý), tree (cây), taxonomy (phân loại), bảng, matrix (ma trận), workflow (quy trình), ontology (mô hình thực thể–quan hệ)?

Đây là lúc dùng:

- decomposition (bóc tách),
- taxonomy (phân loại),
- hierarchy (thứ bậc),
- schema (lược đồ/bố cục cột),
- matrix (ma trận).

### 4.3. Explore — Mở rộng không gian tri thức

Trả lời:

- Toàn bộ miền liên quan gồm những nhánh nào?
- Thuật ngữ, từ khóa, domain lân cận nào cần biết?
- Nhánh nào đáng đào sâu trước?

Dùng:

- breadth-first exploration (khám phá rộng trước),
- depth-first exploration (đào sâu một nhánh) – có chọn lọc,
- query expansion (mở rộng truy vấn/từ khóa),
- faceted exploration (khám phá theo nhiều “mặt” – facet),
- adjacent-domain expansion (mở rộng sang miền gần kề).

### 4.4. Reason — Điều khiển suy luận

Trả lời:

- Mình đang suy nghĩ theo chuỗi tuyến tính hay đa nhánh?
- Cần:
  - so sánh,
  - tìm nhân quả,
  - kiểm giả thuyết,
  - tìm phản ví dụ?

Dùng:

- **Chain of Thought (CoT – chuỗi suy nghĩ)**,
- **Tree of Thought (ToT – cây suy nghĩ đa nhánh)**,
- comparative reasoning (suy luận so sánh),
- causal reasoning (suy luận nhân quả),
- hypothesis-driven reasoning (suy luận dựa trên giả thuyết),
- analogical reasoning (suy luận tương tự/so sánh bằng ẩn dụ),
- counterfactual reasoning (suy luận phản thực tế: “nếu bỏ X thì sao?”).

### 4.5. Validate — Kiểm định tri thức

Trả lời:

- Câu nào là fact (sự kiện), câu nào là interpretation (diễn giải), assumption (giả định), hypothesis (giả thuyết), recommendation (khuyến nghị)?
- Có phần nào mâu thuẫn nhau?
- Có thiếu khía cạnh quan trọng?
- Có giả định ngầm nguy hiểm?
- Độ chắc chắn của từng kết luận?

Dùng:

- self-critique (tự phản biện),
- assumption check (soi giả định),
- gap detection (tìm chỗ thiếu),
- contradiction check (tìm mâu thuẫn),
- multi-model triangulation (soi từ nhiều mô hình/nguồn),
- confidence labeling (gắn nhãn độ tin cậy).

### 4.6. Synthesize — Tổng hợp

Trả lời:

- Từ 20 mảnh output khác nhau, rút được pattern (mẫu lặp) gì?
- Nguyên lý cốt lõi là gì?
- Framework mấy bước có thể dạy và dùng lại?
- Checklist / playbook / decision model nào cần sinh ra?

Dùng:

- pattern extraction (rút mẫu),
- principle extraction (rút nguyên lý),
- framework synthesis (tổng hợp thành khung),
- layered summarization (tóm tắt nhiều tầng: ngắn/gọn/sâu),
- playbook design (thiết kế cẩm nang).

### 4.7. Transfer — Chuyển giao & ứng dụng

Trả lời:

- Áp dụng được ở đâu, vai trò nào, điều kiện gì?
- KPI / tiêu chí thành công là gì?
- Workflow / SOP / mini-course / rubric nào cần thiết kế?
- Làm sao để dạy lại hoặc scale cho team?

Dùng:

- use-case mapping (map vào tình huống dùng cụ thể),
- workflow design (thiết kế quy trình),
- curriculum design (thiết kế chương trình học),
- rubric design (thiết kế bảng tiêu chí),
- teaching translation (dịch tri thức thành dạng dễ dạy),
- scenario design (thiết kế tình huống).

---

## 5. 8 nhóm kỹ thuật lõi

Tất cả kỹ thuật trong khóa đều thuộc 8 nhóm sau. Syllabus và Lesson Notes sẽ chỉ lấy con trong từng nhóm này.

### Framing

- Problem framing (định khung bài toán)
- Goal/output framing (định khung mục tiêu/đầu ra)
- Audience framing (định khung đối tượng)
- Scope design (thiết kế phạm vi)
- Task definition (xác định loại nhiệm vụ)

### Decomposition

- Top-down decomposition (bóc tách từ trên xuống)
- Functional decomposition (bóc tách theo chức năng)
- Conceptual decomposition (bóc tách theo khái niệm)
- Stakeholder decomposition (bóc tách theo bên liên quan)
- Temporal/process breakdown (bóc tách theo thời gian/quy trình)

### Information Architecture (IA – kiến trúc thông tin)

- Taxonomy (phân loại)
- Hierarchy (thứ bậc)
- Ontology thinking (tư duy mô hình thực thể–thuộc tính–quan hệ)
- Table / schema design (thiết kế bảng/lược đồ cột)
- Matrix design (thiết kế ma trận 2 chiều)

### Reasoning

- Chain of Thought (CoT – chuỗi suy nghĩ)
- Tree of Thought (ToT – cây suy nghĩ đa nhánh)
- Comparative reasoning (suy luận so sánh)
- Causal reasoning (suy luận nhân quả)
- Hypothesis-driven reasoning (suy luận theo giả thuyết)
- Analogical reasoning (suy luận tương tự/ẩn dụ)
- Counterfactual reasoning (suy luận phản thực tế)

### Expansion

- Breadth-first exploration (khám phá rộng trước)
- Depth-first exploration (đào sâu từng nhánh)
- Query expansion (mở rộng truy vấn/từ khóa)
- Faceted exploration (khám phá theo nhiều mặt/facet)
- Adjacent-domain expansion (mở rộng sang miền lân cận)
- Keyword mapping (bản đồ từ khóa)

### Validation

- Self-critique (tự phản biện)
- Assumption check (soi giả định)
- Gap detection (tìm chỗ thiếu)
- Contradiction check (tìm mâu thuẫn)
- Multi-model triangulation (tam giác hóa nhiều mô hình/nguồn)
- Confidence labeling (gắn nhãn độ tin cậy)

### Synthesis

- Pattern extraction (rút mẫu)
- Principle extraction (rút nguyên lý)
- Framework synthesis (tổng hợp thành khung)
- Layered summarization (tóm tắt nhiều tầng)
- Playbook design (thiết kế cẩm nang)

### Transfer

- Use-case mapping (map sang tình huống dùng)
- Workflow design (thiết kế quy trình làm việc)
- Curriculum design (thiết kế chương trình học)
- Rubric design (thiết kế bảng tiêu chí đánh giá)
- Teaching translation (dịch tri thức thành dạng dạy được)

Handbook chỉ chuẩn hóa “có những nhóm nào, dùng để làm gì”. Chi tiết từng kỹ thuật + prompt mẫu sẽ nằm trong Syllabus / Technique table / Lesson Notes.

---

## 6. Lộ trình trưởng thành: 6 level

SID nhắm tới người đã dùng AI 1–3 năm, nhưng muốn “lên level”. Khóa học định nghĩa 6 mức năng lực:

| Level | Tên                  | Đặc trưng                                                                 |
|-------|----------------------|---------------------------------------------------------------------------|
| L1    | Prompted User        | Biết định khung cơ bản, viết prompt rõ hơn, bớt cảm tính                   |
| L2    | Structured Extractor | Biết bóc tách chủ đề, ép AI trả ra cấu trúc (outline, bảng, taxonomy)     |
| L3    | Reasoning Operator   | Biết điều khiển AI suy luận (CoT, ToT, causal, comparative, hypothesis)  |
| L4    | Validation Analyst   | Biết kiểm định, phản biện, triangulation, epistemic labeling             |
| L5    | Knowledge Synthesizer| Biết rút pattern, nguyên lý, framework, playbook, quyết định model      |
| L6    | Intelligence Architect| Biết xây workflow, prompt stack, rubric, mini-course/knowledge system   |

### 6.1. Năng lực cốt lõi mỗi level

**L1 – Prompted User**

- Problem/Audience/Output framing.
- Prompt stack cơ bản (không còn dùng 1 master prompt cho mọi thứ).

**L2 – Structured Extractor**

- Top-down decomposition, taxonomy, hierarchy.
- Ép AI xuất ra outline, bảng, matrix có logic.

**L3 – Reasoning Operator**

- CoT, ToT, comparative, causal, hypothesis-driven.
- Biết chọn kỹ thuật reasoning theo bài toán.

**L4 – Validation Analyst**

- Self-critique, assumption check, gap detection, triangulation.
- Phân biệt fact / interpretation / assumption / hypothesis / recommendation.

**L5 – Knowledge Synthesizer**

- Pattern & principle extraction.
- Framework & playbook synthesis.
- Layered summarization (executive vs deep dive).

**L6 – Intelligence Architect**

- Workflow & SOP (Standard Operating Procedure – quy trình chuẩn) design.
- Curriculum & rubric design.
- Thiết kế mini-course, playbook, hoặc knowledge system.
- (Trong track nâng cao / builder: spec (bản đặc tả) cho Gem/GPT/RAG/tutor).

---

## 7. Quy trình chuẩn: nghiên cứu một chủ đề với AI

Đây là “recipe” (công thức) mà học viên sẽ thực hành lặp đi lặp lại.

### Bước 1 — Frame

Xác định:

- mục tiêu nhận thức,
- audience,
- output,
- scope,
- loại nhiệm vụ (**task type**: explain/compare/design/critique/teach…).

Kết quả: **Framing Brief**.

### Bước 2 — Explore rộng

- Breadth-first exploration:  
  map miền lõi / miền gần / miền mở rộng / out-of-scope.
- Query expansion:  
  core / near / technical / adjacent terms (từ khóa lõi/gần/kỹ thuật/liên quan).
- Faceted exploration:  
  technical / user / organizational / educational / ethical-epistemic (kỹ thuật/người dùng/tổ chức/giáo dục/đạo đức–tri thức).

Kết quả: **exploration map + keyword map + facet matrix.**

### Bước 3 — Architect

- Decomposition:
  - cây 3–4 tầng.
- IA:
  - taxonomy,
  - hierarchy,
  - bảng so sánh,
  - matrix 2 chiều (ví dụ: technique × mục tiêu).

Kết quả: **IA pack** cho chủ đề (outline + taxonomy + bảng + matrix).

### Bước 4 — Reason sâu

- Chọn vài node quan trọng:
  - phân tích bằng CoT, ToT, causal, comparative, hypothesis.

Kết quả: **reasoning pack** (CoT analysis, ToT branches, hypothesis table,…).

### Bước 5 — Validate

- Dán nhãn:
  - fact / interpretation / assumption / hypothesis / recommendation.
- Self-critique:
  - các điểm yếu, thiếu, mơ hồ.
- Assumption check, gap detection, contradiction check.
- (Khi cần) triangulation với mô hình/nguồn khác.

Kết quả: **validation report**.

### Bước 6 — Synthesize

Từ toàn bộ phân tích:

- rút pattern,
- rút 5–9 nguyên lý lõi,
- đóng gói thành framework 5–7 bước.

Tạo:

- checklist,
- decision model (mô hình quyết định),
- executive summary + deep dive (tóm tắt cho lãnh đạo + bản phân tích sâu).

Kết quả: **framework + checklist + summaries.**

### Bước 7 — Transfer

Map framework sang:

- use-case cụ thể,
- vai trò (PM, designer, educator, researcher, manager,…),
- điều kiện triển khai, rủi ro, KPI.

Thiết kế:

- workflow / SOP,
- mini-course / module,
- rubric đánh giá.

Kết quả: **workflow + teaching/operational asset.**

Khóa học SID sẽ đưa người học đi qua quy trình này nhiều lần, mỗi lần một chủ đề, mỗi lần sâu hơn.

---

## 8. Rubric đánh giá năng lực (tóm tắt)

Dưới đây là rubric rút gọn để đánh giá tiến bộ:

### 8.1. Năng lực 1 – Framing

- 0–1: câu hỏi mơ hồ, trộn nhiều mục tiêu, không audience, không output.
- 3: có problem, audience, output cơ bản.
- 5: framing sắc, nhìn ra misframing, viết Framing Brief chuẩn.

### 8.2. Năng lực 2 – Information Architecture

- 0–1: ý rời rạc, outline lộn xộn.
- 3: có outline, bảng, nhưng chưa tối ưu.
- 5: decomposition MECE (Mutually Exclusive, Collectively Exhaustive – không trùng, không thiếu), taxonomy/hierarchy rõ, bảng/matrix chọn đúng dạng.

### 8.3. Năng lực 3 – Reasoning

- 0–1: chỉ mô tả, không lập luận.
- 3: có CoT cơ bản.
- 5: chọn đúng kỹ thuật (CoT/ToT/causal/hypothesis/comparative), lập luận chặt, đa góc nhìn.

### 8.4. Năng lực 4 – Validation

- 0–1: tin output AI mặc định.
- 3: biết yêu cầu self-critique, check assumption.
- 5: validation hệ thống, tách lớp epistemic rõ, triangulation bài bản.

### 8.5. Năng lực 5 – Synthesis & Transfer

- 0–1: chỉ tóm tắt.
- 3: biết ghép ý thành checklist/framework cơ bản.
- 5: framework có logic, tái dùng được; có workflow, rubric, module dạy lại; map tốt sang use-case thực.

---

## 9. Chuẩn đầu ra cuối khóa

Một người hoàn thành SID (core) phải làm được ít nhất:

- Biến một chủ đề mơ hồ trong domain của mình thành **Framing Brief** chuẩn.
- Bóc tách một lĩnh vực thành:
  - outline 3–4 tầng,
  - taxonomy,
  - comparison table.
- Phân tích một vấn đề phức tạp bằng:
  - CoT,
  - ToT,
  - causal reasoning,
  - hypothesis-driven reasoning,
  - comparative reasoning.
- Kiểm định một output AI dài:
  - dán nhãn epistemic,
  - self-critique,
  - assumption/gap/contradiction check,
  - viết validation memo (bản ghi chú kiểm định).
- Tổng hợp chủ đề thành:
  - framework 5–7 bước có tên,
  - checklist triển khai,
  - executive summary + deep dive.
- Chuyển framework đó thành một trong các dạng:
  - mini-course 2–3 buổi,
  - playbook cho team,
  - knowledge workflow cho công việc,
  - (với học viên advanced) spec thô cho một Gem/GPT hoặc AI tutor.

---

## 10. Cách sử dụng Handbook trong khóa học

- **Trước khóa học:**
  - đọc chương 1–4 để nắm triết lý và framework 7 bước.
- **Trong khóa học:**
  - dùng phần 8 nhóm kỹ thuật + quy trình 7 bước như bản đồ tổng,
  - mỗi buổi sẽ zoom vào 1–2 nhóm kỹ thuật,
  - mỗi project sẽ bám vào bước cụ thể trong SID 7 bước.
- **Sau khóa học:**
  - dùng lại SID 7 bước + 8 nhóm kỹ thuật như “checklist tinh thần” mỗi khi làm việc tri thức với AI (nghiên cứu, viết sách, thiết kế course, build assistant,…).

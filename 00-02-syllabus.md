Dưới đây là bản Syllabus tổng hợp, gọn, bám đúng Handbook mới. Phần lesson chi tiết, ví dụ, project sẽ làm ở bước sau.

---

# Structured Intelligence Design (SID)  
Syllabus 8 Buổi — Bản Chuẩn Hóa

## 0. Định vị khóa học

- **Đối tượng**: người dùng AI 1–3 năm (đã dùng thường xuyên) nhưng:
  - hỏi prompt dài nhưng lệch gốc (mục tiêu, audience, output không rõ),
  - chưa bóc tách/kiến trúc hóa một chủ đề,
  - chưa kiểm định đầu ra AI,
  - chưa biết biến output AI thành framework, workflow, syllabus, playbook, hoặc knowledge system.

- **Mục tiêu tổng**:  
  Sau khóa học, học viên có thể:
  - Dùng AI để **khai thác, tổ chức, suy luận, kiểm định, tổng hợp và chuyển giao tri thức** có hệ thống,  
  - Xây được **một hệ tri thức mini** cho domain của mình (framework + workflow + asset dạy lại),  
  - Ở mức cao hơn: dùng các artifact đó làm nền để xây **Gem/GPT/tutor/assistant** (expert track).

- **Trục năng lực**:
  - 8 nhóm kỹ thuật: Framing, Decomposition, IA, Reasoning, Expansion, Validation, Synthesis, Transfer.
  - 6 level: Prompted User → Structured Extractor → Reasoning Operator → Validation Analyst → Knowledge Synthesizer → Intelligence Architect.

---

## 1. Kiến trúc chương trình

### 1.1. 8 buổi và mapping vào SID 7 bước

| Buổi | Tên | Bước SID trội | Level chính |
|------|-----|---------------|-------------|
| 1 | Framing as Cognitive Control | Frame | L1 |
| 2 | Prompt as Cognitive Interface & Prompt Stack | Frame → Reason (sơ) | L1 |
| 3 | Decomposition & Knowledge Mapping | Architect | L2 |
| 4 | Information Architecture & Representation | Architect | L2 |
| 5 | Expansion & Research Depth | Explore | L2–L3 |
| 6 | Reasoning Design with AI | Reason | L3 |
| 7 | Validation & Epistemic Control | Validate | L4 |
| 8 | Synthesis, Frameworking & Transfer | Synthesize → Transfer | L5–L6 |

### 1.2. Artifact chính mỗi buổi

| Buổi | Artifact bắt buộc |
|------|-------------------|
| 1 | Framing Brief + Misframing Analysis |
| 2 | Prompt Stack v1 cho 1 domain thật |
| 3 | Decomposition Tree (3–4 tầng) + Stakeholder/Functional map |
| 4 | IA Pack: taxonomy + hierarchy + comparison table/matrix |
| 5 | Exploration Map + Keyword Matrix + Research Path v1 |
| 6 | Reasoning Pack: CoT + ToT + causal + comparative + hypothesis |
| 7 | Validation Report + Epistemic Labeling + Triangulation Matrix |
| 8 | Framework (5–7 bước) + Workflow + Mini-teaching asset (outline khóa nhỏ / playbook / SOP tri thức) |

### 1.3. Capstone & Final project

- **Mini-capstone 1 (sau Buổi 2)**  
  - Đầu ra: Framing Brief + Prompt Stack cho 1 domain thực tế.

- **Mini-capstone 2 (sau Buổi 4)**  
  - Đầu ra: Knowledge Map (decomposition + IA pack) cho cùng domain.

- **Mini-capstone 3 (sau Buổi 7)**  
  - Đầu ra: Reasoning & Validation Pack cho 1 bài toán phức tạp trong domain đó.

- **Final Project (sau Buổi 8)**  
  - Đầu ra:
    - 1 framework 5–7 bước có tên,
    - 1 workflow triển khai,
    - 1 asset chuyển giao (mini-course 2–3 buổi / playbook cho team / knowledge workflow),
    - 1 rubric đánh giá.
  - Domain: do học viên chọn (ưu tiên domain thật họ đang làm việc).

---

## 2. Bảng khái niệm & kỹ thuật theo buổi (chỉ liệt kê – chi tiết ở Lesson Notes)

### Buổi 1 — Framing as Cognitive Control

**Mục tiêu buổi**

- Chuyển từ “hỏi theo bản năng” sang “định khung bài toán”.
- Biết viết **Framing Brief** làm nền cho mọi tương tác với AI.

**Khái niệm chính**

| Khái niệm | Vai trò |
|----------|---------|
| Topic vs Problem | Phân biệt chủ đề với bài toán thật cần giải |
| Problem Framing | Định rõ nhiệm vụ nhận thức (hiểu, so, thiết kế, dạy, chẩn đoán, quyết định) |
| Goal/Output Framing | Chọn loại artifact tri thức (bảng, framework, checklist, syllabus, rubric…) |
| Audience Framing | Gắn nội dung với trình độ/mục tiêu/bối cảnh người nhận |
| Scope Design | Xác định in-scope / out-of-scope để tăng chiều sâu |
| Task Definition | Phân loại nhiệm vụ: explain / compare / diagnose / design / critique / teach |
| Framing Brief | Bản tóm tắt khung bài toán dùng làm input cho Buổi 2 trở đi |

**Kỹ thuật trọng tâm (Framing group)**

- Problem framing
- Goal/output framing
- Audience framing
- Scope design
- Task definition

**Deliverables**

- 1 Framing Brief cho domain của học viên (150–250 từ).
- 1 bảng Misframing Analysis (ít nhất 3 prompt “dài nhưng lệch gốc” được mổ xẻ và viết lại).

---

### Buổi 2 — Prompt as Cognitive Interface & Prompt Stack

**Mục tiêu buổi**

- Hiểu prompt như **giao diện điều khiển nhận thức**, không phải câu lệnh đơn.
- Thiết kế **prompt stack nhiều bước** dựa trên Framing Brief.

**Khái niệm chính**

| Khái niệm | Vai trò |
|----------|---------|
| Prompt Architecture (RTC-COE) | Role – Task – Context – Constraints – Output – Evaluation |
| Prompt Stack | Chuỗi prompt theo phase (frame → extract → reason → validate → synthesize) |
| Constraints | Giảm nhiễu, ép phạm vi, độ sâu, tiêu chí |
| Output Specification | Chỉ định format, schema, artifact cụ thể |
| Evaluation-guided Prompting | Cho AI tiêu chí tự chấm / tự critique output của chính nó |

**Kỹ thuật trọng tâm (thuộc Framing + Reasoning tầng bề mặt)**

- Prompt architecture (RTC-COE)
- Constraint design
- Output specification
- Evaluation criteria trong prompt
- Prompt stack design (3–6 bước) cho 1 workflow tri thức

**Deliverables**

- 1 Prompt Stack v1 cho chính domain trong Framing Brief (tối thiểu 3 bước: Frame → Structure → Validate).
- 1 bảng so sánh “prompt xấu – prompt khá – prompt tốt” (trên prompt dài thực tế).

---

### Buổi 3 — Decomposition & Knowledge Mapping

**Mục tiêu buổi**

- Biết bóc tách 1 chủ đề thành **cấu trúc nhiều tầng**.
- Nhìn chủ đề từ nhiều logic: khái niệm, chức năng, stakeholder.

**Khái niệm chính**

| Khái niệm | Vai trò |
|----------|---------|
| Top-down Decomposition | Chia từ tổng quan → miền → nhóm → node chi tiết |
| Functional Decomposition | Chia theo chức năng / nhiệm vụ trong hệ thống |
| Conceptual Decomposition | Chia theo khái niệm nền, khái niệm trung gian, ứng dụng |
| Stakeholder Decomposition | Nhìn theo vai trò (learner, user, manager, expert, org) |
| MECE Discipline | Không trùng, không thủng trong decomposition |

**Kỹ thuật trọng tâm (Decomposition group)**

- Top-down decomposition (3–4 tầng)
- Functional decomposition
- Conceptual decomposition
- Stakeholder decomposition
- Overlap/gap checking

**Deliverables**

- 1 Decomposition Tree 3–4 tầng cho domain (ít nhất 20 node).
- 1 Functional map **hoặc** Stakeholder map cho cùng domain.
- 1 short memo: chọn logic decomposition nào phù hợp nhất cho dạy học / thực hành.

---

### Buổi 4 — Information Architecture & Representation

**Mục tiêu buổi**

- Biết chọn dạng biểu diễn (tree / taxonomy / table / matrix / flow) theo mục tiêu.
- Từ decomposition của Buổi 3, dựng **IA Pack** có thể dùng để dạy, so sánh, ra quyết định.

**Khái niệm chính**

| Khái niệm | Vai trò |
|----------|---------|
| Taxonomy | Phân loại thành nhóm theo tiêu chí rõ ràng |
| Hierarchy | Cấu trúc cha–con, từ tổng quan đến chi tiết |
| Ontology (thinking) | Mô hình hóa thực thể–thuộc tính–quan hệ–phụ thuộc |
| Table / Schema Design | Thiết kế cột trước khi đổ nội dung để so sánh / đánh giá |
| Matrix | Biểu diễn 2 chiều (ví dụ: kỹ thuật × mục tiêu, facet × độ sâu) |
| Representation Fit | Chọn format theo mục tiêu nhận thức, không phải “thói quen” |

**Kỹ thuật trọng tâm (IA group)**

- Taxonomy design
- Hierarchy building
- Table schema design
- Matrix design
- Ontology sketch (ở mức conceptual)

**Deliverables**

- 1 Taxonomy cho domain (theo 1 tiêu chí rõ).
- 1 Hierarchy phục vụ dạy học (outline khóa / handbook).
- 1 comparison table **hoặc** matrix (ví dụ: kỹ thuật × mục tiêu, facet × audience).
- Mini-IA Pack: lý do chọn mỗi dạng biểu diễn, dùng để làm gì.

---

### Buổi 5 — Expansion & Research Depth

**Mục tiêu buổi**

- Không còn đào sâu theo bản năng; biết **quét rộng có kỷ luật** rồi mới chọn nhánh để đào.
- Thiết kế **research path** cho chủ đề: breadth → chọn node → depth.

**Khái niệm chính**

| Khái niệm | Vai trò |
|----------|---------|
| Knowledge Space | Không gian tri thức của 1 chủ đề |
| Breadth-first Exploration | Quét toàn miền core/near/extended/out-of-scope |
| Depth-first Exploration | Đào sâu 1 nhánh theo nhiều lớp (định nghĩa → cơ chế → use case → giới hạn…) |
| Query Expansion | Core / near / technical / adjacent terms |
| Faceted Exploration | Phân tích theo facet: technical, user, org, educational, epistemic/ethical |
| Adjacent-domain Expansion | Kéo sang domain lân cận để làm giàu cách hiểu |
| Keyword Mapping | Bản đồ từ khóa cho nghiên cứu và dạy học |
| Node Prioritization | Chọn node đào sâu theo centrality, dependency, applicability, confusion risk |
| Research Path | Lộ trình breadth → selection → depth |

**Kỹ thuật trọng tâm (Expansion group)**

- Breadth-first exploration
- Depth-first exploration (có khung 6–8 lớp)
- Query expansion + keyword mapping
- Faceted exploration
- Adjacent-domain expansion
- Node prioritization
- Research path design

**Deliverables**

- Exploration Map (core / near / extended / out-of-scope).
- Keyword Expansion Matrix (core / near / technical / adjacent).
- Facet Matrix cho chủ đề.
- Depth Selection Memo (chọn 1–2 node đào sâu, có lý do).
- Research Path v1 (3 pha với checkpoint).

---

### Buổi 6 — Reasoning Design with AI

**Mục tiêu buổi**

- Biết **chọn và điều khiển kỹ thuật suy luận** phù hợp với bài toán.
- Tách rõ: mô tả bề mặt vs phân tích có logic, có trade-off, có phản biện.

**Khái niệm chính**

| Khái niệm | Vai trò |
|----------|---------|
| Chain of Thought (CoT) | Suy luận tuyến tính từng bước, để giải thích/trace logic |
| Tree of Thought (ToT) | Suy luận đa nhánh, xử lý bài toán mở, nhiều phương án |
| Hypothesis-driven Reasoning | Đặt, kiểm và so sánh các giả thuyết cạnh tranh |
| Causal Reasoning | Tìm nguyên nhân gốc (root cause), phân biệt tương quan và nhân quả |
| Comparative Reasoning | So sánh theo tiêu chí rõ ràng, phục vụ quyết định |
| Analogical Reasoning | Dùng tương tự để dạy và làm rõ khái niệm khó |
| Counterfactual Reasoning | “Nếu bỏ X đi thì sao?” để thấy điều kiện cần, phụ thuộc |

**Kỹ thuật trọng tâm (Reasoning group)**

- CoT (với nhấn mạnh “mỗi bước phải có cơ sở”)
- ToT (3–5 nhánh khác thật, không đổi câu chữ)
- Hypothesis-driven reasoning
- Causal reasoning (root cause vs symptom)
- Comparative reasoning (chọn tiêu chí trước)
- Analogical reasoning (ẩn dụ không méo nghĩa)
- Counterfactual reasoning (đúng bối cảnh)

**Deliverables**

- Reasoning Pack cho 1 vấn đề thật trong domain:
  - CoT analysis,
  - ToT 3+ nhánh,
  - hypothesis table (3–5 giả thuyết),
  - causal chain/root cause map,
  - comparative table (A/B/C theo tiêu chí).

---

### Buổi 7 — Validation & Epistemic Control

**Mục tiêu buổi**

- Không “tin AI vì nghe thuyết phục”.
- Biết đọc output qua lens:
  - fact / interpretation / assumption / hypothesis / recommendation,
  - self-critique,
  - triangulation.

**Khái niệm chính**

| Khái niệm | Vai trò |
|----------|---------|
| Fact / Interpretation / Assumption / Hypothesis / Recommendation | Phân lớp phát biểu để tránh “ảo tưởng tri thức” |
| Self-critique | Ép AI (và chính mình) tự phản biện output |
| Assumption Check | Lôi giả định ngầm ra ánh sáng |
| Gap Detection | Tìm phần thiếu, blind spot |
| Contradiction Check | Tìm mâu thuẫn nội bộ trong tài liệu dài |
| Multi-model Triangulation | Đối chiếu nhiều nguồn/mô hình để tìm vùng đồng thuận/bất đồng |
| Confidence Labeling | Gắn nhãn độ chắc chắn: high / medium / speculative |
| Epistemic Hygiene | Kỷ luật nhận thức khi đọc/dùng output AI |

**Kỹ thuật trọng tâm (Validation group)**

- Epistemic labeling (gắn nhãn câu/phần)
- Self-critique prompts
- Assumption check
- Gap detection
- Contradiction check
- Multi-model triangulation
- Confidence labeling

**Deliverables**

- Validation Report cho 1 output AI dài (do học viên chọn, liên quan domain của mình):
  - labeling bảng,
  - self-critique,
  - assumption list,
  - gap & contradiction findings,
  - (nếu có) triangulation với 1–2 output khác,
  - revision memo (sửa/viết lại phần trọng yếu).

---

### Buổi 8 — Synthesis, Frameworking & Transfer

**Mục tiêu buổi**

- Biết **từ nhiều mảnh rời rạc** (đã phân tích, validate) rút thành:
  - pattern,
  - nguyên lý,
  - framework mấy bước có tên,
  - workflow,
  - asset dạy lại/áp dụng.

**Khái niệm chính**

| Khái niệm | Vai trò |
|----------|---------|
| Pattern Extraction | Rút mẫu lặp từ nhiều case/output |
| Principle Extraction | Cô đọng pattern thành nguyên lý cốt lõi |
| Framework Synthesis | Đóng gói thành mô hình 5–7 bước có logic |
| Layered Summarization | Tóm tắt theo nhiều tầng (1 câu, 1 đoạn, deep dive) |
| Workflow Design | Biến framework thành chuỗi hành động (input → step → output → checkpoint) |
| Use-case Mapping | Map framework vào bối cảnh/role cụ thể |
| Teaching Translation | Chuyển tri thức chuyên gia thành bài giảng, ví dụ, hoạt động dạy |
| Rubric Design | Tiêu chí đánh giá năng lực/thực thi theo framework |

**Kỹ thuật trọng tâm (Synthesis + Transfer group)**

- Pattern extraction
- Principle extraction
- Framework synthesis
- Layered summarization
- Workflow design
- Use-case mapping
- Teaching translation
- Rubric design (cơ bản)

**Deliverables**

- 1 Framework 5–7 bước (có tên, từng bước có mục tiêu, input, output, lỗi phổ biến).
- 1 Workflow thực thi (với checkpoint).
- 1 asset chuyển giao:
  - mini-course outline (2–3 buổi), **hoặc**
  - playbook triển khai trong team, **hoặc**
  - knowledge workflow chi tiết cho một nhiệm vụ thật.
- 1 Rubric v1 (3–5 tiêu chí, 4–5 mức độ) để đánh giá áp dụng framework.

---

## 3. Cấu trúc đánh giá (Assessment)

- **Bài tập hằng buổi** (deliverable per session): 30%
- **3 Mini-capstone** (sau buổi 2, 4, 7): 30%
- **Final Project** (sau buổi 8): 40%

**Điều kiện qua khóa (gợi ý)**

- Tổng điểm ≥ 70/100.
- Final Project ≥ 60/100.
- Không bỏ quá 2 deliverables buổi.

---

## 4. Chuẩn đầu ra theo Level

Sau 8 buổi, một học viên:

- **L1 – Prompted User**:  
  - Viết được Framing Brief, Prompt Stack cơ bản.
- **L2 – Structured Extractor**:  
  - Tạo Decomposition Tree, Taxonomy, Hierarchy, Comparison Table cho domain.
- **L3 – Reasoning Operator**:  
  - Dùng CoT, ToT, causal, comparative, hypothesis vào 1 vấn đề thật.
- **L4 – Validation Analyst**:  
  - Viết Validation Report có labeling, self-critique, assumption/gap detection.
- **L5 – Knowledge Synthesizer**:  
  - Tạo Framework 5–7 bước + Workflow + Checklist, có logic.
- **L6 – Intelligence Architect (entry)**:  
  - Thiết kế 1 mini-course / playbook / knowledge workflow dựa trên framework đó,
  - Có rubric đánh giá.

(Expert Builder Track – Gems / Custom GPT / RAG / Tutor – sẽ là **khóa tiếp theo**, dùng chính artifact từ khóa này làm đầu vào.)

---



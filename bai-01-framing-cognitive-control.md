# Buổi 1 — Framing as Cognitive Control  
> Problem Framing & Goal Structuring for AI-mediated Knowledge Work

## 0. Bạn sẽ nhận được gì sau buổi này?

Sau khi hoàn thành Buổi 1, bạn sẽ:

1. Phân biệt rõ:
   - **Chủ đề (topic)** vs **bài toán (problem)** vs **đầu ra (output)**.
2. Nhìn ra vì sao prompt mình đang dùng **dài nhưng vẫn sai gốc**.
3. Viết được **Framing Brief** cho 1 chủ đề trong domain của bạn:
   - có **mục tiêu, audience, scope, output, task** rõ ràng,
   - dùng được làm **input** cho mọi buổi sau (prompt stack, decomposition, IA,…).
4. Tự **chẩn đoán misframing** trong 3–5 prompt cũ của bản thân.

> Nếu bạn làm nghiêm túc, chỉ riêng buổi này đã làm chất lượng làm việc với AI tăng rõ rệt, ngay cả khi chưa học tiếp các buổi khác.

---

## 1. Tại sao “Framing” là buổi đầu tiên?

### 1.1. Lỗi điển hình của người dùng AI 1–3 năm

Bạn (chắc) đã từng:

- Viết một prompt rất dài, kiểu:

  > “Bạn hãy đóng vai chuyên gia hàng đầu thế giới về RAG, giải thích cho tôi một cách cực kỳ chi tiết và sâu sắc, liệt kê các bước triển khai, các best practice, các sai lầm thường gặp, đưa ví dụ thực tế và cho tôi lộ trình học tập từ cơ bản đến nâng cao…”

- Và nhận một câu trả lời:
  - nghe **rất hay**,
  - trông **rất đầy đủ**,
  - nhưng:
    - khó dùng ngay,
    - không ăn khớp với bối cảnh của bạn (VD: bạn không cần triển khai production, chỉ cần dạy workshop nội bộ),
    - đọc xong vẫn… hơi “mù”.

Đó là triệu chứng của **framing sai**, không phải do model “ngu” hay bạn “viết chưa đủ dài”.

### 1.2. Bản chất của lỗi

Các prompt “dài mà sai gốc” thường có những lỗi:

- Chủ đề rõ (VD: “RAG”, “AI literacy”), **nhưng bài toán mờ**:
  - bạn muốn **hiểu**, **so sánh**, **thiết kế**, **dạy**, hay **ra quyết định**?
- Không nói rõ audience:
  - ai là người sử dụng kiến thức này? người mới, PM, dev, giáo viên, lãnh đạo?
- Không nêu output dưới dạng artifact:
  - bảng, framework, workflow, syllabus, rubric…?
- Scope trôi dạt:
  - vừa muốn từ cơ bản đến nâng cao,  
    vừa muốn cả lý thuyết lẫn production lẫn teaching,  
    trong 1 prompt duy nhất.

**Framing** là bước bạn **chỉnh lại gốc tư duy**, trước khi nghĩ đến “prompt cho hay hơn”.

---

## 2. Bức tranh tổng: Buổi 1 nằm ở đâu trong toàn khóa?

Khung 7 bước SID:

> Frame → Architect → Explore → Reason → Validate → Synthesize → Transfer

Buổi 1 chính là **Frame**.

- Nếu Frame sai:
  - Architect (bóc tách, dựng cấu trúc) sẽ lạc,
  - Explore (quét rộng) sẽ quá rộng/hẹp,
  - Reason (suy luận) sẽ “sâu nhầm chỗ”,
  - Validate (kiểm định) sẽ chấm nhầm tiêu chí,
  - Synthesize/Transfer sẽ đóng gói ra thứ không dùng được.

Từ Buổi 2 trở đi, bạn sẽ luôn xuất phát từ **Framing Brief** viết ở buổi này.

---

## 3. Bản đồ khái niệm của Buổi 1

### 3.1. Các khái niệm trụ cột

| Khái niệm            | Nghĩa / Vai trò chính                                                                 |
|----------------------|----------------------------------------------------------------------------------------|
| Topic                | Chủ đề, miền nội dung (“RAG”, “AI literacy”, “AI agents”, “HCI for AI tools”…)       |
| Problem Framing      | Định rõ **nhiệm vụ nhận thức** cần làm với chủ đề: hiểu/so/thiết kế/dạy/đánh giá…    |
| Goal/Output Framing  | Định rõ **đầu ra** là artifact gì: bảng, framework, checklist, syllabus, rubric…     |
| Audience Framing     | Ai sẽ dùng đầu ra: nền tảng, kinh nghiệm, mục tiêu, bối cảnh                         |
| Scope Design         | Phạm vi: nói tới đâu, không nói gì, sâu tới đâu, theo góc nào                         |
| Task Definition      | Loại nhiệm vụ AI được dùng: explain / compare / diagnose / design / critique / teach |
| Framing Brief        | Bản tóm tắt 150–250 từ, gom toàn bộ 5 thứ trên, làm “đầu não” cho mọi bước sau      |
| Misframing           | Định khung sai: chủ đề đúng nhưng bài toán/đầu ra/audience/scope/task sai hoặc mơ hồ |

### 3.2. Mô hình 5W-O

Đây là “khung xương” đơn giản nhưng cực mạnh:

> **What – Why – Who – Where – Width/Depth – Output**

- **What**: đang bàn về **cái gì**? (topic, lĩnh vực, vấn đề)
- **Why**: hỏi để **làm gì**? (mục tiêu nhận thức, quyết định nào phụ thuộc?)
- **Who**: cho **ai**? (audience học / dùng)
- **Where**: trong **bối cảnh** nào? (công ty, ngành, level, ràng buộc)
- **Width/Depth**: rộng/sâu tới đâu? (không quá nông, không quá ôm đồm)
- **Output**: cần **ra cái gì**? (artifact nào, dùng để làm gì tiếp?)

> Một Framing Brief tốt **ít nhất** phải chạm đủ 6 ô này.

---

## 4. Học từng kỹ thuật – có ví dụ sai thật

### 4.1. Kỹ thuật 1 — Problem Framing

#### 4.1.1. Cốt lõi

- **Topic** = “đang nói về cái gì”
- **Problem** = “đang cần làm gì với cái đó”

Ví dụ thực tế (sai):

> “Hãy giải thích thật chi tiết về AI agents, các khái niệm liên quan, các kỹ thuật phổ biến, các công cụ hiện nay, đưa ví dụ ứng dụng trong doanh nghiệp.”

Vấn đề:

- Topic = AI agents → rõ.
- Nhưng Problem:
  - Bạn muốn **hiểu** để làm gì?
  - Để **xây**, **mua**, **đánh giá**, hay **dạy**?

AI sẽ trả lời “đúng chủ đề” nhưng **sai vấn đề**.

#### 4.1.2. Cách tư duy lại

Tự hỏi:

- Tôi đang muốn:
  - hiểu cho bản thân,
  - so sánh các hướng/giải pháp,
  - chẩn đoán vấn đề đang gặp,
  - thiết kế thứ gì mới (framework, quy trình, khóa học),
  - hay đánh giá/kiểm định 1 thứ hiện có?

Đổi từ:

> “Giải thích AI agents”

sang:

> “Tôi muốn hiểu AI agents **đủ để** [mục đích]…”

Ví dụ tốt hơn:

- “Tôi muốn hiểu AI agents đủ để **thiết kế 1 AI assistant** hỗ trợ team customer support hiện tại.”
- “Tôi muốn hiểu AI agents để **dạy lại cho đội PM nội bộ**, không đi sâu vào code, chỉ tập trung vào kiến trúc, use case, và rủi ro.”

#### 4.1.3. Prompt mẫu (để AI giúp bạn frame problem)

Bạn có thể dùng thẳng với model:

```text
Tôi đang quan tâm chủ đề: [TOPIC].

Hãy giúp tôi định khung bài toán thật sự tôi đang cần giải quyết.

Yêu cầu:
1. Liệt kê 4–6 bài toán nhận thức khác nhau có thể ẩn dưới chủ đề này, ví dụ:
   - hiểu khái niệm
   - so sánh giải pháp
   - chẩn đoán vấn đề
   - thiết kế giải pháp
   - thiết kế khóa học
   - thiết kế framework đánh giá
2. Với mỗi bài toán, mô tả:
   - mục tiêu thực sự
   - loại đầu ra (output) phù hợp
   - rủi ro nếu nhầm sang bài toán khác
3. Dựa trên mô tả của tôi: [MÔ TẢ NGẮN VỀ MỤC TIÊU/BỐI CẢNH],
   hãy đề xuất 1 problem framing tối ưu và viết thành 1 câu rõ ràng.

Trả ra:
- 1 bảng các bài toán tiềm năng
- 1 câu problem statement bạn nghĩ phù hợp nhất với tôi.
```

---

### 4.2. Kỹ thuật 2 — Goal/Output Framing

#### 4.2.1. Cốt lõi

**Output** không phải “câu trả lời dài hơn”.  
Output = **artifact tri thức**.

Ví dụ các artifact:

- concept note,
- comparison table,
- framework 5–7 bước,
- checklist,
- decision tree,
- workflow,
- syllabus,
- rubric,
- playbook,…

Sai lầm rất phổ biến:

> “Hãy giải thích thật chi tiết…” → không nói cần “chi tiết” dưới dạng **gì**.

#### 4.2.2. Ví dụ prompt sai → sửa

Prompt sai (rất giống người dùng 1–3 năm):

> “Hãy phân tích thật chi tiết về RAG, đưa ra các thành phần, cách hoạt động, so sánh với fine-tuning, đưa best practice triển khai trong doanh nghiệp, nêu các sai lầm phổ biến và cho tôi lộ trình học trong 3 tháng.”

Lỗi:

- quá nhiều task (explain + compare + best practice + learning path),
- không nói output muốn ở **dạng gì**.

Sửa theo Goal/Output Framing:

> “Mục tiêu của tôi là: trong 2 tuần tới, tôi phải **dạy 1 buổi nội bộ 90 phút** cho team product (không phải engineer) về RAG, để họ đủ hiểu cách RAG ảnh hưởng tới thiết kế sản phẩm.
>
> Hãy:
> 1) đề xuất 3 dạng output có thể phù hợp nhất (ví dụ: outline bài giảng, comparison table, framework pipeline),
> 2) phân tích ưu/nhược của mỗi dạng,
> 3) sau đó chọn 1 dạng tối ưu và tạo **outline bài giảng 90 phút** (cho người đã biết LLM cơ bản) với: mục tiêu học, các section chính, thời lượng dự kiến.”

Thấy khác biệt?

- Bài toán rõ (dạy 90 phút),
- Audience rõ,
- Output = outline bài giảng,
- Scope (không phải engineer, đã biết LLM cơ bản).

#### 4.2.3. Template ngắn để tự check

Trước khi hỏi AI, tự hỏi:

- Output mình cần là:
  - Bảng?
  - Framework?
  - Checklist?
  - Syllabus?
  - Rubric?
  - Playbook?

Nếu chưa trả lời được → **chưa xong Goal Framing**.

---

### 4.3. Kỹ thuật 3 — Audience Framing

#### 4.3.1. Cốt lõi

Nội dung **đúng** không đủ; nó phải **đúng với người này**.

Bạn cần nêu rõ cho AI:

- nền tảng (IT, non-IT, business,…),
- trải nghiệm với AI (chưa dùng / dùng 1–3 năm / kỹ sư),
- mục tiêu (hiểu, dạy, triển khai, quản lý chiến lược),
- ràng buộc (thời gian, ngôn ngữ, tài nguyên).

Ví dụ:

- “Người học đã dùng ChatGPT/Gemini 2 năm, chủ yếu để viết content và tóm tắt, nhưng chưa học NLP hoặc ML.”

#### 4.3.2. Case thực tế

Prompt thực tế (sai):

> “Hãy giải thích về ontology trong AI một cách chi tiết, có ví dụ minh họa.”

AI sẽ đưa 1 bài giảng… **chung chung**.

Sửa với Audience Framing:

> “Hãy giải thích về ontology trong AI cho **PM sản phẩm** đã dùng AI 2 năm nhưng chưa học formal về NLP.
> 
> Bối cảnh:
> - họ không cần viết code,
> - họ cần hiểu đủ để làm việc với team kỹ thuật và thiết kế sản phẩm tốt hơn.
> 
> Hãy:
> - tránh ký hiệu toán,
> - tập trung vào ví dụ gần gũi với việc thiết kế schema thông tin, user journey, và search,
> - chỉ ra 3 hiểu lầm phổ biến của PM khi nghĩ về ‘ontology’.”

---

### 4.4. Kỹ thuật 4 — Scope Design

#### 4.4.1. Cốt lõi

Scope tốt = **chọn cái không làm** rõ ràng.

Ví dụ prompt sai (rất phổ biến):

> “Hãy dạy tôi về RAG từ A đến Z, từ kiến thức cơ bản đến triển khai production, từ góc nhìn kỹ thuật và kinh doanh, giúp tôi có thể tự triển khai cho doanh nghiệp của mình.”

Lỗi:

- A–Z,
- cơ bản → production,
- kỹ thuật lẫn business,
- trong 1 shot.

Sửa với Scope:

> “Tôi **không** muốn học cách build RAG sản phẩm production.
> 
> Mục tiêu hiện tại:
> - hiểu **đủ** về RAG để:
>   - phân biệt được với fine-tuning,
>   - thảo luận với CTO/engineer,
>   - và dạy lại 1 buổi 2 tiếng cho đội product/PM.
> 
> Do đó:
> - **in-scope**: khái niệm, pipeline ở mức high-level, ưu/nhược vs fine-tuning, use case đặc biệt phù hợp/không phù hợp, các lỗi hiểu sai phổ biến.
> - **out-of-scope**: code chi tiết, config cụ thể, tối ưu hạ tầng.
> 
> Hãy thiết kế 1 outline nội dung 2 tiếng phù hợp với scope trên.”

Scope rõ → AI hết “bị kéo” vào chuyện code/hạ tầng.

---

### 4.5. Kỹ thuật 5 — Task Definition

#### 4.5.1. Cốt lõi

Bạn đang yêu cầu AI làm **nhiệm vụ gì**?

Các task điển hình:

- **Explain** – giải thích, định nghĩa, mô tả.
- **Compare** – so sánh A/B/C theo tiêu chí.
- **Diagnose** – tìm nguyên nhân, lỗi, nguyên nhân gốc.
- **Design** – tạo framework, quy trình, kiến trúc, khóa học.
- **Critique** – phản biện, tìm điểm yếu, rủi ro.
- **Teach** – soạn giáo án, bài tập, ví dụ để dạy người khác.

Sai lầm: nhét **4–5 task** vào 1 prompt mà không tách phase.

Ví dụ xấu rất quen:

> “Hãy giải thích, so sánh, thiết kế, phản biện và dạy tôi về prompt engineering trong một câu trả lời duy nhất, càng chi tiết càng tốt.”

Thay vào đó, tách phase; ví dụ:

1. Explain → hiểu khái niệm.
2. Compare → so với cách dùng AI cảm tính.
3. Design → thiết kế syllabus/buổi học.
4. Critique → phản biện syllabus đó.
5. Teach → final lesson notes.

---

## 5. Framing Brief – sản phẩm cuối của Buổi 1

### 5.1. Framing Brief là gì?

Một đoạn 150–250 từ, mô tả:

- Topic,
- Problem (bài toán),
- Audience,
- Context,
- Scope (in/out),
- Output sơ bộ,
- Task type chính.

Framing Brief **không phải prompt**; nó là **mô tả bài toán** để dùng:

- cho chính bạn,
- cho AI (như context),
- cho các buổi sau (bóc tách, IA, reasoning…),
- cho mentor/đồng đội hiểu bạn đang làm gì.

### 5.2. Template Framing Brief

Bạn có thể dùng khung dưới để tự viết:

```text
[1] Chủ đề (topic)
Tôi đang làm việc với chủ đề: [TOPIC].

[2] Bài toán (problem)
Bài toán thực sự tôi cần giải quyết là: [PROBLEM STATEMENT 1–2 câu].
(Mục đích cuối cùng: [MỤC ĐÍCH], ví dụ: dạy lại, thiết kế sản phẩm, ra quyết định, vv.)

[3] Audience
Đầu ra của tôi sẽ dùng cho: [AI CHO AI? CHO TÔI? CHO TEAM? CHO NGƯỜI HỌC NÀO?]
- Nền tảng: [VD: đã dùng AI 1–3 năm, không code, làm PM/marketer/educator…]
- Mục tiêu học/dùng: [vd: hiểu để dạy lại, hiểu để áp dụng…]

[4] Scope (in-scope / out-of-scope)
Trong phạm vi này, tôi:
- In-scope: [NHỮNG GÌ SẼ BÀN]
- Out-of-scope: [NHỮNG GÌ KHÔNG BÀN] (vì [LÝ DO])

[5] Output & Task Type
Tôi đang cần AI hỗ trợ chủ yếu cho nhiệm vụ: [EXPLAIN/COMPARE/DESIGN/CRITIQUE/TEACH…]
Đầu ra ưu tiên: [VD: outline 3 buổi học + framework 5–7 bước + checklist triển khai].

[6] Rủi ro nếu framing sai
Nếu định khung sai, rủi ro là: [VD: học lệch trọng tâm, output không dùng được, dạy sai đối tượng…]
```

---

## 6. Thực hành từng bước – với prompt sai thật của bạn

### 6.1. Bài tập 1 — Misframing Diagnosis Lab (dùng prompt thật của bạn)

**Mục tiêu**  
Nhìn ra **lỗi ở gốc** trong cách mình hỏi AI.

**Bước 1: Lấy dữ liệu thật**

- Mở lịch sử chat AI (ChatGPT/Gemini/Grok/Claude…),
- Chọn **3–5 prompt** mà bạn:
  - đã từng rất kỳ vọng,
  - nhưng output nhận về dù “hay” vẫn **không dùng được** hoặc **không đúng cái bạn cần**.

Ví dụ (giả lập):

> “Hãy đóng vai chuyên gia hàng đầu về RAG, giải thích cho tôi tất cả những gì cần biết về RAG từ cơ bản đến nâng cao, bao gồm kiến trúc, các ứng dụng, cách triển khai trong doanh nghiệp, các công cụ phổ biến hiện nay và cho tôi lộ trình học trong 3 tháng để trở thành chuyên gia RAG.”

**Bước 2: Tự chấm prompt**

Cho mỗi prompt, tạo 1 bảng như sau (có thể viết tay hoặc markdown):

| Yếu tố      | Trạng thái hiện tại                     | Ghi chú lỗi |
|------------|------------------------------------------|------------|
| Topic      | [Có / Không]                            |            |
| Problem    | [Rõ / Mơ hồ / Trộn nhiều bài toán]      |            |
| Audience   | [Có / Mơ hồ / Không]                    |            |
| Scope      | [Có / Quá rộng / Quá hẹp / Không]       |            |
| Output     | [Rõ dạng artifact / “trả lời chi tiết”] |            |
| Task type  | [1 nhiệm vụ / 3–4 nhiệm vụ trộn]        |            |

Đánh dấu lỗi, ví dụ:

- Problem: “muốn biết tất cả mọi thứ” → **không phải bài toán**.
- Audience: **không nêu**.
- Scope: từ cơ bản đến nâng cao, kỹ thuật lẫn kinh doanh.
- Task: explain + design lộ trình học → ít nhất 2 task.

**Bước 3: Viết lại prompt theo tư duy Framing (chưa cần hoàn hảo)**

Đừng nhảy ngay sang “prompt đẹp”; trước hết, viết 1–3 câu tóm lại **Framing Brief rút gọn** cho prompt đó.

Ví dụ:

> “Tôi là PM sản phẩm, đã dùng AI 2 năm nhưng không code. Trong 1 tháng tới tôi phải dạy 1 buổi nội bộ 90 phút về RAG cho team marketing + product. Mục tiêu là mọi người hiểu vì sao RAG quan trọng trong thiết kế trải nghiệm tra cứu tri thức nội bộ, chứ không dạy họ tự build. Tôi cần 1 outline bài giảng 90 phút + 1 comparison table giữa RAG và fine-tuning ở mức high-level.”

---

### 6.2. Bài tập 2 — One Topic, Many Problems

**Mục tiêu**  
Hiểu sâu rằng **chủ đề =/= bài toán**.

**Bước 1: Chọn 1 chủ đề trong domain của bạn**

Ví dụ:

- “AI literacy trong đội ngũ giảng viên đại học”
- “AI agents cho doanh nghiệp nhỏ”
- “Prompt engineering cho UX research”
- “RAG trong knowledge work cho luật sư”

**Bước 2: Liệt kê ít nhất 5 bài toán khác nhau**

Ví dụ với “AI literacy trong đội ngũ giảng viên đại học”:

1. Hiểu/định nghĩa AI literacy cho bối cảnh đại học.
2. So sánh AI literacy với digital literacy / information literacy.
3. Thiết kế một framework năng lực AI literacy cho giảng viên.
4. Thiết kế khóa học 4 buổi về AI literacy cho giảng viên.
5. Thiết kế rubric đánh giá AI literacy của giảng viên trong năm tới.

**Bước 3: Với mỗi bài toán, gán 1 output chính & 1 task type**

Ví dụ:

- Bài toán 3:
  - Output: framework năng lực (bảng level).
  - Task type: design.
- Bài toán 5:
  - Output: rubric 4–5 tiêu chí, 4–5 mức mỗi tiêu chí.
  - Task type: design + critique.

---

### 6.3. Bài tập 3 — Audience Shift Exercise

**Mục tiêu**  
Nhận ra audience thay đổi thì **cách đặt bài toán & output** cũng đổi hẳn.

**Bước 1: Chọn 1 chủ đề**

Ví dụ: Prompt engineering.

**Bước 2: Viết 3 phiên bản framing cho 3 audience**

1. Audience A: người mới dùng AI (sinh viên năm 1).
2. Audience B: người dùng AI 1–3 năm (power user, marketer).
3. Audience C: quản lý/giám đốc muốn hiểu để ra quyết định chiến lược.

Với mỗi audience, viết 3–4 câu:

- mục tiêu,
- phạm vi,
- output.

So sánh 3 bản: bạn sẽ thấy **framing thay đổi rất mạnh**, dù topic vẫn là “prompt engineering”.

---

## 7. Assignment Buổi 1 – Framing Brief cho domain của bạn

### 7.1. Đề bài

Chọn **một chủ đề thuộc domain thật** của bạn (càng thực tế càng tốt).

Ví dụ:

- AI trong thiết kế chương trình đào tạo nội bộ.
- AI hỗ trợ UX research.
- AI cho content marketing B2B.
- AI hỗ trợ kiểm tra tài liệu pháp lý.
- AI tutor cho luyện thi.

Viết **1 Framing Brief hoàn chỉnh** theo template dưới.

### 7.2. Yêu cầu cấu trúc

Bài nộp nên có dạng markdown:

```markdown
# Framing Brief — [Tên chủ đề]

## 1. Chủ đề (Topic)
...

## 2. Bài toán (Problem)
...

## 3. Audience
...

## 4. Scope (In-scope / Out-of-scope)
...

## 5. Output & Task Type
...

## 6. Rủi ro nếu framing sai
...
```

**Gợi ý độ dài**: 150–250 từ.

### 7.3. Gợi ý rubric tự chấm

| Tiêu chí            | Mô tả                                                                                          | Điểm (0–5) |
|---------------------|------------------------------------------------------------------------------------------------|------------|
| Problem clarity     | Phân biệt rõ topic và problem? Problem statement sắc, không chung chung?                      | /5         |
| Goal/Output framing | Artifact đầu ra được nêu rõ? (bảng, framework, syllabus…) Dùng được ngay trong bước sau?     | /5         |
| Audience fit        | Audience mô tả cụ thể (nền tảng, mục tiêu, bối cảnh), không chỉ “người mới/người dùng AI”?   | /5         |
| Scope quality       | In-scope / out-of-scope rõ? Phù hợp với mục tiêu, không A–Z một lượt?                         | /5         |
| Task definition     | Có chỉ ra nhiệm vụ chính (explain/compare/design/teach/critique…)? Không trộn quá nhiều?     | /5         |
| Clarity & usability | Bản brief rõ ràng, đọc xong có thể dùng ngay làm input cho prompt stack buổi 2?              | /5         |

> Nếu tổng < 20/30, hãy quay lại chỉnh cho đến khi đạt. Bạn sẽ “nợ” chính mình ở các buổi sau nếu Framing Brief chưa đạt.

---

## 8. Cách dùng Buổi 1 cho các buổi sau

- **Buổi 2 (Prompt Stack)**: dùng Framing Brief này làm **context** để:
  - thiết kế role,
  - assignment rõ task per prompt,
  - tránh nhồi quá nhiều task trong 1 prompt.
- **Buổi 3–4 (Decomposition & IA)**:
  - dùng topic + scope trong brief để **bóc tách và dựng cấu trúc**.
- **Buổi 5 (Expansion)**:
  - dùng problem + audience để **chọn trọng tâm khi quét rộng và đào sâu**.
- **Buổi 6–7 (Reasoning & Validation)**:
  - dùng goal/output + task type để:
    - chọn kỹ thuật reasoning,
    - đặt tiêu chí validation.
- **Buổi 8 (Synthesis & Transfer)**:
  - dùng toàn bộ brief để:
    - chọn framework phù hợp,
    - thiết kế asset dạy/áp dụng sát với bối cảnh thực tế.

---

## 9. Tự kiểm cuối buổi – 5 câu hỏi bạn nên trả lời “Có”

1. Tôi có thể nhìn vào 1 prompt dài (của chính mình) và chỉ ra:
   - nó đang thiếu gì trong: Problem, Audience, Scope, Output, Task?
2. Tôi có thể viết 3–5 bài toán nhận thức khác nhau cho **cùng 1 chủ đề**.
3. Tôi có thể nêu rõ **output ưu tiên** cho một nhiệm vụ (VD: “tôi cần 1 framework 5–7 bước + checklist”, không chỉ “trả lời chi tiết”).
4. Tôi đã viết xong **Framing Brief** cho 1 chủ đề thật của mình.
5. Tôi cảm thấy, nếu chỉ cần thay đổi framing, chất lượng làm việc với AI của tôi đã **khác đi rõ ràng**, mà chưa cần kỹ thuật nâng cao.

Nếu bạn chưa thoải mái với bất kỳ câu nào ở trên, hãy:

- quay lại assignment,
- hoặc gửi lại 1 prompt cũ của bạn (trong thực tế),  
  rồi áp dụng lại mọi thứ trong buổi này để “phẫu thuật” đến khi thấy rõ mình đã đổi.

---

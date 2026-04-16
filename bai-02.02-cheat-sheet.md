### Cheat Sheet — Buổi 2: Prompt như Giao Diện Nhận Thức & Prompt Stack

---

#### 1. Khung RTC‑COE (cấu trúc một prompt tốt)

RTC‑COE = **Role – Task – Context – Constraints – Output – Evaluation**

1. **Role (vai trò)**  
   - Mô hình đang “đóng vai” ai?  
   - Ví dụ: chuyên gia, giáo viên, cố vấn, reviewer khó tính, business analyst…

2. **Task (nhiệm vụ)**  
   - Một nhiệm vụ chính: explain / design / critique / compare / teach / diagnose / summarize…  
   - Tránh trộn 4–5 task trong một prompt.

3. **Context (bối cảnh)**  
   - Domain, audience, thời gian, mục tiêu, tài nguyên, phạm vi (in/out‑of‑scope).  
   - Giúp mô hình hiểu “đang giải bài toán trong thế giới nào”.

4. **Constraints (ràng buộc)**  
   - Không làm gì / phải làm gì.  
   - Độ dài, mức chi tiết, phong cách, điều cần tránh.  
   - Constraints phải **có nghĩa**, không phải “hãy nói thật chi tiết”.

5. **Output (dạng đầu ra)**  
   - Artifact cụ thể: bảng, checklist, outline, framework, email mẫu, kế hoạch 30 ngày…  
   - Không chỉ “trả lời cho kỹ”.

6. **Evaluation (tiêu chí đánh giá)**  
   - Định nghĩa thế nào là “output tốt/kém”.  
   - Ví dụ: “tốt nếu có ví dụ cụ thể, tránh buzzword, có thể dùng làm xương sống cho khóa học…”

---

#### 2. Master Prompt vs Prompt Stack

**Master prompt 1000 chữ:**

- Nhồi nhiều task vào 1 câu.
- Context mơ hồ, constraints kém, output không rõ.
- Kết quả: câu trả lời dài, lan man, thiếu chiều sâu.

**Prompt Stack:**

- Chuỗi **3–6 prompt**, mỗi prompt = 1 phase riêng.
- Mỗi prompt có RTC‑COE bên trong.
- Output của bước trước là input của bước sau.

Ví dụ các **phase điển hình**:

1. Clarify – làm rõ bài toán (tóm tắt + giả định + câu hỏi).
2. Structure – bóc tách & cấu trúc (danh sách mảnh/kỹ năng/thành phần).
3. Refine – rút gọn & thiết kế khung (5–7 năng lực/kỹ năng).
4. Design – đóng gói (lộ trình, kế hoạch, tài liệu dạy học…).
5. Critique – phản biện & chỉnh sửa (điểm mạnh, điểm yếu, phiên bản A/B).

---

#### 3. Hai tầng “stack”

1. **Tầng vi mô – RTC‑COE trong mỗi prompt**  
   - Bên trong một prompt: Role → Task → Context → Constraints → Output → Evaluation.  
   - Đây là “stack thành phần” của **một** prompt.

2. **Tầng vĩ mô – Prompt Stack giữa các prompt**  
   - Nhiều prompt nối nhau theo phase: Prompt 1 → Prompt 2 → Prompt 3 → Prompt 4…  
   - Mỗi prompt có Role/Task/Context khác, xử lý một phần khác của bài toán.

---

#### 4. Dấu hiệu prompt “dài‑sai”

- Không rõ Role.
- Trộn nhiều Task (giải thích + thiết kế + dạy lại + phê bình…).
- Context mờ (không biết đang nói cho ai, trong bối cảnh nào).
- Constraints mơ hồ (“thật chi tiết”, “chuẩn xác tuyệt đối”).
- Output không phải artifact (chỉ là “hãy trả lời cho kỹ”).
- Không có Evaluation (không biết căn cứ nào đánh giá tốt/xấu).

---

#### 5. Cách chuyển từ master prompt sang Prompt Stack

1. **Viết Framing Brief** (Topic, Problem, Audience, Scope, Output, rủi ro).  
2. **Bước 1 – Clarify Prompt**  
   - Cho mô hình tóm tắt bài toán, liệt kê giả định, đặt câu hỏi làm rõ.  
3. **Bước 2 – Structure Prompt**  
   - Bóc tách thành danh sách kỹ năng/thành phần, nhóm theo category.  
4. **Bước 3 – Refine Prompt**  
   - Gom thành 5–7 năng lực/kỹ năng cốt lõi, có mô tả + ví dụ + hành vi.  
5. **Bước 4 – Design Prompt (nếu cần)**  
   - Dùng khung để thiết kế lộ trình, kế hoạch, tài liệu.  
6. **Bước 5 – Critique Prompt**  
   - Reviewer khó tính: nêu điểm mạnh/yếu, rủi ro, gợi ý phiên bản A/B.

---

#### 6. Thói quen tốt khi viết prompt sau Buổi 2

- Luôn **nghĩ theo RTC‑COE** trước khi gõ.
- Hạn chế **nhồi quá 2 task** trong một prompt.
- Ưu tiên **chuỗi prompt** hơn là một câu “làm hết mọi thứ”.
- Mỗi prompt đều:
  - có **Role** rõ ràng,
  - nhắm **Task** chính,
  - đặt vào **Context** cụ thể,
  - có **Constraints** dùng được,
  - yêu cầu **Output** là artifact,
  - kèm theo **Evaluation** (ít nhất là một vài tiêu chí cơ bản).

---

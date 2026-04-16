
## 10 Câu hỏi trắc nghiệm tự kiểm tra (Buổi 2)

Format:  
- Mỗi câu có 4 lựa chọn A/B/C/D.  
- Đáp án ở cuối (phần “Đáp án”).

---

### Câu 1

Mục tiêu chính của khung RTC‑COE là gì?

A. Làm prompt dài hơn để mô hình “hiểu đủ”.  
B. Giúp cấu trúc một prompt thành các phần rõ ràng: vai, nhiệm vụ, bối cảnh, ràng buộc, đầu ra, tiêu chí.  
C. Bắt buộc mọi prompt phải dùng tiếng Anh.  
D. Giúp mô hình trả lời nhanh hơn về mặt kỹ thuật.

---

### Câu 2

Thành phần nào sau đây **không** thuộc RTC‑COE?

A. Role  
B. Task  
C. Context  
D. Memory

---

### Câu 3

Trong RTC‑COE, “Constraints” nên được hiểu đúng là:

A. Mọi yêu cầu càng nhiều càng tốt để mô hình cố gắng đáp ứng.  
B. Những ràng buộc cụ thể về độ dài, phong cách, điều phải tránh hoặc phải có.  
C. Phần giải thích chi tiết lý thuyết nền tảng.  
D. Các câu hỏi phụ để mô hình tự hỏi lại.

---

### Câu 4

Đặc điểm quan trọng nhất của **Prompt Stack** (so với master prompt) là gì?

A. Mỗi prompt trong stack phải ngắn hơn 2 câu.  
B. Tất cả prompt trong stack có cùng Role và Task.  
C. Mỗi prompt trong stack xử lý một phase khác nhau và dùng output bước trước làm input bước sau.  
D. Stack chỉ dùng cho lập trình viên, không phù hợp người dùng phổ thông.

---

### Câu 5

Ví dụ nào dưới đây là dấu hiệu của **master prompt dài‑sai**?

A. “Đóng vai giáo viên, giải thích khái niệm A cho học sinh lớp 5, có ví dụ đơn giản.”  
B. “Đóng vai chuyên gia, hãy giải thích khái niệm A, liệt kê mọi mô hình liên quan, so sánh chúng, đưa ví dụ, chỉ ra sai lầm phổ biến, đề xuất công cụ áp dụng trong 5 ngành khác nhau, và thiết kế luôn một khóa học 10 buổi.”  
C. “Đóng vai reviewer, hãy chấm điểm bản kế hoạch này theo 3 tiêu chí.”  
D. “Đóng vai project manager, tóm tắt 5 ý chính của tài liệu kèm 3 rủi ro chính.”

---

### Câu 6

Trong một Prompt Stack chuẩn, các prompt **nên**:

A. Là 3–4 phiên bản sửa lại cùng một câu hỏi, để “tối ưu dần” kết quả.  
B. Là các bước khác nhau về nhiệm vụ: clarify → structure → refine → critique…  
C. Luôn có độ dài bằng nhau để dễ so sánh.  
D. Sử dụng ngẫu nhiên Role và Task để tạo đa dạng.

---

### Câu 7

Khi viết “Output” trong RTC‑COE, lựa chọn nào mô tả đúng nhất?

A. Chỉ cần nói “hãy trả lời chi tiết”.  
B. Chỉ cần yêu cầu “trả lời ngắn gọn trong 1 đoạn”.  
C. Cần chỉ rõ dạng artifact: bảng, danh sách, khung, checklist, kế hoạch…  
D. Chỉ cần viết “hãy cho câu trả lời đúng”.

---

### Câu 8

Khi nào nên thêm phần “Evaluation” vào prompt?

A. Khi muốn mô hình tự kiểm tra chất lượng output theo một số tiêu chí cụ thể.  
B. Khi muốn prompt ngắn nhất có thể.  
C. Khi không có Framing Brief.  
D. Khi cần mô hình viết code.

---

### Câu 9

Phát biểu nào sau đây mô tả đúng **hai tầng stack** đã học?

A. RTC‑COE là stack giữa các prompt; Prompt Stack là stack bên trong một prompt.  
B. RTC‑COE và Prompt Stack là một, không có sự khác biệt.  
C. RTC‑COE là “stack vi mô” bên trong 1 prompt; Prompt Stack là “stack vĩ mô” giữa nhiều prompt theo phase.  
D. Cả hai chỉ là tên gọi marketing, không có ý nghĩa thực tế.

---

### Câu 10

Trong quy trình thiết kế Prompt Stack, bước nào dưới đây thường nên làm **trước**?

A. Viết ngay prompt Design lộ trình/hệ thống mà không cần Framing Brief.  
B. Bỏ qua phase clarify, đi thẳng vào structure.  
C. Viết Framing Brief, sau đó dùng Clarify Prompt để mô hình tóm tắt + nêu giả định + đặt câu hỏi.  
D. Yêu cầu mô hình tự đoán bối cảnh và làm tất cả các bước cùng lúc.

---

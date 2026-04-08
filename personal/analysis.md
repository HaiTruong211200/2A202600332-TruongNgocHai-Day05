# UX exercise — MoMo Moni AI

## Sản phẩm: MoMo — Moni AI Assistant (phân loại chi tiêu)

## 4 paths

### 1. AI đúng

- User Hỏi lịch trình của chuyến bay có mã vé cụ thể -> NEO trả lời đúng lịch trình cho chuyến bay
- User thấy trả lời đúng, không cần làm gì thêm

### 2. AI không chắc

- User hỏi lịch trình của chuyến bay nhưng không có mã vé → NEO trả lời các thông tin của các chuyến bay mà không hỏi lại xem là chuyến bay có mã vé nào, sau đó tự kết thúc và đưa ra gợi ý đánh giá chất lượng dịch vụ cho người dùng mà chưa phục vụ được mục đích người dùng
- Vấn đề: không có cơ chế hỏi lại khi thiếu thông tin

### 3. AI sai

- User hỏi thông tin chuyến bay rẻ nhất hiện tại -> NEO trả lời thông tin các chuyến bay đã cũ (ví dụ trong 2025)
- Vấn đề: AI không rõ thời điểm của các chuyến bay hiện tại

### 4. User mất niềm tin

- Sau nhiều lần sai, user muốn chuyển sang hỏi người chăm sóc khách hàng nhưng việc chuyển sang CSKH rất lâu và trong thời gian đó người dùng có thể tự đi tra được vấn đề của mình.

## Path yếu nhất: Path 2

- Khi AI bị không chắc chắn, không có cơ chế hỏi lại người dùng để xác định đầy đủ thông tin hoặc không có cơ chế rằng tôi chưa đủ thông tin để trả lời
- Bị hallucination, trả lời không chính xác, lan man, không có ích với người dùng

## Gap marketing vs thực tế

- Marketing: Chatbot thông minh hướng dẫn và giúp đỡ đặt chuyến bay dễ dàng
- Thực tế: Không có guide bắt đầu để hướng dẫn người dùng, không trả lời thông tin chính xác, làm mất thời gian người dùng. Thời gian phản hồi lâu, không có cơ chế "contextual loading message" làm cho người dùng không biết rằng liệu chatbot có đang phản hồi với câu hỏi của mình hay không
- Gap lớn nhất: marketing nói về giúp đỡ đặt chuyến bay dễ dàng -> khi hỏi về thông tin, chatbot trả lời sai và phản hồi lâu, không có hướng dẫn cụ thể cho người dùng.

## Sketch

(Ảnh đính kèm: sketch.jpg)

- As-is: giao dịch → auto-tag → user thấy kết quả → nếu sai phải vào sửa thủ công
- To-be: giao dịch → auto-tag → nếu confidence thấp: hiện "Bạn muốn phân loại?"
  → user chọn → AI ghi nhận correction → hiện "Đã học, lần sau sẽ chính xác hơn"

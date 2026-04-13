# BT1_MOBILE
BT1_MOBILE  
PHÁT TRIỂN ỨNG DỤNG VỚI MÃ NGUỒN MỞ  
HỌ TÊN: NGUYỄN THI KIM HUỆ  
LỚP: K58KTP  
Link:  

NỘI DUNG BÀI TẬP:  
1. [Phần A:  Đăng ký tên miền cho cá nhân:](./A.md)
2. [Phần B: Cài đặt Ubuntu + Docker](./B.md)
3. [Phần C: Cấu hình docker compose:](./C.md)
4. [Phần D:(Bonus - không bắt buộc))](./D.md)
5. [Phần E:Triển khai (level test) ứng dụng](./E.md)
6. [Phần F: Gỡ lỗi](./F.md)
7. [Phần G: Triển khai ứng dụng đến End-user và trả lời câu hỏi](./G.md) 

- Trang web ban đầu chỉ mang tính chất thử nghiệm, giúp làm quen với cách vận hành của server. Tuy nhiên, để tăng tính ứng dụng và chiều sâu cho bài tập, em đã điều chỉnh hướng phát triển sang xây dựng một hệ thống tạo nội dung thông minh. Việc thay đổi này không chỉ giúp cải thiện trải nghiệm người dùng mà còn tạo cơ hội thực hành việc tích hợp API và quản lý nhiều container Backend (như Node-RED và Python), đảm bảo các thành phần hoạt động đồng bộ thay vì chỉ dừng lại ở một website tĩnh đơn giản.  

- Cơ chế xử lý dữ liệu hai luồng (Hybrid Processing)

Hệ thống được thiết kế với hai cách xử lý dữ liệu riêng biệt, thể hiện rõ sự khác nhau giữa xử lý phía client và phía server:  

a) Chế độ "Tạo Offline" (Client-side Processing)  
Khi người dùng chọn chế độ này, toàn bộ quá trình tạo nội dung sẽ diễn ra trực tiếp trên trình duyệt. Cụ thể, chương trình sẽ sử dụng một cơ chế chọn ngẫu nhiên từ tập dữ liệu đã được định nghĩa sẵn trong file script.js. Nhờ đó, người dùng có thể nhận kết quả ngay lập tức mà không cần gửi yêu cầu lên server, giúp giảm độ trễ và vẫn đảm bảo hoạt động ngay cả khi không có kết nối mạng.  


G: TRIỂN KHAI ỨNG DỤNG ĐẾN END - USER    
1. Tạo Tunnel trong Cloudfare
   <img width="1451" height="707" alt="image" src="https://github.com/user-attachments/assets/b2549725-dbc7-46be-ba7a-28afe0679405" />
2. Sinh ra file.pem sau khi login thành công
   <img width="1158" height="691" alt="image" src="https://github.com/user-attachments/assets/a4347dcb-9d6b-495f-8e4c-718a824a05a1" />
3. Tạo tunnel 
<img width="1164" height="702" alt="image" src="https://github.com/user-attachments/assets/e301f05c-819c-4253-b0e4-bf385af774ec" />
4. Tạo tunnel
<img width="677" height="78" alt="image" src="https://github.com/user-attachments/assets/94581dbd-ca5c-47b0-bf84-deef0195ba05" />  
5. Gắn Domain với Tunnel
<img width="1211" height="70" alt="image" src="https://github.com/user-attachments/assets/e86a87bd-b872-409d-a4c6-6ed69ceb0921" />
6.chạy tunnel bằng lệnh cloudflared tunnel run mytunnel
<img width="1270" height="692" alt="image" src="https://github.com/user-attachments/assets/349283c9-c420-4abf-9a29-91207e28c826" />
7.mở trình duyệt test
<img width="1827" height="965" alt="image" src="https://github.com/user-attachments/assets/b6d59649-41b1-4049-ada4-36ff4943c796" />
8.Thêm service cloudfare
<img width="1260" height="631" alt="image" src="https://github.com/user-attachments/assets/aa35ef3a-dd2f-45e7-8856-70c893988f83" />
9.sửa config tunnel để trỏ vào Docker
<img width="1015" height="557" alt="image" src="https://github.com/user-attachments/assets/4f3225b6-c112-4c38-aff7-4f1d7d8e9a74" />
10.Test cuối cùng
<img width="1804" height="961" alt="image" src="https://github.com/user-attachments/assets/2f41d38a-c890-4b6e-b8b0-ac6110058f67" />
https://app.huek58.io.vn/








G. Câu hỏi về bài làm?  
1.Tại sao phải dùng Nginx làm Reverse Proxy mà không trỏ thẳng Tunnel vào Node-RED?  
2.Sự khác biệt giữa việc Mount file và Mount thư mục trong Docker là gì?  
3.Nếu thay đổi file index.html ở máy Ubuntu, nội dung trên web có thay đổi ngay không? Tại sao?  
4.docker-compose.yml khai báo các services có phần restart: always hoặc restart: unless-stopped : chúng để làm gì?  
5.Cách khai báo để tất cả các services đều dùng chung 1 network? lợi ích của việc khai báo này là gì? Sửa đổi file docker-compose để tất cả các service đều   dùng chung 1 network.  
6.Tìm cách đưa Cloudflare Token vào trong file .env rồi sau đó thêm .env vào file .gitignore trước khi push code lên github. Tại sao nói đây là điều quan   trọng về bảo mật mã nguồn?  
7.Tại sao chúng ta nên thêm hậu tố :ro khi mount file cấu hình Nginx?  
8.Khi dùng Cloudflare Tunnel: có cần thiết phải mở cổng cho các service nữa không?  
Trả lời  
1. Tại sao dùng Nginx làm Reverse Proxy?  
- Bảo mật: Ẩn backend (Node-RED)  
- Quản lý nhiều service qua 1 domain  
- Hỗ trợ SSL, cache  
→ Giúp hệ thống an toàn và linh hoạt hơn  

2. Mount file vs Mount thư mục  
- Mount file: ánh xạ 1 file (config)  
- Mount thư mục: ánh xạ cả folder (code, data)  
→ File: chi tiết | Folder: linh hoạt  

3. Sửa index.html có cập nhật ngay không?  
- Có (nếu dùng volume)  
→ Vì container đọc trực tiếp từ máy host  
- Không mount → phải build lại  

4. restart: always / unless-stopped  
- always: luôn tự chạy lại  
- unless-stopped: chạy lại trừ khi stop thủ công  
→ Đảm bảo hệ thống luôn hoạt động  

5. Dùng chung network  
Cấu hình:  
networks:  
  mynetwork:  

services:  
  nginx:  
    networks:  
      - mynetwork  
  app:  
    networks:  
      - mynetwork  

Lợi ích:  
- Giao tiếp bằng tên service  
- Không cần mở port nội bộ  
- Tăng bảo mật  

6. Cloudflare Token + .env + .gitignore  
- Token là thông tin nhạy cảm  
→ Nếu lộ có thể bị hack  
→ .env + .gitignore giúp bảo vệ mã nguồn  

7. Tại sao dùng :ro khi mount Nginx?  
- Read-only (chỉ đọc)  
→ Tránh bị sửa hoặc tấn công  
→ Tăng bảo mật  

8. Cloudflare Tunnel có cần mở port không?  
- Không cần  
→ Kết nối từ trong ra ngoài  
→ Không expose server  
→ Bảo mật cao hơn  


  







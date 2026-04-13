1. Tạo : ./myapi

2. <img width="1102" height="141" alt="image" src="https://github.com/user-attachments/assets/2fd4e2a5-4af2-44d0-b4be-6e1c26f892ec" />

 3. TẠO FILE: ./myapi/requirements.txt

 4. Kiểm tra  
cat ~/myapp/myapi/requirements.txt

4. TẠO FIEL: ./myapi/Dockerfile

5. SỬA ĐỔI DOCKER-COMPOSE ĐỂ SỦE DỤNG MYAPP  
Mở file: docker-compose.yml  
nano ~/myapp/docker-compose.yml  
  
Sửa thành như sau:  

6. SỬA: nginx/nginx.conf để /api trỏ tới service myapi cổng 9630
Mở file: Nginx.conf
nano ~/myapp/nginx/nginx.conf  

Sửa thành như sau:  

7. TEST  
a) Truy cập http://172.24.250.160:9630


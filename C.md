C.CẤU HÌNH DOCKER COMPOSE  
1. Tạo project ~/myapp  
2.  Vào thư mục myapp

   <img width="370" height="66" alt="image" src="https://github.com/user-attachments/assets/9ab71868-74b3-4e0b-9f9a-212838fb7739" />    
   
3. TẠO THƯ MỤC: ./myweb  
mkdir -p myweb nginx nodered

<img width="515" height="41" alt="image" src="https://github.com/user-attachments/assets/1ecc98a3-fb1c-466b-80a2-72a9fefbd6e0" />  

4. Tạo File index.html  
nano myweb/index.html

<img width="1101" height="643" alt="image" src="https://github.com/user-attachments/assets/14b27c73-bf1f-4070-9347-c7ec8d8c4075" />  

5. Tạo docker-compose.yml  
nano docker-compose.yml


<img width="1110" height="636" alt="image" src="https://github.com/user-attachments/assets/0823127b-9c41-4fda-97fd-8af003a31bc5" />  

6. Edit file ./nodered/settings.js để nodered bắt buộc đăng nhập 
chay lệnh: docker compose up -d


<img width="1102" height="642" alt="image" src="https://github.com/user-attachments/assets/4f0da935-5417-4f98-b614-9d0d95ee8ab8" />  








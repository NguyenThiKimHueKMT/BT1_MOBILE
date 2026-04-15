E. TRIỂN KHAI (LEVEL TEST) ỨNG DỤNG  
1. CHUYỂN VÀO THƯ MỤC: ~/myapp

   <img width="722" height="60" alt="image" src="https://github.com/user-attachments/assets/59e1d25d-40aa-4ee9-abe6-8209a50a9ce3" />
2. CHẠY HỆ THỐNG BẰNG DOCKER COMPOSE

   <img width="661" height="215" alt="image" src="https://github.com/user-attachments/assets/178b227a-ce51-4ab1-bf81-96d77a187fba" />

3. KIỂM TRA CÁC CONTAINER ĐANG CHẠY

   <img width="1204" height="245" alt="image" src="https://github.com/user-attachments/assets/a21f3771-05eb-4c8c-b63f-60c34b653e52" />
   
a) KIỂM TRA TỪNG SERVICE ĐỘC LẬP QUA IP VÀ PORT

   <img width="1917" height="798" alt="image" src="https://github.com/user-attachments/assets/fb3e8885-192c-401b-9198-55e7c04c48a0" />

b)Nginx Web  

<img width="1000" height="673" alt="image" src="https://github.com/user-attachments/assets/1c4d6677-c47c-4661-9829-f7d9ef500afb" />  

c) cấu hình function 

<img width="1542" height="946" alt="image" src="https://github.com/user-attachments/assets/0aed67dc-7ecd-442d-8d81-1adedf89afc2" />    

d) Test API Node-red trực tiếp  

<img width="1696" height="810" alt="image" src="https://github.com/user-attachments/assets/6b651571-4208-4c2a-8853-9f5cbf6a097c" />  

5. TẠO API GET ĐƠN GIẢN TRONG NODE-RED  
a) Kéo 3 Node (http in, function, http response)

<img width="1524" height="951" alt="image" src="https://github.com/user-attachments/assets/70fe22c1-3928-45a5-97ea-4752431a2ec4" />    

b) Cấu hình http in  

Method: GET  
URL: /hello  

<img width="804" height="484" alt="image" src="https://github.com/user-attachments/assets/c6dc2362-4a33-47ab-ab6e-4af86c72b5e7" />    
c) Test API Node-red trực tiếp    
<img width="1624" height="861" alt="image" src="https://github.com/user-attachments/assets/45415b32-7829-4d23-9b3f-e1c75365f9ab" />  

6. KIỂM TRA API QUA Nginx  
a) Trường hợp A: /api đang trỏ sang Node-RED

b) Trường hợp B: /api đang trỏ sang Flask API  

7. SỬA: ./myweb/index.html ĐỂ DÙNG API ĐÃ KHAI BÁO PROXY_PASS  
Mở file: index.html  
nano ~/myapp/myweb/index.html
<img width="1106" height="639" alt="image" src="https://github.com/user-attachments/assets/39963425-8ddf-4775-97d7-f567f3f26c7e" />

Kết quả  
<img width="1625" height="851" alt="image" src="https://github.com/user-attachments/assets/eabbdd00-7945-4e39-a917-51037d45dae3" />  
<img width="1570" height="843" alt="image" src="https://github.com/user-attachments/assets/d30b1894-0629-4f89-8574-5882636b5b75" />  
















   




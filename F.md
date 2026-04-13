F.Gỡ Lỗi  
1. KIỂM TRA NHANH KHI docker compose up -d có lỗi  

2. THÊM HEALTHCHECK CHO myapi  
Mở file: docker-compose.yml  
nano ~/myapp/docker-compose.yml  


<img width="1163" height="703" alt="image" src="https://github.com/user-attachments/assets/4dd17f20-a9ed-4b56-825e-435dd3146e9f" />  

 
Mở Dockerfile: nano ~/myapp/myapi/Dockerfile  

Sửa thành  

<img width="1185" height="708" alt="image" src="https://github.com/user-attachments/assets/0e16be90-85d7-470d-ac8c-4eca50a7a3a6" />  
Sau đó build lại: docker compose up -d --build  

<img width="1104" height="656" alt="image" src="https://github.com/user-attachments/assets/b7506ff5-53c0-436e-8cf2-0d0f843c7f4d" />  

3. GIỚI HẠN RAM CHO 1 SERVICE

   <img width="1102" height="649" alt="image" src="https://github.com/user-attachments/assets/bbbd30c9-fad5-4a81-bd77-cc023fbe70e3" />
4. DÙNG docker compose stats

   <img width="1107" height="635" alt="image" src="https://github.com/user-attachments/assets/997c73e2-1af3-4c7d-9178-e45f0fa60f55" />






F.Gỡ Lỗi  
1. KIỂM TRA NHANH KHI docker compose up -d có lỗi  
docker compose ps  

Lệnh này giúp xác định  
container nào đang Up  

container nào Restarting  

container nào Exited  

2. THÊM HEALTHCHECK CHO myapi  
Mở file: docker-compose.yml  
nano ~/myapp/docker-compose.yml  

Sửa thành:

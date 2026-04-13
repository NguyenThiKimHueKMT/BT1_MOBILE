G: TRIỂN KHAI ỨNG DỤNG ĐẾN END - USER  
1. TẠO TUNNEL TRONG CLOUDFARE  
Bước 1: Tạo thư mục  

mkdir -p /home/duong/.cloudflared  

Bước 2: Set quyền  

sudo chown -R 1000:1000 /home/duong/.cloudflared  

sudo chmod -R 777 /home/duong/.cloudflared  

Bước 3: Đăng nhập Cloudflare trên Ubuntu.  

Chạy lệnh : sudo docker run -it --rm -v /home/duong/.cloudflared:/home/nonroot/.cloudflared cloudflare/cloudflared tunnel login  
 Sau khi chạy:  

Nó sẽ đưa 1 link  



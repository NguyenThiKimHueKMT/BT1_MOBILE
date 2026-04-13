<img width="917" height="533" alt="image" src="https://github.com/user-attachments/assets/ebf1281f-c7a5-4467-a09f-cc8e91c35776" />B. CÀI ĐẶT UBUNTU VÀ DOCKER  
1. Cài đặt UBUNTU 24.04.4 LTS
2. a) Kiểm tra Hyper - V
Nhấn Win + R -> Gõ: optionalfeatures .
Tích:  
Hyper-V  
Hyper-V Platform  
Hyper-V Management Tools

<img width="684" height="593" alt="image" src="https://github.com/user-attachments/assets/f708067b-2891-4c60-bb73-15f1f77f2fae" />  

2. TẢI UBUNTU TRÊN HYPER-V  
a) Dowload Ubuntu  

Download file iso để cài đặt  

<img width="349" height="54" alt="image" src="https://github.com/user-attachments/assets/a3a5680d-21e0-420e-88cd-a4e050795696" />    

b) Tạo máy ảo trong Hyper-V  

Bước 1: Mở Hyper-V Manager  

New → Virtual Machine  

<img width="597" height="251" alt="image" src="https://github.com/user-attachments/assets/9f607e1f-e2d1-4cac-9d65-3c921af8017e" />  
Cấu hình:  

Name: Ubuntu  
Specify Generation: Chọn Generation 2 (Bắt buộc để hỗ trợ tốt nhất cho Ubuntu mới).  
Assign Memory: Nhập 2048 MB (2GB). Nên tích chọn Use Dynamic Memory   
Configure Networking: Tạm chọn Default Switch (để máy ảo có internet)  
Connect Virtual Hard Disk: Để mặc định (thường là 127GB, nhưng nó sẽ chỉ chiếm dung lượng thực tế dùng).  
Installation Options: Chọn dòng Install an operating system from a bootable image file, sau đó nhấn Browse và chọn file ISO Ubuntu đã tải  

Tạo máy ảo ubuntu  

<img width="883" height="670" alt="image" src="https://github.com/user-attachments/assets/215d45ce-bd0d-497e-90c0-8459d124b7bb" />  

Thêm file IOS  

<img width="890" height="677" alt="image" src="https://github.com/user-attachments/assets/bb57576a-4d52-492e-b483-a46c70092f9c" />  
Tạo uername và passwork cho máy ảo ubuntu  

<img width="1283" height="1017" alt="image" src="https://github.com/user-attachments/assets/d4c17e03-e86a-4d22-938a-489f648a52ad" />  

Đăng nhập máy ảo ubuntu  

<img width="1285" height="1014" alt="image" src="https://github.com/user-attachments/assets/a16bf10c-078c-4877-842f-08879578b7d7" />  

Chạy lệnh ip -4 appr lấy ip  

<img width="1028" height="551" alt="image" src="https://github.com/user-attachments/assets/eaf70021-9ab4-4816-a1ed-1e283a103d88" />  

Chạy lệnh ssh@hue172.19.234.139 để kết nối với window  

<img width="931" height="547" alt="image" src="https://github.com/user-attachments/assets/8aa1e6cb-8f36-481f-9b9b-e4e08ec4f037" />  

Chạy 2 lệnh để cài docker  
sudo apt update    
sudo apt install docker.io -y   

<img width="915" height="531" alt="image" src="https://github.com/user-attachments/assets/7632f698-1c95-4f39-85b8-ee226e414984" />  

Chạy lệnh docker --version để kiểm tra phiên bản Docker  

<img width="913" height="551" alt="image" src="https://github.com/user-attachments/assets/a1c84be8-9931-429e-8bce-655f5553a2f9" />  

Chạy lệnh sudo apt install docker-compose -y để cài docker compose  

<img width="913" height="525" alt="image" src="https://github.com/user-attachments/assets/707e172d-41fa-4e37-a579-849271a60fa1" />  

Chạy lệnh docker-compose --version để kiểm tra phiên bản docker compose  

<img width="908" height="522" alt="image" src="https://github.com/user-attachments/assets/34f78b5c-7f97-415c-a5cb-b9267dd14515" />  

Cấu hình để docker chạy mà không cần tiền tố sudo bằng lệnh sudo usermod -aG docker $USER  

<img width="917" height="530" alt="image" src="https://github.com/user-attachments/assets/0065ba2e-d83d-48ad-be14-2ab9a71b3b2d" />  

9. Đảm bảo tường lửa trên Ubuntu đã cho phép các cổng 80, 1880, 9630 (Lệnh: sudo ufw allow ...)  
1. Cài Ufw  
sudo apt install ufw -y

<img width="816" height="635" alt="image" src="https://github.com/user-attachments/assets/88997a42-5813-47e6-8cbb-e31c0040578c" />  

Bước 2: Mở các port  

<img width="914" height="530" alt="image" src="https://github.com/user-attachments/assets/9c4e58c0-5cb6-4331-a31f-88fc82d87b4e" />  

Bước 3: Cho phép SSH  

<img width="912" height="530" alt="image" src="https://github.com/user-attachments/assets/1379538d-2977-4a98-8639-01ccae45152f" />  

Bước 4: Bật FireWall  
sudo ufw --force enable  

<img width="917" height="533" alt="image" src="https://github.com/user-attachments/assets/d542701f-face-407f-9414-524c12b2ddf1" />  

Bước 5: Kiểm tra  
sudo ufw status   

<img width="886" height="533" alt="image" src="https://github.com/user-attachments/assets/eb593221-d653-41a6-95ce-f9a65103e3a5" />  























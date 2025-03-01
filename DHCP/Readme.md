![image](https://github.com/user-attachments/assets/316be1e0-a050-45a6-b671-ea01f97a43c2)

---

### **Bước 1: Kết nối và Cấu hình cơ bản**

### **Bước 2: Cấu hình DHCP**

### **Trường hợp 1: R1 và R2 làm DHCP server**

Trên R1:

Tạo ra một DHCP pool cho mạng 192.168.1.0/24, tên của pool là LAN1:

![image](https://github.com/user-attachments/assets/987c4023-f24f-4cb7-aa7f-0ee0085ac409)

Tại PC1 ta kiểm tra IP đã nhận chưa:

![image](https://github.com/user-attachments/assets/3e35a41f-5fc0-497e-aeb9-fdc5b6024b1d)

Sau khi PC1 đã nhận được IP, ta thực hiện lệnh kiểm tra danh sách địa chỉ IP đã cấp phát trên R1 bằng câu lệnh "show ip dhcp binding":

![image](https://github.com/user-attachments/assets/d2a8d5e3-f449-4d37-8b91-8fb2cd7eaf00)

Thực hiện cấu hình DHCP một cách tương tự trên R2:

![image](https://github.com/user-attachments/assets/344e5b7e-a9a7-43d7-bea9-17934da6fe30)

### **Trường hợp 2: R1 làm DHCP server, R2 làm DHCP relay agent**

Xóa pool LAN2 đã tạo trên R2 ở trường hợp 1:

![image](https://github.com/user-attachments/assets/ad6db9f3-3c98-41ff-bd68-d04281ea28da)

Trên R1 tạo thêm một DHCP pool có tên là LAN2 cho mạng 192.168.2.0/24:

![image](https://github.com/user-attachments/assets/7f81cd44-1c5f-4f63-8edf-9b3e8081b1c6)

Cấu hình R2 thành DHCP Relay Agent, phục vụ cho việc chuyển tiếp các gói tin DHC các client trên cổng F0/0 đến DHCP server R1:

![image](https://github.com/user-attachments/assets/2342250e-2ec1-403d-a5e8-9a7bf9efd1d8)

Cấu hình static route để R1 có thể gửi trả các thông tin DHCP về mạng 192.168.2.0/24:

![image](https://github.com/user-attachments/assets/a0bbab1b-c1ca-44db-8499-b201bbc979b3)

Sau khi PC2 đã nhận được IP, thực hiện kiểm tra danh sách những địa chỉ IP mà DH( server R1 đã cấp phát bằng câu lệnh "show ip dhcp binding":

![image](https://github.com/user-attachments/assets/c310a3ee-148c-4249-88ff-82d12aa09ee5)












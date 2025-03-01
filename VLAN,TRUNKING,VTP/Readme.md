![image](https://github.com/user-attachments/assets/0d915399-8e8c-4ffd-a9cd-7d6e541b3c70)

---

### **Bước 1: Cấu hình địa chỉ IP**

---

### **Bước 2: Cấu hình trunk**

Thiết lập các đường trunk đấu nối giữa các switch:

![image](https://github.com/user-attachments/assets/5b00cdc8-aed7-457b-8951-cc8374e3de8b)

Kiểm tra thông tin đường trunk:

![image](https://github.com/user-attachments/assets/d5cea49d-55ea-4587-b867-6379618f5285)

Thực hiện cấu hình tương tự với các cổng F0/1, F0/2 của SW2 và F0/2 của SW3.

---

### **Bước 3: Cấu hình VTP**

Cấu hình VTP server trên SW1:

![image](https://github.com/user-attachments/assets/50d0f43c-4b16-4581-ab0e-7abd62c58bff)

Kiểm tra kết quả:

![image](https://github.com/user-attachments/assets/291ec31c-4b39-448a-800d-b7772f51cf4a)

Cấu hình VTP transparent trên SW2:

![image](https://github.com/user-attachments/assets/6c3498a0-9e7a-46e5-9016-c3d8634a2ed8)

Kiểm tra kết quả:

![image](https://github.com/user-attachments/assets/1c127b45-dbc8-4f53-8d48-53b970e9b8f7)

Cấu hình VTP client trên SW3:

![image](https://github.com/user-attachments/assets/cdf73622-0115-4496-b6e4-4ad3439230c9)

Kiểm tra kết quả:

![image](https://github.com/user-attachments/assets/c3b107e0-7321-4340-a667-95c71410aefd)

Kiểm tra thông tin VLAN đồng bộ từ VTP server:

![image](https://github.com/user-attachments/assets/e9cff99e-8b89-4524-b5aa-8a19f49b28cb)

---

### **Bước 4: Cấu hình VLAN cho sơ đồ**

Trên SW1, tạo các VLAN 10, 20, 30:

![image](https://github.com/user-attachments/assets/bc24ed6b-cb9d-4dc0-982d-b790bce49abb)

Kiểm tra cấu hình VLAN vừa tạo trên SW1:

![image](https://github.com/user-attachments/assets/273c6220-87eb-4c56-bd5f-beace35113fd)

Xác nhận rằng cấu hình VLAN này đã được đồng bộ trên SW3:

![image](https://github.com/user-attachments/assets/ade228e0-2d3d-46a8-b5e9-4f98c5abb74c)

Trên SW2 chỉ tạo các VLAN 10 và 20:

![image](https://github.com/user-attachments/assets/394434fa-41a9-4472-ab38-fabf63385118)

---

### **Bước 5:Gán port cho các VLAN**

Thực hiện gán port theo yêu cầu:

![image](https://github.com/user-attachments/assets/ab008234-31cc-45e1-95ee-32ec706b4690)

Kiểm tra kết quả:

![image](https://github.com/user-attachments/assets/0a8d2550-f62e-4f13-a726-575139a49716)

---
















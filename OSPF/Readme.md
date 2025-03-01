![image](https://github.com/user-attachments/assets/62f6adba-5435-4570-9df0-5ed2a5be57ab)

---

### **Bước 1: Kết nối và Cấu hình cơ bản**

### **Bước 2: Cấu hình OSPF đơn vùng**

Cấu hình:

![image](https://github.com/user-attachments/assets/2aa1ffcf-149a-45a6-ad20-792a6cc98afe)

![image](https://github.com/user-attachments/assets/346ea987-5633-41d0-8ca4-6e1d8a9d2bf1)

![image](https://github.com/user-attachments/assets/94990c76-c4e9-41df-9f1b-ccbbeb8abf40)

Kiểm tra:

Bảng neighbor của các router:

![image](https://github.com/user-attachments/assets/cd3877ca-e50a-47e9-9886-65fc96fe3818)

![image](https://github.com/user-attachments/assets/857ba870-72a9-42a4-9ef7-19ba69a69f01)

![image](https://github.com/user-attachments/assets/046bba1e-ff5c-4e2a-bb92-b6de984a5bde)

Bảng định tuyến của các router:

![image](https://github.com/user-attachments/assets/c63967a6-a5dd-4c83-b99c-45c83bd3a597)

![image](https://github.com/user-attachments/assets/3bf3afbd-2801-4577-bcd9-c45235f3c8c1)

![image](https://github.com/user-attachments/assets/ea49f93a-6edf-48b0-9c9b-f90ce8e37a6c)

---

### **Bước 3:Hiệu chỉnh Router - ID**

Cấu hình:

![image](https://github.com/user-attachments/assets/1b5b1394-f67d-4663-a9d8-285a154020c3)

![image](https://github.com/user-attachments/assets/e1a9f329-db13-4514-bd96-bcfac5b78ba4)

![image](https://github.com/user-attachments/assets/38fa98a3-1e5b-4604-b896-b27c5632a37f)

Kiểm tra:

![image](https://github.com/user-attachments/assets/a5ffe882-3050-4858-9504-817528456472)

![image](https://github.com/user-attachments/assets/12bf7c24-6ea0-47e5-bc1a-c547d826d771)

![image](https://github.com/user-attachments/assets/f26cba1a-b8d5-4a41-9f32-a2796370db0c)

---

### **Bước 4:Hiệu chỉnh bầu chọn DR/BDR**

Trên kết nối multiaccess giữa R1 - R2-R3: R1 là DR, R2 là BDR và R3 là DROther

Kiểm tra:

Cấu hình:

![image](https://github.com/user-attachments/assets/0b096505-0f51-4a40-8315-ced8f141dd40)

![image](https://github.com/user-attachments/assets/c918b30b-b0ed-415b-ab52-ba32f31a8fda)

Do ảnh hưởng của luật non – preempt, để xúc tiến bầu chọn lại cho đúng kết quả yêu cả thực hiện reset tiến trình OSPF lần lượt trên R1, R2 và R3:

![image](https://github.com/user-attachments/assets/21f380a3-5a37-4b26-8231-0bf00a70279d)

![image](https://github.com/user-attachments/assets/570d8842-ba85-4f6f-a6fb-e2863a999684)

![image](https://github.com/user-attachments/assets/0a2d9c95-3d10-4c19-bd52-095b043c9425)

Bảng neighbor trên 3 Router thể hiện kết quả bầu chọn:

![image](https://github.com/user-attachments/assets/00ebaaef-d3ec-4698-9fa8-087e4c64e3d0)

![image](https://github.com/user-attachments/assets/04379855-ad51-4ac2-89b2-9bbf4380c659)

![image](https://github.com/user-attachments/assets/b85c1cfb-9501-4ca3-8e73-92617cd50908)

Trên kết nối multiaccess giữa R1 và R3: Đảm bảo R3 luôn là DR.

Cấu hình:

![image](https://github.com/user-attachments/assets/ebcf435c-6cfc-41fe-9ac9-50f425189145)

Thực hiện reset tiến trình OSPF sau đó hiển thị bảng Neighbor của R1 và R3

Bảng neighbor trên 3 Router thể hiện kết quả bầu chọn:
























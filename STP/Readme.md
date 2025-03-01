![image](https://github.com/user-attachments/assets/51b77e16-34c8-481b-bc8a-3f54735614d8)

---

### **Bước 1:  Kết nối và Cấu hình cơ bản**

---

### **Bước 2: Cấu hình trunk giữa các Switch**

Cấu hình:

Trên các switch:

![image](https://github.com/user-attachments/assets/0aa3573f-3fba-4686-9f42-61cea6ddba25)

![image](https://github.com/user-attachments/assets/77c5d222-8231-459b-b874-9ebb424b1a1e)

![image](https://github.com/user-attachments/assets/7f69cb6c-9388-4502-bc1c-0a3eb0b36f83)

### **Kiểm tra:**

![image](https://github.com/user-attachments/assets/d8809cb7-c8c9-42bc-96cc-6403d1401bf9)

![image](https://github.com/user-attachments/assets/3d3b4af0-2c5c-42d4-81b3-02f20462411d)

![image](https://github.com/user-attachments/assets/6f35fd7d-09cc-4b0e-9815-837d0e8361b1)

---

### **Bước 3:Cấu hình VLAN và VTP**

Cấu hình:

SW1:

![image](https://github.com/user-attachments/assets/9d1695ea-637a-4a49-89c3-010c671d7fd6)

SW2 và SW3:

![image](https://github.com/user-attachments/assets/a30bb44c-5649-4e54-b4f0-8789ed3255cf)

![image](https://github.com/user-attachments/assets/fe4ad32a-d2aa-4bc6-bc51-3084b7e5264c)

Kiểm tra:

Kiểm tra trạng thái hoạt động VTP trên các switch:

![image](https://github.com/user-attachments/assets/a555ad8b-be11-4d6d-9aad-c2163ab54449)

![image](https://github.com/user-attachments/assets/1ba8bc34-4b27-4db4-860d-2194aa9b1905)

![image](https://github.com/user-attachments/assets/06a6b864-a067-4548-975c-56d2d6513574)

Kiểm tra rằng cấu hình VLAN trên SW1 đã được lan truyền sang SW2 và SW3:

![image](https://github.com/user-attachments/assets/95e5eb5b-65bc-4983-88cf-62332ed59fb0)

![image](https://github.com/user-attachments/assets/3cdbf82c-34b1-453d-8296-485f54a72d57)

![image](https://github.com/user-attachments/assets/b2100b38-a268-45fd-bca3-66f49f20f87a)

---

### **Bước 4: Cấu hình root switch và khóa cổng thích hợp**

Cấu hình:

![image](https://github.com/user-attachments/assets/b94f06dd-208d-4a2b-97e0-73e1a512f60e)

![image](https://github.com/user-attachments/assets/043ee212-b219-48d8-a16a-916848c438dd)

![image](https://github.com/user-attachments/assets/2ea1186e-dbd6-4a9c-8990-abe384c82619)

Sau khi hiệu chỉnh cost, cổng e0/1 bị khóa:

![image](https://github.com/user-attachments/assets/11c87b8d-8f83-4a7f-b24b-f02bde6388aa)

---



















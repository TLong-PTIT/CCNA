![image](https://github.com/user-attachments/assets/6da28492-9201-45bd-905b-97bd42cb8716)

---

### **Bước 1: Kết nối và Cấu hình cơ bản**

### **Bước 2: Standard ACL (1)**

Cấu hình:

![image](https://github.com/user-attachments/assets/ebd3571e-01af-4555-ae29-fe4043bae53a)

Kiểm tra:

Thực hiện đối lại địa chỉ IP trên PC0 và PC1 để thực hiện kiểm tra:

![image](https://github.com/user-attachments/assets/6514595c-fb3c-4e24-b629-4184bda5b707)

![image](https://github.com/user-attachments/assets/babe94c5-355e-49a3-a9bf-a708710ba25a)

Khi sử dụng các IP này thì không đi đến được 192.168.20.2

![image](https://github.com/user-attachments/assets/f33e9e41-2470-4629-bdf3-d5095277fddf)

Khi sử cổng g0/1 ping lại từ R1 thì thành công 

![image](https://github.com/user-attachments/assets/6c0a589d-8ed8-40b2-902b-9a597b0fcc9b)

---

### **Bước 3:Standard ACL (2)**

Cấu hình:

![image](https://github.com/user-attachments/assets/8c00299f-92fb-4a0f-9f6a-a84e53c11306)

Kiểm tra:

Khi sử dụng địa chỉ IP lẻ thì có thể telnet được.

![image](https://github.com/user-attachments/assets/047d9aa4-91d1-4bdf-a50e-7106450111d8)

Khi sử dụng địa chỉ IP chẵn thì bị ACL chặn.

![image](https://github.com/user-attachments/assets/235bdd42-76d0-47eb-8eaa-8211458fb5ca)

---

### **Bước 4: ACL mở rộng**

Cấu hình:

![image](https://github.com/user-attachments/assets/4423edcc-cdd6-4061-8ad3-9a4b428b641f)

Kiểm tra:

Thực hiện cấu hình R1 thành HTTP server để kiểm tra:

![image](https://github.com/user-attachments/assets/8285af48-991d-4aa0-9d73-f1ef6fe3edd9)


Việc truy cập bằng HTTP đến mạng 192.168.10.0/24 đã diễn ra thành công.

Từ bên ngoài vẫn đi đến được mạng LAN 192.168.11.0/24:

![image](https://github.com/user-attachments/assets/00504592-6a9e-402c-839d-cccb8433a743)












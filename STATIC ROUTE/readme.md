![image](https://github.com/user-attachments/assets/355ef06a-f7ca-4d5f-8fd4-97895faeffa8)

---

### **Bước 1: Cấu hình địa chỉ IP**

---

### **Bước 2: Cấu hình Static Route**

Cấu hình

R1 chưa có route đi đến các subnet 192.168.2.0/24, 192.168.23.0/24 và 192.168.3.0/24.
Thực hiện cấu hình các static route đi đến các subnet này trên R1:

![image](https://github.com/user-attachments/assets/29b069ca-a2b7-4f23-b075-edb9ce982f2a)

R2 chưa có route đi đến các subnet 192.168.1.0/24 và 192.168.3.0/24. Thực hiện cấu hình
các route đi đến các subnet này trên R2:

![image](https://github.com/user-attachments/assets/9c8363f8-80e4-4331-8f2b-f2683ca93c27)

R3 chưa có route đi đến các subnet 192.168.1.0/24. 192.168.12.0/24 và 192.168.2.0/20.
Thực hiện cấu hình các route đi đến các subnet này trên R2:

![image](https://github.com/user-attachments/assets/913d176b-df13-4870-8b66-77047ce779bb)

Kiểm tra:

Bảng định tuyến của các Router: 

![image](https://github.com/user-attachments/assets/2e965795-6039-45ff-8757-5188e9c3abd0)

![image](https://github.com/user-attachments/assets/4126cc72-78ad-4478-b37b-b119129c356d)

![image](https://github.com/user-attachments/assets/20f42151-2205-4eab-8f85-971a9d1afea5)

Từ mỗi Router đã đi đến được tất cả các subnet không kết nối trực tiếp với mình

![image](https://github.com/user-attachments/assets/8c8bfe35-d328-415e-b364-cd4f85e64d93)

![image](https://github.com/user-attachments/assets/f04f84b6-2f52-4592-8d6f-05f638761455)

![image](https://github.com/user-attachments/assets/65f4db41-0385-4498-83ef-78c97ec30f08)















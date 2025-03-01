![image](https://github.com/user-attachments/assets/b434594d-a0ec-4f60-b98a-655defe9900f)

---

### **Bước 1: Cấu hình địa chỉ IP**
Cấu hình địa chỉ IP cho các thiết bị theo sơ đồ trong bài lab.

Để giả lập việc cấp phát dải IP 200.0.0.0/29 cho mô hình đang xét, sử dụng một static route trên Router ISP:

![image](https://github.com/user-attachments/assets/8fc7e94a-05d5-4c45-a535-698fd651c1c9)

Cấu hình default route từ R2 chỉ về Router ISP:

![image](https://github.com/user-attachments/assets/539b50b2-e7ac-4a9f-8f92-91e096e8bee5)

---

### **Bước 2: Cấu hình Static NAT**

Cấu hình:

![image](https://github.com/user-attachments/assets/74fd05e1-c8e5-472e-940d-86bc7256adcc)

Kiểm tra:

Bảng NAT của R2:

![image](https://github.com/user-attachments/assets/aef95a75-98b6-427a-a407-5392f5066608)

Từ server, có thể đi được Internet:

![image](https://github.com/user-attachments/assets/b466584e-9ccb-4393-aa2e-c7fc11055b96)


Từ Internet, có thể đi đến được server thông qua địa chỉ 200.0.0.1 của:

![image](https://github.com/user-attachments/assets/a8522286-c40f-4690-b33e-8639b9f80911)

---

### **Bước 3: Cấu hình Dynamic NAT**

Cấu hình:

Trên R2:

![image](https://github.com/user-attachments/assets/e18924d1-aebb-4aae-9ceb-eba80f00e190)

Kiểm tra:

Thực hiện ping đi Internet:

![image](https://github.com/user-attachments/assets/f022433a-2fda-4264-9c64-6f3843c5c7a5)

Bảng NAT trên R2:

![image](https://github.com/user-attachments/assets/b58143f7-1f16-4301-8313-7c20212ed46d)

---

### **Bước 4: Cấu hình NAT overload**

Cấu hình:

Trên R2:

![image](https://github.com/user-attachments/assets/5b5f4322-3007-47ed-9ef0-d808f3bf15f9)

Kiểm tra:

Kiểm tra rằng các địa chỉ khác nhau thuộc mạng 192.168.2.0/24 đi được Internet:

![image](https://github.com/user-attachments/assets/c37abb40-969a-463d-bdd7-6ea5069d3937)

Bảng NAT trên R2: 

![image](https://github.com/user-attachments/assets/981de28e-6f18-4eff-9ee7-1bb8621b304c)








   









![image](https://github.com/user-attachments/assets/e4154a22-5877-4f52-bf6b-9606b670bffc)
---
Dưới đây là hướng dẫn từng bước để cấu hình NAT theo bài lab mà bạn đã chia sẻ.

---

### **Bước 1: Cấu hình địa chỉ IP**
Cấu hình địa chỉ IP cho các thiết bị theo sơ đồ trong bài lab.

#### **Cấu hình trên Router R1 (Router nội bộ)**
```bash
R1(config)# interface g0/0
R1(config-if)# ip address 192.168.0.1 255.255.255.0
R1(config-if)# no shutdown

R1(config)# interface g0/1
R1(config-if)# ip address 200.0.0.2 255.255.255.252
R1(config-if)# no shutdown
```

#### **Cấu hình trên Router R2 (Router ISP)**
```bash
R2(config)# interface g0/0
R2(config-if)# ip address 200.0.0.1 255.255.255.252
R2(config-if)# no shutdown

R2(config)# interface g0/1
R2(config-if)# ip address 210.0.0.1 255.255.255.0
R2(config-if)# no shutdown
```

---

### **Bước 2: Cấu hình Static Route**
Router R1 cần có tuyến tĩnh để đi ra ngoài, và Router R2 cần biết đường quay lại mạng nội bộ.

#### **Cấu hình trên Router R1**
```bash
R1(config)# ip route 0.0.0.0 0.0.0.0 200.0.0.1
```

#### **Cấu hình trên Router R2**
```bash
R2(config)# ip route 192.168.0.0 255.255.255.0 200.0.0.2
```

---

### **Bước 3: Cấu hình Static NAT**
Static NAT giúp ánh xạ một địa chỉ IP nội bộ với một địa chỉ IP công khai.

#### **Cấu hình trên Router R1**
```bash
R1(config)# ip nat inside source static 192.168.0.10 200.0.0.4
R1(config)# interface g0/0
R1(config-if)# ip nat inside
R1(config-if)# exit

R1(config)# interface g0/1
R1(config-if)# ip nat outside
R1(config-if)# exit
```

---

### **Bước 4: Cấu hình Dynamic NAT**
Dynamic NAT giúp ánh xạ một dải địa chỉ IP nội bộ với một nhóm địa chỉ IP công khai.

#### **Cấu hình trên Router R1**
```bash
R1(config)# access-list 1 permit 192.168.0.0 0.0.0.255
R1(config)# ip nat pool NAT-POOL 200.0.0.5 200.0.0.10 netmask 255.255.255.248
R1(config)# ip nat inside source list 1 pool NAT-POOL
```

---

### **Bước 5: Cấu hình PAT (NAT Overload)**
PAT cho phép nhiều thiết bị trong mạng nội bộ sử dụng chung một địa chỉ IP công khai.

#### **Cấu hình trên Router R1**
```bash
R1(config)# access-list 1 permit 192.168.0.0 0.0.0.255
R1(config)# ip nat inside source list 1 interface g0/1 overload
```

---

### **Bước 6: Kiểm tra NAT**
Sau khi cấu hình xong, bạn có thể kiểm tra NAT bằng các lệnh sau:

```bash
R1# show ip nat translations
R1# show ip nat statistics
R1# debug ip nat
```

Nếu bạn có bất kỳ vấn đề nào trong quá trình cấu hình, hãy cho mình biết để mình hỗ trợ bạn nhé! 🚀

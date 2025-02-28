![image](https://github.com/user-attachments/assets/355ef06a-f7ca-4d5f-8fd4-97895faeffa8)

Bước 1: Kết nối và cấu hình cơ bản
Bước 2: Cấu hình static route

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
![image](https://github.com/user-attachments/assets/24bb831f-e877-49d1-b8c6-a27081b2adad)

![image](https://github.com/user-attachments/assets/caa2db74-da57-48f6-afee-4a549276b0f3)

![image](https://github.com/user-attachments/assets/892b9361-6b3b-490e-b127-73f9b606197f)

Từ mỗi Router đã đi đến được tất cả các subnet không kết nối trực tiếp với mình

![image](https://github.com/user-attachments/assets/96c56f01-7dfc-42a8-a785-82146d361ae6)

![image](https://github.com/user-attachments/assets/c05b5581-02c5-4b7a-9e0f-3946067065ec)

![image](https://github.com/user-attachments/assets/9c8f92d4-a44b-4c16-9bfe-a737f2571773)

![image](https://github.com/user-attachments/assets/4d79918b-3561-436a-ac0d-d1eea6128ee7)













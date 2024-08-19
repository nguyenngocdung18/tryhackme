Link room: https://tryhackme.com/r/room/mrrobot

# SCANNING
## using nmap
![image](https://github.com/user-attachments/assets/fea65f65-816c-4338-85cd-8df9b2dc6426)

## using ffuf
![image](https://github.com/user-attachments/assets/d0813492-d75e-4016-99ec-31644bc6347e)

# EXPLOIT
## view robots
![image](https://github.com/user-attachments/assets/33f0979a-c41d-408c-8a20-8389cec570ad)

![image](https://github.com/user-attachments/assets/2eb239a1-6350-4634-8917-ca06cc5593d8)

=> key 1

## view wp-login
tôi đã thử 1 vài payload và có vẻ như nó chỉ đang check username trước, tôi đoán vậy. 

![image](https://github.com/user-attachments/assets/b4e2bedb-05d2-46de-a80f-3e6fcea33ecf)

và thử dùng hydra để brute force username với cái list siêu dài mà ta có được sau khi truy cập /fsocity.dic
![image](https://github.com/user-attachments/assets/00a8241f-2010-4a7b-9044-c3125556257f)

=> username: Elliot

Thử dùng account vừa tim được Elliot:123456 nhưng password bị false, có vẻ như web check từng cái 1 riêng lẻ

![image](https://github.com/user-attachments/assets/96b4ee56-4ec8-47ef-8d78-dec7893f5977)

vậy giờ ta cần đi brute force tiếp mật khẩu cho elliot

## using wp-scan
![image](https://github.com/user-attachments/assets/baeb82fb-e25c-4c5c-b9d5-be9550eab22e)

=> Elliot:ER28–0652

![image](https://github.com/user-attachments/assets/27e02f6a-88ac-4b4d-8560-b3d31b75af5b)

=> Nice!!! 

Đi tới Appearance => Editor => 404.php

![image](https://github.com/user-attachments/assets/c442c5d8-a8f1-46d8-91e4-2ae75496cbd3)

Sử dụng php reverse shell 

![image](https://github.com/user-attachments/assets/0e6634ea-5a32-4bb6-8159-5b5eae697a8c)

![image](https://github.com/user-attachments/assets/7eb18103-2f93-4815-bfc7-964a3b3d6b79)

![image](https://github.com/user-attachments/assets/b2284b8c-cd6c-40f5-a64b-ed1e8e7eccf0)

=> Ngon! Ta đã có được reverse shell với id deamon

![image](https://github.com/user-attachments/assets/2c873a7d-c007-480d-bc84-1a0cbbdb8e9d)

=> Không có quyền xem nhưng tìm thấy identify . và giờ chỉ cần crack md5 hash là ổn

![image](https://github.com/user-attachments/assets/d0e22a79-fb5f-4805-b708-f9af2eeeed4e)

=> Đã có quyền của user robot

![image](https://github.com/user-attachments/assets/9cc8ac9b-1639-438a-af39-712a83cffb94)

=> key 2
# PRIVILEGE ESCALATION
## find SUID
![image](https://github.com/user-attachments/assets/4b9e7520-a383-417b-a038-5157ce525626)

=> Go to GTFOBins 

![image](https://github.com/user-attachments/assets/50f8ec3a-01a4-45c8-bcf6-810de75d14a8)

![image](https://github.com/user-attachments/assets/1d23b933-a012-464f-8742-04230693120c)

=> key 3

=> Done!!

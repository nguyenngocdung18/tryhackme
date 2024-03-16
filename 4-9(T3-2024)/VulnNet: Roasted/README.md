Link room: https://tryhackme.com/room/vulnnetroasted
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0ad41c0a-94e5-4e8b-a978-577de1053918)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d248d329-c58c-471d-91f5-80b42495ea73)

# EXPLOITING
## using smbclient
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5de42c39-c378-4c53-9edc-6df9de99ab06)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7ed107be-fb60-4597-8755-e2b910f575d9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/074432bd-3223-4bad-b47a-2ab6b34efda3)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/29de4bc0-eca2-4aed-8360-e0ba143a33f3)

Do the same with VulnNet-Enterprise-Anonymous Disk

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c97ec578-8aeb-4242-8368-3e2a1a6d48d6)

=> I see a lot of names mentioned in the messages. 
## using impacket-lookupsid
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e39f7fce-edb1-429f-bf11-ace915e7c0bd)

I have noted the names with parentheses "SidTypeUser" in the user.txt file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/36b3f678-dda1-46ed-999f-88a2ce193c5e)

## using /usr/share/doc/python3-impacket/examples/GetNPUsers.py
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/11ecf271-371f-4ac5-9fbf-367428e31b56)

=> I get a hash for user t-skid!
## using hashcat
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/20d63f31-3410-4f2b-b0f7-c73d47bfde79)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/de2d62ac-4023-4118-b46f-ae7581676a87)

=> t-skid:tj072889*
## using smbmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/422ace5a-4c00-4a59-9c45-2f4a6ddd8d25)

I use ```more``` command to read file.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c8b1c124-179b-4f4f-9b4a-70db648a1e2c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/14a35610-310d-4415-b311-f30efd5ec024)

=> a-whitehat:bNdKVkjv3RR9ht
## using impacket-secretsdump
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f75ca8a5-fe68-4880-9422-d52332483f32)

=> Administrator:500:aad3b435b51404eeaad3b435b51404ee:c2597747aa5e43022a3a3049a3c3b09d

# PRIVILEGE ESCALATION
## using impacket-wmiexec
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cf7d215b-2399-42a0-9a00-1a17be923f2a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/132a9874-dfd1-48af-a51e-e4cfbbf6125e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e58aabf1-b26c-48da-a1dc-141f0a6d6eb0)

=> user.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5deada2d-4496-4526-a402-6b8b3142bd0b)

=> root.txt
## Done!!!
Thanks for reading. Bye!

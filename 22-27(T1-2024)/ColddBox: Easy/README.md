Link room: https://tryhackme.com/room/colddboxeasy
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1070df2a-5a43-4e42-bf7e-2bc9393adc9d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/786e80ab-6365-4877-83e0-1458ffa6d0ed)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3dc825a8-bf6c-4f21-9405-56cf552961e2)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d4dce1c5-a016-4146-9ab3-16b0e5b4661a)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bd4dfb49-f8be-4a2a-9bc2-b30019b8ad3d)
## view /hidden
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fb70e2e1-32f7-4c5e-ba13-01da66742f57)

# EXPLOITING
## /wp-admin
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1f3dce7d-bc1d-4512-b729-d75c729236fe)

## using wpscan
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/632b3e5d-9aad-4146-90bd-31eeb08ce45e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6cf7d5c2-a8df-402c-8f8f-32bbea629595)

=> I receive username and password

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ff75e0ca-81a6-432b-8744-96ab4a5d37c3)

=> I got php-reverse-shell on pentestmonkey and edited footer.php by replacing it by php-reverse-shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/70d3f384-3a07-43c2-9256-f85aa0bd2b32)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fc3cee5e-5aaa-44cf-aef1-1393703ced20)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fc9a7136-059e-433a-9915-9ad4004e18ab)

=> Nice!! Now I upgrade tty for shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b7cd26f6-2efd-496b-936e-07919da7e86a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3231678d-3108-40d9-a7ed-85b4c533c159)

www-data doesn't have permission to read user.txt file. I walk around and find c0ldd's password in wp-config.php file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fec802c3-5e35-4c70-b96d-db874cb8ac15)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8ff75e3f-c85b-473a-b631-bb519f1888ee)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b7f57e03-d964-45e2-be0b-af9b98f0086a)

=> user.txt
# PRIVILEGE ESCALATION
## Check permission with ``` sudo -l``` command
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/22e44405-f76b-42bb-bfbd-a8405898b820)

=> Go to GTFOBINS website 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/877a7c7d-1e52-4668-9486-aed12f6a2561)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cd693527-2a11-4d2f-b087-c571928551c6)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/07116c93-3d95-4a82-b999-2e4477dd9d0d)

=> root.txt
## Done!!!
Thanks for reading. Bye!

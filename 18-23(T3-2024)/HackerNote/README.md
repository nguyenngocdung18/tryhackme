Link room: https://tryhackme.com/room/hackernote

# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7ac6ad78-49af-46a3-a475-7a997846c75a)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d665b4bd-0d5f-4e00-b9a2-af93e683c58a)

## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/365526c4-8fac-400f-8a19-9c30b330d161)

# EXPLOITING
## find username
### According to the introduction, go to this github page and download the timing attack file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5ce084b8-b0eb-4543-ae69-82fa1fc30707)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f2c94753-2c85-481b-b4d7-4ebe1b6c849f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/84c2503e-9bb3-4885-80ed-d672f0445def)

### Let's remember to change the target ip in the source code 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a9694feb-3bcd-4db3-8d71-d7b8d06eb4da)

=> username: james

## Find password
### Downloading task file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6132314e-3193-4572-90d0-97d5d717b4a1)

### Downloading hashcat-utils

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f6b5402c-8860-4078-adee-44356f9d2de8)

### Creating wordlist.txt file from colors.txt and numbers.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6013445f-03e4-44dc-bd2d-d86e335dfd5e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7c55c046-9837-436f-a799-524c5e201cec)

### using Burp Suite

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e8c46691-99a2-4a2d-a299-6f2ef8eb49f4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/726216ee-2ee1-44c4-8cd4-0fd9b0715dc6)

=> james:blue7
## Logining web

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f5a8f9e6-bad8-4d7e-be94-ce987e4a477d)

=> ssh password for user james
## connecting to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/df7e8d24-bbd0-46cf-8dfe-7151f8629056)

=> user.txt
# PRIVILEGE ESCALATION
## using sudo -l
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8dd3263f-7174-45a0-81bf-f441a58d3a43)

I search on google with keyword "pwdfeedback"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a6351e21-b646-4e70-8c76-4820cda5b812)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d7901588-233f-4a1f-9483-b3e4dd302e51)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7ee39313-a7f9-4be8-9e05-6715e1678d1b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b325f191-b040-4fb4-8916-0b2000d074d8)

I first tried compiling the "exploit.c" file on my local machine and uploading the "exploit" file but the GLIBC_2.34 version on the ssh server didn't match. So I uploaded the "exploit.c" file first and then compiled it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/512f4fe8-db79-48b5-a84e-bca5c70d1c0f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f3cfbce5-3a37-4843-bf0c-1483bbe61719)

=> root.txt
## Done!!!
Thanks for reading. Bye!

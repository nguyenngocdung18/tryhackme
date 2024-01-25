Link room: https://tryhackme.com/room/teamcwT
# SCANNING
## using nmap

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c7eb594b-63ae-4879-accb-b5bca8bb8b80)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/369ac762-d71c-465e-9e20-e3b7c23e8fb7)
## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b023de0d-1ab3-47f4-b8fe-e0492aceb2f4)
## view page source
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0f3dbe66-19d4-4479-9307-815f86555199)

=> " add team.thm to your hosts"
# EXPLOITING
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0a9aaae6-fa4e-4f6d-a297-17d79dfe7807)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c0d43bc5-7398-4ef3-97b2-9b519c997eed)
## using ffuf for team.thm
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bbe2439d-a6ea-4196-959e-88a2550ae92c)

## team.thm/robots.txt
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/29debb7e-9825-4b6b-bba8-ab473da44b6b)
## team.thm/scripts
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/73c11060-1818-4652-812e-272759d69447)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8a26a411-538d-4762-ab64-61ef4267c4d0)

I see the script has no extension. So it might be a folder but I don't have permission to see more. So I used ffuf to find hidden files in there but there was nothing.hmm... Maybe I have to search by extension. But I don't know exactly what extension the hidden file has. That's why I'll probably use gobuster to try again.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/042d3ac0-cd8f-4db5-99b8-f4790c0c7250)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b4fa87fe-92e4-4621-9de4-cf4c9c45385e)

=> I pay attention to the note: "# Note to self had to change the extension of the old "script" in this folder, as it has creds in". When I access /script.old, a file is downloaded

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9a2241b6-124f-4bf7-bc73-d7303511c18f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/838774f2-4331-49ff-b81a-e6e64c97c06e)

Actually, when the scan found port 21 open, I tried accessing it anonymously but it didn't work. Now I will use the username and password I just got to connect to the ftp server.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e4ddc608-d71e-433b-9c61-91711fa5297c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/63083762-791b-42fd-8d3c-9d9b7491e600)

I tried team.thm.dev, team.dev.thm .And result is dev.team.thm. I add "dev.team.thm" to /etc/hosts

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/31a3a24c-1056-43a7-b2ed-7f8d0003f534)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eec1e89b-f5ff-4423-a875-2a0399f7c45d)

I tried to find /etc/passwd using Burp Suite but got nothing from /etc/passwd

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/22ed952f-1803-4b2e-b52a-ab5d00b5a2d1)

Actually, it's not really nothing. I see ```sshd:x:111:65534::/run/sshd:/usr/sbin/nologin```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/872be94a-c36f-476c-9405-aed221220c99)

Because My kali machine doesn't have  "/usr/share/wordlists/SecLists/Fuzzing/LFI/LFI-gracefulsecurity-linux.txt"
, so I download it on github. Now, I can use cmd or burpsuite to find hidden files.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c9e04f87-ec9c-4bce-a9ab-734be9f2e134)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/16c89163-4177-42e4-a4fe-f21741f56651)

or with Burp Suite 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bb1d5539-e258-469a-815e-36960831383c)

In /etc/ssh/sshd_config, I find private key

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/63a42a61-0099-4d66-b95e-4e8f5e95c77a)

=> I find ssh key for user dale. I copy it and don't forget to remove the hashtags and give the file permissions

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e88f534b-a16f-4bb4-a6c9-b4af1a66b11d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bddfcef6-afcc-485e-9180-bee15ea849bc)

=> user.txt
# PRIVILEGE ESCALATION
## ```sudo -l```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2cc9cec9-2434-442e-a778-6c1db6b274c2)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/059bdde2-96da-4b7e-b7f8-781f0c96d76b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8d1f379b-a062-4139-bab5-5e200c4a3606)

I use ```less .bash_history``` to read 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fb928d1a-874e-4233-825c-d46466b99708)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/61b1f634-7a29-49b3-b5eb-dd0c61d038da)

hmm... it seems everything is related to /opt/admin_stuff/

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/91e6701f-b1f7-4c1c-967a-80efdc66a5cc)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2828fd40-d7d6-4c47-a586-392ccac48dc5)

Go to pentest monkey

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/259435e1-07bc-4842-bc2a-8c501e6b5e58)

I fix main_backup.sh file with ```nano```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cbd15bfc-1353-40b1-a824-5e713f51ba57)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f3b7d811-9f68-439b-bb8b-25ab0fc56132)

## Done!!!
Thanks for reading.Bye!


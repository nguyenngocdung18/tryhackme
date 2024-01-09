Link room: https://tryhackme.com/room/tomghost
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b20728e4-0e51-446c-ada9-1ff36de5f6b1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e2e1eb01-7929-4237-bae1-4072cd3ef101)

=> There is no port 80 as usual but instead port 8080 also runs http
## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c26b09db-ba3b-4393-a2e3-3c40723022ec)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b2a6a596-5cfa-4363-84a1-3af610c60383)

=> When I run ffuf , I don't see any hidden files.
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c14c4bf8-4afc-48cd-9785-fa96619173a9)

# EXPLOITING
- While scanning, I noticed that port 8009 was running the ajp13 service
## using searchsploit
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6ee34fd3-e6c7-49c3-899d-5fa8f09f6f16)

I search on the web and find https://raw.githubusercontent.com/Digitemis/Ghostcat/master/exploit.py for python3

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f455677b-ed09-413a-948a-080b280428bf)

=> I get skyfuck's password to connect ssh server

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b2057216-c316-4640-b6da-bd7e5dba1a1e)

After that, I get the user flag

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/86c3e5b6-6f5a-4cb4-af5b-c56c46e610d3)

# PRIVILEGE ESCALATION
I use command ```sudo -l``` but skyfuck may not run sudo on ubuntu

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/21463497-75df-4882-b9aa-98b23223b3cb)

Walking around, I find two files.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/44b61139-1413-44e7-9595-a0357162d074)

Use scp to bring them to the local machine

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eb14a0d8-7898-48a1-a43f-afe30a6a5373)

Looking at the pgp extension of the credential file, it appears to be PGP encryption. So, I might try using GPG to decode it
## using gpg2john
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ba0a6312-7090-4258-acd5-a83dc20ddf88)

Then, I use john to crack the hash and get a password

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/95543f03-b200-4bca-88b6-01771f074629)

The ```gpg --import tryhackme.asc``` command is used to import the public key from the "tryhackme.asc" file into your GPG system.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/490ba4dc-b434-4fb3-abfd-92d7e75af40a)

=> Now, I just need to use ``` gpg -d credential.pgp``` to decrypt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f01c83d1-0728-4e9a-92f5-fc1257bbf806)

=> As a result I get merlin'password. I switch to merlin account and now I can use sudo
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ef8b297a-b938-4253-bebf-1699a00809c1)

Go to gtfobins website
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a7240bf9-705c-4c0c-89fb-ea6071c745bd)

Do this and get root privileges

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e0b39f39-45b8-4aa5-83fb-06b3a7ec3879)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/32b35a0a-555a-4f9a-86df-71865a779610)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/759789b0-5edb-464e-a2cf-7e2d36f1b787)

## Done!!!
Thanks for reading.Bye!

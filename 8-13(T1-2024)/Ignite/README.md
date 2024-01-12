Link room: https://tryhackme.com/room/ignite
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a5fd4785-2270-43bf-9158-8e9a1d98db96)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/61de467c-9d7d-4312-b60e-94e4d631b7a0)
## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/267174ab-9178-4039-a5f5-05b70d17b5a4)
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f6fa8357-d495-4f0f-96fb-2614d7a3fd4d)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d796f6d9-725b-4cff-afef-3538deb0da89)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b6e6e0e6-1410-429c-bc18-46632d5e6fc9)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/de6b87db-3590-45c4-9808-284638426382)
- /assets/

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a979681e-c9d3-4644-b83d-53842a4d8102)

# EXPLOITING
## using searchsploit
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8f855a0b-a726-4990-afe1-7be6be1bd497)

=> Remote Code Execution. I download and run it with python3

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/20370687-2677-48eb-96d4-e23b8cbd2d41)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/010e2518-55ee-4de6-9276-4209a6d9a5ea)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/87d69e45-9dd4-4eee-956f-2b4a2da2c9b9)

=> Nice! Now, I walk around and look for more information.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1735dc1d-0e9c-42a9-b8b1-0859c5ebea35)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d7596b21-682c-4661-a5b2-60de132325b9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d7ab563c-e0fb-4139-afba-73625c2c9535)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/29b9ada2-638b-43a2-a73c-478863eba1e9)

=> So lucky, I accidentally found the database.php file and got root's user and password. Haha.. 

The remaining thing is to find the user flag

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/82d72b15-fbc6-408c-b5f8-1bf1c80e115a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/71177c6d-c53f-49d8-a8d0-392914bb4f5f)

Good!
# PRIVILEGE ESCALATION
I will launch an HTTP server at port 80 on my computer, using Python 3

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2a1d13aa-f146-4b21-a739-487c53a6deef)

Then, I use wget to upload the php-reverse-shell.php5 file to the web, or in other words, download the file from my computer to this server

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c53a489d-7fad-44f7-bbcd-838ce846b4e9)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/60fe3968-d9ed-4608-b366-65e6165f0f64)

Okay, now I just need to use ```nc``` to connect to this server.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7012728d-1356-4856-a242-713dfedc3ce1)

Because I already have root's account and password from before. Now I can easily log in as root and get the root flag

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c498c55e-ef88-429e-a84f-aaf8ee6bd011)

## Done!!!
Thanks for reading.Bye!

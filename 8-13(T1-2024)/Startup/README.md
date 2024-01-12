Link room: https://tryhackme.com/room/startup
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a6257203-b1a3-4d49-8757-766c4afda9d5)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/058670ec-a0f0-4fae-a420-fc0158f47cab)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/292c76cc-2eb5-40b5-af49-22f4c3babeb7)

=> /files
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/372291d6-4e54-4baf-8ee2-7b8f7dfe92f1)

# EXPLOITING
IP = 10.10.99.17
## view http://10.10.99.17/files
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/33e70166-0dac-40c7-8baa-8477e3c3eff2)

view notice.txt
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/44a3522a-e5ba-465c-ba4e-243c4fbd521b)

I connect to ftp server with anonymous

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a4d4b812-4abc-488e-9962-77e956f421d8)

I go to the ftp directory and uploaded the reverse shell file using the ```put``` command

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f2e1cfe0-ee1a-4d96-80a5-a0a08cc9b102)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/465f031e-68c1-45d8-a3a0-e6398bfa77e7)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/31926f6e-ac9c-40ba-b991-1c6659ad13f4)

I execute it and use ```nc```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0185d17c-63f3-4039-91e4-becba2d929b1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2c837806-68be-4362-ad29-70e572c61749)

=> I get answer for question1: love

Then 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7b729e26-3c11-46a0-9a75-a5cd3bdde391)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f3b21947-767e-44f7-9b9f-bae1300f2bce)

=))) It's interesting that there is a file named suspicious. Furthermore, I see a file with the .pcapng extension. It immediately reminded me of Wireshark.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/22fdc005-9998-4b55-bbb8-dfb1f48bc028)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f5948ed2-a75c-4f5b-87eb-46aeef84917b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7030bf43-6117-4e6b-a13b-2ebd8b18f7a9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/79d0c4b7-cd67-4c31-98a1-0425fa535b2c)

=> I find a password. it may be from another user
And I try using that password to connect to the ssh server with the user lennie

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0d049d04-b8fd-4f14-b614-889c992ad2d7)

=))) Lucky!! I get user.txt
# PRIVILEGE ESCALATION
I try using ```sudo -l``` but user lennie doesn't have permissson.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3396ea14-00ed-470d-968d-b06433f752c0)

Searching further I find the 'scripts' folder and  planner.sh file.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b55f2dc8-921c-463a-baed-0294d5ae1e2a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ed723958-4488-44ec-add9-0aa0d7bbdd5b)

Hmmm.... Looks like we can execute scrips in /etc/print.sh file with user lennie. So I think I can get the reverse shell with it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/899e7792-3a5f-4678-a2b9-6ec42f941479)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b4df3963-a091-43e2-a6b8-f98e7b4caba5)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/37d4e797-236a-457e-9c26-aee7ef4eaad5)

=))) Nice!!
## Done!!!
Thanks for reading.Bye!

# SCANNING
## nmap

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/08a5186e-9b8b-43b5-a0b4-0d5e3b64f747)
## gobuster
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/393401f9-3a0c-435b-987c-f5a2fcd39441)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fe35d6f1-438c-4835-a861-1e89221709ce)

# EXPLOITING
## searchsploit
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/df62822d-bc1b-4592-ae9c-202a4545ce47)

=> see SweetRice 1.5.1 - Arbitrary File Upload (php/webapps/40716.py) => error upload file

   and SweetRice 1.5.1 - Backup Disclosure     (php/webapps/40718.py) => You can access to all mysql backup and download them from this directory.
                                                                         (/inc/mysql_backup)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d5d714bd-73a3-474e-8ead-453c384a1549)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8176b5b2-0464-4f3c-9129-d2fc6f5bd824)

admin:manager
passwd:42f749ade7f9e195bf475f37a44cafcb => Password123

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f394dd58-7754-4de6-bae5-29c061269551)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9858146b-2b5f-4f6e-8bf7-5c1f6b44083f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/05bbeda5-a1ba-4ce0-8a26-9fbf0608d602)
=> Logged in successfully
## upload file
Then, go to Media Center and upload php_reverse_shell.php5

Run it and do nc to connect

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b09b2855-e8f8-4117-bd79-512f0de5859b)

=> I got the user.txt file
# PRIVILEGE ESCALATION
## First,
I tried sudo -l 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d10f1e2f-64c1-4ab8-b63e-55dcc506b70a)

see /usr/bin/perl /home/itguy/backup.pl
## Then,
Read file backup.pl


Edit the copy.sh file.  I will create a copy of bash and setuid for it 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c8a037c6-5c41-477e-a0ed-04b18f3a8632)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f616d93c-b4e3-458e-b2a3-74952f8219f6)
## Done
Actually , I can also edit copy.sh file to reverse shell using nc 

and ...

Thanks for reading. Bye!

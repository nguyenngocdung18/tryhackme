Link room: https://tryhackme.com/room/plottedtms
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/252a1b0a-a7d5-4ca9-b5db-28c9934925be)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b6f849bd-bc02-4e34-9b2c-41474b2e2d03)
## using ffuf with port 80
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7e66a40b-69a8-4e8a-9c6d-dce99f7a8108)
## view /admin
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/34b5b91f-308b-49e7-99b8-2c0f934985f9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b2bfd974-4e24-47af-8146-06d0456278d7)

=))))))))) 
## view /passwd
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/099cc237-8e3a-4a07-a49f-0c3ea87f6e73)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1706c8bb-79dc-4c7c-ac96-9a3f336929d4)

=(((
## using ffuf with port 445
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9cfe21cc-9f5b-4bfc-9e17-a765a10026e5)

## view /management
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4addf013-8085-4021-9334-93b2b5272f69)

I click on login button.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/99d77035-d280-4640-a998-5ef43f149a80)

# EXPLOITING
## using Burp Suite
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c640a87b-ded8-4eba-8713-b34da0e2647e)

=> I see a sql command ``` SELECT * from users where username = 'admin' and password = md5('admin') "}``` 
=> Maybe sqli

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cdb970c1-0668-49ab-8040-3b19008552e8)

That's great!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d8b38d1a-e670-4a1d-a209-af904d4c3632)

=>Logged in successfully
## upload file
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d509807d-7771-4c13-868c-7283fd3b1db5)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/da09dada-0572-4663-9d3c-9a0664803a36)

=> I get a shell with id www-data

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7ff3bec2-cead-491b-8028-97facdda02b9)

=> I don't have permission to read user.txt file :<
## look at /etc/crontab
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5e9755cf-c010-42ed-937a-d6cdfa789158)

=> backup.sh file may be exploited

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1c86c6df-408d-4eb0-9e1d-c3c3ad423aa6)

First, I remove backup.sh file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c7e3148b-3a4e-4d4c-b412-6819f27a3d79)

Then, I upload new backup.sh file 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ab6184bb-3eb3-4215-a9fa-fe4fccad2ea6)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e64dbd82-85ff-4024-aa2f-216187925bc3)

Finally, I run command ```date```.because if I run ./backup.sh the reverse shell I get is still user www-data. and I see the backup.sh file is added to the crontab to run periodically, the ```date``` command can be used to create a time clock to determine when it should execute the cron job. During cron job execution, I can get reverse shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/08158e11-1d10-4e19-bdd8-2e178ba1fd54)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b58af1e8-d9da-44c6-8a27-125052bfd299)

=> user.txt
# PRIVILEGE ESCALATION
## check with sudo -l
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a8a12e5d-63e7-4bf2-93cc-1c5bbbe3e8e5)

=> I can't check with command ```sudo-l```
## check Setuid/ Setgid permission
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aced6b94-f5d8-4493-b58a-9c6b8c30c27d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b6539468-3f6b-479c-80ad-3d35f96dbb06)

=> /usr/bin/doas
## search on google

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3e5255d2-ae9c-4f9f-8e40-6e9a99f7de87)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bf55fb16-23eb-4e7d-9cfd-04cf2ecac71e)

## Do
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/22372f6b-501e-474f-ab36-376acadac0ab)

I go to gtfobins website to get command

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bbde9474-f2a1-486b-85d8-6ad4812b57f0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3216416e-d00e-4861-bce1-8dcf8e5b425c)

=> root.txt
## Done!!!
Thanks for reading. Bye!

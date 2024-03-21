Link room: https://tryhackme.com/room/anonymous
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/068f5bfc-7781-4517-a858-0b529ea8f65d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1c5153ec-d11e-4794-8d5a-5fe22271ac03)

## using smbclient
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e81023d6-7eb3-4cf4-9904-b4071f2184bf)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/253c42f4-77bc-4c43-8d25-db9be93e8d0f)

# EXPLOITING
## connect to ftp server
Reading to_do.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cf408579-8af1-4e2e-9d9f-fca0fe94be5c)

Reading removed_files.log

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/80270ea5-417f-4ee9-8ebf-518989e755df)

Reading clean.sh
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/01b0520f-ef7b-4260-9ac8-ed7000ec0f66)

Creating clean.sh at local machine

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7dfbe72a-81be-4b2e-817a-bfb806f61095)

## upload file
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fa7bf224-9bf6-47e7-8898-ec63f72ccc56)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7aecb2ff-e276-47c1-8c23-e865fe1cc24a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c6c09900-8e85-4e41-9dfd-c689291afa8c)

=> user.txt
# PRIVILEGE ESCALATION
## using sudo -l to check permission
but it doesn't work!!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6c293332-62c3-44fb-b69b-a83d4f8c81dd)

I also try reading /etc/crontab but I don't get anything useful
## find Setuid and Setgid files

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5962d619-d1c6-46a8-8c22-06b47ec18f7c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/dbbd1361-80fd-45d0-9309-e8d8f734ee43)

=> /usr/bin/env

Going to GTFOBins website

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9fb48627-5e1d-4bc5-876e-1eb96db99385)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/72ad5dd9-35cb-4e33-8e57-312d97f88df9)

=> root.txt
## Done!!!
Thanks for reading. Bye!

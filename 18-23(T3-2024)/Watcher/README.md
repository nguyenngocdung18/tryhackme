Link room: https://tryhackme.com/room/watcher
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5b82f0ff-62ff-403a-9f13-1a7014f12713)

## using ffuf
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/45564dd6-0c4a-4aa6-9045-d83c7106f070)


# EXPLOITING
## Flag 1 : robots.txt
Read robots.txt file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/20ea546a-5f1f-4d4e-a891-91d620043c9f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fc18f5aa-5766-4013-b9f2-008b71a87dbb)

=> flag 1

## Flag 2 : Local File Inclusion (LFI)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5adb1514-1564-48ac-ab67-8db91539835e)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/06ceecec-d65e-4477-a9b6-d59cdb8899b2)

=> ftpuser:givemefiles777
### connect to ftp server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/616a148f-3923-41cd-b95f-bbeb332ecc9b)

=> flag 2
## Flag 3 : Remote Code Execution (RCE)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/05e5ef54-5aa9-4a7d-b7d7-d2d8b7e64e59)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8a61ade9-0a1b-4696-b9cb-b8950c27c549)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4f7efc08-85a0-4fb6-ace6-a7351c8611e9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2e3142c9-a3f5-4019-867f-bce6043c4987)

=> flag 3
## Flag 4 : sudo -l
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/28c7a79f-7bde-4ae3-a5a2-55f8812d356f)

=> flag 4
## Flag 5 : /etc/crontab
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/15bbd075-926c-4147-a222-d981acc49f4b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/02edd440-8da5-4548-a233-c95bac89eaea)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/45d35b27-43ae-40ac-9574-638f729ed534)

Wait a minute!! 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4e2d1108-6df8-45d9-ba51-c1abdee17250)

=> Mat's shell and flag 5
## Flag 6 : Python Library Hijacking
I see note.txt 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c3575f36-2493-4347-acd7-72f960617c41)

I read python files 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/47cf5c07-0617-4491-9f66-acf99dab9cac)
 
Using ```sudo -nl```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3718045d-ccbc-4120-adb1-83eebfed40ba)

I edit cmd.py file to get reverse shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/02c628f5-531f-4475-88a4-89c5c5df6351)

Then, I use  ```sudo -u will /usr/bin/python3 /home/mat/scripts/will_script.py 1``` and ```nc``` commands

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/637c34b4-cebf-4974-852c-7fafa567ca33)

=> flag 6

# PRIVILEGE ESCALATION
## Flag 7 : SSH connection

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ffd0d9f8-30d1-474f-b310-7ac38fbc0dd7)

I receive a hash. So I use CyberChef website to crack it.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3dffdfab-1978-478f-a9a5-e07b2bd1f129)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ba48f56a-857f-4350-8fea-f7ec9366a637)

=> "RSA PRIVATE KEY"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bfe35500-11af-408a-ae5b-1c5dcdf606a2)

### connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6000e1bd-7999-433b-8462-bd3a92df8574)

=> flag 7 

## Done!!!
Thanks for reading. Bye!

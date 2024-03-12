Link room: https://tryhackme.com/room/flatline
# ENUMERATING
## ping
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2e3fd957-60dc-445b-b50b-f5a7593502e6)

=> Can't ping
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4087f267-7b3e-46da-8251-701b655b204d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7158c07b-a994-4575-8920-5a11b187e7b2)

# EXPLOITING
## using searchsploit
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a7f1fd16-6ee6-4d28-a267-89b4cf78ad9d)

I use ```wget``` command to download 47799.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/72a26da4-d7b2-4d2e-bb61-c18fc454c554)

or I can download it another way

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/92e0cef6-e516-4759-9154-aa04805b0528)

I read file 47799.txt and saw python3 code

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8ae147d3-20f9-444b-9e2f-a067beb93f5a)

I saved it at freeswitch.py

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c975fbed-1d3d-4e69-8a27-557a356a1f65)

## remote code execulation (RCE)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e76d998d-a0f0-4d0a-addc-9c82c958f1eb)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aeeb0e89-be00-4f5e-9539-db7566af9fcc)

I see the path "C:\Program Files\FreeSWITCH" and since it uses the windows operating system, I will try going to the Users folder

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f713756c-c964-4553-bdb8-3f4a6fc3219e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f9d69539-69ec-4198-ba05-dc4c174030e9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c4015af4-7e93-445b-9c2a-228545d6d695)

=> I find the file user.txt and root.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ab838aeb-29d8-4044-aa87-935f3f6bdf24)

=> user.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e7e1442c-031a-43ef-aaca-27e0258877a4)

=)))) Haha... Of course. Reading the root.txt file cannot be easy
# PRIVILEGE ESCALATION
## using msfvenom
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/43e776db-8f69-4310-ab2f-0df986df69f7)

=> I get payload.exe file
## upload file
I upload payload.exe file 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eae79ca0-5a83-4152-9d62-ed7408082725)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/474b828a-ba6f-4158-b497-2acd39895c07)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/77ff5441-0910-42cf-b020-4ce8e0266548)

## using msfconsole
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/11357f18-b2b1-4e07-914f-b2a1397aec57)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/56a978dd-8098-48a6-bb6d-75a53e5dd781)

At the same time, I executed the command ```python3 freeswitch.py 10.10.244.113 'C:\Users\Nekrotic\Desktop\payload.exe'```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fd125097-3659-4fba-9312-a54026fa8d41)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/da2ac387-061c-4b43-8de7-7951d3455cb2)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e7d8a3c9-7d57-4493-a859-0850bfc0946b)

=> root.txt
## Done!!!
Thanks for reading. Bye!



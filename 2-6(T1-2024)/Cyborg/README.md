Link room: https://tryhackme.com/room/cyborgt8
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0d6d38d5-055b-45d3-8f0a-0dc8541f359f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e36a646e-2e3d-450a-84a0-d2c0ffb8114f)

## using gobuster
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b6339c97-d06a-44d5-a504-55b19e5cbe5e)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/481550a8-5314-46f3-a39a-d26fe3cf61db)

## view web 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/77d34fca-f7fa-44ef-84c2-4ba59b3ca746)

ahha.. there is a hash here.
# EXPLOITING
## using hash-identifier
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fa601347-56c4-4905-92a3-bd6410e22f3a)

=> hash type: MD5(APR)
## using hashcat

Before I use "hashcat --help | grep APR" to find 1600 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2435504e-f9b2-488c-a03c-6c0026b1c8fe)

run hashcat and i have a password. I don't know what this password is used for. Leave it there for now

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2652d519-d355-4687-9890-c61d30bc0c9a)

in /admin i download file .tar 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/50f15982-81ae-4561-b7d8-2aa912a16c3a)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/215e48c2-b1ba-4611-8b48-4a6ede5e5bed)

Read README.md 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/37d2ebbf-1ab6-4fa0-81a3-c8ceb50944f2)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1ea6a1b1-3a76-4ab9-9151-ac8c435a491a)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/02cc119d-070f-482b-bef1-644e0ff632fd)

After extraction, I find alex's password to connect ssh server

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cdbf5feb-4f44-4d0c-b55a-a8a89a07c102)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e96f4bd0-56ff-45ab-9943-94d54ed7259a)

The only thing left to do is find the user.txt file
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ffdea3a9-a6ba-4635-8050-2724ac0e951f)

# PRIVILEGE ESCALATION

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e8cebdea-6316-4d2b-b492-cf0afa4e5c6d)

=> So I can do many things from executing backup.sh like creating a root user in passwd for example but I will choose the simpler way which is reverse shell

Let's go to pentestmonkey Reverse Shell Cheat Sheet

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aba17155-466f-4bc9-a58d-305862b389ba)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eed26b2e-6a39-40a3-a797-add2e57418b2)

hmm... permission denied.I'll try to check the permissions of this file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1bc9054d-ec97-4863-830f-d68725bc8602)

That's right! I know. I just use chmod.
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c2e71a67-0e08-4169-9967-6ef9dd9812f4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bc4c508e-bbef-4626-b66d-2c134871024c)

## using nc
Finally, I use netcat and finish the lab

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/be32f7ff-38aa-44c5-9a85-ab2cc253846a)

## Done!!!
Thanks for reading.Bye!

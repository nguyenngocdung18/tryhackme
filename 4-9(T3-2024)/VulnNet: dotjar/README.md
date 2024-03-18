Link room: https://tryhackme.com/room/vulnnetdotjar
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4c1a8b1a-e0a9-4082-bd61-33cf1694028e)

# EXPLOITING
## using searchsploit
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1cea86bb-27e8-4a84-b6fd-9b7d9c886cb9)

I search on the web and find https://raw.githubusercontent.com/Digitemis/Ghostcat/master/exploit.py for python3

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f4cffccd-ab44-4e1c-afbe-38d779ffde3b)

=> webdev:Hgj3LA$02D$Fa@21

if necessary, Let's use chmod 600 to give permissions to the exploit.py file
## login web

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/32d8982e-c353-4bfc-8dc4-6af6e9f9f336)

## using msfvenom
I search on google msfvenom payload for java

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cb6422a1-2917-40f3-b7ef-2b4f388cf9e7)

I use ```msfvenom``` command to create shell.war

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9423329e-5ed1-47d7-acfb-02e4bc14805c)
## upload file
I search on google with keyword "tomcat upload file with curl"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1f2df732-e870-418e-aea7-256f8218310c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4d48a833-cf8e-44b4-8afb-3d1b3cdbc856)

=)))) Nice!!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4f40c218-a0e3-4450-8b5f-0c401ec2379c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4da7e91d-32fb-4f9c-913b-76867d055864)

Walking around and I found a rather suspicious folder called backups

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2b21771d-4029-4e08-8a52-058cb7587894)

I copied the .gz file to /tmp and extracted it using the ```gunzip``` command

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aba7a986-3067-4378-877a-4a6e82874987)

I read it and find a hash for users jdk-admin and root

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/88ab3c69-442b-46dd-8624-c8c5cc5a82cc)

But unfortunately I only cracked the password for the jdk-admin user

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3b538db4-cab6-4739-a437-6900bef50393)

=> jdk-admin:794613852

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f1ebd1bd-5267-443b-a0bd-e60b0d169b46)

=> user.txt
# PRIVILEGE ESCALATION
## using ```sudo -l``` to check permissions
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c6aff74a-3d91-4a34-8f18-b0df80231196)

I search on google with keyword "sudo privileges using java"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/60e2ca3b-cd5b-415f-8a4b-f2f915dd9625)

## using msfvenom
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/38811a26-72b0-4da5-bd3c-166de3e20980)
## uplaod file
I tried uploading with curl but it didn't work so I used another method

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/847ba3ce-f9db-4b8a-b05c-3719aca36484)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/06abfd04-2946-4b94-9284-75d583bbd5e9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4424febd-ca74-4f75-a192-e3ce5022b81e)

=> Uploaded successfully!!!!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0e80c735-7b0f-4714-b45e-adc602372dcd)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/667ea035-3965-4735-af20-a9d6dc45ded1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d44ccf2d-c5a0-437a-8cd3-9478075b4b07)

=> root.txt 
## Done!!!

Thanks for reading. Bye!

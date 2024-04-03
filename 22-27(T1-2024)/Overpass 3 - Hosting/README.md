Link room: https://tryhackme.com/room/overpass3hosting
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8731a98f-3f4c-43a0-8a1e-7c2f7c563d0e)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/48881ba9-1289-453c-880f-46eef9b15aa7)

## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d45f12b5-5b58-46b3-a8a1-1a48113d4ce8)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cc52a7e2-4f82-4f67-8f85-c7fbe6555065)

I download backup.zip file and extract it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6c36815c-4e09-4ba3-b6f5-32a47f3bd420)

Cracking pgp encryption

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ae3d11c7-127a-4d78-bcaf-f9b5145f4b8f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8df5b0de-1c39-4cae-aa5c-65e1b747fefa)

=> paradox : ShibesAreGreat123
# EXPLOITING
## Connect to ftp server

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/922ea2a4-cb43-4b64-b799-e247ecc332a9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/203cebd8-f2a2-476f-971a-81c4c5a9f154)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/26b70913-2235-4371-b100-700abc7a6877)

=> user "paradox" is OK. So I upload file "hello.php" to get reverse shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/dd2fc78a-e91d-4e50-b6d7-a2e81eaf0e52)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/77400c20-fcca-4e5c-9c83-d853ad28a28d)

=> Nice!! I get a reverse shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2afac421-b243-4400-8559-c4ea40dd7893)

=> webflag

## I add my public key to authorized_keys file.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/28cb0344-297a-45d8-93ad-d66ad97cc4e9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3b03e623-d5df-4b26-8ca7-d45299125642)

if you don't already have a public and private key pair to use for SSH authentication, uou can use "ssh-keygen -t rsa" command to create them.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d12db30e-be92-401a-8400-103da0dfe404)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c8b6b05f-5d04-4431-814a-98a488bf54fc)

## connect to ssh server

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/79390ada-5ecf-447f-bfa5-b55acf243ce5)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aae97d73-210b-477c-a8f0-bf88545dcc3d)

=((( Not lucky! So I upload linpeas.sh to analysis and Collect system information

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9d76528c-5349-4f3e-9d7e-b527744faa38)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/88e609f6-48b7-4187-a2e7-dcaba37cbc41)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bebc2dfd-5ec4-46f5-84cf-3e66862b0b7f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/dc563a4b-55df-4e53-9373-f761954aa81d)

Read file.txt 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/90b6af7a-d93f-4049-9524-8b3ede02d093)

=> the "no_root_squash" option is used, it allows the root user from the client to access files without being limited by the normal security policy.

Check port

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/60d8fc1e-9e70-46c0-a0c8-1ca3f5cfd3e9)

=> port 2049 : nfs

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7e2e78c1-3eab-4621-bcbc-e03f02f18194)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5f590b82-2a83-4f19-bae0-13aa8c1191d9)

In my local machine , port 2049 is closed
## Using ```sshpass```
To establish an SSH connection from your machine to the remote machine with the paradox of username and IP address 10.10.11.11. At the same time, this command also sets up port forwarding from port 2049 on your computer to port 2049 on the remote machine via an SSH connection.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b3768657-5d3b-47ce-9757-1f83ca76de18)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8b8bdfe3-1a02-49a2-be68-99fda8f27013)

Now, port 2049 is open

## using ```mount```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2a586f6d-ee01-42ad-96d1-2905a2fffaf0)

=> user.flag
# PRIVILEGE ESCALATION
## connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/92c42409-6b32-4eb8-9f0f-5b38401a068f)

Copy /bin/bash to /home/james

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cdc5f480-b45c-4e6d-bb8b-b64a87d3ed34)

Going to my local machine, I change the owner and group of the "bash" file to root and set the setuid or setgid bit for that file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6e694a6a-cf71-4deb-8a87-6f20a507e8cc)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a68dc6ac-2932-43ed-94ab-353d36755905)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c385cb6e-b1c4-4273-bf0b-58bf5db39d55)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e67646ee-da9d-4586-ac0e-c90e2d94c748)

=> root.flag
## Done!!!
Thanks for reading. Bye!

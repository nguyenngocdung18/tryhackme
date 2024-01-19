Link room: https://tryhackme.com/room/lianyu
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/210816b7-68fa-42d0-88da-370aa79dcb25)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6af816a2-8f29-4e9d-86c5-0c70458c7753)

## using gobuster
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/55308f0c-9372-44ca-835f-ea698fb77859)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c87a97c5-a90e-4a3e-a167-5ed5f75d0a1b)

## view /island
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9f37d3fc-f687-49f6-9302-3a0942da5ad7)

view page source

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/367b0ca6-1407-42c7-8e8f-c5fb5c45e92b)

=> code word: vigilante
## view /island/2100
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2c18d82f-f5d1-42d8-8ecc-9885064949aa)

=> extension: .ticket

continue using gobuster

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/02a1dff9-6b78-4d1d-a96c-54b9f2b55764)
## view/island/2100/green_arrow.ticket
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6a7d588b-ba90-4ccb-9705-7729829e27d9)

# EXPOLITING
## cyberchef
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ef01c794-760a-4e0e-91aa-6b7c298a6795)

=> !#th3h00d
## connect to ftp server
with user: vigilante
<br>      password: !#th3h00d

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7b7c1d08-906b-4315-8e56-0f047574e7a9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/94bdcae7-d46b-4654-837a-8415e77a1b2f)

hmm... In .other_user file, there is a passage about the life of Slade Wilson.
Putting that aside, let's go look at the files we just downloaded.
I see a file with the .jpg extension: aa.jpg => use ```stegseek```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5df12ad5-d8f0-40eb-b1c2-4c1125bbb10c)

open aa.jpg.out 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8cde5374-3397-4190-bbc6-afe77d8c5187)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/60126561-cd71-4ade-8991-d3e79401f6d6)

## connect to ssh server
with user: slade
<br>      password: M3tahuman
     
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/395137ce-f29f-4069-bacc-de9a23f52424)

# PRIVILEGE ESCALATION
## check with ```sudo -l```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/22f4a0c6-1157-4389-80e6-4461bc65cc14)

Go to Gtfobins 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b3b70fc8-6a19-4fc4-a630-3e9c3cc2da82)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4eda8d32-f1fb-44a2-9a0a-2fd71a715dd9)

## Done!!!
Thanks for reading.Bye!

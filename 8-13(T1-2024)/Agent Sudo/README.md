# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7b30029d-7ec3-47e1-9da4-a8bbf6a61871)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a74b248e-d11b-4d56-86e0-36571000a4b6)
## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1bfc2073-38a1-4af2-8043-b42ecb8f55ff)

=> no hidden files.
# EXPLOITING
## using extension User-Agent Switcher and Manager

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/00cf42b8-6b72-436c-ae8b-6934ed7c90f0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fb9f7e33-445c-414c-93c0-433a7b4b08d0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/46e6122b-ee8f-43fd-9540-d283525ee5b0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aa55cf28-33f5-46a9-8d62-66db1f6c196c)
=> chris

## using hydra
Finding password to connect to ftp server.
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b9cecad5-c5ee-4d74-9e96-7c4e96a5f37c)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/23e8bfba-3120-46b1-a645-49832a08e701)

I connect to ftp server and get 3 files
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9bd1e4af-f2d3-44fd-be3f-945a74105ffb)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/027744db-cdf9-4879-961e-cbf5c1c8a1f4)

read To_agentJ.txt. 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/79c15c77-5f9d-4500-8b46-cc6d577f26b8)
## using binwalk

while use Exiftool to parsing image, I see binary data and notice the warning line.
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/98d2f6dc-c77a-4c59-91a7-f15dd8c12c77)

Using binwalk .

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b7312ef0-bed9-42eb-99c5-0cffe0004d7e)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/12211f4e-3305-4bdb-b00e-0470bb4229ea)

cat To_agentR.txt.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2fab7a60-9fbd-4e88-a298-25a167f150ed)

=> nothing

## using zip2john 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/43f8cc25-b3f6-46eb-8ae3-03ed5eecff32)

I get a password: alien.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/57a6b30e-4fc7-45c3-bd71-0773b46a8004)

Now, I try cat To_agentR.txt and get a hash.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/db72bf0c-77fd-4992-b375-61df4483f281)

Go to CyberChef website to crack the hash.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/af5fe409-42cc-4507-b65e-6ecbdf495940)

## using steghide
Previously we had a decrypted password that looked like passphrase: Area51.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9c810743-8536-4540-96f7-e19f4c77f78e)

Nice! Now, I cat message.txt.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/339c4f50-30a5-4773-ba51-3bed8afde752)

## Or more simply, I just need to use stegseek

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cbecd3a0-1ab8-4c93-bcf1-56a7b84b01ee)

Either way, I finally have James's account password. Then, I can connect to ssh server with user james.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9dd7d0ee-903e-417c-991a-d8c477832746)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/981c1e7e-cbc6-4737-b1e9-161298c58bce)

So great! I find user_flag.txt.

Besides, The lab asked what the name of the picture was? So we scp it to the local computer and search on google.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2c54ccbb-1d00-4e24-b561-5535a0095f0b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4d110e00-be23-4dec-906d-82b2c441e159)

=> Roswell alien autopsy is name of image.
# PRIVILEGE ESCALATION
## Check for the user sudo permissions

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/db934fe1-c2cc-459a-8d3e-b40c96d55242)

After that, we searched Google and found a report about this error.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2c1e4531-8aac-4d02-a5dd-05a3704dccb2)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f5c50ec5-febb-47ee-8034-738590509078)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5a567f54-7852-4e16-b500-f7a1ff70170c)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/746c8519-d5a9-44bb-85e7-a281892c16d5)

=> I get root flag.
## Done!!!
Thanks for reading.Bye!


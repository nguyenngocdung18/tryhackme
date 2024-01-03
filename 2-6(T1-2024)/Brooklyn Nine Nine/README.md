# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8efa5a80-c870-482d-aee4-fa7629c15bf4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f142fd40-daf4-4a1d-854b-e1842a4175e3)

look this, I can connect ftp with anonymous
## using gobuster

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b0883fe5-ac99-41d7-8ad8-10b4918e7306)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0fbb12b3-57c2-4b7d-8d9b-369d38c41a89)

hmm... Looks like there are no hidden files

# EXPLOITING
Well, I'll visit the ftp server to see if it has anything

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3d584357-609b-4620-919f-d206956af73b)

I see one file .txt. I'll take it to my local computer
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5925b4fb-7b5d-4892-8fcd-14f8d6e4b41d)

See what's in it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0e605047-e208-4ba8-856b-af2dc8ec0602)

I see a name - jake. I think that I can use it to bruteforce attack and find password for ssh.
## use hydra
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9271ab07-6484-4fa4-a6c7-672b5d76184d)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/276d2a7f-769a-44f8-8e55-cbf4e4e6fb7a)

haha, I had password. Then, I will connect to ssh server

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/41781556-bed3-4ee6-a1c6-7dd212141cd6)

and get user.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0d749c51-2d74-44cb-b552-6189ed23a39b)

# PRIVILEGE ESCALATION
sudo -l and i see

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fff44932-fc6c-4531-8edd-fc37050cb5c4)

go to gtfobins 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/caf202cc-d697-4a5f-9436-c3f4c202c588)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eb2e05da-0f84-4a62-a0a1-a3067e736a80)

## Done!!!
Thanks for reading. Bye!

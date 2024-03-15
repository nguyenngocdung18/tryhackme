Link room: https://tryhackme.com/room/ide
# ENUMERATING
## using nmap

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ff67cb0c-b19b-4f48-bf63-c6d9474b36b7)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9ef6195c-9d29-4766-84b4-546fd7aed980)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0bf012dc-21f1-447a-80a9-4fe7eeb70c67)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3e094ad7-759e-443d-9e6e-966ada0e05b4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/088a40e4-f60b-48c9-94d2-602023ae89eb)

## connect to ftp server (port 21)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5e6e501b-c2a8-4e19-8a38-5399cd66e082)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5b0b7c98-3010-4a9c-a98f-f3541aeb187d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c38ff2be-b7a9-4a31-8947-1a5eb5e378d2)

I rename it to "ftp"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ae17acb3-1657-4915-b056-24636e0dcc9b)

=> user: drac and john. 


## view web with port 62337
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b9b3e1b5-8b9f-4281-8264-af5fd524191f)

=> title: Codiad 2.8.4
<br>
In "ftp" file, I see that user john has a default password. So i use Burpsuite to brute-force with check list password

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d8fc1b77-a0ad-4dc5-9dd3-4e851ef6e6c8)

=> I find authentication. john:password
# EXPLOITING
I couldn't find any exploitable points from what I found. So, I try using searchsploit with keyword "codiad"
## using searchsploit
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f0eefb90-86c8-42d6-a472-035becd8b780)

I download and run it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6d61c0ea-6042-421f-b0f1-dcd641d591da)

It asked me to execute the other 2 command lines first. So I ran those two commands at the same time. Then, I select "y" to continue execution

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/aa6f2c21-b742-4f7b-8152-3daf430a3c5c)

It's worked!! 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ddfa6c71-73d9-4e63-8a64-d9ebc266d382)

I find user.txt file but i don't have permission to read it. So I try read ".bash_history" file to try my luck

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/02dd3a59-ab6a-464c-b749-9e4927238ed4)

=)))) Nice. haha look at this, there is still a mysql access statement here. I have the password for user drac

## connect ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/42dff344-d795-4ce8-a5f9-33afe8edfa27)

=> I easily connected to the ssh server and received the first flag - "user.txt" 
# PRIVILEGE ESCALATION
## using sudo -l
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/546079ad-3d8f-4a02-a085-55bf2e069345)

I search on google.com 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5618d82a-2b6b-4a03-8234-09ee462703a1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4a52fa44-0ace-4adc-bbeb-e10f47f1e530)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/30f99040-38a6-4d9e-9ba4-a5d9633570d9)

Now I just need to follow it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e23dba9c-3e60-4f06-a158-2351053108ae)

I edit file with ```nano```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/138131c1-0f19-49bb-9ea0-47c7a3bd63b5)

In the browser, they edit "ExecStartPre = ..." and use ```nc``` . I don't do it. I edit "ExecStart=/bin/chmod +s /bin/bash". Because I don't want to use ```nc```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/732efdcb-48a6-47d6-80d0-28918fde74ed)

=> root.txt
## Done!!!
Thanks for reading. Bye!

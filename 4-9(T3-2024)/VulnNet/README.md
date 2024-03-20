Link room: https://tryhackme.com/room/vulnnet1

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4d86dfd8-9a1b-4fdc-848b-8b4b804575e7)

Editing /etc/hosts/ file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1fc6de8c-9169-47a0-802b-4cb06d935491)

# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d24646d2-c514-433c-b054-877c575a260a)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fa8651ce-ae84-4bb1-bf76-ee5370b80fe1)

## view page source
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0a93103c-c091-4274-8315-d3f8d065dd4a)

=> I see two suspicious js files

view "/js/index__7ed54732.js"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7f54b39e-4ecf-4892-8d24-3d90b9602f22)

I copied the content into notepad for easy viewing

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6c76a1be-5736-4cf8-9936-44e4e8f638ec)

=> broadcast.vulnnet.thm

view "/js/index__d8338055.js"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2c5a356c-e7df-41f4-99d7-5578da02855e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/45ed0694-c1e7-4c67-9e64-a9eb39cd7e92)

=> a suspicious URL

# EXPLOITING 
I add "broadcast.vulnnet.thm" to my "/etc/hosts" file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bc1b8e88-1c12-47e9-8238-f85e6010139d)

## using BurpSuite
I use BurpSuite to check suspicious URL

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4807d8f9-6aa9-4adb-8114-df62884e12b7)

Try with /etc/passwd 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8ad0e822-005a-4217-b36b-096ed53d6ec4)

=))))) Nice!!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d7d2cd3e-1d1b-4280-abb1-2c4fe4a10a49)

=> I find the "/etc/apache2/.htpasswd" path

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4d696e38-793e-4d83-be03-cf35849b2b57)

=> developers:$apr1$ntOz2ERF$Sd6FT8YVTValWjL7bJv0P0

## using john the ripper

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c05bee3e-3924-44a2-95f6-6e4d1f329cd0)

=> developers:9972761drmfsls 
## login to broadcast.vulnnet.thm

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/578c94ac-9fe2-4967-b7ec-67afcef86312)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/03d160ff-a1c3-4f95-9e2d-9724284ae442)

I see the title "ClipBucket v4.0". So I try search it by ```searchsploit``` command

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9fafb80e-3c26-49c6-9a86-d98ac3e93fd7)

reading 44250.txt file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0c1b5028-d403-432d-adfe-2930b1db6d9f)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4f177580-2f7a-4222-bebf-448afa2ada57)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2c2fbb09-eaeb-4c45-92a5-33e43c7dc007)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/26b1e9fa-ed0c-465d-a7f1-0553784565b2)

=> Look at this. It's uploaded successfully.Then I use ```nc``` to get reverse shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3dad1101-9496-4cfc-957d-6da2c96a7ee1)

=> It's so bad!!!! I don't have permission to access directory

I try ```sudo -nl``` command to check permission. But it require password

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d3cc34a8-6d21-4aa5-a2f1-add8b4997e52)

I use ```find / -type f -user server-management -exec ls -l {} + 2>/dev/null``` command. It's used to find all the files that the user server-management and displays information about them using the ls -l command.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e0f13425-065a-46ba-8584-c9fb48b8b43f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2e10de2e-9cd5-49c7-9007-31f1bcbd578a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/debb2f11-8971-42c8-83fc-0cba8464691c)

Hmm... I still don't have permission. I try copy  all files in "/var/backups" to "/tmp"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/56963f3f-6048-4bbe-a6fa-fed176c32be2)

=> It's worked!!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e9ce2d20-a19b-4eca-a939-e8e73795f8c6)

## using john the ripper

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/39a2e144-5939-4930-9345-3a5201ffca22)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3d2a3360-a838-4817-a734-50bd440b6986)

## connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a45537ba-aa55-4c59-a105-def136632cf5)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/40c33111-8264-4b63-8362-6e765d716a7a)

=> user.txt
# PRIVILEGE ESCALATION
## read /etc/crontab
When I use the command "sudo -nl" it still asks for password.so I try reading the crontab file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b1dccad0-4cab-4b64-a9cb-ca8f5346bec9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d89d61a7-6b54-4e03-92aa-e8eac8090e0b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8fb318f2-9613-4964-8f4e-1ace1facf278)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/55a99c37-b4b1-435a-b164-8deb23cc566a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ff54b84b-fc97-4809-98c5-ff9f57108b9c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fdd73d8b-21e5-456b-b939-c89fcd606968)

=> root.txt
## Done!!!
Thanks for reading. Bye!

Link room: https://tryhackme.com/room/cowboyhacker
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6751bd5c-9ab5-4bb2-9df1-537dde87a88f)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/96ea8ed1-a268-4ec4-943c-0008ac63d721)

continue

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fe356558-6c76-47d1-9cfb-cb1c44ac794a)

I can connect to ftp server with anonymous.
## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2128b059-e003-4609-a5e0-3b7ce849764b)

=> no hidden files
# EXPLOITING
I connect to ftp server and get 2 files.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c8397330-30e9-4a6b-9419-49084b26b492)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7a5f3779-6868-4602-9ff2-7dfaa2c9a427)

cat task.txt => I get user: lin

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9f4cc309-9f03-4f7f-9b0a-edaf68ddad64)

cat locks.txt => I think it's the file containing the password

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/57c16f5e-844a-4cf5-9420-4d76cfa3bf46)

## using hydra
So, I use hydra and get password for lin

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3191391f-4b4d-4960-9e77-07721d2b28bb)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e6187265-1d62-4c68-9ff0-8124a9e3f74f)

=> user.txt
# PRIVILEGE ESCALATION
## Check for the user sudo permissions
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d3634e8f-f744-436c-bafb-8091f7ff1983)

Go to GTFOBins website 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ab078909-485c-4755-ab85-c8f87fb6e3b1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5089c07f-355a-4159-ac35-2431b619a9cc)

=> root.txt
## Done!!!
Thanks for reading.Bye!

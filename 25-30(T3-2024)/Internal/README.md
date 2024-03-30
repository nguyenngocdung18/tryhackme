Link room: https://tryhackme.com/room/internal
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/76336fc0-935c-4e0b-a6d5-8059ce60dbd6)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b7ebc111-83fd-43c5-89a0-fb4b851617ef)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8142816e-3aed-470b-acc6-7e633e706e14)

## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/368954fc-e1f3-4625-a15b-59bd6217881e)

=> wordpress
# EXPLOITING
## using wpscan
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7d26fa76-2235-4bc6-8549-4b53a7d2b93f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b969bf1f-2154-41d4-93bb-9329262b8946)

=> admin

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f3b38566-ce24-49f5-b4c7-b5a3bf870a2b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bb41239d-3b3b-4ae2-8119-da591b7049b9)

=> admin: my2boys

when clicking the login button. it navigates to internal.thm/blog/wp-admin but it's pretty simple (at least on my machine, it still doesn't load). so I added 10.10.233.4 Internal.thm to /etc/hosts file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7edb6088-6518-42d4-b274-c636b9c8a2bf)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a0b07893-aabf-4a24-92b5-287e5fbd67bd)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ab18f260-fece-403f-8e37-6c055c5e7296)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5f63fa28-a465-4c60-8c04-f4b199aa60a1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f62778a0-5f35-4284-bebe-6a9009e90d9e)

=> I get reverse shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4a02c965-b9f0-415a-84e3-63e458f4a0ac)

=((( no lucky

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ccd51253-a64d-44a3-b652-2232fdc78bd3)

=> aubreanna: bubb13guM!@#123

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/903cf7ab-5f26-43ac-a477-71f3d3598fbf)

=> user.txt
# PRIVILEGE ESCALATION
## using sudo -l
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/53a773ed-d775-45e6-9b47-18396fce4873)

 no lucky again :< 
 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/99d70367-ea88-40f1-beaa-9e5fa19eca77)

## using msfvenom
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e187076b-1ece-4171-a1a3-c42fe07eebc6)

## upload file
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/08f64906-3c94-424a-a07a-5104c9cab8e9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/27e9636a-b9b8-44ef-9cfe-6e8b8de07b88)

## using msfconsole
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/870bbee2-748e-4a6b-bc18-6d766105c4d7)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/74d75f44-a960-4ea9-9830-09f95462449e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/455bbd89-8bcb-488a-a2c1-209d35919498)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/111c5e50-9e13-43cd-a5b4-329bc5a5cc83)

Continue to use msfconsole

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/acbdf10f-7d03-4eba-9e3a-0ac07febeca4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a25591f5-e87a-49c7-aa66-c7244dcb196e)

=> admin : spongebob

Go to Manage Jenkins -> Script Console

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5f39f9d4-267b-438f-86ae-29f44fa61fcf)

=> Groovy script
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a7cb6891-0161-4064-b212-2b038ee1515e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1265f605-0165-4892-8554-35001924fa3e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5f8c199e-d634-408f-ac50-6949bd9180d0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c368dc01-0367-4e80-88cb-b2d76426c301)

=> root:tr0ub13guM!@#123

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b3ef6ebe-0587-4bfc-8a38-66c56af73dea)

=> root.txt
## Done!!!
Thanks for reading. Bye!

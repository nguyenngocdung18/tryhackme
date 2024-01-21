Link room: https://tryhackme.com/room/archangel
# ENUMERATING
## using nmap

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/71f093dc-459b-483f-b5b9-1c46d3bceab1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4250f28c-0811-4916-a39f-cf3d580aaff6)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/be265f30-cd35-424d-b6da-657f03246497)

## view page 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7e9164ad-2859-44bb-8928-04358cb1fe89)

=> Hostname: mafialive.thm
# /flags
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3bd968da-18c9-4022-b6b6-cca81cdd495d)

hmm... I find flag.html and click on it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ed9b6df9-bf35-49b5-8da7-d40bb475f6f6)

=))))))))))))))) Rickroll.. haha
# EXPLOITING
## sudo nano /etc/hosts
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c9c1ed63-be86-4af1-b913-4d889115f427)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/beb61b6e-5866-4f8a-9b0c-0f255bf136f9)

=> flag 1
## using ffuf to find hidden files

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b6ca889e-c5d0-4da7-a064-3bb7abcc9282)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cb34d515-2fe1-4fac-99cb-3db09abc1396)

=> test.php

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/606cd83a-32a6-4862-8c15-be0f846b469d)

Click on button

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a20c5abf-d44d-4466-ad6f-77c87829629e)

I search on google.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cf19f460-bdb9-4876-849b-5f35807e041a)

edit URL:

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ab02645f-f79c-4d35-b01e-58137354076d)

=> I receive the hash code. I crack it using the CyberChef website.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4c62ecf9-15e9-4621-898f-e9bc782e68e6)

=> flag 2

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d73c2732-ae3a-4393-b0ab-d95bef3c0218)
 I see the code <pre>
```php
      if(isset($_GET["view"])){
	    if(!containsStr($_GET['view'], '../..') && containsStr($_GET['view'], '/var/www/html/development_testing')) {
            	include $_GET['view'];
            }else{
		echo 'Sorry, Thats not allowed';
            }
       }
 ```
  </pre>
After a few tries it seems I have access to the log

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ccc3cb81-4d6c-45a2-889f-448b18cc3e56)

## using BurpSuite
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8c9ea9c1-ffb0-4e35-827b-0401cfbfe334)

send it to Repeater. Then, I edited the user-agent as shown below

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/57f4a216-f16b-45df-8add-8d6b709638c7)

Click on send and reload page 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/606dd687-eed9-4e6b-8d69-cc467ac9e490)

=> I get a reverse shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0151df57-f9a3-45c0-988f-b5da50a4b957)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6184b7eb-c693-4c12-bfbf-af719f5dffc4)

=> user flag 1.
# PRIVILEGE ESCALATION
Try ``` sudo -l``` but not successful

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/91062eee-1d1c-4892-a4d3-848469b1edcb)

Because I couldn't find python on this server, I used another way to upgrade the tty

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/13b0d8e0-8ba6-411c-909e-93eb76b74af0)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eccfa884-7463-4cf1-bd84-aa490a68e317)

but still not successful. So, I tried looking at ``` /etc/crontab ```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e5449e50-9471-4e9a-acf6-1c091c21fb3d)

I see ```/opt/helloworld.sh```has archangel user rights and try checking again with ``` ls -la```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/badeda81-bd40-4ef6-ae98-b37c68a85fab)

=> Nice!! Now I can edit with nano to get the shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1ddf4c7e-cf8c-45af-a73d-b904e61d5984)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/dc913e98-23ae-41e5-9fac-cd241abb598f)

Successfully obtained the shell but it still needs to be upgraded tty

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0f6f166a-1635-45ad-9058-f6dbcd788dad)

=> user flag 2.

I use the ```cat``` command  to view the backup file and find ```cp /home/user/archangel/myfiles/* /opt/backupfiles```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3a2880b8-f1a8-4e0d-8cba-10ff69f51894)

I create cp file and edit it

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/14f7366a-8763-4e5a-b87b-98f9904aba99)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/39c27f71-19b7-49ef-a02a-1382d83579b0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/94f6e7e2-a8e7-4df0-bd31-cf2a3b65f5d4)

=> root flag.
## Done!!!
Thanks for reading.Bye!

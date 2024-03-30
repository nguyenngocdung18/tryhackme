Link room: https://tryhackme.com/room/gatekeeper
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e9036813-c7cd-4862-a0a0-670909619225)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fbc7c9dd-ae8d-4313-bf12-2a55c3d765c7)

## using smbclient

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/94493525-3f11-46a8-b3bf-16b1ee7824fe)

# EXPLOITING

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4764188e-c272-4a13-b307-829bf4fd8465)

=>  I discovered that's the program which run on the port 31337

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/027ce6ad-bdb5-4f7b-b133-a9efee108aaf)

Download it on windows machine

Use this script to test 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0658506e-7e9e-4522-9284-075af8e36168)

Then I found the bad characters "\x00\x0A"

## using msfvenom
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a0e627a8-4b7f-4296-8add-358b38387c97)

Edit exploit.py file 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9c9d75bb-8428-4d28-b9ce-dd1c56543ab2)

## using msfconsole
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e1b3be38-ea16-4cb8-86aa-c70a6a3a7543)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/58fc6a58-ad7e-46df-950c-6c508cf2def0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/026f36f5-6cc3-4185-9669-a008d0effeae)

=> user.txt
# PRIVILEGE ESCALATION
## Dumping file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/81a7215a-a003-4f49-b243-39912d25d3ec)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a4a57c79-aa99-45a0-a2cc-a4364ae9bd27)

I use ```gitclone``` command to download tool

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9ee9406f-cf15-47ca-9eab-32af0ec7c704)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/992d6b6e-e372-46a8-be98-37337e8b6551)

=> mayor : 8CL7O1N78MdrCIsV

## using psexec.py
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a3c960ae-065b-44cd-b1ed-65dd86e7f8a2)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e9d50188-c53c-486f-975d-4d177c659701)

=> root.txt
or 
## using smbclient
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a5440aee-f992-468c-b185-65a0c5d9a77a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/78beab52-d53c-41ae-8275-ae9cc87d190b)

=> root.txt
## Done!!!
Thanks for reading. Bye!

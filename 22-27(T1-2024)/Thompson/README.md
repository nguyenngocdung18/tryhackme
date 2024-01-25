Link room: https://tryhackme.com/room/bsidesgtthompson
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d741ca1d-0acc-47b7-be9d-f015fad43ab7)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e3d49c76-231c-4f4a-85b3-6089e4cc59f7)
## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ec773a27-72bb-428f-b85f-1dd40f8de042)

## view /manager
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/60c5d3a1-1d64-41f2-87e5-54414ed79367)

=> username and password

# EXPLOITING
## using msfvenom
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/79698e5d-f537-4553-a56d-bc5533955101)

## login to manager app
upload shell.war

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ad5e1840-332d-46de-81d6-4a099e1e200d)
## using msfconsole
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b9cc426e-3338-4dbd-8cd9-f961c946f8fb)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eff5f439-1b16-4c52-815f-87ec65b870b0)

=> Nice . I get shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ba27db97-5592-4a13-9171-9152e1a801ec)

# Get root.txt
## view /etc/crontab
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6132823d-2674-4216-accb-273ae6f37570)

=> bash id.sh
## view id.sh
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6617af71-aea1-44b2-88f8-9b335760b004)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/df237ff8-0f45-4b8f-a367-c588d21b9573)

## using echo
I fix id.sh file with ```echo```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4b2b24e1-6bf1-4975-8614-0cc391577622)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bb339cce-cd7b-45d1-a011-dc9a322c6d6f)

=> root.txt


## Done!!!
Thanks for reading.Bye!

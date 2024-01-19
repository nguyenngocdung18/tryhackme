Link room: https://tryhackme.com/room/easypeasyctf
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/25da8cc9-49ce-4c16-a005-fd50ef55ae42)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c5f581ef-0236-4a89-8e03-c00229f0fad2)

## using ffuf
Actually, I can use gobuster too.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7796fb5b-32c1-4b04-a05f-73f3f7f038ce)

Continue

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8f38422b-fc7c-41ce-989d-b15112f5fe9d)

## view page source 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fdc4e83d-1aee-4962-af6c-fd423b423299)

=> I get a hash code.
# EXPLOITING
## CyberChef
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/639419c7-d930-40c6-a8c1-adc697f1ecaa)

=> flag 1
## use ffuf to find hidden files with port 65524
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0c649f62-f875-4c08-ad49-aaa68861e373)

=> robots.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1fb567cd-2d4a-4522-863a-93b24d97c34a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7f632988-0f78-43b9-b90e-affcdb0b1ab6)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3904433c-0126-48e1-ae36-cbb7bd6dd567)

=> flag 2
## view web with port 65524
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/53158585-85d6-4d52-9d8d-f73b15f15858)

=> flag 3

## view page source
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/82db4b5c-29d3-4ec6-a4e6-c750bbd301fe)

=> I continue to receive a hash code.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d66d556e-425d-4adc-9fc0-cf846c994f64)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2a8d0bfb-1ab0-419e-934e-b2f046f0b885)

view page source

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a8e43c28-746d-4ddc-838e-4a2e4c11894d)

=> A hash code

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bda13427-b09c-4e11-8b38-0548b5f82b87)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/31e0cb06-daac-4b0a-af9b-e33a984ef3c9)

or I can use the wordlist that provided in this task crack the hash

Then I download image from website

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/074765ac-b587-4af9-ba18-fac2fabff004)

## using steghide
with passphrase: mypasswordforthatjob

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a4d888f6-ce26-42b2-b8d0-40f756a10404)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/066a0ab7-4b85-42ab-b9ef-c9c8357092b3)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b94179dd-9227-4a28-b9d6-033b5f52b471)

## connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6284ff1f-284a-4ff0-80bd-4faae7ceebe2)

=> I get user flag but it seems incorrect.I cracked it with ROT13 and received the correct user flag.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/689c3058-8cd1-425c-b06f-f33c6341dd33)

# PRIVILEGE ESCALATION
## check with ```sudo -l```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/da67babb-0a18-4ff9-9f11-5cbabe26912d)

but boring user isn't permission to run sudo

## cat /etc/crontab
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a6d9204f-7f31-45a3-8734-9c29896d1976)

It looks like .mysecretcronjob.sh file can run with sudo permissions

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1dbec28b-7a45-4880-83bb-5949d7b6ae43)

=> Nice!! Now I just fix it with command ```nano``` and get reverse shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2466144b-daa6-4947-ab17-48e9efdf3e95)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/41c4848d-5a2c-4b4a-b927-f6d713fab650)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3f127974-0847-4c4c-a8ca-5b6261588210)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2195a310-fbd3-47ab-afad-dd3e0b32b0e9)

=))))) Phewww... I get root shell . Then, I'll find root flag.
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ac5807c7-546a-4f00-9e32-0ef8ddc4dee0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8a5b5906-6fe5-42a9-aee9-dc971ddcfa10)

## Done!!!
Thanks for reading.Bye!

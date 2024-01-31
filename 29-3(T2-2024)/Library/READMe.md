Link room: https://tryhackme.com/room/bsidesgtlibrary
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c012ee71-0551-4e5b-a672-bf6c0470087a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ade07098-6a2d-45c3-ad29-557a0a7f0918)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b2b9c34d-5fa8-4403-ab6d-a5fc626ff2ac)
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4f86c12a-5abd-43a7-8665-41734fc69242)

oh... I find the author's name - meliodas. Maybe it's useful.
## view /robots.txt
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0fab6ccd-cc64-41cb-933f-f2423e455bfe)

## view /images
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d0a071c3-ae4d-4d29-a290-923ba9b29743)

# EXPOLITING
Hmm... I don't find any clues. So I try to brute force attack with ```hydra```

## using ```hydra```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/15a3e8d9-3c0c-4b87-89b3-36652af7e50f)

That's great! I receive meliodas's password to connect ssh server
## connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5537bdbd-e8d6-4629-b26b-efa3e1cf57a5)

=> user.txt
# PRIVILEGE ESCALATION
## check with sudo -l
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/288e26f1-58b5-4234-ae9a-48b64a0377a0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/25db4f83-58e5-4075-aae4-e8e0db497778)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5c8d34fd-6c16-4770-979e-a42bbc54be5e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2aa85b73-55f9-4407-8261-a67cb913ae45)

There are many ways it can be used. And here I will illustrate the two most basic ways
## 1. Pseudo-terminal
First, I remove bak.py with flag -f . Then I create new bak.py file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2ebafdae-3112-4c74-9607-fb20b376956a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/132cb7e3-856f-40f4-9f66-bf9c80ab828e)

=> root.txt
## 2. Get reverse shell
I go to pentestmonkey website.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5bb3ddd0-a853-4aef-bcfd-997ef3821bc1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a027796a-4974-49bf-9ecd-4af72660ee92)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1b22b02d-317b-4058-9eac-4fa85a60fb2c)

=> root.txt
## Done!!!
Thanks for reading. Bye!

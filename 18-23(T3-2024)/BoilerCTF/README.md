Link room: https://tryhackme.com/room/boilerctf2
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fb6667f0-1121-49e5-9087-853635ea1fd3)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/82ccef4c-911d-4385-923a-9d0c83dd1d01)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bed8a791-4863-46e0-ad57-c4ecde5843e8)

## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7c8ab0d3-6caa-497e-b68e-1259bfc61346)

## view /joomla/_test
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e50c055b-1e7b-42ad-b68a-930ba88c928e)

# EXPLOITING
I search on google with keyword "sar2html"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c3a8fb5c-7d9a-4b48-9656-7afe1eae64ae)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c1e26a34-55df-4c31-a855-0bc800a86fdd)

=> log.txt

## using ```cat``` command to read log.txt file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/98c6dc94-147a-4bb3-b5d2-7b6842062617)

=> basterd:superduperp@$$
## conect to ssh server with port 55007
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/575e56c3-df9d-47b3-aea4-99724704b3f2)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8317a769-1f1d-4019-ac61-ef11dc581370)

=> USER=stoner #superduperp@$$no1knows
## using ```sudo -l``` to check permission
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7367c4b0-6532-4df1-b373-8d5b60b6e936)

hmm...

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5c51893a-0af5-4aa7-96f6-c0e22f9294a0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6cd91aa1-abe6-4e20-9ca2-67e5898f339c)

=> user.txt
# PRIVILEGE ESCALATION
## using ```sudo -nl```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/896cd1f0-7254-4834-9626-acf1f7575d86)

hmm... nothing

## using ```find```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/86ce441f-2d7b-4cfa-8687-3bc3bcb6e771)

=> /usr/bin/find

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6349c4ad-1e14-45fc-9b26-7c15ff093796)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fc26318a-9952-4f63-88a0-73acb80cf37a)

=> root.txt
## Done!!!
Thanks for reading. Bye!

Link room: https://tryhackme.com/room/bsidesgtdav
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6d28ce72-b4b3-40b9-80e7-26492ac675de)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c32385ef-5122-463a-8ddd-8f2332cc1204)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b5b720d5-ef08-4428-9a46-132705efda5c)

=> /webdav
## view /webdav
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/51e0b268-7253-42d7-a273-ef06cf73e05c)

=> hmmm... I need user and password to login website.
# EXPLOITING
## searching
Except for /webdav, I don't find any useful information to mine. Therefore, I try to search on google with "webdav login form vulnerable" and I find the website. (Ah.... and It's not on the first page. I had to browse quite a bit to find it)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0b610a15-d74f-477e-bb35-b06f9062a848)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/17359468-f2a8-4606-84ef-0ec565e8fa42)

=> Yeah! I find user and password to login web dav. So lucky!!! Not only that, I also found the exploit in the hacktricks website
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/08a50b73-1147-4b10-a16a-a4e67aad6241)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/733b7565-946c-4705-b9a4-bf26e161c358)

## using ```cadaver```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d0478e8b-6d31-4110-9fb4-e371c0b9c2bd)

=> Nice! Now, I use command ```put``` to upload file.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7aee6566-a15f-4e6a-8d54-8808cf207b4d)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e00d1c9e-f76b-4f03-90db-ec555d8d9c09)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/474397e5-bfc9-425c-9173-6e6d70a247fc)

=> I get reverse shell.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/72cc6d03-ff27-42f2-81bb-8ae76aa61436)

=> user.txt

# PRIVILEGE ESCALATION
## using ```sudo-l```
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/71011f2e-02b4-4ad7-b9ff-7a9b32ff3917)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/07affcaf-2f11-4bca-bc57-42320575102e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/acfcd77c-91e8-4095-8cf0-cc3f01c2df48)

=> root.txt
## Done!!!
Thanks for reading. Bye!

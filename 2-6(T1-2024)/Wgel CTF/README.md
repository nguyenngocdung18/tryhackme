# SCANNING
## use nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2578fcce-c971-4281-9c8d-48f02a4845bf)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/30cf747c-8038-412f-8253-a689c8c52b63)

## use gobuster
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/953ac92d-3916-4964-9826-c387f42d65b9)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1a35dab8-89af-46ff-9538-b599562a52fc)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4ebbcb06-9647-4635-980d-b0712be2defd)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/56985247-2e83-4830-bfa2-d8a1fea08776)

## view web
While waiting for gobuster to run, I went to look at the web page source
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5f0653fc-cae4-4bbf-8fb3-bc66a8f550c5)

I see <!-- Jessie don't forget to udate the webiste --> , hmm... I don't know what it is but it's worth paying attention to

Now, with /sitemap/.ssh , I have id_rsa

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9eabc6b0-52e8-409c-b726-24ed85e312d6)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2f7307d3-9287-4897-bbb7-906f5355aef9)

# EXPLOITING
I try using john the ripper but id_rsa no password. Well, I can connect ssh

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/63922265-391b-411a-ac31-60b44e9ee965)

I walk arround and find user_flag.txt in Documents

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2fa6b066-f0c6-4616-824a-d3d8da946005)
# PRIVILEGE ESCALATION

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c861a094-8d39-40f7-a45e-23b3bf7cead4)

search on GTFOBINS
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d1e18084-62bf-4de7-8c9b-ce292134dc69)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0e20fd92-85db-471f-bcfc-a8590755bc3c)
## Done!!!

Thanks for reading. Bye!

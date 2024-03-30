Link room: https://tryhackme.com/room/cmess
# SCANNING
Editing /etc/hosts

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0907f1e1-e891-4f2a-8887-a92062b2a701)

## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5a4d9d2b-d1a9-4cf8-bf66-12bd49c30225)

=> /robots.txt

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1d0358fa-1f4a-4568-bd3b-edcf2bf68e85)

## using ffuf

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6f745b7e-414e-4c17-b2c1-f71e7e00bc4c)

## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8fb8a39f-35d4-4487-85e2-609496a5b44e)

# EXPLOITING
## using ```wfuzz``` to find subdomain
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6c1bfb5a-4084-4b85-b215-3ddca806d21d)

Add to /etc/hosts

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ece84089-9f34-4c3d-8350-62ec6aa8bbb8)

## view dev.cmess.thm

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c6da2bc3-12ad-42e5-a037-36d3240a2bcf)

=> andre@cmess.thm : KPFTN_f2yxe% 

## login web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/adf7410b-7a73-4805-bed9-a9901083a670)

## upload file
Go to Content -> File Manager and upload file.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e5b36792-cdb2-4b5e-b62f-47e5ef69f7f9)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/25e812de-d736-4b51-b445-da482e7207d1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b680e2f5-7524-47f3-8afa-117f2de7f0fc)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bb95509f-f297-4f8e-9530-15f064d40f3a)

=> I get reverse shell

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d3802057-48cb-40ba-9bb4-2517104f4561)

=> I don't have permission to access the andre folder
## Walking around
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b1d8fa91-9436-4113-852d-1a2a13b9d546)

=> andre:UQfsdCB7aAP6

## connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7c58ca93-91dd-439f-a5c9-5e64207045d0)

=> user.txt
# PRIVILEGE ESCALATION
## cat /etc/crontab
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e523b239-7b6e-4b7a-8e53-f40e213c2e1e)

Go to GTFOBins

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/591fbc0e-71c5-48c1-9164-eb9cd481d2a2)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/31d656ea-e61c-4675-952f-9bdf485e8afb)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4e1fa59a-8ca3-4374-ba99-f0710c06289c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/67970ec7-ac39-49ef-90ec-787d04bf6968)

=> root.txt
## Done!!!
Thanks for reading. Bye!

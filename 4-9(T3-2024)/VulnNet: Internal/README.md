Link room: https://tryhackme.com/room/vulnnetinternal
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b3ce6f00-372b-4865-91a0-9886a5d72652)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/adfec87d-5f7d-4a7f-9aa1-40a035feac7a)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a6233cd0-8374-4b60-87b1-90f598ba4cc0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/14908491-6861-4232-8d19-0a314ece43a2)

# EXPLOITING
## First Flag
### using smbclient

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/570e7504-7c98-4e98-b1ef-b6d9af62bf5f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5bded2e7-c451-41ef-9902-d8a5b98a6eb0)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f8d958f4-1951-47de-8a8a-417bf2f9b905)

=> services.txt

## Second Flag
I create a directory with ```mkdir```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f83d47c4-7c2a-435b-a307-dd406a391924)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/adeb05ce-71d2-4f38-8fb5-6c6a64550826)

I go to redis directory and read redis.conf file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/44659c15-bf64-469a-badf-eca8c11154eb)

I find requirepass 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5890d171-8f99-4edb-baa2-019afbbfcbe0)

### using redis-cli

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/610e1fb1-00ea-4b81-8a09-fce3fc465f85)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b349ab03-be3c-4007-ab11-d36e7872008d)

I go to the CyberChef website and get a message after cracking the hash: ```Authorization for rsync://rsync-connect@127.0.0.1 with password Hcg3HP67@TW@Bc72v```

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/dbce7da7-05d5-4221-97fd-f6def0b39b15)

Also I receive the second flag

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/5402157d-de03-48a1-9572-598efcc323cb)

## Third Flag
### using rsync

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8d36d54d-5b47-47b1-b804-f1e354c2f3aa)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8ecf1b14-1775-44d9-bdb9-dad2bbeca788)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1a330d09-fada-47b7-b6b3-fc11ade91499)

### using ssh-keygen
To generate a new SSH key using mathematical RSA.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/755b8767-f748-4ba2-9e55-04017d03c5a7)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/435e4bf2-aa5a-4647-85fc-5b61ea95e349)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f8e89640-ab7d-405c-a917-b420be38f80a)

### connect to ssh server

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c9ed31fe-1293-40ad-9b19-5e91922a6af1)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3f1a67ca-38d3-447f-8a3a-baacb238ab2d)

=> user.txt
# PRIVILEGE ESCALATION
## Final Flag
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/889e2940-31a1-40ae-b795-7992c57c48e4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d0f04ff5-3848-4b37-b9f9-b882914228a9)

=> localhost:8111

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d6a2b0e3-f59d-4f8f-8978-373b0dd7bdc4)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f48c122b-ba82-4ffc-9380-06ba940eb063)

=> I see that I have permission to read the catalina.out file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4abbd47a-477f-49fc-abe5-c764ca095c91)

=))))) It's too long. And most of all, I don't know what to do with it. so I will look at localhost first
### localhost

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/474c2f0b-bf0a-4dff-9e7a-926a27058279)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e3a0440c-7931-40f5-8db1-8e51f001df04)

I read catalina.out with the keyword "Super user authentication token:"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2391bfdd-13f7-4c1e-b803-732becd7ecf3)

I tried several times and found the correct authentication - "8947768120969038085"

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9852b0d1-4d21-4f69-be92-1d4b929a927f)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eade8e1b-c41a-43fd-9b13-aa866da7c2be)

Click the " Create build cofiguration" button

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/746fdacb-566e-4599-ab64-b2c2481e0c43)

Still click the "Manually" button

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a922e255-e844-4cc9-882f-59b865334cd6)

Skip  New VCS Root

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f5b9775c-65b1-45d5-80a0-7f73dda43dc8)

Then click "Build Steps" button and choose Python

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/304f79ac-c41b-4d83-a81c-8871220564aa)

Choose " Custome Script" and then I go to revshells.com 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/009c6c73-f6bc-408b-9b30-1644aa239762)

I copy from the "import socket..." paragraph and remove the comma at the end
<br>
Finally,
<br>
I use ```nc``` and click the run button

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/872f848f-0121-4233-9ca0-e9ace17a859c)


![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/94d57cc7-bc7f-438c-a8d5-175fbf33527a)

=> root.txt
## Done!!!
Thanks for reading. Bye!

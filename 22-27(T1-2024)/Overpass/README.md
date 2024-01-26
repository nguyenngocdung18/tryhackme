Link room: https://tryhackme.com/room/overpass
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/1de87d1e-eef3-4b9b-9a90-ca6aad23e878)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7e9cacdd-5a9d-470c-a00a-97fb0472f5a2)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/84d286da-a876-46f7-bb85-90ea9bfc5629)
## view /admin
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e8557443-5167-4585-a38e-8f6cec74e8f8)

I see the login form but the hint is said that it's top 10 OWASP and don't bruteforce.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ad6aa721-deb1-4791-8eba-50e8e62b597f)

## view page source
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/584379dc-a05a-4363-b961-b15bd9c9abcd)

I see login.js excuted with java script code .Look at this!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2e5db0e7-43e0-4c97-bc17-f84cc1f2c142)

=> Maybe it's Insecure Deserialization (for Cookies) on top 10 OWASP
# EXPLOITING
I can set cookies in 2 ways
## Storage in Devconsole
In filter item, I add item and change : ```Name : SessionToken``` and ```Value: /```
         
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9aefa3c8-a1e7-4803-b7c7-906376b95e44)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f0748c53-bee2-432a-91f0-7250aae770be)

=> I get private key to connect ssh server for user james

OR
## Console in Devconsole
using command:  ```Cookies.set("SessionToken", "myCookieValue")``` and run it.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4093c018-788b-429b-a584-757af40ea16c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/cb7fd283-d585-4b6e-9792-44df0a57ab0f)

## using john the ripper
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/add44d2d-ee58-4d46-a996-5cb74e4c7b7b)

=> I receive passphrase for key 'id_rsa': james13

## connect to ssh server
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/26ccb463-fa8b-48e1-894f-b11d79effb78)

=> Successfull!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f89fcb23-af70-479d-a69f-44ab617ec9a3)

=> user.txt

# PRIVILEGE ESCALATION
I look at todo.txt But it doesn't seem very useful

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0d5ec9ab-c041-4096-9aad-47e340272937)

I try ```sudo -l``` command but I don't know password for user james

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/14e801b2-3a2b-44d4-9bc4-d8de1e8cc6cd)

So I look at /etc/crontab file
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/05c1076f-47b7-4d55-b560-b284b814dd12)

I see the command ```curl``` executed by bash.Hmm... If so then maybe I can get the reverse shell by fixing the buildscript.sh file.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c808d2c4-639c-4a08-83e0-f9b4073a6b9c)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8a3a0c18-da89-472d-8fb3-7f64c9173c81)

I fix /etc/hosts file 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/81a2814e-728e-4364-8df5-d4c815178c1b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/44c855d3-355e-4f9c-9ce0-84a6124ea4e5)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/8a1b833e-a32f-424b-9b54-9d4acc197f9f)

Looks like the preparations are done. Now I just need to upload the file and I'm done

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a5f4fa51-ff57-4f74-9d67-2cd44aee4082)

I use the command ```wget```.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6aff37c8-62b0-4f62-8142-d11fd3342c16)

Along with that I also use netcat
 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/daa6419a-f57c-4015-b5e3-756200444908)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/29fd3745-8dec-47ca-84d9-b13cca4b27b4)

=> Uploaded!!!

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/fb97ef66-fd48-4324-8d8b-d4941ca28054)

=> root.txt
## Done!!!
Thanks for reading. Bye!

Link room: https://tryhackme.com/room/anthem
# ENUMERATING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/69f0a02b-e763-4d5b-a89a-c78edcd760ad)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/701ab3c2-003c-4a23-9b2b-1d4f519ebf2c)
## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e4e77162-d585-41e0-a506-d787771e8273)

## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/6e6f40b1-c24b-43dd-8e4e-31dbcdee70eb)

## view page source
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/4bdad611-9500-44a9-ac91-d995e4f187b5)

=> THM{G!T_G00D}

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/524d4f59-47e2-4bc0-a49d-751cfa10fc0f)

=> THM{L0L_WH0_D15}

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/db319ee0-0e58-4eaa-9eaf-ddf960948f5a)

=> domain: anthem.com
## view page source blog "We are hiring"
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eb0227f6-2af9-45be-9645-a2f8faf78bf4)

=> THM{L0L_WH0_US3S_M3T4}
## view page source blog "A cheers to our IT department"
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d8f13fc0-1498-4a65-a633-66b307e11536)

=> THM{AN0TH3R_M3TA}
# EXPLOITING
## /robots.txt
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/90eecc51-4f10-4398-9c6a-65946d6bd569)

=> possible password: UmbracoIsTheBest!
## search on google
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/a367ae1b-b1f0-4aea-b663-f2d12ee5333a)

=> Solomon Grundy

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/632c87ae-ff9c-498e-a2fa-23baa0e669de)

=> Hmm Jane Doe has the email as JD@anthem.com =))))) So, Solomon Grundy may have  email as SG@anthem.com haha..
## connect to remote desktop
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/d2607cce-c816-4bf9-8d42-a433a45049bc)

=))) but username is incorrect. Then I fixed it with the username "SG" as follows: ```-u SG``` => Logged in successfully

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/74bfeb3f-9edb-4ab5-b80e-6408964f7cd7)

=> user flag: THM{N00T_NO0T}
# PRIVILEGE ESCALATION
Because The hint refers to hidden files. So, I will show it by file explorer options (Remmeber to change view by: large icon to see app)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/30bc8e21-e40a-410e-a4a1-aaf5a3def65b)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e75b2b12-a036-4dcc-ae7e-af8aeb288845)

And I find restore.txt but I don't have permission to read it
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/51eb3e12-9eab-40b5-8a2e-8339448f0206)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/80372ece-5b5c-4eca-ab1f-1bb230445a58)

hmmm then I just need to add permissions in the security tab

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e19e4667-129f-41fe-a389-50780bbe4df8)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/eeba19d5-80bb-4766-95ac-6f9b866de6df)

After I go to Administrator directory and enter the previously obtained password.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3a5726d4-951f-4d76-88ba-fd17bfb6a91e)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9786d053-c374-4034-a39b-94e09cc12c28)


## Done!!!
Thanks for reading.Bye!

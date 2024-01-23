Link room: https://tryhackme.com/room/githappens
# SCANNING
## using nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b2a240d6-7d40-4d44-b7d6-da1e9fceb1e3)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/475cd44e-e801-471d-92c2-9e743602c00e)

## using ffuf
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/66289891-4657-4e02-b6f0-b6c511490adf)

# EXPOLITING
## /.git
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/14ca4617-bc4c-459a-8ae0-c2810924df90)

## /.git/HEAD
when I visit this URL it downloads 1 HEAD file

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c1ed8904-7c43-4ee6-abca-00bbb962c394)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9a390eb8-a422-44a0-9c4c-e6a004bc9de9)
## /.git/refs/heads/master
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3039bc06-b6cf-4690-9dc3-06153793d078)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/65414c79-8e7d-494c-ba74-4c1d68835565)

hmm... I get a string and I can't crack it. So I go to github and download GitTools.

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/17a81a64-0ce2-4e86-b53f-faff61c5e404)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/100e13a2-d5d1-4f7c-87c2-c04151531160)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/3b0b966a-ff5e-4613-878e-d4bbc73374db)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/b6eb9a44-1b66-4d20-8f82-57b97bea1891)

Now , I go to /GitHappens and use ```git log``` command

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/2d251431-0680-4324-af32-1f063f456649)

I see many commits but the line "Made the login page, boss!" caught my attention again

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/c4c261b9-6e79-4c7c-b056-0a1b19f057a6)

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ac5c3816-ec3e-4447-9a37-a09c0b0d96b4)

Press the Enter button until the end. I see the script code

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f7874e6a-e0cb-4bcd-b829-24e26f57a616)

super secret password: Th1s_1s_4_L0ng_4nd_S3cur3_P4ssw0rd!
## Done!!!
Thanks for reading.Bye!

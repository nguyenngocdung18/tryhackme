# SCANNING
## use  nmap
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/57f6d3da-a171-4857-a445-1deaaca9f1b2)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f5a4440f-59c3-4d14-98b6-deb188211c14)

## use gobuster
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/9fa50e70-4ccc-4539-b926-c9798d1b469d)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e298d75f-268f-498c-820d-55b25f3a1484)

oh , robots.txt
## view web
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/abece35e-43ab-4e04-b9ab-41996734cd96)
=> view page source

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/e77327a7-a676-42bc-b420-618883de50d0)

see username: R1ckRul3s
and see robots.txt . I see Wubbalubbadubdub => maybe password 

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/bcb55f93-5bb6-4a16-a402-620ec32cb6cd)
# EXPLOITING

![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/0b52f438-efae-49ca-a738-d778cec56ece)
=> Logged in successfully
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/7d400f50-65bb-45a6-a2a4-87c1c720b728)

## checking 
hmm... I tried sudo -l
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/ec3830cd-6de5-456a-961f-6342fae3d387)

=> nice! i can run all with sudo

## find
Now, I try viewing each file
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/86449407-6ac3-476a-aac1-b2c31471ba6a)

=> the first ingredient: mr. meeseek hair

Continue viewing other files
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/846d3688-dc6b-4d82-9e20-6172c855c9f1)
hmm... 
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/429b431a-740d-4ba1-b5d3-51ab306da969)

=> i see rick and ubuntu

View rick and i find kìn cha nà =)))) the second ingredient
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/99afd9a2-e8fd-4806-80ff-2c045f27de54)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/246515ca-e796-4e58-947f-f235bf2b4125)
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/f43432dc-2f57-463e-a0b1-75f11ebfff4a)

=> the second ingredient: 1 jerry tear

Continue viewing ubuntu
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/435cce5f-8be5-4496-a1d5-82881db54511)

Use less to view each file. Luckily, right in the first file. We have found the third ingredient
![image](https://github.com/nguyenngocdung18/tryhackme/assets/134156226/368044f9-a5b0-431c-a44c-1dfd8f0e4709)
=> the third ingredient: fleeb juice
## Done!!!
Thanks for reading. Bye!

Here I will list the privilege escalation techniques that I know
# 1. Account Manipulation
## SSH Authorized Keys
- using private key to connect ssh server.
- 
# 2. Abuse Elevation Control Mechanism 
## 	Sudo and Sudo Caching
- ```sudo -l``` or ```sudo -nl``` to check
## 	Setuid and Setgid
- ```find / -type f -perm -4000 2>/dev/null```
- ```find / -user root -perm -u=s 2>/dev/null```

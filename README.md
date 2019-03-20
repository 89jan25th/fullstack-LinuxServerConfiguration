# Linux Server Configuration
## From Udacity Full Stack Web Developer Nanodegree Program Project: Linux Server Configuration
### Preface
This is a linux server configuration project preceeded by the project Item Catalog (https://github.com/89jan25th/fullstack-item-catalog)

### How to run the program
Connect to http://52.78.93.23.xip.io with Safari or Chrome browser.

### Server setup
1. The server is on Amazon Lightsail
* name: my-udacity-project
* specification: 512 MB RAM, 1 vCPU, 20 GB SSD
* O.S.: Ubuntu
* Location: Seoul, Zone A (ap-northeast-2a)

2. UFW status
2200(SSH), 80(HTTP), 123(NTP) are allowed.
```
grader@ip-172-26-0-162:~$ sudo ufw status
Status: active

To                         Action      From
--                         ------      ----
2200                       ALLOW       Anywhere                  
80                         ALLOW       Anywhere                  
123                        ALLOW       Anywhere                  
2200 (v6)                  ALLOW       Anywhere (v6)             
80 (v6)                    ALLOW       Anywhere (v6)             
123 (v6)                   ALLOW       Anywhere (v6)   
```

3. SSH setup
* grader's SSH private key locates at the following path:
```
~/.ssh/authorized_keys
```

* grader has the sudo access.

* /etc/ssh/sshd_config setup
Password authentification is set to no to prohibit password login.
```
# Change to no to disable tunnelled clear text passwords
PasswordAuthentication no
```

Root login is prohibited as below.
```
# Authentication:
LoginGraceTime 120
PermitRootLogin no               
StrictModes yes
```# fullstack-LinuxServerConfiguration

What is Fail2Ban used for?

>Fail2Ban is a log-parsing application that **protects Linux virtual server host against many security threats, such as dictionary, DoS, DDoS, and brute-force attacks**. It works by monitoring system logs for any malicious activity and scanning files for any entries matching identified patterns.

### Install :
````bash
 foo@bar:~$  sudo apt-get install fail2ban
````

### Start :  
````bash
 foo@bar:~$  sudo service fail2ban status
````

If u enter the password to many times and the service block your ip, u can stop the service to reload 
### Stop :  
````bash
 foo@bar:~$  sudo service fail2ban stop   
````

### Config :  
````bash
 foo@bar:~$  sudo nano /etc/fail2ban/jail.conf
````

The most important is;
+ Bantime: the time that the user was ban
+ Port: the port where the service will working
+ MaxRetry: the number of times that the user retry the password
+ FindTime: Time to wait for each counts of retry
+ Enabled : Can be true or false 

## Logs:

````bash
 foo@bar:~$  sudo nano /var/log/fail2ban.log
````

### Start service:
````bash
 foo@bar:~$  sudo systemctl enable fail2ban.service
````

````bash
 foo@bar:~$  sudo systemctl start fail2ban.service
````
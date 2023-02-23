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
 foo@bar:~$  nan
````
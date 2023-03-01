# How to open ssh 22/TCP port using ufw on Ubuntu/Debian Linux]
 
## Open SSH port using ufw [~]

* The syntax is as follows to open ssh port using ufw command:  
````bash
 foo@bar:~$  sudo ufw allow ssh
````

* OR  
````bash
 foo@bar:~$  sudo ufw allow 22/tcp 
````

* One can add the comment as follows:  
````bash
 foo@bar:~$ ufw allow 22/tcp comment 'Open port ssh tcp port 22'`  
````

* If you are running ssh on TCP port # 2222, enter:  
````bash
 foo@bar:~$  ufw allow 2222/tcp` 
````

## Allowing SSH connections +

In this example, I am going to configure my server to allow incoming SSH connections but only from IP address 192.168.1.100 and sub/net (CIDR) 192.168.2.0/24:  
````bash
 foo@bar:~$  sudo ufw allow from 192.168.1.100 to any port 22   $ sudo ufw allow from 192.168.2.0/24 to any port 22 proto tcp`
````
  
Verify it:  
````bash
 foo@bar:~$  sudo ufw status
````

Status: active
 
To                         Action      From
--                         ------      ----
22/tcp                     ALLOW       192.168.2.0/24

## Remove Connections -

 Display ufw firewall rules, run:
````bash
 foo@bar:~$  sudo ufw status numbered
````

 Remove a ufw firewall rule by rule number:
````bash
 foo@bar:~$  sudo ufw delete 3
````

 Another option to erase a firewall rule is to run:
````bash
 foo@bar:~$  sudo ufw delete allow 22/tcp
````



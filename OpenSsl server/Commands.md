##                           Service Commands 
* Stop service
````bash
 foo@bar:~$  sudo systemctl stop ssh.service
````
* Start service
````bash
 foo@bar:~$  sudo systemctl start ssh.service
````
* Restart service
````bash
 foo@bar:~$  sudo systemctl restart ssh.service
````
* Reload service
````bash
 foo@bar:~$  sudo systemctl reload ssh.service
````
* Conectarse al servidor Remote
````bash
 foo@bar:~$  ssh dolphin@dolphin-desktop@<Public IPV4>
````
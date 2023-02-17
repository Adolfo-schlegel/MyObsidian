# instalar

 
````bash
 foo@bar:~$  sudo apt update  
  oo@bar:~$  sudo apt upgrade
````

* Sudo apt-get install openssh-server
````bash
foo@bar:~$ Sudo apt-get install openssh-server
````

* Habilitarlo en el system
````bash
 foo@bar:~$ sudo systemctl enable ssh --now
````

* Verify that ssh service running
````bash
 foo@bar:~$ sudo systemctl status ssh
````

* Saber la direcciones de ip
````bash
 foo@bar:~$ ip a
````

* Cambiar direccion de ip para usar la ip estatica de la computadora
````bash
 foo@bar:~$  sudo nano /etc/ssh/sshd_confi
````

* Saber mi hostname
````bash
 foo@bar:~$ hostname -I
````

* Saber nombre
````bash
 foo@bar:~$ whoami
````

### Configure firewall and open port 22
You must configure the Ubuntu Linux firewall called ufw. Here is how open or allow port 22 when using ufw on Ubuntu #ConfigFirewall

````bash
 foo@bar:~$  sudo ufw allow ssh  
 foo@bar:~$  sudo ufw enable  
 foo@bar:~$  sudo ufw status
````

* Conectarse al servidor
````bash
 foo@bar:~$  ssh dolphin@dolphin-desktop@192.168.1.255
````

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
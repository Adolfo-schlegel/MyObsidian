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

## Localhost Connection
* Conectarse al servidor
````bash
 foo@bar:~$  ssh dolphin@dolphin-desktop@192.168.1.10
````

## Remote Connection
Para conetctarte de forma remota a tu servidor que esta corriendo sshd, necesitas abrir un puerto en tu router. Normalmente en las configurariones del router existen 2 opciones; 

$$Port Forwarding$$**Port forwarding allows remote computers, located on the Internet, to connect to a specific computer or service within a private local area network (LAN)**. Port forwarding rules are set on routers or other network devices that act as an Internet gateway for other computers in a local network.![[PortForwardingRuleSSH.png]]$$ Remote Conection $$
Allow the remote connection to the computer but befeore you need configure a forward connection with an specific computer/local ip

![[PortForwardingRuleSSH.png]]






* Conectarse al servidor Remote
````bash
 foo@bar:~$  ssh dolphin@dolphin-desktop@<Public IPV4>
````



## Service Commands 
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
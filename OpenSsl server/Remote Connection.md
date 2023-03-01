
>Para conetctarte de forma remota a tu servidor que esta corriendo sshd, necesitas abrir un puerto en tu router. Normalmente en las configurariones del router existen 2 opciones; 

$$Port Forwarding$$
![[PortForwardingRuleSSH.png]]

Port forwarding allows remote computers, located on the Internet, to connect to a specific computer or service within a private local area network (LAN)**. Port forwarding rules are set on routers or other network devices that act as an Internet gateway for other computers in a local network.

External host will accept all ip from the out side world, so we 


$$ Remote Conection $$

![[RemoteAccesSSH.png]]
Allow the remote connection to the computer but befeore you need configure a forward connection with an specific computer/local ip

* Conectarse al servidor Remote
````bash
 foo@bar:~$  ssh dolphin@dolphin-desktop@<Public IPV4>
````



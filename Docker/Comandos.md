*Para descargar una imagen
````bash
foo@bar:~$ Pull mysql
````

*Para ver las imagenes 
````bash
 foo@bar:~$ Docker Images
````

*Para descargar la imagen/instalador en un docker
````bash
 foo@bar:~$ Docker run hello-world
 ````


#Ejemplo -> Mysql

*Para desplegar una imagen de docker default
````bash
 foo@bar:~$ Docker run -e MYSQL_ROOT_PASSWORD=adolfo123 --name mymysql mysql 
 ````

En este caso creamos un usuario en sql solo para un contenedor

*Para ejecutar programas de docker en modo interactivo, osea para meterte al contenedor y ver las version de mysql que esta corriendo 
````bash
 foo@bar:~$ Docker exec -it mymysql bash
 ````

Esto nos abrira una consola dentro de un sistema linux dentro del contenedor

*Para hacer login en mysql
````bash
 foo@bar:~$ mysql -u root -p adolfo123
 ````

En el caso de querer abrir otra terminal para crear otro usuario mysql podemos hacer lo siguiente:

*Para correr desplegar mysql con otro usuario
````bash
 foo@bar:~$ Docker  run --name MiOtraBaseDeDatos -p 7777:3306 mysql -e MYSQL_ROOT_PASSWORD=adolfo123
 ````

*Para ver todos los contenedores que se estan ejecutando
````bash
foo@bar:~$ Docker ps
````


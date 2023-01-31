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

<!-- OL -->
1. Pull mysql
2. Docker run -e MYSQL_ROOT_PASSWORD=adolfo123 --name mymysql mysql 

En este caso creamos un usuario en sql solo para un contenedor

*Para ejecutar programas de docker en modo interactivo
````bash
 foo@bar:~$ Docker exec -it mymysql bash
 ````

Esto nos abrira una consola dentro de un sistema linux dentro del contenedor

*Para hacer login en mysql
````bash
 foo@bar:~$ mysql -u root -p adolfo123
 ````
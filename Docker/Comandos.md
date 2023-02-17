*Para descargar una imagen
````bash
foo@bar:~$ Pull <image name>
````

*Para ver las imagenes 
````bash
 foo@bar:~$ Docker Images
````

*Para desplegar un contenedor con desde una imagen
````bash
 foo@bar:~$ Docker run <image name>
 ````

*Para ejecutar programas de docker en modo no interacitvo
````bash
 foo@bar:~$ docker exec -it <container name>
 ````

*Para ver todos los contenedores que se estan ejecutando
````bash
foo@bar:~$ Docker ps
````

*Remove container
````bash
foo@bar:~$ Docker rm <id_container>
````

*Containers activos
````bash
foo@bar:~$ Docker ps -a
````

*Correr container
````bash
foo@bar:~$ Docker start <container name/id>
````

*Correr container y que muestre informacion
````bash
foo@bar:~$ Docker start -i <container name/id>
````

*Stop container
````bash
foo@bar Docker stop <container name/id>
````

*Remove a image
````bash
foo@bar:~$ Docker rmi <id_image>
````

*Build image from DockerFile
````bash
foo@bar:~$ Docker bild -t <name image> .
````
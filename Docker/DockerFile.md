¿Que es DockerFile?
El archivo DokerFile es un arhcivo de configuracion de doker, sirve para crear una imagen de nuestro proyecto, es la misma imagen que se encuentra en los paquetes oficiales de https://hub.docker.com.

¿Para que sirve?
Sirve para poder pasarselo a nuestros amigos asi ellos pueden tener la misma configuracion de nuestro proyecto y no tengan que descargarse mysql, node, mongodb por separado, ya que dentro del archivo tambien podemos agregar que paquetes queremos instalar de nuestro proyecto

.dockerignore
Se pueden ignorar carpetas que no se desean agregar, por ejemplo; las carpetas bin y obj en c# o la carpeta node_modules en node son carpetas que se generan automaticamente donde se instalan las dependencias que tenemos, por ende es mejor ignorarlas ya que le vamos a decir a docker file que instale esas dependencias por nosotros

Este archivo copia los archivos necesarios para le despliegue de la imagen de docker, tambien se indican los puertos en que va a correr y las paltaformas que va a utilizar 


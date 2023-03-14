# instalar

 
````bash
foo@bar:~$  sudo apt update  
Foo@bar:~$  sudo apt upgrade
````

* How to install
````bash
foo@bar:~$ Sudo apt-get install nginx
````

 Drirectory
````bash
foo@bar:~$ cd /etc/nginx/
````

Los directorios sites-available y sites-enables son para tener mas ordenados nuestros sitios

Dentro de sites-available vamos a tener configurados nuestros sitios, vamos a poder tener configurados nuestros virtual hosts, ademas nos sirve para posteriormente moverlos a sites enables para activarlos y desactivarlos sin necesidad de borrar todos los archivos de enables y tener que hacer un git clone otra vez pq es una paja

### Crear un sitio dentro de sites-available:

1. Entramos dentro de /etc/nginx/sites-available
2. Creamos un archivo cp default site.utilities.com 
3. Modificamos el archivo con nano site.utilities.com
4. Modificamos la linea server_name _; por linea server_name  site.utilities.com;
5. Root /var/www/html va a ser donde se encuentre nuestro contenido html del sitio, lo vamos a modificar para luego crear una carpeta con el nombre de nuetro site  /var/www/site1
6. En el mismo archivo modificaremos las dos lineas listen 80 y le quitaremos el #DefaultServer, nos quedara algo como;  -> listen 80;
7. (Ctrl + x ) para guardar
8. Nos vamos a sites-enables podemos ver que hay un link simbolico, es basicamente un puntero a otra direccion de memoria, o facilmente se puede interpretar como una #accesodirecto de #windows
9. Para crearlo vamos a hacer un ln -s ../sites-available/site.utilities.com

10. Para recargar nginx y que tome nuestra nueva configuracion
````bash
foo@bar:~$ nginx -s reload 
````

11. El ultimo paso es configurar el archivo host de ubuntu para que haga un bind de nuestra direccion ip con el nombre de dominio que le acabamos de asignar 
12. En /etc/hosts accedemos y al lado de nuetra ip ponemos el nombre de sitio, algo asi como 0.0.0.00 pelado.tienda.com

## Comandos utiles para nginx ~~>

````bash
foo@bar:~$ Sudo systemctl enable nginx
````

````bash
foo@bar:~$ Sudo nginx -v
````
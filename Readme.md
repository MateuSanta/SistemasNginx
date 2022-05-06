# Instalación y configuración del servidor web Nginx: Virtual Hosts

Para la instalación y configuración de nginx utilizaremos una máquina virtual de ubuntu.

Primero de todo usaremos el comando:

''sudo apt install nginx''

Una vez instalado, iremos a la carpeta /var/www/ y crearemos 2 carpetas llamadas carpeta 1 y carpeta2.

![ng1](https://user-images.githubusercontent.com/91744614/167161620-9c042e63-3657-45d8-9b95-42c5fce230a8.PNG)

Estas carpetas se utilizarán para meter los html cuyos vamos a hostear.

Para obtener los html usaremos el comando, una vez situados en la carpeta en la que queremos el archivo.

''sudo wget url''

![sudoawget](https://user-images.githubusercontent.com/91744614/167161111-744ea361-e7fa-4c42-827d-fb50020c94ba.PNG)

Repetiremos el proceso para el otro archivo.

Nos dirigiremos a la carpeta sites-avaliables de nginx y copiaremos dos veces el archivo default:

![cpdefault](https://user-images.githubusercontent.com/91744614/167162117-eb2b4eb1-13ee-4168-9db6-b08b35e7fb90.PNG)

Una vez copiados los modificaremos cambiando el puerto a 80 , el root, /var/www/carpeta1 y /var/www/carpeta1 que es donde tenemos los archivos guardados, y el server name.
![carpeta1subdominio](https://user-images.githubusercontent.com/91744614/167162534-804f59bf-998e-4336-8ab3-5e169bb75eff.PNG)
![carpeta2subd](https://user-images.githubusercontent.com/91744614/167162550-29bc270d-6b6b-4e85-9a64-22a8e4b8db05.PNG)

Ahora nos dirigiremos en sites-enabled y copiaremos los dos archivos que hemos creado en sites-avaliable.

![sitesenabled](https://user-images.githubusercontent.com/91744614/167171420-0e9f4e34-bf2a-4c64-b9e8-3b08eadb6023.PNG)

A continuación, iremos a /etc/hosts y añadiremos las dos direcciones:

![hosts](https://user-images.githubusercontent.com/91744614/167166977-80a9a2a9-de15-4c8d-ac1b-cc8206083add.PNG)

Cambiaremos el nombre de los dos html a index.html:

![cambiarnombre](https://user-images.githubusercontent.com/91744614/167167307-a383d659-44f2-471b-b53d-3edf78bbc353.PNG)

Para finalizar en la máquina virtual utilizaremos el comando:

''sudo nginx -s reload''

Como lo hemos hecho en una máquina virtual, tendremos que cambiar el archivo hosts en la computadora local.

En windows, abriremos un bloc de notas como administrador, y añadiremos las dos direcciones que nos interesan, guardando el archivo en C://Windows/System32/drivers/etc/:
![blocdenotashosts](https://user-images.githubusercontent.com/91744614/167169505-ddf7a5da-bfa3-401f-b4d7-4af17049a9fe.PNG)

Ahora comprobamos que funcionan las páginas:

![cakejuego](https://user-images.githubusercontent.com/91744614/167169703-4c0e9f9a-0016-4fb0-8e7a-39d9626fc0b1.PNG)

![babyindex](https://user-images.githubusercontent.com/91744614/167169726-e5ee9e81-6967-419b-8ed5-7b43f48b3351.PNG)

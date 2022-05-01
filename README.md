# COMO INTALAR DOCKER EN ALPINE

# 1.Instalar el  software Alpine
(El primer paso, en teoria seria instalar el VMB pero, como no hay mucho y despues habra que cambiar cosas, ese paso, lo salto.)

* 1.1 Para instalar el Alpine nos iremos a la pagina oficial del sistio web y en downloads, iremos a a la opcion de standard y descargaremos la opcion de 86x64.

![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

# 2.Instalar el  software (Alpine) dentro de Virtual Box

* 2.1 Cuando tengamos el Alpine ya descargado, nos iremos a Virtual Box y alli, lo primero sera ir a la opcion de "nueva".
* 2.2 El nombre le pondremos Alpine1, la ruta por defecto, el tipo sera "Other" y la version sera "Other/Unknown (64bits)".
* 2.3 Despues le pondremos la RAM, que nos bastara con 1024 MB.
* 2.4 Luego el disco, le daremos a "crear disco virtual ahora".
* 2.5 El tamaño "reservado dinamico".
* 2.6 Le pondremos un espacio de 2 GB
* 2.7 Eso habria sido la configuracion para tener el disco, ahora habra que meter el archivo de instalacion dentro del disco
* 2.8 Nos iremos dentro del "alpine1" y la damos a configuracion, almacenamiento y dentro le vermeos un disco vacio y cuando le demos pulsaremos el archivo que nos hemos descargado
* 2.9 Luego en el mismo sitio de la maquina, iremos a "red" y seleccionamos la opcion de Adaptador puente.


# 3. Instalacion de Alpine

* 3.1 Cuando iniciemos el isntalador, nos pedira que nos registremos con un usuario, pero como no tendremos, iremos con el root.
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/8381d6af8ebe99a580fb7c43cdb21e1423881ece/2.PNG)


* 3.2 Cuando entremos ya con el root,ejecutaremos el comando "setup-alpine"
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/75950f58077d1908025bd96cb26e9b8416460707/3.PNG)

* 3.3 Le daremos al enter, y nos pedire que seleccionemos el idioma de teclado, y ponemos "es"
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/58c1a5cdba2f5678112950501607629a8b94dd40/4.PNG)

* 3.4 Despues nos pedira que pongamos un localhost, le pondremos "node1"
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/93f97e93228f4f867906a579ca64e818141b5df6/5.PNG)

* 3.5 Nos dira si queremos poner una ip tanto en eth o dhcp, le damos enter, que es como omitir

* 3.6 Despues de darle a nter, el siguiente paso sera darle una contraseña, le ponemos una contreña y confirmamos otra vez


* 3.7 Luego elegiremos la zona horaria, damos al ? y nos saldra una lista y seleccionamos "Europe" y despues que Cuidad le ponemos "Madrid"

![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/d4585837c30c0af706a03f44997bf6ddfd084b99/6.PNG)
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/531555ea680b92d21061388c5ddbb924291e677c/7.PNG)

* 3.8 En las siguientes dos opciones las dejamos por defecto, y le damos a enter.
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/61522ae416e501703d329a02639e868e97ea91a5/8.PNG)

* 3.9 Ahora nos saldra un listado de archivos y nosotros le damos a enter que es el 1 por defecto
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/58a1b5213965bf21dc48737eca1d2a7c6292a1a1/9.PNG)

* 3.10 En la siguiente opcion pondremos la que viene por defecto con el openssh


* 3.11 Ahora nos pedira que disco queremos utilizar y le pondremso el "sda" y despues nos pedira como queremos usarlo y pondremos "sys"
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/f447c3e792b63e4c3c6a2362188ba5084a2c49b8/10.PNG)

* 3.12 Justo despues no pedira si queremso continuar con el disco le diremos que si
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

* 3.13 Nos pedira reiniciar y los reiniciamos poniendo "poweroff"
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

* 3.14 Ahora lo volveremos a iniciar, depsues cuando entremos nos iremos a un editor de repositorios, y ponemos esto vi /etc/ssh/sssh_config
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

* 3.15 Cuando le demos a enter, ahora nos iremos abajo del todo y vamos a la opcion de "PermitRootLogin" le quitamos el # y depsue borramos lo que tiene delante suyo y los sustituimos por "yes" 
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

* 3.16 Salimos con "esc :wq" y despues ponemos ssh service restart
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

* 3.17 Luego nos iremos a nuestro powershell y intentaremos conectarnos a nuestro alpine desde ahi,  desde Power shell ya conectados, pondremos "vi /etc/apk/repositories"
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

* 3.18 Justo dentro quitaremos la #  a todos las frases que nos poene ahi, y despues con el "esc :wq" 
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

* 3.19 Y ahora añadiremos el docker poniendo "apk add docker"
![Alpine](https://github.com/AlejandroRocaMateu/Docker_Alpine/blob/3feb94a8ed77b50e17ca2a5a2c7e6d7b15d6acdc/1.PNG)

* 3.20 Y ahora para probar que funciona pondremos el comando "docker version" y si nos ha funcionado nos saldra toda la informaciondel docker.


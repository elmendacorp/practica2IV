# Practica 2 IV "La Jaula"
He aquí los pasos seguidos para la realización de la practica.
* 1º creación de la imagen:
  `sudo debootstrap --arch=i386 quantal /home/jaulas/quantal/ http://archive.ubuntu.com/ubuntu`
* 2º acceso y configuración
  usamos chroot para acceder al directorio de instalación, en el cual podemos instalar los paquetes 
`apt-get install apache2`
`sudo service apache2 start`
`sudo apt-get install php5 libapache2-mod-php5 php5-cli php5-mysql`
`mount -t proc proc /proc`
pertinentes, en este caso LAMP
* 3º comprobación:
  en mi caso he editado el archivo por defecto de apache, poniendo un simple hola mundo.
* 4º la comprobación de que la jaula esta aislada es que el gestor de paquetes no identifica los paquetes pre-   instalados en el sistema anfitrión, lo que nos indica que el espacio de nombres es distinto.


## Capturas del proceso, y demostración.
* Como podemos observar en las capturas se tiene la independencia de la maquina anfitriona, lo curioso es que no se disponen accesos a los adaptadores de red, pero a la hora de montar apache este no coge el de la anfitriona, supongo que antes tendríamos que configurar un virtual aparte.

![](https://github.com/elmendacorp/practica2IV/blob/master/img/1.png?raw=true)
![](https://github.com/elmendacorp/practica2IV/blob/master/img/2.png?raw=true)
![](https://github.com/elmendacorp/practica2IV/blob/master/img/3.png?raw=true)
![](https://github.com/elmendacorp/practica2IV/blob/master/img/4.png?raw=true)
![](https://github.com/elmendacorp/practica2IV/blob/master/img/5.png?raw=true)
![](https://github.com/elmendacorp/practica2IV/blob/master/img/6.png?raw=true)
![](https://github.com/elmendacorp/practica2IV/blob/master/img/7.png?raw=true)
![](https://github.com/elmendacorp/practica2IV/blob/master/img/8.png?raw=true)

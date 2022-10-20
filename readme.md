# Pila Lamp en dos niveles

## Creación de repositorio GitHub para el proyecto

Repositorio creado para subir el proyecto.

![](capturas/git.PNG)


## Configuración de Vagrantfile

En el archivo Vagrantfile, crearemos 2 máquinas para crear nuestro Lamp a dos niveles. 
En dicho archivo, usaremos debian11 como SO de nuestros servidores, le asignaremos una IP privada para unirlas entre sí y una IP pública al servidor Web para tener acceso a Internet.
![](capturas/file.PNG)

## Creación de aprovisionamiento

Para aligerar el proceso, crearemos un script para cada máquina de tal forma que ya tengamos todo listo para comenzar la configuración de cada una de ellas.
Script del servidor Mysql: ![](capturas/apmysql.png)

Script del servidor Apache:
![](capturas/apapache.PNG)

## Configuración de las máquinas

### Servidor Web

Dentro del servidor web, tendremos que crear un nuevo directorio dentro de "/var/www/" con el nombre que nosotros elijamos y cambiarle el dueño y grupo al que pertenecen.

![](capturas/apapache.png)



### Servidor Mysql
En el servidor Mysql, importaremos desde el repositorio Github dado en la práctica, una base de datos y la configuraremos para nuestra red. 

![](capturas/creacion de la bbdd.PNG)

En el archivo .conf, cambiaremos la linea de "bind-address 172.0.0.1" por nuestra dirección IP del servidor Mysql.

![](capturas/creacion de la bbdd.PNG)

Para finalizar los ajustes de nuestra base de datos, crearemos un usuario al cual le daremos permisos totales a la BD importada previamente.

![](capturas/3.PNG)

Una vez hecho esto, reiniciamos nuestro servidor Mysql con el siguiente comando:

![](capturas/reseteo.PNG)

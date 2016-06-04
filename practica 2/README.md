# Práctica 2

Cuestiones a resolver de la Práctica 2 : 

1. Probar el funcionamiento de la copia de archivos por ssh

Para probar el funcionamiento de la copia de archivos por ssh muestro la siguiente imagen:



2. Clonado de una carpeta entre las dos máquinas:

Para clonar la carpeta, en este caso la carpeta www de apache pongo el siguiente comando:

´rsync -avz -e ssh maquina1@172.16.83.154:/var/www/ /var/www/´

Donde maquina1 es el usuario de la máquina, y la Ip, la ip del servidor al que se mandará los datos. En la imagen muestro como se traspasan los datos desde la máquina2 a la máquina1.

![imagen](imagen1.png)

A continuación muestros los datos en ambas máquinas

![imagen](imagen2.png)
![imagen](imagen3.png)

3. Acceso sin contraseña para ssh

Primero establezco la contraseña , lo muestro en la imagen :

![imagen](imagen4.png)

A continuación ejecuto ssh-copy-id -i .ssh/id_rsa.pub root@10.211.55.19 y cuando introduzca root@10.211.55.19 no me pedirá contraseña a la hora de entrar en la máquina virtual, tal y como se puede ver en la siguiente imagen.

![imagen](imagen5.png)

4. Establecer una tarea en cron que se ejecute cada hora para mantener actualizado el contenido del directorio /var/www entre las dos máquinas
Para ello me dirijo a /etc/crontab, lo abro con nano, y añado la línea que aparece en la siguiente imagen.

![imagen](imagen6.png)

Como se puede apreciar , añado la ip de la máquina 1 , a continuación muestro en la siguiente imagen el resultado, se puede ver como ha añadido un archivo creado en la máquina 1 en mi máquina 2

![imagen](imagen7.png)













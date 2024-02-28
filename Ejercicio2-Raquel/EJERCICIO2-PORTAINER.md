#	EJERCICIO2-PORTAINER

###	Realizado por Raquel.



**-Instalación de portainer:**

```bash
sudo docker volume create portainer_data
```

![img](./01/clip_image001.png)

```bash
sudo docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data --name portainer portainer/portainer
```

![Texto  Descripción generada automáticamente](./01/clip_image004.gif)



**-Accedemos desde el navegador a http://localhost:9000 :**

![Interfaz de usuario gráfica, Texto, Aplicación  Descripción generada automáticamente](./01/clip_image006.gif)

Contraseña : desarrolloweb.

Ya estamos situados en la interfaz de portainer.

![Interfaz de usuario gráfica, Aplicación  Descripción generada automáticamente](./01/clip_image008.gif)



**-Gestionamos el contenedor.**

Esta es la interfaz de los contenedores:

![Interfaz de usuario gráfica, Aplicación  Descripción generada automáticamente](./01/clip_image010.gif)

Creo un contenedor:

![Interfaz de usuario gráfica, Texto, Aplicación, Correo electrónico  Descripción generada automáticamente](./01/clip_image012.gif)

Y compruebo su correcta creación:

![Interfaz de usuario gráfica, Aplicación  Descripción generada automáticamente](./01/clip_image014.gif)

Eliminamos el contenedor:

![Interfaz de usuario gráfica, Aplicación  Descripción generada automáticamente](./01/clip_image016.gif)

 



**-Operación con redes Docker**

Panel de las redes:

![Interfaz de usuario gráfica, Texto, Aplicación, Correo electrónico  Descripción generada automáticamente](./01/clip_image018.gif) 

Voy a conectar una red a un contenedor nuevo:

![Interfaz de usuario gráfica, Texto, Aplicación, Chat o mensaje de texto, Correo electrónico  Descripción generada automáticamente](./01/clip_image020.gif)

![Interfaz de usuario gráfica, Texto, Aplicación, Correo electrónico  Descripción generada automáticamente](./01/clip_image022.gif)

![Interfaz de usuario gráfica, Texto, Aplicación, Correo electrónico  Descripción generada automáticamente](./01/clip_image024.gif)

Comprobamos que la red ha sido creada correctamente:

![Tabla  Descripción generada automáticamente](./01/clip_image026.gif)

Como se muestra, se comprueba que la ip del contenedor es la misma que la de la red lola, por tanto, se han conectado correctamente.

![Captura de pantalla de computadora  Descripción generada automáticamente](./01/clip_image028.gif)

 

 

**-Operaciones con volúmenes Docker:**

Creo el volumen.

![Interfaz de usuario gráfica, Texto, Aplicación, Correo electrónico  Descripción generada automáticamente](./01/clip_image030.gif)

Creo un contenedor nuevo asociándole el volumen1 creado:

![Interfaz de usuario gráfica, Texto, Aplicación, Correo electrónico  Descripción generada automáticamente](./01/clip_image032.gif)

![image-20240228104317498](../../../snap/typora/86/.config/Typora/typora-user-images/image-20240228104317498.png)

Y lo compruebo:

![Interfaz de usuario gráfica, Texto, Aplicación, Correo electrónico  Descripción generada automáticamente](./01/clip_image034.gif)
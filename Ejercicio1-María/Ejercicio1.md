# Ejercicio 1. Servidor de Bases de Datos

> María Clemente Luengo. 
>

### Crear el contenedor "bbdd" con MariaDB

```bash
docker run --name bbdd -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=prueba -e MYSQL_USER=invitado -e MYSQL_PASSWORD=invitado -d mariadb
```

![image-20240223102110061](./Ejercicio1.assets/image-20240223102110061.png)

### Verificar que el contenedor está corriendo

```bash
docker ps
```

![image-20240223102128088](./Ejercicio1.assets/image-20240223102128088.png)

### Creación archivos index.html y mes.php

```bash
nano index.html
```

![image-20240223102443216](./Ejercicio1.assets/image-20240223102443216.png)

```bash
nano mes.php
```

![image-20240223102550917](./Ejercicio1.assets/image-20240223102550917.png)

```bash
sudo docker run -v /home/linux/Escritorio/DockerTareaEvaluable/Ejercicio1-María:/var/www/html -p 80:80 -d php
```



![image-20240226091237512](./Ejercicio1.assets/image-20240226091237512.png)



### Capturas de pantalla

- [x] Captura de pantalla de acceso al archivo "index.html" desde un navegador.![image-20240226091542006](./Ejercicio1.assets/image-20240226091542006.png)

- [x] Captura de pantalla de la salida del script "mes.php" desde un navegador.

  ![image-20240226091827013](./Ejercicio1.assets/image-20240226091827013.png)

- [x] Captura de pantalla del tamaño del contenedor web después de crear los archivos.

  ![image-20240226092007424](./Ejercicio1.assets/image-20240226092007424.png)

  

- [x] Captura de pantalla y documento donde desde un cliente de base de datos (instalado en tu ordenador) se pueda observar que hemos podido conectarnos al servidor de base de datos con el usuario creado y que se ha creado la base de datos prueba ( `show databases` ). El acceso se debe realizar desde el ordenador que tenéis instalado docker, no hay que acceder desde dentro del contenedor, es decir, no usar docker exec .

​	![image-20240226092614898](./Ejercicio1.assets/image-20240226092614898.png)

![image-20240226094037886](./Ejercicio1.assets/image-20240226094037886.png)

_Mostrar los contendores que estám creados y arrancados_

![image-20240226094409559](./Ejercicio1.assets/image-20240226094409559.png)

_Eliminar contendor con imagen mariadb_

```bash
docker rmi mariadb
```

![image-20240226094720121](./Ejercicio1.assets/image-20240226094720121.png)

---


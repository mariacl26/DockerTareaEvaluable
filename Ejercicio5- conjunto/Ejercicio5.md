# Ejercicio 5. Imagen con Dockerfile - Aplicación Web. 

> María Clemente y Raquel Cabezas. 

Para la realización de este ejercicio es necesario tener una cuenta en Docker Hub.

## Creación inicial del contenedor - documenta los pasos hasta el borrado del mismo

**Creación cuenta en DockerHub**

![image-20240226100619113](./Ejercicio5.assets/image-20240226100619113.png)

**Creación del index.html**

![image-20240226101446325](./Ejercicio5.assets/image-20240226101446325.png)

**Creación del mes.php**

![image-20240226101419005](./Ejercicio5.assets/image-20240226101419005.png)

```bash
docker run -d --name web -p 8000:80 -v /home/linux/Escritorio/DockerTareaEvaluable/Ejercicio5-\ conjunto/:/var/www/html php:7.4-apache
```

![image-20240226101950058](./Ejercicio5.assets/image-20240226101950058-1708939236475-1.png)

![image-20240226102024649](./Ejercicio5.assets/image-20240226102024649.png)



_Entramos al navegador desde el puerto 8000_

![image-20240226102112121](./Ejercicio5.assets/image-20240226102112121.png)

_Salida del script del mes.php_

![image-20240226102203424](./Ejercicio5.assets/image-20240226102203424.png)



***Borrar contenedor***

1. Parar

2. Borrar

   ![image-20240226102424764](./Ejercicio5.assets/image-20240226102424764.png)

   

## Bloque de código con el Dockerfile

```bash
nano Dockerfile
```

![image-20240228103500814](./Ejercicio5.assets/image-20240228103500814.png)

![image-20240228103411327](./Ejercicio5.assets/image-20240228103411327.png)



#### Captura de pantalla y documento donde se vea el comando que crea la nueva imagen.

```bash
docker build -t my-php-web .
```

![image-20240228104020727](./Ejercicio5.assets/image-20240228104020727.png)



#### Captura de pantalla y documento donde se vea la imagen subida a tu cuenta de Docker Hub.

_Inicio de sesión en Docker_

```bash
docker login
```

![image-20240228104715439](./Ejercicio5.assets/image-20240228104715439.png)

_Imagen_

```bash
docker tag my-php-web mariialuenngo/my-php-web
```

![image-20240228104930123](./Ejercicio5.assets/image-20240228104930123.png)

```bash
docker push mariialuenngo/my-php-web
```

![image-20240228105227583](./Ejercicio5.assets/image-20240228105227583.png)

#### Captura de pantalla y documento donde se vea la bajada de la imagen - por parte de otra persona del grupo - y la creación de un contenedor.



#### Captura de pantalla y documento donde se ve el acceso al navegador con el sitio servido
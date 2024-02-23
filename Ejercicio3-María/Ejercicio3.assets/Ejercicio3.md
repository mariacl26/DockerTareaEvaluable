# Ejercicio 3. Contenedores en red: MariaDB y Adminer.

> María Clemente Luengo. 

1. **Crear una red bridge:**  
   
   ```bash
   docker network create redbd
   ```
   
   ![image-20240221105727294](../Ejercicio3.assets/image-20240221105727294.png)
   
2. **Crear un contenedor de MariaDB:**  
   
   ```bash
   docker run -d --name mariadb-container --network redbd -p 3309:3306 -e MYSQL_ROOT_PASSWORD=1234 -v mariadb_data:/var/lib/mysql mariadb
   ```
   
   ![image-20240221105815047](../Ejercicio3.assets/image-20240221105815047.png)
   
3. **Crear un contenedor de Adminer:**  
   
   ```bash
   docker run -d --name adminer-container --network redbd -p 8080:8080 adminer
   ```
   
   ![image-20240221105839402](../Ejercicio3.assets/image-20240221105839402.png)
   
4. **Verificar la conexión entre Adminer y MariaDB:**  
   
   ![image-20240221105913344](../Ejercicio3.assets/image-20240221105913344.png)
   
   ![image-20240221111243212](../Ejercicio3.assets/image-20240221111243212.png)

![image-20240221111430724](../Ejercicio3.assets/image-20240221111430724.png)


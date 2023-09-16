# Api-Rest-Intermedian

| API REST |  SpringBoot | Spring JPA | Spring Security | Hibernate | PostgreSQL | Swagger |

# DOCKER

Como el api se encuentra dockerizada es necesario:

1) Clonar el repositorio especifico de la rama main-security-in-memory-dockerized, se puede realizar con la siguiente linea de comandos:
   
   - $ git clone -b main-security-in-database-dockerized https://github.com/Julian1699/Api-Rest-Intermedian.git
     
3) Una vez clonado el repositorio, se debe abrir una terminal (powershell o git bash) dentro del directorio que contenga el proyecto.
   
4) Ejecutar el comando de docker
   
   - $ docker compose up
     
6) Una vez levantandos los contenedores se procede a realizar lo siguiente:
   
7) Ejecutar el siguiente comando en una terminal git o power shell para entrar en el contenedor de la base de datos:
   
   - $ winpty docker exec -it db-postgres bash
     
   ![image](https://github.com/Julian1699/Api-Rest-For-Learning/assets/114323630/53eeb015-cdb9-4b69-b9ba-6ee624fe0aa7)

8) Ejecutar el siguiente comando en una terminal git bash o power shell para entrar en la base de datos:
   
   - $ psql -U postgres -d tryapi
  
   ![image](https://github.com/Julian1699/Api-Rest-For-Learning/assets/114323630/074eb095-6ac8-44d3-8155-0c47d91e2283)
     
10) Ahora se debe ubicar el archivo "data.sql" que se encuentra dentro del directorio "resources":

   ![image](https://github.com/Julian1699/Api-Rest-For-Learning/assets/114323630/cd4d7162-1776-473d-8ea1-b464836c7097)

7) Tomar los datos que se encuentran allí:

   ![image](https://github.com/Julian1699/Api-Rest-For-Learning/assets/114323630/b3760a93-11d2-4652-b718-beec165e6f73)

8) Pegar los datos en la terminal de la base de datos para insertarlos:

   ![image](https://github.com/Julian1699/Api-Rest-For-Learning/assets/114323630/c7ff47f4-0af8-4672-9e4e-cad3c9add258)

4) Consultar como consumir el API en la ruta generada por el Swagger: http://localhost:8080/swagger-ui/index.html#/

# Configuración de Seguridad:

En este proyecto de Spring Security, se han creado dos usuarios en la memoria que requieren autenticación y tienen diferentes niveles de autorización.

- Primer Usuario (admin):

-Nombre de usuario: admin.

-Contraseña: admin.

-Rol: ADMIN.

Este usuario tiene permisos para realizar todas las operaciones HTTP (GET, POST, PUT, DELETE) de manera normal.

- Segundo Usuario (customer):

-Nombre de usuario: customer.

-Rol: CUSTOMER.

-Contraseña: customer.

El usuario "customer" tiene autorización solamente para realizar consultas a la base de datos utilizando el verbo HTTP GET.

# Ejemplos:

A continuación, se proporciona un ejemplo de cómo llevar a cabo la autenticación en Postman:

![image](https://github.com/Julian1699/Api-Rest-Intermedian/assets/114323630/7a47bceb-4a01-4081-8dbe-f900ed929fbb)

También, se proporciona un ejemplo de cómo llevar a cabo la autenticación en Swagger:

![image](https://github.com/Julian1699/Api-Rest-Intermedian/assets/114323630/525e1c06-9f9c-4af0-b270-80cfee58f8d0)

# API de Productos

Esta API RESTful proporciona una manera de gestionar datos de productos utilizando Spring Boot. Está diseñada para ser utilizada por desarrolladores que necesitan crear, leer, actualizar y eliminar productos.

# La API proporciona las siguientes características:

- Obtener todos los productos: Recupera una lista de todos los productos disponibles en la base de datos.
- Agregar un nuevo producto: Agrega un nuevo producto a la base de datos.
- Actualizar un producto existente: Actualiza un producto existente en la base de datos.
- Eliminar un producto existente: Elimina un producto existente de la base de datos.
- Obtener un producto por ID: Recupera un producto por su identificador único.
- Buscar productos: Busca productos por nombre, referencia o categoría.
- Tecnologías utilizadas

# La API está construida utilizando las siguientes tecnologías:

- Java 17: La versión de Java.
- Spring Boot 3.0.10: Un potente marco de trabajo para construir aplicaciones web basadas en Java.
- Spring Data JPA: Simplifica el acceso y la gestión de bases de datos.
- Swagger: Proporciona documentación interactiva de la API.
- Hibernate Validator: Para la validación de los datos enviados en las solicitudes.
- Lombok: Reduce el código repetitivo.
- Cross-Origin Resource Sharing (CORS): Permite solicitudes entre dominios desde aplicaciones web.

# Documentación

La documentación de la API está disponible en Swagger: http://localhost:8080/swagger-ui/index.html#/

![image](https://github.com/Julian1699/Api-Rest-Intermedian/assets/114323630/2cfe3ae7-b943-49fa-8749-b208f9501bf5)

# Endpoints

Los endpoints de la API son los siguientes:

- PUT /api/v1/product/put/{id}: Actualiza un producto existente.
- POST /api/v1/product/post: Agrega un nuevo producto.
- GET /api/v1/product/search/{search}: Busca productos por nombre, referencia o categoría.
- GET /api/v1/product/id/{id}: Obtiene un producto por ID.
- GET /api/v1/product/all: Obtiene todos los productos.
- DELETE /api/v1/product/delete/{id}: Elimina un producto existente.



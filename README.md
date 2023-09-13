# Api-Rest-Intermedian

| API REST | SpringBoot | Spring JPA | Hibernate | PostgreSQL | Swagger | Docker |

# DOCKER

Como el api se encuentra dockerizada es necesario:

1) Clonar el repositorio especifico de la rama main-dockerized, se puede realizar con la siguiente linea de comandos:
   - $ git clone -b main-dockerized https://github.com/Julian1699/Api-Rest-Intermedian.git
2) Una vez clonado el repositorio, se debe abrir una terminal (powershell o git bash) dentro del directorio que contenga el proyecto.
3) Ejecutar el comando de docker
   - $ docker compose up
4) Consultar como consumir el API en la ruta generada por el Swagger: http://localhost:8080/swagger-ui/index.html#/
   
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

# Book API Client - README

## Descripción

La aplicación **Book API Client** es un cliente REST que permite interactuar con una API externa de libros, específicamente con la API de **Gutendex**, para buscar libros por título, registrar información de libros y autores en una base de datos local, y obtener información sobre autores y libros registrados.

### Funcionalidades principales:
- Buscar un libro por título en la API externa y almacenarlo en una base de datos local si no está registrado.
- Obtener todos los libros registrados en la base de datos.
- Obtener todos los autores registrados.
- Obtener autores vivos en un año determinado.
- Buscar libros por idioma.

## Tecnologías

- **Java**: Lenguaje de programación principal.
- **Spring Boot**: Framework para el desarrollo de aplicaciones Java basadas en microservicios.
- **JPA (Java Persistence API)**: Para la gestión de la persistencia de datos (base de datos).
- **RestTemplate**: Para realizar solicitudes HTTP a la API externa.
- **H2 Database**: Base de datos en memoria utilizada para almacenar la información de libros y autores.

## Requisitos previos

- **Java 17+** (recomendado).
- **Maven**: Para la construcción y gestión del proyecto.
- **IDE** como **IntelliJ IDEA** o **Eclipse** para el desarrollo.

## Instalación

1. Clona el repositorio:

    ```bash
    git clone https://github.com/tu-usuario/tu-repositorio.git
    ```

2. Ingresa al directorio del proyecto:

    ```bash
    cd tu-repositorio
    ```

3. Construye el proyecto con Maven:

    ```bash
    mvn clean install
    ```

4. Ejecuta la aplicación:

    ```bash
    mvn spring-boot:run
    ```

La aplicación debería iniciarse y estará disponible en `http://localhost:8080`.

## Endpoints

### 1. Buscar libro por título
- **URL**: `/books/search`
- **Método**: `GET`
- **Parámetros**:
  - `title`: Título del libro a buscar.
  
  Ejemplo:
  ```bash
  GET /books/search?title=Harry+Potter

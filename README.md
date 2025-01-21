# Foro Hub: API REST para un Foro de Discusión

## Descripción
Foro Hub es una API REST desarrollada como parte de un desafío de backend dictado por Oracle en colaboración con Alura LATAM. Su objetivo es proporcionar una plataforma funcional para gestionar tópicos de discusión, implementando operaciones CRUD y autenticación basada en tokens JWT.

## Tecnologías Utilizadas
- **Java**: Lenguaje de programación principal.
- **Spring Boot**: Framework para el desarrollo de aplicaciones.
- **MySQL**: Base de datos relacional.
- **JWT (JSON Web Tokens)**: Para autenticación y autorización.
- **Insomnia**: Herramienta para pruebas de la API.

## Estructura del Proyecto
- **`src/main/java`**: Contiene el código fuente principal de la aplicación.
- **`src/test/java`**: Incluye pruebas unitarias para garantizar la calidad del código.
- **`resources`**: Archivos de configuración, como `application.properties`, y scripts de migración de base de datos.

## Características Principales
- CRUD para gestión de tópicos (Crear, Leer, Actualizar, Eliminar).
- Autenticación segura con JWT.
- Configuraciones de migración de base de datos.
- Pruebas unitarias para garantizar la robustez del sistema.

## Instalación y Configuración

### 1. Clonar el Repositorio
```bash
git clone <https://github.com/keheez/desafioForo.git>
```

### 2. Configurar la Base de Datos
1. Crea una base de datos MySQL.
2. Actualiza el archivo `src/main/resources/application.properties` con las credenciales y configuraciones de tu base de datos.

Ejemplo:
```
spring.datasource.url=jdbc:mysql://localhost:3306/foro_hub
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
```

### 3. Ejecutar Migraciones de Base de Datos
Las migraciones están definidas en `src/main/resources/db/migration/` y se ejecutan automáticamente al iniciar la aplicación.

### 4. Ejecutar la Aplicación
Usa Maven para compilar y ejecutar el proyecto:
```bash
./mvnw spring-boot:run
```

### 5. Probar la API
Utiliza herramientas como **Insomnia** o **Postman** para probar los endpoints de la API.

## Endpoints Principales

### Autenticación
- **POST** `/auth/login`: Iniciar sesión y obtener un token JWT.

### Tópicos
- **GET** `/topicos`: Obtener todos los tópicos.
- **POST** `/topicos`: Crear un nuevo tópico.
- **PUT** `/topicos/{id}`: Actualizar un tópico existente.
- **DELETE** `/topicos/{id}`: Eliminar un tópico.

## Contribución
Las contribuciones son bienvenidas. Por favor, abre un issue o envía un pull request con tus mejoras.

## Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

---
**Autor:** keheez.


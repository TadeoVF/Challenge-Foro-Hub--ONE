🚀 ForoHub: Tu API REST para un Foro de Programación
¡Bienvenido a ForoHub! Este proyecto es la culminación de los conocimientos adquiridos en la formación Java y Spring Boot de Alura en colaboración con Oracle ONE. Se trata de la construcción de una API REST completa y robusta, diseñada para gestionar un foro donde los usuarios pueden compartir y resolver dudas de programación.

📝 Descripción del Proyecto
ForoHub no es solo un simple CRUD (Create, Read, Update, Delete). Es una API diseñada con las mejores prácticas y estándares del mercado. Entre sus características principales se encuentran:

Persistencia de Datos: Utiliza una base de datos relacional (MySQL) para almacenar la información de forma estructurada. La gestión del esquema de la base de datos se realiza de manera controlada y segura mediante Flyway Migrations.

Seguridad Integral: Implementa una capa de seguridad para proteger los endpoints más sensibles. La autenticación se gestiona con Spring Security y JSON Web Tokens (JWT), garantizando que solo los usuarios verificados puedan realizar ciertas acciones.

Validaciones y Reglas de Negocio: Asegura la integridad de los datos mediante validaciones automáticas. Esto previene que se registren tópicos o usuarios con información incompleta o incorrecta, cumpliendo con las reglas de negocio del foro.

Documentación Interactiva: La API se autodocumenta gracias a SpringDoc, generando una interfaz visual (Swagger UI) que permite a otros desarrolladores explorar y probar los endpoints sin necesidad de código adicional.

Pruebas Automatizadas: Incluye tests unitarios y de integración para garantizar que las funcionalidades principales (controladores y repositorios) funcionen según lo esperado, evitando la regresión de errores.

🛠️ Tecnologías y Herramientas
Este proyecto fue construido utilizando un stack tecnológico moderno y ampliamente utilizado en la industria:

Lenguaje: Java 17+ (usando la última versión LTS).

Framework: Spring Boot 3.3+.

Base de Datos: MySQL 8.0+.

Gestor de Dependencias: Maven.

IDE: IntelliJ IDEA.

📦 Dependencias (Archivo pom.xml)
Las siguientes dependencias fueron cruciales para construir cada funcionalidad del proyecto:

Spring Web: Provee el núcleo para construir las APIs REST.

Spring Data JPA: Facilita la interacción con la base de datos.

MySQL Driver: El conector oficial para MySQL.

Flyway Migration: Gestiona las migraciones de la base de datos.

Validation: Permite las validaciones de los DTOs usando Bean Validation.

Lombok: Reduce el boilerplate code (getters, setters, constructores).

Spring Security: Ofrece las herramientas de autenticación y autorización.

Auth0 JWT: Librería para la creación y validación de JSON Web Tokens.

SpringDoc: Genera la documentación de la API.

Spring Boot DevTools: Herramienta de desarrollo que permite el reinicio automático.

🔗 Endpoints de la API
Los siguientes son los endpoints principales de la API, diseñados para ser intuitivos y seguir los estándares REST:

Autenticación 🔒
POST /login: Valida las credenciales de un usuario y devuelve un JWT para futuras solicitudes.

Tópicos 💬
POST /topicos: Crea un nuevo tópico en el foro. (Requiere JWT).

GET /topicos: Devuelve una lista paginada de todos los tópicos del foro.

PUT /topicos/{id}: Actualiza la información de un tópico existente. (Requiere JWT).

DELETE /topicos/{id}: Elimina un tópico de la base de datos. (Requiere JWT).

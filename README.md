# Foro Hub

**ForoHub** es una plataforma de preguntas y respuestas desarrollada como parte del desafío final del programa **Oracle Next Education**, ofrecido por **Alura LATAM**. El desafío consistió en la creación de una **API REST** que permite a los usuarios realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) sobre temas y preguntas. La plataforma implementa un sistema de autenticación y autorización para restringir el acceso a la información, utilizando una base de datos para la persistencia de datos y siguiendo las mejores prácticas del modelo REST.

---

## **Descripción del Proyecto**

**ForoHub** tiene como objetivo proporcionar una plataforma robusta para la gestión de foros, donde los usuarios pueden:

- **Gestionar tópicos y respuestas:** Crear, leer, actualizar y eliminar tópicos y respuestas.
- **Autenticación y autorización:** Restringir el acceso a recursos protegidos mediante tokens JWT.
- **Validaciones robustas:** Implementar reglas de negocio para garantizar la integridad de los datos.
- **Persistencia de datos:** Utilizar MySQL para el almacenamiento seguro y eficiente de la información.

---

## **Características Principales**

- **Autenticación y autorización:**
  - Registro e inicio de sesión de usuarios con generación de tokens JWT.
  - Acceso a recursos protegidos basado en roles y permisos.
- **Gestión de tópicos y respuestas:**
  - Operaciones CRUD para tópicos y respuestas.
  - Visualización de tópicos y respuestas por ID o mediante rutas específicas.
- **Validaciones avanzadas:**
  - Campos no vacíos ni en blanco.
  - Prevención de títulos o mensajes duplicados.
  - Restricción para que cada usuario pueda crear un máximo de 10 tópicos.
- **Documentación interactiva:**
  - Generada automáticamente con Swagger para facilitar las pruebas.

---

## **Requisitos del Sistema**

- **Java JDK 17** o superior ([Descargar aquí](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html))
- **MySQL 8.0** o superior ([Descargar aquí](https://dev.mysql.com/downloads/mysql/))
- **Maven 4.0.0** o superior
- Herramientas de prueba como **Postman** o **Insomnia**

---

## **Instalación y Configuración**

### **Pasos de Instalación**

1. Clona este repositorio:
   ```bash
   git clone https://github.com/JeanRodriguezdev/Foro-Hub.git
   ```

2. Navega al directorio del proyecto:
   ```bash
   cd Foro-Hub
   ```

3. Configura la base de datos y las propiedades en el archivo `application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/tu_base_de_datos
   spring.datasource.username=tu_usuario
   spring.datasource.password=tu_contraseña
   api.security.secret=tu_clave_secreta
   ```

4. Instala las dependencias con Maven:
   ```bash
   mvn clean install
   ```

5. Ejecuta el proyecto en tu IDE favorito:
   ```bash
   mvn spring-boot:run
   ```

6. Accede a la documentación Swagger en el puerto configurado:
   ```
   http://localhost:8080/swagger-ui.html
   ```

---

## **Ejemplos de Solicitudes**

### **Crear un Tópico** (POST `/topicos`):
```json
{
  "titulo": "string",
  "mensaje": "string",
  "curso": "string",
  "autorId": 9007199254740991
}
```

### **Registrar un Usuario** (POST `/usuarios`):
```json
{
  "nombre": "string",
  "correoElectronico": "string",
  "contrasenia": "string"
}
```

### **Crear una Respuesta** (POST `/respuestas`):
```json
{
  "mensaje": "string",
  "topicoId": 1,
  "autorId": 1
}
```

---

## **Tecnologías Utilizadas**

- **Lenguaje de programación:** Java 17 ☕
- **Framework:** Spring Boot 3 🌱
- **Base de Datos:** MySQL 8.0 🐬
- **Seguridad:** JSON Web Tokens (JWT) 🔐
- **Gestor de Dependencias:** Maven 4.0.0 📦
- **Dependencias:**
  - Spring Boot DevTools
  - Spring Web
  - Spring Data JPA
  - Spring Security
  - MySQL Driver
  - Validation
  - Lombok
  - Flyway Migration
  - Auth0
  - SpringDocs (Swagger)

---

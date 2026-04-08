# 🎓 API REST - Sistema de Gestión Escolar

**Autor:** José Ángel Olmedo Guevara  

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

Proyecto final correspondiente al **Módulo 8 del Diplomado de Desarrollo de Sistemas con Tecnología Java (UNAM)**. 

Esta API RESTful proporciona un backend completo para la gestión de una institución educativa, permitiendo la administración de usuarios, asignaturas, grupos e inscripciones mediante operaciones CRUD completas y relaciones complejas entre entidades.

---

## 🚀 Características Principales

* **Operaciones CRUD Completas:** Implementación de `GET`, `POST`, `PUT` y `DELETE` en 4 tablas principales (Usuarios, Asignaturas, Grupos e Inscripciones).
* **API Principal (Inscripciones):** Manejo de relaciones profundas (Muchos a Uno) integrando Alumnos, Padres, Grupos, Profesores y Asignaturas en una sola respuesta estructurada.
* **Manejo Global de Excepciones:** Implementación de `@ControllerAdvice` para interceptar errores de validación y devolver respuestas estructuradas (`400 Bad Request`) en lugar de errores internos del servidor.
* **Prevención de Recursividad:** Uso estratégico de `@JsonIgnore` para evitar ciclos infinitos en las respuestas JSON generadas por las relaciones bidireccionales de Hibernate/JPA.
* **Población Automática de Datos:** Script `data.sql` integrado para cargar catálogos y datos de prueba al iniciar el servidor.

---

## 🛠️ Requisitos Previos e Instalación

Para ejecutar este proyecto localmente, necesitas tener instalado:
* **Java** (JDK compatible con Spring Boot 4.0.2-M)
* **MariaDB**
* IntelliJ IDEA preferentemente

### Configuración de la Base de Datos

1. Crea una base de datos en MariaDB llamada `escuela`.
2. Las credenciales configuradas por defecto en el archivo `application.properties` son:
   * **Usuario:** `josolmedo`
   * **Contraseña:** `Angel.2020`

> 💡 **Nota:** La aplicación está configurada con `spring.sql.init.mode=always`, por lo que creará las tablas y las poblará con datos iniciales automáticamente al arrancar.

---

## 📡 Endpoints de la API

La URL base para consumir la API localmente es: `http://localhost:8080/api/v1`

| Recurso | Endpoint | Operaciones Soportadas |
| :--- | :--- | :--- |
| **Inscripciones** | `/inscripciones` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |
| **Grupos** | `/grupos` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |
| **Asignaturas** | `/asignaturas` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |
| **Usuarios** | `/usuarios` | `GET`, `POST`, `PUT /{id}`, `DELETE /{id}` |

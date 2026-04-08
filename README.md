# 🚀 Proyecto Módulo 8 - API REST Escuela

**Autor:** José Ángel Olmedo Guevara  
**Tecnología:** Java + Spring Boot (versión 4.0.2 milestone)  
**Base de datos:** MariaDB  
**Objetivo:** Desarrollar una API REST completa con operaciones CRUD sobre cuatro tablas relacionadas, aplicando manejo de excepciones y validaciones.

---

## 📚 Tablas implementadas (CRUD completo)

| # | Tabla | Endpoint base |
|---|-------|---------------|
| 1 | Asignaturas | `/api/v1/asignaturas` | 
| 2 | Grupos | `/api/v1/grupos` | 
| 3 | **Inscripciones** (API Principal) | `/api/v1/inscripciones` | 
| 4 | Usuarios | `/api/v1/usuarios` | 

> ⭐ La tabla **Inscripciones** es la *API Principal* y contiene relaciones bidireccionales manejadas con `@JsonIgnore` para evitar bucles infinitos en el JSON.

---

## ⚙️ Configuración necesaria

### 1. Requisitos previos
- Java 17+
- MariaDB (o MySQL con adaptación)
- Maven / Gradle (según tu proyecto)
- Postman o cURL (para consumir la API)

### 2. Base de datos
Crear una base de datos local llamada `escuela`:

```sql
CREATE DATABASE escuela;

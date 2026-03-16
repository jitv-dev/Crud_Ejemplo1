# CRUDApplication

Proyecto de demostración con **Spring Boot 4** que implementa una API REST con operaciones CRUD básicas, usando una base de datos en memoria H2 y JPA/Hibernate.

---

## 🛠 Tecnologías

- Java 21
- Spring Boot 4.0.3
- Spring Data JPA
- Spring MVC
- H2 Database (en memoria)
- Lombok
- Maven Wrapper

---

## 📋 Requisitos previos

- Java 21+
- Maven (o usar el wrapper incluido `./mvnw`)

---

## 🚀 Cómo ejecutar

```bash
# Clonar el repositorio
git clone <url-del-repositorio>
cd CRUDApplication

# Ejecutar con Maven Wrapper
./mvnw spring-boot:run
```

La aplicación estará disponible en `http://localhost:8080`.

---

## 🗄 Consola H2

Puedes inspeccionar la base de datos en memoria desde el navegador en:

```
http://localhost:8080/h2-console
```

| Campo    | Valor                  |
|----------|------------------------|
| JDBC URL | `jdbc:h2:mem:testdb`   |
| Usuario  | `sa`                   |
| Password | *(vacío)*              |

---

## 🧪 Tests

```bash
./mvnw test
```

---

## ⚙️ Configuración

Las propiedades de la aplicación se encuentran en `src/main/resources/application.properties`:

| Propiedad                          | Valor                          |
|------------------------------------|--------------------------------|
| `spring.datasource.url`            | `jdbc:h2:mem:testdb`           |
| `spring.jpa.hibernate.ddl-auto`    | `update`                       |
| `spring.jpa.show-sql`              | `true`                         |
| `spring.h2.console.enabled`        | `true`                         |

---

## 📁 Estructura del proyecto

```
src/
├── main/
│   ├── java/com/example/CRUDApplication/
│   │   └── CrudApplication.java
│   └── resources/
│       └── application.properties
└── test/
    └── java/com/example/CRUDApplication/
        └── CrudApplicationTests.java
```
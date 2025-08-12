# 🦷 ClínicaMVC — Sistema Web para Gestión de Turnos Odontológicos

Este proyecto es una aplicación **web** desarrollada en **Java 17 con Spring Boot 3**, que permite gestionar turnos entre pacientes y odontólogos, usando una base de datos relacional (**MySQL** o **H2**) y vistas renderizadas con **Thymeleaf**.

---

## ⚙️ Tecnologías utilizadas

- ✅ Java 17
- ✅ Spring Boot 3.2.7 (SNAPSHOT)
- ✅ Spring Data JPA (Hibernate)
- ✅ Spring Web (MVC)
- ✅ Thymeleaf (plantillas HTML)
- ✅ Lombok
- ✅ ModelMapper
- ✅ MySQL / H2
- ✅ Logback para logging

---

## 🧠 Funcionalidades

- Crear y consultar pacientes, odontólogos, especialidades y turnos.
- Asignación de turnos por fecha entre pacientes y odontólogos.
- Asociación de múltiples especialidades a un odontólogo (relación ManyToMany).
- Mapeo completo de entidades usando JPA.
- Interfaz web básica para interacción a través del navegador.

---

## 🧱 Modelo de Datos

### Paciente
- Nombre, apellido, DNI, fecha de ingreso.
- Asociación OneToOne con domicilio.
- Relación OneToMany con turnos.

### Odontólogo
- Matrícula, nombre, apellido.
- Relación OneToMany con turnos.
- Relación ManyToMany con especialidades.

### Especialidad
- Tipo de especialidad (ej: Ortodoncia, Endodoncia).
- Relación ManyToMany con odontólogos.

### Turno
- Fecha
- Asociación ManyToOne con paciente y odontólogo.

### Domicilio
- Calle, número, localidad, provincia.

---
## 🚀 Cómo ejecutar

1. Clonar el repositorio:

```bash
git clone https://github.com/tuusuario/ClinicaMVC.git
cd ClinicaMVC

spring.datasource.url=jdbc:mysql://localhost:3306/clinica_mvc
spring.datasource.username=root
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update

./mvnw spring-boot:run

http://localhost:8080
```

## 🙋‍♂️ Autor

**Maximiliano Soriano**

💼 Desarrollador Java Full Stack  
📧 maxi.soriano.70.23@gmail.com
🔗 LinkedIn: [linkedin.com/in/maximilianosoriano](https://www.linkedin.com/in/maximiliano-soriano/)


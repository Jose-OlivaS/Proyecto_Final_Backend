# Sistema de Gestión de Alquiler de Vehículos

Es una aplicación Java Web realizada por el grupo 8 como proyecto final 
Este proyecto implementa un sistema de gestión de alquiler de vehículos que permite a los clientes registrarse, buscar vehículos disponibles, realizar reservas, y gestionar el estado de sus alquileres (modificar o cancelar). Los administradores pueden gestionar la flota de vehículos, las reservas, y los usuarios, además de consultar reportes sobre los alquileres realizados y la disponibilidad de los vehículos.

## Requisitos Técnicos

- **Lenguaje**: Java 17
- **Base de datos**: MySQL
- **ORM**: Hibernate
- **Gestión de dependencias y APIs REST**: Spring (Spring Boot 2.7.11)
- **Frontend**: Thymeleaf con Spring Boot
- **Colecciones y Streams**: Uso de streams para filtrar y procesar listas de vehículos, clientes, y reservas
- **APIs**: APIs REST para gestionar las reservas

## Configuración del Proyecto

### Requisitos Previos

- JDK 17
- Maven
- MySQL Server

## Diagramas
Se incluyen los siguientes diagramas, en el archivo resources, en el directorio diagramas
- Diagrama de Clases
- Diagrama de Secuencias
- Diagrama de flujo

### Configuración de la Base de Datos

1. Crear una base de datos llamada `alquilervehiculos` en MySQL:

```sql
CREATE DATABASE alquilervehiculos;

## Configuración de la base de datos
spring.datasource.url=jdbc:mysql://localhost:3306/alquilervehiculos
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# Configuración JPA
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

# Deshabilitar spring.jpa.open-in-view
spring.jpa.open-in-view=false

# Configuración Thymeleaf
spring.thymeleaf.cache=false

# Servidor
server.port=8000

###Acceso a la Aplicación
Accede a la aplicación en http://localhost:8000

Credenciales de Acceso
Username: user, admin

Password: 1234


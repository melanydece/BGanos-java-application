[English](README.md) | **Español**

# Aplicación B-Ganos

## Descripción General

B-Ganos es un sistema de gestión transaccional de escritorio desarrollado en Java, diseñado para la administración de un jardín botánico recreacional y su tienda asociada.

El sistema implementa una arquitectura multicapa con persistencia relacional y soporta dos estrategias de persistencia: la 1º basada en DAO y la 2º basada en JPA. Incluye gestión de transacciones y control de concurrencia.

Todas las entidades del dominio, la lógica de negocio y la interfaz de usuario están implementadas en español ya que el proyecto se desarrolló en el contexto de la asignatura **Modelado de Software** de la Universidad Complutense de Madrid.

Este proyecto se realizó en el curso 3º de Ingeniería de Software (2024–2025) por un equipo de 12 personas.

Este repositorio representa una copia fiel del proyecto colaborativo original.

---

## Arquitectura

La aplicación sigue una arquitectura multicapa estricta:

- **Capa de Presentación** → Interfaz gráfica Java Swing  
- **Capa de Negocio** → Servicios de aplicación y lógica de negocio  
- **Capa de Integración** → Persistencia y acceso a datos  
- **Capa de Base de Datos Relacional** → Definición de esquema SQL (.sql)

Aspectos clave de la arquitectura:

- Gestión de transacciones  
- Control de concurrencia  
- Separación clara entre objetos de negocio y objetos de transferencia (según la versión)  
- Diseño guiado por patrones de software establecidos

---

## Versiones Implementadas

### 1. Persistencia basada en DAO

- Persistencia relacional directa usando SQL/MySQL  
- Implementación de:
  - Data Access Object (DAO)  
  - Transfer Object  
  - Transfer Object Assembler  
  - Application Service  
  - Service to Worker  
  - Consultas personalizadas

En esta versión, la capa de negocio opera utilizando **objetos de transferencia (Transfer Objects)**.

---

### 2. Persistencia basada en JPA

- Persistencia usando JPA (Java Persistence API)  
- Persistencia del modelo de dominio usando JPA  
- Integración del patrón Business Object  
- Se recomienda EclipseLink como proveedor

En esta versión la capa de negocio opera utilizando **objetos de negocio del dominio**, mejorando la modularidad y la separación de responsabilidades.

---

## Patrones de Diseño Aplicados

- Service to Worker  
- Application Service  
- Data Access Object  
- Transfer Object  
- Transfer Object Assembler  
- Business Object  
- Domain Store  

Nota: Los patrones aplicados siguen los requerimientos de la asignatura y reflejan un diseño multicapa basado en patrones.

---

## Tecnologías Utilizadas

- Java  
- Swing  
- MySQL  
- SQL (definición de esquema .sql)  
- JPA 2.x  
- EclipseLink  
- JUnit  
- Git  

---

## Estructura del proyecto

```
├── Presentacion (Presentation Layer)
├── Negocio (Business Layer)
├── Integracion (Integration Layer)
```

Los nombres de las carpetas se mantienen en español como en la implementación original.  
Cada capa está estructuralmente aislada para garantizar mantenibilidad y separación de responsabilidades.

---

## Funcionalidades Principales

### Gestión del Invernadero

- Gestión de facturas  
- Gestión de entradas  
- Administración de invernaderos  
- Gestión de sistemas de riego  
- Gestión de plantas  
- Gestión de fabricantes  
- Consultas analíticas (por ejemplo, fechas con más entradas vendidas por invernadero)

---

### Gestión de la Tienda

- Gestión de productos y marcas  
- Gestión de proveedores  
- Gestión del ciclo de ventas  
- Gestión de empleados y turnos  
- Actualización de inventario  
- Procesamiento de ventas y devoluciones

---

## Pruebas

Se implementaron pruebas unitarias con **JUnit**, las cuales cubren:

- Validación de la lógica de negocio  
- Comportamiento de la persistencia  
- Flujos críticos de transacciones  

---

## Modelado UML

Los diagramas UML fueron creados siguiendo los estándares de **IBM RSAD**.  

La documentación completa de diseño UML (diagramas de clases, diagramas de secuencia, diagramas de componentes y diagramas de despliegue) se encuentra en un repositorio separado:  
https://github.com/melanydece/BGanos-UML-modeling

---

## Equipo

Proyecto desarrollado de forma colaborativa por un equipo de 12 miembros en la asignatura **Modelado de Software**.  
Puedes echar un vistazo a la lista completa de colaboradores en la sección "Contributors" del repositorio.
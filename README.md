# ⚡️ TurnApp: Backend Ágil para la Asignación Aleatoria de Turnos

[![Java](https://img.shields.io/badge/Language-Java-007396?style=for-the-badge&logo=java)](https://www.java.com/)
[![Spring Boot](https://img.shields.io/badge/Framework-Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot)](https://spring.io/projects/spring-boot)
[![API REST](https://img.shields.io/badge/Interface-REST%20API-lightgrey?style=for-the-badge&logo=rest)](https://en.wikipedia.org/wiki/Representational_state_transfer)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

---

## 💡 Sobre el Proyecto

**TurnApp** es el servicio de backend diseñado para **automatizar y equilibrar** la carga de trabajo en tu negocio.

El objetivo principal es tomar los servicios o clientes entrantes y asignarlos a un empleado disponible de **forma aleatoria**, asegurando una distribución justa y rápida. Este proyecto es ideal para quien busca una solución de gestión de colas (queues) rápida de implementar y fácil de mantener usando el ecosistema de **Spring Boot**.

## ✨ Funcionalidades Destacadas

* **Asignación Aleatoria:** Implementa lógica para distribuir nuevos turnos a empleados disponibles de forma *randomizada*.
* **Gestión de Empleados:** CRUD completo para registrar, actualizar y eliminar empleados.
* **Ciclo de Turnos:** Endpoint para tomar un nuevo turno y otro para finalizarlo, liberando al empleado.
* **API RESTful:** Toda la lógica es accesible mediante endpoints sencillos y limpios, listos para ser consumidos por cualquier frontend (Web o Móvil).

## 🛠️ Tecnologías y Estructura

Este proyecto sigue una arquitectura de capas estándar (Controller, Service, Repository), lo que facilita su comprensión y desarrollo.

| Capa | Propósito | Tecnología Clave |
| :--- | :--- | :--- |
| **Controlador** | Recibe peticiones HTTP y devuelve respuestas. | Spring Web / REST |
| **Servicio** | Contiene la lógica de negocio (asignación aleatoria, validaciones, etc.). | Java / Spring Components |
| **Repositorio** | Interactúa con la capa de persistencia (Base de Datos). | Spring Data JPA |
| **Herramienta** | Manejo de dependencias y compilación. | Gradle |

## 🚀 Puesta en Marcha

### Requisitos

Asegúrate de tener instalado:

1.  **JDK 17** o superior.
2.  **Gradle** (se incluye el wrapper `gradlew`).

### Instalación

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/SHUNNIORR/turn-app.git](https://github.com/SHUNNIORR/turn-app.git)
    cd turn-app
    ```

2.  **Compilar y construir el proyecto:**
    ```bash
    ./gradlew build
    ```

3.  **Ejecutar la aplicación:**
    ```bash
    ./gradlew bootRun
    ```

La API estará activa en `http://localhost:8080` por defecto.

## 🔗 Endpoints Principales (Ejemplo)

Una vez que la aplicación esté corriendo, puedes interactuar con los siguientes endpoints:

| Método | Ruta | Descripción |
| :--- | :--- | :--- |
| `POST` | `/api/v1/turnos/nuevo` | Crea y asigna un nuevo turno a un empleado al azar. |
| `GET` | `/api/v1/turnos` | Obtiene el listado de todos los turnos activos. |
| `PUT` | `/api/v1/turnos/{id}/finalizar` | Marca un turno como finalizado y libera al empleado. |
| `POST` | `/api/v1/empleados` | Registra un nuevo empleado disponible. |

---

## 🛣️ Próximos Pasos

* Integración con un frontend (React, Vue, etc.)
* Añadir sistema de colas (RabbitMQ o Kafka) para un manejo asíncrono.
* Implementar un sistema de autenticación (JWT).

¡Siéntete libre de contribuir!

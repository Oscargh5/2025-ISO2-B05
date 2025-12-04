# ISOII-B05
# 🧩 Diagrama de Clases del Cliente (GF5)

El siguiente diagrama representa la arquitectura interna del **cliente** desarrollada para el Grupo Funcional 5 (GF5).  
Este diseño define las pantallas del usuario, los controladores de interacción, los validadores y las entidades que permiten gestionar asignaturas, bibliografía y grupos académicos desde el lado cliente.

El objetivo de esta versión es documentar la estructura utilizada en el cliente y asegurar su coherencia con los requisitos funcionales **RF-06, RF-07, RF-08, RF-09 y RF-10**.

---

## 🖥️ 1. Capa de Presentación — `Presentation.client`

Esta capa contiene todas las **interfaces de usuario (UI)** que interactúan directamente con el usuario final.

### ✔ Pantallas del cliente

- `UIAccesoGrupos`
- `UICrearAsignatura`
- `UIGestionBibliografia`
- `UIGrupoEstudio`
- `PantallaGrupoInvestigacionUI`

### ✔ Funciones principales

- Mostrar información obtenida del servidor.  
- Recoger datos y acciones del usuario.  
- Validar datos básicos.  
- Invocar a los controladores correspondientes.  
- Gestionar la navegación entre pantallas.

> Esta capa NO realiza lógica de negocio.
---

## 🧠 2. Capa de Control — `Application.client`

Incluye los controladores del cliente que coordinan la interfaz con las entidades del dominio y preparan las operaciones que serán enviadas al servidor.

### ✔ Controladores del cliente

- `ControladorAccesoGrupos`
- `ControladorAsignatura`
- `ControladorBibliografia`
- `ControladorGrupoEstudio`
- `ControladorGrupoInvestigacion`

### ✔ Validadores asociados

- `ValidadorAcceso`
- `ValidadorAsignatura`
- `ValidadorBibliografia`
- `ValidadorGrupoEstudio`
- `ValidadorGrupoInvestigacion`

### ✔ Responsabilidades

- Validación previa de datos antes de mandarlos al servidor.  
- Construcción de los objetos enviados al dominio.  
- Coordinación entre pantallas.  
- Gestión de errores enviados por el backend.  

> Esta capa NO accede a la base de datos.
---

## 🧱 3. Capa de Dominio — `Domain.client`

Modela las entidades que utiliza el cliente para representar la información proveniente del servidor.

### ✔ Entidades modeladas

- `Asignatura`
- `Bibliografia`
- `GrupoEstudio`
- `GrupoInvestigacion`
- `Usuario`  
  - `Profesor`  
  - `Estudiante`

Estas clases sirven para almacenar y manipular datos que el servidor envía y que el cliente debe representar o utilizar en las operaciones de los casos de uso.

---

## 📌 Relación con los Casos de Uso del Cliente

| Caso de Uso | Controlador Cliente | Entidades Involucradas |
|-------------|--------------------|--------------------------|
| RF-06 — Acceder a grupo | `ControladorAccesoGrupos` | `Estudiante`, `GrupoEstudio` |
| RF-07 — Crear asignatura | `ControladorAsignatura` | `Asignatura`, `Profesor` |
| RF-08 — Gestionar bibliografía | `ControladorBibliografia` | `Asignatura`, `Bibliografia` |
| RF-09 — Registrar grupo de estudio | `ControladorGrupoEstudio` | `GrupoEstudio`, `Asignatura` |
| RF-10 — Registrar grupo de investigación | `ControladorGrupoInvestigacion` | `GrupoInvestigacion`, `Profesor` |

---

## 🖼️ Diagrama de Clases del Cliente (GF5)

![Diagrama de Clases del Cliente GF5](./DiagramasCliente/Diagrama-Clases-Cliente.png)
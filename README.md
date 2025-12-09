## 🧩 Grupo Funcional 6 — Lado Cliente

Este módulo contiene la documentación completa del **lado cliente** del Grupo Funcional 6, incluyendo tanto los **requisitos funcionales**, como los **casos de uso** correspondientes.

El objetivo de este grupo funcional en el cliente es cubrir:

* **Solicitar estudios bibliométricos** por parte del profesor.

---

## 📊 Diagrama de Casos de Uso (Cliente)

El siguiente diagrama representa la interacción entre los actores del lado cliente (profesor) y el caso de uso asociado al requisito funcional **RF-11**.

![Diagrama Cliente](./diagramas-cliente/cdu-gf6-cliente.png)

---

## 📃 Resumen de Casos de Uso del Cliente

| ID        | Caso de Uso                     | Actor Principal | Descripción breve                                                                      |
| --------- | ------------------------------- | --------------- | -------------------------------------------------------------------------------------- |
| **CU-11** | Solicitar estudio bibliométrico | Profesor        | Permite al profesor solicitar estudios bibliométricos o estadísticas de investigación. |

---

## 📌 Descripción de Casos de Uso

A continuación se encuentra el caso de uso detallado que forma parte de este grupo funcional. Cada uno incluye: actores, precondiciones, postcondiciones, flujo normal, flujos alternativos y reglas de negocio.

---

### 🎓 **CU-11 — Solicitar estudio bibliométrico**

**Requisito asociado:** RF-11
**Actor principal:** Profesor

**Descripción:**
El sistema permite al profesor solicitar un estudio bibliométrico basado en diversos parámetros (citas, autor, publicaciones, etc.).

**Precondiciones:**

* El profesor ha iniciado sesión correctamente.
* El sistema tiene acceso a los datos necesarios para generar el estudio.

**Postcondiciones:**

* El sistema genera y envía la solicitud de estudio al servidor para su procesamiento.

**Flujo principal:**

1. El profesor accede al módulo de estudios bibliométricos.
2. El sistema muestra las opciones de personalización del estudio.
3. El profesor selecciona los parámetros del estudio.
4. El sistema valida la solicitud.
5. El sistema envía la solicitud al servidor para su procesamiento.

**Flujos alternativos:**

* No se encuentran datos suficientes para realizar el estudio.
* El formato de los parámetros de búsqueda es incorrecto.

---

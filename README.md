## 🧩 Grupo Funcional 6 — Lado Servidor

Este módulo contiene la documentación completa del **lado servidor** del Grupo Funcional 6, incluyendo tanto los **requisitos funcionales**, como los **casos de uso** correspondientes.

El objetivo de este grupo funcional en el servidor es cubrir:

* **Generación de informes de actividad** por parte del bibliotecario.
* **Generación de estadísticas globales** por parte del administrador.

---

## 📊 Diagrama de Casos de Uso (Servidor)

El siguiente diagrama representa la interacción entre los actores del lado servidor (bibliotecario, administrador) y los casos de uso asociados a los requisitos funcionales **RF-14** y **RF-17**.

![Diagrama Servidor](./diagramas-servidor/cdu-gf6-servidor.png)

---

## 📃 Resumen de Casos de Uso del Servidor

| ID        | Caso de Uso                   | Actor Principal | Descripción breve                                                                 |
| --------- | ----------------------------- | --------------- | --------------------------------------------------------------------------------- |
| **CU-14** | Generar informe de actividad  | Bibliotecario   | Permite al bibliotecario generar informes sobre la actividad del sistema.         |
| **CU-17** | Generar estadísticas globales | Administrador   | Permite al administrador generar estadísticas generales y auditorías del sistema. |

---

## 📌 Descripción de Casos de Uso

A continuación se encuentran los casos de uso detallados que forman parte de este grupo funcional. Cada uno incluye: actores, precondiciones, postcondiciones, flujo normal, flujos alternativos y reglas de negocio.

---

### 🧑‍🏫 **CU-14 — Generar informe de actividad**

**Requisito asociado:** RF-14
**Actor principal:** Bibliotecario

**Descripción:**
El sistema permite al bibliotecario generar informes detallados sobre la actividad del sistema, como el número de préstamos, material más utilizado, entre otros.

**Precondiciones:**

* El bibliotecario ha iniciado sesión correctamente.
* Existen datos sobre la actividad del sistema.

**Postcondiciones:**

* El informe se genera y queda disponible para su visualización o descarga.

**Flujo principal:**

1. El bibliotecario accede a la sección de informes.
2. Selecciona el tipo de informe a generar.
3. El sistema valida la solicitud y consulta los datos.
4. El informe es generado y enviado al bibliotecario.

**Flujos alternativos:**

* El sistema no encuentra datos suficientes para generar el informe.
* El formato de los datos solicitados no es válido.

---

### 🔬 **CU-17 — Generar estadísticas globales**

**Requisito asociado:** RF-17
**Actor principal:** Administrador

**Descripción:**
El sistema permite al administrador generar estadísticas globales del uso del sistema, como auditorías de seguridad, cantidad de usuarios activos, etc.

**Precondiciones:**

* El administrador tiene acceso completo al sistema.
* El sistema ha registrado suficiente información para generar las estadísticas.

**Postcondiciones:**

* Las estadísticas son generadas y disponibles para su revisión.

**Flujo principal:**

1. El administrador accede a la sección de estadísticas.
2. Selecciona el tipo de estadística a generar.
3. El sistema consulta los datos y genera las estadísticas solicitadas.
4. El administrador recibe el resultado.

**Flujos alternativos:**

* No hay suficientes datos para generar las estadísticas.
* El formato de las métricas solicitadas no es válido.

---

# 🧠 **Fase de Análisis (Servidor)**

En esta fase se estudian los comportamientos, reglas de negocio y responsabilidades que asumirá el servidor para cumplir los requisitos. Se describen las entidades principales, las validaciones críticas y las interacciones internas necesarias para garantizar coherencia y seguridad en el backend.

### 🔍 Elementos analizados

#### ✔ **Actores internos del servidor**

* **Administrador**: puede generar informes de actividad
* **Bibliotecario**: puede generar estadísticas globales

---

# 📌 Casos de Uso Detallados del Servidor

A continuación se detallan los casos de uso internos que ejecuta el backend cuando los actores del cliente realizan acciones en la interfaz.

---

## Diagrama de Clases de Análisis (SRV-14)
![Diagrama de Clases - SRV-14](./diagramas-servidor/dca-cdu14-servidor.png)

## Diagrama de Clases de Análisis (SRV-17)
![Diagrama de Clases - SRV-17](./diagramas-servidor/dca-cdu17-servidor.png)


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


## 💻 Fase de Implementación

En esta fase se llevará a cabo la implementación del código del servidor a partir de la lógica definida por los diagramas anteriores, haciendo uso de ingeniería directa.

### ⚙️ Backend

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

## 🧠 2. Fase de Análisis — Diagramas del Servidor

# Diagrama de análisis del caso de uso:

![Diagrama Analisis](./diagramas-cliente/analisis-gf6-cliente.png)

## 📐 Diagrama de Clases – Cliente (CU: Petición de Estudios Bibliométricos)

Este apartado describe el **diagrama de clases del lado cliente**, elaborado siguiendo el modelo  
**Presentación – Dominio – Persistencia**, y basado exclusivamente en los diagramas funcionales proporcionados.

---

## 🖥️ Capa de Presentación

### UIEstudiosbibliometricos
Clase responsable de la interacción con el usuario para la solicitud de estudios bibliométricos.

**Métodos principales:**
- `solicitarEstudio() : void`
- `mostrarResultado(msg : String) : void`
- `mostrarError(msg : String) : void`

**Relaciones:**
- Depende de `ControladorEstudioBibliometrico`

---

## 🧠 Capa de Dominio

### ControladorEstudioBibliometrico
Gestiona el flujo del caso de uso y coordina la validación y el acceso a persistencia.

**Métodos principales:**
- `solicitarEstudio(solicitud : SolicitudEstudioBibliometrico) : void`

**Relaciones:**
- Usa `ValidadorEstudioBibliometrico`
- Accede a `SolicitudEstudioBibliometricoRepository`
- Accede a `ProfesorRepository`

---

### ValidadorEstudioBibliometrico
Encargado de validar los datos de la solicitud antes de su procesamiento.

**Métodos principales:**
- `validar(solicitud : SolicitudEstudioBibliometrico) : boolean`

---

### SolicitudEstudioBibliometrico
Entidad de dominio que representa la solicitud de un estudio bibliométrico.

**Atributos:**
- `profesor : Profesor`
- `parametros : String`

**Métodos principales:**
- `getProfesor() : Profesor`
- `setProfesor(p : Profesor) : void`
- `getParametros() : String`
- `setParametros(p : String) : void`

**Relaciones:**
- Asociación **1..1** con `Profesor`

---

### Profesor
Entidad de dominio que representa al profesor solicitante.

**Atributos:**
- `id : String`
- `nombre : String`

**Métodos principales:**
- `getId() : String`
- `setId(id : String) : void`
- `getNombre() : String`
- `setNombre(n : String) : void`

---

## 🗄️ Capa de Persistencia

### SolicitudEstudioBibliometricoRepository
Repositorio encargado de la gestión de solicitudes de estudios bibliométricos.

**Atributos:**
- `solicitudes : List<SolicitudEstudioBibliometrico>`

**Métodos de consulta:**
- `obtenerTodas() : List<SolicitudEstudioBibliometrico>`
- `obtenerPorProfesor(profesor : Profesor) : SolicitudEstudioBibliometrico`
- `existeSolicitud(profesor : Profesor) : boolean`

---

### ProfesorRepository
Repositorio encargado de la gestión de profesores.

**Atributos:**
- `profesores : List<Profesor>`

**Métodos de consulta:**
- `obtenerPorId(id : String) : Profesor`
- `obtenerTodos() : List<Profesor>`
- `existeProfesor(id : String) : boolean`

---

## 🔗 Relaciones entre Clases

- `UIEstudiosbibliometricos` → `ControladorEstudioBibliometrico` (dependencia)
- `ControladorEstudioBibliometrico` → `ValidadorEstudioBibliometrico` (dependencia)
- `ControladorEstudioBibliometrico` → `SolicitudEstudioBibliometricoRepository` (dependencia)
- `ControladorEstudioBibliometrico` → `ProfesorRepository` (dependencia)
- `SolicitudEstudioBibliometrico` — `Profesor` (asociación **1..1**)
- `SolicitudEstudioBibliometricoRepository` — `SolicitudEstudioBibliometrico`
- `ProfesorRepository` — `Profesor`

---

Este diseño garantiza una **separación clara de responsabilidades** y mantiene coherencia con la arquitectura utilizada en el lado servidor del proyecto.

![Diagrama Analisis](./diagramas-cliente/DiagramaClasesClienteIt6.png)

## 💻 3. Fase de Implementación

En esta fase se llevará a cabo la implementación del código del cliente acorde a los diagramas anteriores, por medio de ingeniería directa.

### ⚙️  Backend

<img width="350" src="./diagramas-servidor/Backend-servidor.png" />

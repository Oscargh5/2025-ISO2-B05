# 🧩 Grupo Funcional 5 — Lado Cliente
Este módulo contiene toda la documentación correspondiente a los requisitos del **lado cliente** del Grupo Funcional 5, orientado a las funcionalidades que realizan directamente los usuarios finales (estudiantes y profesores) a través de la interfaz gráfica.

El objetivo de este grupo funcional es cubrir las capacidades relacionadas con:
- Gestión académica por parte del profesor
- Interacción social y académica del estudiante
- Asociación de bibliografía a asignaturas
- Creación y participación en grupos de estudio
- Gestión de grupos de investigación

---

## 📊 Diagrama de Casos de Uso (Cliente)

El siguiente diagrama representa la interacción entre los actores del lado cliente (estudiante y profesor) y los casos de uso asociados a los requisitos funcionales RF-06 a RF-10.

![Diagrama Cliente](./diagrama-gf5-cliente.png)

---

## 📃 Resumen de Casos de Uso del Cliente

| ID | Caso de Uso | Actor Principal | Descripción breve |
|----|--------------|-----------------|-------------------|
| **CU-06** | Acceder a grupos de estudio y clubs de lectura | Estudiante | Permite visualizar y unirse a grupos creados por profesores o la biblioteca. |
| **CU-07** | Crear asignatura | Profesor | Permite registrar nuevas asignaturas en el sistema. |
| **CU-08** | Gestionar bibliografía específica | Profesor | Permite asociar material bibliográfico a las asignaturas creadas. |
| **CU-09** | Crear grupo de estudio | Profesor | Permite crear grupos de estudio vinculados a sus asignaturas. |
| **CU-10** | Crear grupo de investigación | Profesor | Permite crear grupos de investigación asociados a líneas o proyectos. |

---

## 📌 Descripción de Casos de Uso

A continuación se encuentran los casos de uso detallados que forman parte de este grupo funcional. Cada uno incluye: actores, precondiciones, postcondiciones, flujo normal, flujos alternativos y reglas de negocio.

---

### 🎓 **CU-06 — Acceder a grupos de estudio y clubs de lectura**  
**Requisito asociado:** RF-06  
**Actor principal:** Estudiante  

**Descripción:**  
El sistema permite al estudiante visualizar los grupos disponibles y unirse a aquellos que estén activos.

**Precondiciones:**  
- El estudiante ha iniciado sesión mediante SSO.
- Existen grupos disponibles.

**Postcondiciones:**  
- El estudiante queda unido al grupo seleccionado.

**Flujo principal:**  
1. El estudiante accede al módulo de grupos.  
2. El sistema muestra los grupos disponibles.  
3. Selecciona un grupo y visualiza la información.  
4. Solicita unirse.  
5. El sistema confirma la operación.  

**Flujos alternativos:**  
- El grupo está completo.  
- El grupo es privado y requiere aprobación.  

**Reglas de negocio:**  
- El estudiante puede unirse a múltiples grupos.  
- Los grupos pueden ser públicos o privados.

---

### 🧑‍🏫 **CU-07 — Crear asignatura**  
**Requisito asociado:** RF-07  
**Actor principal:** Profesor  

**Descripción:**  
Permite a un profesor crear asignaturas nuevas en el sistema.

**Precondiciones:**  
- El profesor tiene permisos adecuados.  

**Postcondiciones:**  
- La asignatura queda registrada.  

**Flujo principal:**  
1. El profesor accede a “Mis asignaturas”.  
2. Selecciona “Crear asignatura”.  
3. Introduce los datos requeridos.  
4. El sistema valida la información.  
5. La asignatura es creada.  

**Flujos alternativos:**  
- Código ya existente.  
- Datos incompletos.  

**Reglas de negocio:**  
- El código debe ser único.  

---

### 📚 **CU-08 — Gestionar bibliografía específica**  
**Requisito asociado:** RF-08  
**Actor principal:** Profesor  

**Descripción:**  
El profesor puede añadir, eliminar o modificar bibliografía recomendada para una asignatura.

**Precondiciones:**  
- La asignatura existe.  
- El recurso bibliográfico está registrado.  

**Postcondiciones:**  
- La bibliografía queda actualizada.  

**Flujo principal:**  
1. El profesor abre la asignatura.  
2. Accede a “Bibliografía recomendada”.  
3. Añade o elimina recursos.  
4. El sistema valida los cambios.  
5. Se actualiza la lista.

**Flujos alternativos:**  
- Recurso no existe.  
- El recurso es obligatorio y no puede eliminarse.

---

### 👥 **CU-09 — Crear grupo de estudio**  
**Requisito asociado:** RF-09  
**Actor principal:** Profesor  

**Descripción:**  
Permite crear grupos de estudio asociados a una asignatura.

**Precondiciones:**  
- La asignatura existe y pertenece al profesor.

**Postcondiciones:**  
- El grupo queda visible para estudiantes.

**Flujo principal:**  
1. Seleccionar asignatura.  
2. Pulsar “Crear grupo de estudio”.  
3. Introducir datos.  
4. Validación.  
5. Registro del grupo.

**Flujos alternativos:**  
- Datos incompletos.  
- Nombre duplicado.

---

### 🔬 **CU-10 — Crear grupo de investigación**  
**Requisito asociado:** RF-10  
**Actor principal:** Profesor  

**Descripción:**  
Permite al profesor crear grupos de investigación.

**Precondiciones:**  
- El profesor pertenece a un departamento válido.

**Postcondiciones:**  
- El grupo queda registrado.

**Flujo principal:**  
1. Acceder al módulo “Grupos de investigación”.  
2. Pulsar “Crear grupo”.  
3. Introducir nombre, temática y miembros.  
4. Validación.  
5. Confirmación.

**Flujos alternativos:**  
- Nombre duplicado.  
- Miembros inválidos.

---

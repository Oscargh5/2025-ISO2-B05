## 🧩 Grupo Funcional 7 — Lado Cliente

Este módulo contiene la documentación correspondiente al **lado cliente** del Grupo Funcional 7, incluyendo el **requisito funcional RF-16** y su análisis asociado.

El objetivo de este grupo funcional en el cliente es cubrir:

* **Gestión y configuración del sistema** por parte del usuario administrador.
* Consideración de la **interoperabilidad** del sistema con otros servicios universitarios (RNF-10).

---

## 📊 Diagrama de Casos de Uso (Cliente)

El siguiente diagrama representa la interacción entre el actor del lado cliente (Administrador del sistema) y el caso de uso asociado al requisito funcional **RF-16**.

![Diagrama Cliente](./diagramas-cliente/cdu-gf7-cliente.png)

---

## 📃 Resumen de Casos de Uso del Cliente

| ID        | Caso de Uso                       | Actor Principal | Descripción breve                                                              |
| --------- | --------------------------------- | --------------- | ------------------------------------------------------------------------------ |
| **CU-16** | Gestionar y configurar el sistema | Administrador   | Permite ajustar parámetros generales del sistema desde la interfaz de usuario. |

---

## 📌 Descripción de Casos de Uso

A continuación se encuentra el caso de uso detallado que forma parte de este grupo funcional.
Incluye actores, precondiciones, postcondiciones, flujo normal, flujos alternativos y reglas de negocio.

---

### ⚙️ **CU-16 — Gestionar y configurar el sistema**

**Requisito asociado:** RF-16
**Actor principal:** Administrador del sistema

---

### **Descripción**

El sistema permite al administrador gestionar y configurar los parámetros generales de funcionamiento desde el lado cliente, tales como políticas de préstamo, horarios de servicio, sanciones y otros ajustes globales.

Esta configuración se realiza mediante una interfaz gráfica que centraliza las opciones de administración del sistema.

---

### **Precondiciones**

* El administrador ha iniciado sesión correctamente.
* El administrador dispone de permisos de configuración del sistema.

---

### **Postcondiciones**

* Los parámetros configurados quedan guardados y enviados al servidor.
* El sistema aplica la nueva configuración de forma global.

---

### **Flujo principal**

1. El administrador accede al módulo de configuración del sistema.
2. El sistema muestra los parámetros configurables disponibles.
3. El administrador modifica los valores deseados.
4. El sistema valida los datos introducidos.
5. El sistema envía la configuración al servidor.
6. El sistema confirma que los cambios han sido aplicados correctamente.

---

### **Flujos alternativos**

* Los valores introducidos no cumplen las restricciones definidas.
* Error de comunicación con el servidor.
* El administrador cancela la operación antes de confirmar los cambios.

---

### **Reglas de negocio**

* Solo los usuarios con rol de administrador pueden acceder a este módulo.
* Los valores introducidos deben respetar los límites y formatos definidos.
* Los cambios de configuración afectan al comportamiento global del sistema.

---

## 🧠 2. Fase de Análisis — Diagrama de Análisis del Cliente

El siguiente diagrama representa la estructura lógica del lado cliente para el caso de uso **CU-16**, mostrando la interacción entre la interfaz de usuario, los controladores de aplicación y las entidades utilizadas para gestionar la configuración del sistema.

![Diagrama Analisis](./diagramas-cliente/analisis-gf7-cliente.png)

---

## 📌 Consideración del Requisito No Funcional RNF-10

**RNF-10 — Interoperabilidad**

El cliente debe estar diseñado para permitir la integración con otros servicios universitarios externos, tales como:

* Sistemas académicos.
* Bases de datos institucionales.
* Servicios de estadísticas y gestión docente.

Este requisito no funcional condiciona el diseño del cliente, asegurando que los datos de configuración y las solicitudes se envían mediante interfaces estándar y mecanismos compatibles con servicios externos.

---


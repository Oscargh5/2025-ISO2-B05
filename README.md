# ISOII-B05
# 🧩 Diagrama de Clases del Servidor (GF5)

El siguiente diagrama representa la *estructura interna del servidor* para el Grupo Funcional 5.
En él se definen las capas, las entidades principales, los controladores de dominio y los repositorios que permiten al backend gestionar asignaturas, bibliografía y grupos académicos.

El objetivo de esta fase es preparar la *arquitectura que será implementada en la siguiente iteración*, asegurando separación por capas, claridad en las responsabilidades y cumplimiento de los requisitos funcionales RF-06, RF-07, RF-08, RF-09 y RF-10.

---

## Estructura del Servidor por Capas

El servidor sigue una arquitectura en *tres capas*, donde cada una tiene un rol específico en la ejecución de los casos de uso.

---

## 🎨 1. Capa de Presentación (Presentation.server)

Contiene los controladores que reciben las solicitudes desde el cliente para:

* *AsignaturaController*
* *BibliografiaController*
* *GrupoController*

### Funciones principales:::::::::

* Recibir peticiones (crear grupo, asociar bibliografía, registrar asignatura…)
* Validar datos básicos
* Llamar a los controladores de dominio
* Devolver la respuesta al cliente

> Esta capa solo gestiona, *no lógica de negocio*.

---

## 🧠 2. Capa de Dominio (Domain.server)

Es el núcleo del sistema. Incluye las *entidades* y los *controladores de lógica de negocio* que implementan los casos de uso del servidor.

### ✔ Entidades modeladas

* *Asignatura*
* *BibliografiaEspecifica*
* *GrupoEstudio*
* *GrupoInvestigacion*
* *Usuario*, con roles diferenciados:

  * Profesor
  * Estudiante

Cada entidad representa información gestionada por los requisitos del GF5.

### ✔ Controladores de dominio

* *ControlAsignatura* (SRV-07)
* *ControlBibliografia* (SRV-08)
* *ControlGrupoEst* (SRV-09)
* *ControlGrupoInv* (SRV-10)
* *ControlRegistroEstGr* (SRV-06)

### Responsabilidades

* Validar reglas de negocio
* Verificar permisos según rol (profesor, administrador, bibliotecario)
* Comprobar unicidad, pertenencia y relaciones entre entidades

> Aquí se ejecuta toda la lógica interna del servidor.

---

## 🗃️ 3. Capa de Persistencia (Persistence.server)

Contiene los repositorios responsables de almacenar y recuperar datos:

* *AsignaturaRepository*
* *BibliografiaRepository*
* *GrupoRepository*
* *UsuarioRepository*

### Funciones:

* Consultas, inserciones y actualizaciones en la BD
* Proveer información al dominio
* Mantener encapsulada la lógica de persistencia

> El dominio nunca accede directamente a la base de datos: siempre pasa por los repositorios.

---

## 📌 Relación con los Casos de Uso del Servidor

Este diseño soporta los casos internos del GF5:

| Caso de Uso                                 | Controlador          | Entidades Relacionadas             |
| ------------------------------------------- | -------------------- | ---------------------------------- |
| *SRV-06* Registrar unión a grupo          | ControlRegistroEstGr | Estudiante, GrupoEstudio           |
| *SRV-07* Validar y registrar asignatura   | ControlAsignatura    | Asignatura, Profesor               |
| *SRV-08* Asociar bibliografía             | ControlBibliografia  | Asignatura, BibliografiaEspecifica |
| *SRV-09* Registrar grupo de estudio       | ControlGrupoEst      | GrupoEstudio, Asignatura           |
| *SRV-10* Registrar grupo de investigación | ControlGrupoInv      | GrupoInvestigacion, Profesor       |

---

# 🖼️ Diagrama de Clases del Servidor

![Diagrama de Clases del Servidor GF5](./DiagramasServidor/Diagrama-Clases-Servidor.jpg)
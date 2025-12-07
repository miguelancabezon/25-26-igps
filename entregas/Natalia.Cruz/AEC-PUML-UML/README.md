# Sistema de Gestión de Biblioteca Universitaria

##  Descripción del Proyecto

Sistema de gestión integral para la Biblioteca Central de la Universidad que permite a estudiantes y profesores realizar préstamos de libros, gestionar reservas y manejar devoluciones. El sistema controla el estado de cada préstamo desde su solicitud hasta su finalización, con diferentes operaciones según el rol del usuario.

##  Objetivos

- Modelar un sistema completo usando diferentes tipos de diagramas UML
- Practicar la creación de diagramas de objetos, casos de uso y estados
- Comprender las relaciones entre diferentes vistas del sistema
- Aplicar PlantUML en un caso de uso real

## Diagramas UML

### 1. Diagrama de Casos de Uso

<div align=center>

| Descripción | Diagrama |
|:------------|:--------:|
| **Propósito:** Modelar las interacciones entre los actores del sistema (Estudiante, Profesor, Bibliotecario y Sistema) y las funcionalidades disponibles.<br><br>**Características principales:**<br>- 4 actores del sistema<br>- 16 casos de uso organizados en packages<br>- Gestión de préstamos, reservas, búsqueda y penalizaciones<br>- Generación de reportes para bibliotecarios | ![Diagrama de Casos de Uso](./imagenes/01-diagrama-casos-uso.svg) |
| | Código fuente: [01-diagrama-casos-uso.puml](./diagramas/01-diagrama-casos-uso.puml) |

</div>

---

### 2. Diagrama de Objetos

<div align=center>

| Descripción | Diagrama |
|:------------|:--------:|
| **Propósito:** Representar una instancia concreta del sistema en un momento específico (15 Nov 2025, 14:30h), mostrando objetos reales y sus relaciones.<br><br>**Escenario modelado:**<br>- 3 usuarios (2 estudiantes, 1 profesor)<br>- 5 libros del catálogo de programación<br>- 5 préstamos en diferentes estados<br>- 2 reservas pendientes<br>- 1 multa por préstamo vencido<br><br>**Relaciones implementadas:**<br>- Composición, Agregación, Dependencia y Asociación | ![Diagrama de Objetos](./imagenes/02-diagrama-objetos.svg) |
| | Código fuente: [02-diagrama-objetos.puml](./diagramas/02-diagrama-objetos.puml) |

</div>

---

### 3. Diagrama de Estados

<div align=center>

| Descripción | Diagrama |
|:------------|:--------:|
| **Propósito:** Modelar el ciclo de vida completo de un préstamo, desde su creación hasta su finalización, incluyendo todos los estados posibles y transiciones.<br><br>**Estados principales:**<br>- Solicitado (pendiente aprobación)<br>- En Curso (Activo, Renovado, Vencido)<br>- Devuelto / Cancelado (estados finales)<br><br>**Características:**<br>- Estados compuestos con subestados<br>- Puntos de decisión para renovaciones<br>- Eventos temporales (vencimiento a 14 días)<br>- Multas diferenciadas por tipo de usuario<br>- Máximo 2 renovaciones por préstamo | ![Diagrama de Estados](./imagenes/03-diagrama-estados.svg) |
| | Código fuente: [03-diagrama-estados.puml](./diagramas/03-diagrama-estados.puml) |


</div>

---

## Reglas de Negocio del Sistema

### Préstamos para Estudiantes
- ✅ Máximo 3 libros simultáneos
- ⏱️ Duración: 14 días
- 🔄 Renovaciones: hasta 2 veces (si no hay reservas)
- 💶 Multa por retraso: €0.50/día

### Préstamos para Profesores
- ✅ Máximo 5 libros simultáneos
- ⏱️ Duración: 30 días
- 🔄 Renovaciones: hasta 2 veces
- 💶 Multa por retraso: €0.30/día

### Estados de un Libro
- 🟢 Disponible
- 🔵 Prestado
- 🟡 Reservado
- 🔴 En Mantenimiento

### Estados de un Préstamo
- 📝 Solicitado
- ✅ Activo
- 🔄 Renovado
- ⚠️ Vencido
- ✔️ Devuelto
- ❌ Cancelado

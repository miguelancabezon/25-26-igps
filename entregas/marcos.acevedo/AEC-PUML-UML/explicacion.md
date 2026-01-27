# Explicación de Diseño – Sistema de Gestión de Biblioteca
**Universidad – Proyecto UML**  
**Fecha:** 8/12/2025

---

# 1. Introducción
Este documento explica las decisiones de diseño tomadas para los tres diagramas UML entregados:

- Diagrama de Casos de Uso
- Diagrama de Objetos
- Diagrama de Estados (Ciclo de vida del préstamo)

El objetivo es justificar la estructura, la organización y las relaciones utilizadas para modelar correctamente el sistema de gestión de la biblioteca.

---

# 2. Decisiones de Diseño – Casos de Uso

## 2.1 Actores Escogidos
Se incluyeron los siguientes actores principales para reflejar todos los roles del sistema:

- **Estudiante:** Principal usuario del sistema; puede buscar libros, solicitar préstamos, renovar, reservar y pagar multas.
- **Profesor:** Similar al estudiante, pero con más privilegios (mayor número de préstamos y duración).
- **Bibliotecario:** Gestiona todas las operaciones administrativas y de control, incluyendo registro de préstamos, devoluciones, multas y reportes.
- **Sistema de Notificaciones:** Actor automatizado que envía alertas sobre reservas, vencimientos y multas.

## 2.2 Agrupación de Casos de Uso
Se organizaron los casos de uso en paquetes para mayor claridad:

- **Búsqueda y Consulta:** Buscar libros, ver historial y consultar estado de libro.
- **Gestión de Préstamos:** Solicitar, renovar, devolver, registrar y procesar préstamos.
- **Gestión de Reservas:** Hacer, cancelar reservas y notificar disponibilidad.
- **Penalizaciones:** Calcular, pagar y aplicar multas.
- **Reportes:** Generar reportes de préstamos y multas.

Esta agrupación ayuda a visualizar rápidamente las responsabilidades y la relación de cada actor con el sistema.

## 2.3 Relaciones
- Se utilizaron flechas `-->` para mostrar interacciones directas.
- Se agregaron relaciones complejas con etiquetas, por ejemplo, las notificaciones automáticas de disponibilidad de libros a los estudiantes.

---

# 3. Decisiones de Diseño – Diagrama de Objetos

## 3.1 Escenario
El diagrama de objetos representa una **instancia concreta del sistema** en la fecha 15/11/2025 a las 14:30h, con varios préstamos activos y reservas pendientes.

## 3.2 Objetos Seleccionados
- **Usuarios:** 2 estudiantes y 1 profesor, con atributos reales como ID, nombre, email, préstamos activos y multas acumuladas.
- **Libros:** 5 libros con ISBN, título, autor, ejemplares y disponibilidad.
- **Préstamos:** 4 préstamos con fechas, estado, renovaciones y multas.
- **Reservas:** 2 reservas activas con posición en cola.
- **Multa:** 1 multa asociada a un préstamo vencido.

## 3.3 Relaciones
- Cada usuario tiene sus préstamos asignados.
- Cada préstamo apunta al libro correspondiente.
- Reservas vinculadas a libro y usuario.
- Multa asociada a préstamo y usuario.
- Estas relaciones permiten visualizar la instancia real y las interacciones entre objetos.

---

# 4. Decisiones de Diseño – Diagrama de Estados

## 4.1 Estados del Préstamo
Se definieron los estados completos del ciclo de vida del préstamo:

- Solicitado
- Activo
- Renovado
- Vencido
- Devuelto
- Cancelado
- Estado final [*]

Se creó un **estado compuesto “En Curso”** que agrupa Activo, Renovado y Vencido, para simplificar la visualización de préstamos activos.

## 4.2 Transiciones y Acciones
- Las transiciones incluyen aprobaciones, rechazos, renovaciones, devoluciones y vencimientos.
- Se implementaron etiquetas como `[libro disponible]` y `[renovaciones < 2]` para reflejar reglas de negocio.
- Se añadieron acciones `entry` y `exit` para reflejar notificaciones automáticas, actualización de disponibilidad, cálculo de multas y liberación de libros.

## 4.3 Estados Especiales
- Estado inicial: [*]
- Estado final: [*]
- Estado de decisión [choice]: para verificar renovaciones
- Historia [H]: recuerda el último subestado dentro de “En Curso”

---

# 5. Consideraciones Generales
- Se priorizó la **claridad y consistencia** de colores y estilos entre diagramas.
- Se utilizó PlantUML para mantener los diagramas fácilmente editables y reproducibles.
- Cada diagrama refleja tanto la **estructura** del sistema como las **reglas de negocio** de la biblioteca universitaria.


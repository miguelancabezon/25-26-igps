# Decisiones de diseño - Diagrama de Estados "Ciclo de Vida del Préstamo"

## 1. Propósito y Alcance

El diagrama representa el ciclo completo de un préstamo en la Biblioteca Central, desde la creación (solicitado) hasta su finalización o cancelación, incluyendo todos los posibles estados y transiciones requeridos por las reglas de negocio de la biblioteca universitaria.

## 2. Estados Principales

Se definieron los estados requeridos:
- **Solicitado**: Estado inicial tras la petición del usuario.
- **Activo**: Préstamo aprobado y en curso.
- **Renovado**: Préstamo ampliado tras una renovación.
- **Vencido**: El plazo de devolución se ha superado.
- **Devuelto**: El préstamo se ha completado exitosamente.
- **Cancelado**: Se cancela antes de activarse.
- **VencidoCrítico**: Préstamos vencidos de más de 30 días.
- **Estado inicial y final ([*])**: Para representar el inicio y término del proceso.

## 3. Estructura Compuesta

Para una visión realista y mantenible, se usó un **superestado "En Curso"** que agrupa los subestados _Activo, Renovado y Vencido_. De esta forma, se muestran claramente los posibles caminos de un préstamo una vez aprobado.  
Esto facilita el mantenimiento del diagrama y la percepción del ciclo principal del préstamo.

## 4. Acciones y Eventos

Se utilizaron acciones en las entradas y salidas de los estados clave (_entry_, _exit_) para dejar claro el efecto en el sistema:
- Ejemplo: `entry/enviarEmailConfirmacion()` en "Activo" muestra que el usuario recibe una notificación al activarse.
- Multa y notifición automática en "Vencido".
- Acciones de liberar libro y procesar reservas en "Devuelto".

## 5. Transiciones y Reglas de Negocio

Todas las transiciones incluyen condiciones y etiquetas explicativas para reflejar las reglas reales. Ejemplos:
- Solo se puede renovar si hay menos de 2 renovaciones y sin reservas pendientes.
- Se aplica multa al devolver después de la fecha.
- Se cancela si el libro no está disponible o por decisión del usuario.

Las condiciones están especificadas en las transiciones para mayor claridad del flujo.

## 6. Sintaxis y PlantUML

Se respetaron las reglas de anidamiento de PlantUML, definiendo correctamente estados compuestos y cerrando todos los bloques.  
Se unificó la paleta de colores para facilitar la legibilidad y diferenciar agrupaciones y tipos de estado.  
Sólo se emplearon alias y estereotipos donde son válidos en PlantUML (si lo requieres, pueden extenderse más para integración con otras herramientas).

## 7. Extensibilidad

El diagrama está diseñado para poder agregar nuevos estados (por ejemplo, _En Revisión_, _Perdido_) y eventos (fork, history) en el futuro.  
Puede adaptarse fácilmente a nuevos requisitos sin perder legibilidad.

## 8. Legibilidad y Documentación

Cada decisión de estado y transición está acompañada de etiquetas y comentarios para facilitar la comprensión por parte de desarrolladores, diseñadores y stakeholders de la biblioteca.

---

**En resumen:**  
Se modeló el ciclo vital de un préstamo universitario siguiendo estándares UML y la sintaxis correcta de PlantUML, asegurando claridad, extensibilidad y apego a las reglas del negocio real.
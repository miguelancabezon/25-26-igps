# Decisiones de Diseño - Sistema de Biblioteca

## 1. Diagrama de Casos de Uso
- **Herencia de Actores:** Se estableció que el `Profesor` hereda de `Estudiante` para simplificar el diagrama, ya que comparten la base de funcionalidades de préstamo y búsqueda.
- **Paquetes:** Se agruparon los casos de uso por módulos funcionales (Reservas, Reportes, etc.) para mantener la legibilidad y modularidad del sistema.

## 2. Diagrama de Objetos
- **Consistencia de Datos:** Se han instanciado los objetos respetando estrictamente los ID y atributos proporcionados en el enunciado (fecha 15 de Noviembre 2025).
- **Relaciones Cruzadas:** Se modelaron las relaciones entre estudiantes y libros a través de la entidad `Prestamo`, mostrando cómo un usuario puede tener múltiples estados (multas y préstamos activos) simultáneamente.

## 3. Diagrama de Estados
- **Super-estado "En Curso":** Se agrupó `Activo`, `Renovado` y `Vencido` dentro de un estado compuesto para simplificar las transiciones de salida (como la devolución), aunque se mantuvieron las transiciones específicas internas.
- **Choice (Rombo):** Se utilizó un elemento de decisión dinámica para la lógica de "Renovar", permitiendo visualizar gráficamente la condición de `[renovaciones < 2]`.
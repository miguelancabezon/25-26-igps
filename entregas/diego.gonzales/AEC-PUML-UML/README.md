# Decisiones de Diseño - Sistema de Gestión de Biblioteca

## 1. Diagrama de Casos de Uso
- **Herencia de Actores:** Se decidió utilizar una relación de herencia (`<|--`) entre *Estudiante* y *Profesor*. Dado que el Profesor tiene "el mismo acceso que estudiante + extras", esto simplifica el diagrama y evita duplicar flechas para acciones comunes como "Buscar libros" o "Solicitar préstamo".
- **Paquetes:** Se agruparon los casos de uso en paquetes funcionales (Reservas, Reportes, etc.) para mantener la legibilidad y modularidad del sistema.

## 2. Diagrama de Objetos
- **Separación de Responsabilidades:** Se instanciaron objetos separados para *Usuario*, *Préstamo*, *Libro* y *Multa*.
- **Relaciones Cruzadas:** Se muestra explícitamente cómo un usuario (`estudiante1`) puede tener relaciones simultáneas con un préstamo activo (`prestamo1`) y uno vencido con multa (`prestamo3`), cumpliendo el escenario del 15 de Noviembre.
- **Datos Reales:** Los ISBN y IDs se mantuvieron fieles al enunciado para facilitar la trazabilidad.

## 3. Diagrama de Estados
- **Estado Compuesto "En Curso":** Se agruparon los estados *Activo*, *Renovado* y *Vencido* dentro de un super-estado. Esto permite simplificar la transición hacia *Devuelto*, ya que la acción de devolver puede ocurrir desde cualquiera de estos sub-estados.
- **Choice (Rombo):** Se implementó un nodo de decisión `<<choice>>` para la lógica de renovación. Esto visualiza claramente que el sistema evalúa la condición `[renovaciones < 2]` antes de permitir el cambio de estado.
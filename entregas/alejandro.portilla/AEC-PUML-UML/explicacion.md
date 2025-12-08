# README - Entregable AEC-PUML-UML


## Resumen
Este paquete contiene 3 diagramas UML en PlantUML y una breve explicación de las decisiones de diseño. Los diagramas cubren Casos de Uso, Objetos (instancias) y Estados (ciclo de vida del préstamo) para la Biblioteca Central de la Universidad.


## Decisiones de diseño (por diagrama)


### Casos de Uso
- **Actores**: Se incluyeron Estudiante, Profesor, Bibliotecario y el Sistema (como actor que representa notificaciones automáticas). Esto permite mostrar tanto interacciones humanas como procesos automáticos.
- **Agrupación en packages**: Se agruparon casos de uso en paquetes (Búsqueda y consulta, Gestión de Reservar, Penalizaciones, Préstamos, Reportes) para mejorar la legibilidad y cumplir el requisito de agrupación lógica.
- **Relaciones y etiquetas**: Se añadieron etiquetas en relaciones complejas (p.ej. "si falla auto-proceso -> manual") para clarificar flujos alternativos.
- **Cobertura funcional**: Se incluyeron más de 12 casos de uso solicitados en la enunciado y se asignaron roles según reglas de negocio (p.ej. préstamos largos para profesores).


### Diagrama de Objetos
- **Escenario con fecha y hora**: Se modeló el 15/11/2025 14:30 tal como pide el enunciado.
- **Objetos y atributos**: Todos los objetos pedidos están representados (usuarios, libros, préstamos, reservas, multa) con sus atributos concretos.
- **Relaciones**: Se añadieron relaciones solicitadas (p.ej. estudiante1 tiene prestamo1 y prestamo3) y distintos tipos de enlaces: asociación directa, dependencia y flechas coloreadas para resaltar relaciones importantes (p.ej. multa generada por un préstamo vencido).
- **Notas explicativas**: Pequeñas notas ayudan a entender
# Decisiones de diseño - AEC PUML UML


**Resumen:**
Se han creado tres diagramas PlantUML (Casos de Uso, Objetos y Estados) y un breve documento de decisiones. Las decisiones más relevantes son:


- **Casos de uso:** He agrupado funcionalidades en paquetes lógicos: "Búsqueda y consulta", "Gestión de Reservas", "Penalizaciones", "Préstamos" y "Reportes". El actor "Sistema" (renombrado Notificador) modela acciones automáticas (notificaciones y cálculos programados).


- **Objetos:** El diagrama de objetos representa una foto fija del sistema a fecha 15-11-2025 14:30. Incluye las instancias indicadas en el enunciado (usuarios, libros, préstamos, reservas y multa) y relaciones entre ellos. He usado atributos literales para facilitar trazabilidad.


- **Estados:** El ciclo de vida del préstamo incluye el super-estado "En Curso" (Activo, Renovado, Vencido). Se han añadido entry/exit actions tal y como pedía el enunciado. También se ha mostrado un ejemplo de uso de fork/join para representar acciones paralelas (p.ej. aprovisionamiento + notificación).


**Notas sobre reglas de negocio implementadas en los diagramas:**
- Renovaciones controladas por la condición [renovaciones < 2] y comprobación de reservas pendientes.
- Penalizaciones y cálculo de multas se representan como acciones de entrada al estado Vencido.
- El actor Bibliotecario puede forzar préstamos (registrar manualmente) y aplicar penalizaciones.


**Sugerencias para entrega:**
1. Copia cada bloque de código a su archivo `.puml` correspondiente: `aec-puml-casosUso.puml`, `aec-puml-objetos.puml`, `aec-puml-estados.puml`.
2. Comprueba render con PlantUML (online o local) y ajusta colores si tu plataforma de entrega exige estilos particulares.
3. Guarda los tres archivos y este markdown `AEC_PUML_DISEÑO.md` en: `entregas > nombre.apellido > AEC-PUML-UML`.






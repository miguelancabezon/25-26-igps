Filename: README_diseno.md
# Diseño y notas para entrega (Biblioteca Central)

## Archivos incluidos
- `casos_de_uso.puml` — Diagrama de Casos de Uso (PlantUML).
- `diagrama_objetos.puml` — Diagrama de Objetos para el escenario 15/11/2025 14:30.
- `diagrama_estados.puml` — Diagrama de Estados (ciclo de vida del préstamo).
- `README_diseno.md` — Este archivo: decisiones de diseño y recomendaciones.

## ¿Por qué 4 archivos?
La especificación pedía 3 archivos `.puml` (uno por diagrama). Añadí este `README_diseno.md` con las decisiones de diseño y el procedimiento para renderizar, ya que la especificación extra pedía "Incluir un documento markdown explicando decisiones de diseño". Si prefieres **no** incluir este MD, me lo dices y lo convierto en un comentario dentro de uno de los `.puml`.

## Decisiones de diseño (resumen)
- **Separación por paquetes** en el diagrama de casos de uso para mejorar la legibilidad: *Búsqueda y consulta*, *Gestión de Reservar*, *Penalizaciones*, *Préstamos y Devoluciones*, *Reportes*.
- **Actor Sistema** claramente representado para procesos automáticos (notificaciones, cálculos nocturnos).
- **Relaciones y etiquetas**: añadí etiquetas explicativas en relaciones críticas (ej. rechazo de renovación por reservas).
- **Diagrama de objetos** modela un snapshot real con 15+ objetos solicitados, atributos literales y asociaciones claras (prestamo → libro, reserva → libro/usuario, multa → prestamo/usuario).
- **Estado compuesto "En Curso"**: agrupa Activo, Renovado y Vencido. Uso de `[H]` (history) para recordar el subestado anterior al salir/volver.
- **Transiciones**: incluí las 12+ transiciones solicitadas, con guards como `[renovaciones < 2 AND sin reservas pendientes]` y eventos temporales (`after 14 days`, `after 30 days`) tal como pediste.
- **Acciones (entry/exit)**: implementadas en Activo, Vencido y Devuelto con los nombres de las funciones tal como pediste.
- **Fork/Join**: modelado para representar la ejecución paralela (liberar libro y procesar siguiente reserva al devolver).
- **Estética**: parámetros `skinparam` para color de fondo y consistencia visual entre diagramas.

## Cómo renderizar (PlantUML)
1. Tener Java instalado y PlantUML (o usar una extensión VSCode: PlantUML).
2. Desde la terminal:
   - `plantuml casos_de_uso.puml`
   - `plantuml diagrama_objetos.puml`
   - `plantuml diagrama_estados.puml`
3. Generará imágenes `.png` (o `.svg` si configuras `-tsvg`).
4. Si usas VSCode + PlantUML: abrir el `.puml` y elegir "Preview Current Diagram".

## Notas finales y recomendaciones
- Revisa los textos de notas y etiquetas si tu profesor exige un lenguaje más formal o localizaciones distintas.
- Si quieres, puedo:
  - Generar versiones en español/inglés alternas.
  - Convertir el `README` a PDF o integrarlo como comentario dentro de cada `.puml`.
  - Ajustar colores o tamaños para impresión.
- Si necesitas que empaquete todo en un ZIP listo para entregar, dímelo (te diré exactamente los pasos o, si usas mi entorno, podría generar el zip localmente).

---

Si quieres que los combine en un único archivo con `@startuml` / `@enduml` múltiples diagramas, o que genere imágenes directamente para descargar, dime cómo prefieres la entrega y lo adapto ahora mismo.

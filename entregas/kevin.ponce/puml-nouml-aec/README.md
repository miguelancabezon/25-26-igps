# Documentación del directorio `puml-nouml-aec`

_Este README resume los archivos presentes en este directorio y explica su propósito y cómo renderizarlos._

## Ubicación

`entregas/kevin.ponce/puml-nouml-aec/`

## Autor

Kevin Ponce (información incluida en algunos diagramas).

---

## Archivos y descripción

- `diagrams-json.puml`
  - Contenido: un bloque JSON ( delimitado con `@startjson` / `@endjson` ) que describe metadatos del proyecto y definiciones de clases/objetos para un juego FPS.
  - Qué incluye: información general (name, version, description), objeto `author`, `metadata`, y un arreglo `classes` con ejemplos (Weapon, Character, Level, GameMechanic). También contiene `actions` que describen operaciones como `createCharacter`, `equipWeapon` y `startLevel`.
  - Uso: referencia estructurada para modelado de objetos del juego o para convertir a otros formatos.

- `Wireframe.puml`
  - Contenido: un wireframe escrito con el estilo SALT de PlantUML que muestra un boceto de la interfaz (menú principal) con componentes como: Home, Inventory, Shop, Settings, Leaderboard; buscador; tabla de inventario; tarjeta de jugador; acciones rápidas.
  - Uso: referencia visual rápida para el diseño de la UI/UX del menú principal.

- `Gantt.puml`
  - Contenido: un diagrama Gantt que describe el cronograma de desarrollo del videojuego FPS (fases: Preproducción, Producción, Postproducción), tareas, porcentajes completados, notas de equipo y dependencias entre tareas.
  - Uso: planificación y seguimiento de hitos (milestones) como Prototipo, Beta y v1.0.

- `fps-mindmap.puml`
  - Contenido: un mapa mental (mindmap) que organiza la visión general del juego: gameplay, motor/tech, arte/audio, infraestructura/ops, equipo/roles, riesgos y áreas transversales como seguridad, monetización y QA.
  - Uso: visión estratégica y organización de áreas del proyecto.

---

## Cómo renderizar los diagramas

Estos archivos están escritos para PlantUML. Algunas formas comunes de renderizarlos:

- Usando la utilidad de PlantUML (si tienes `plantuml` o `plantuml.jar`):

```bash
# Generar PNG para un archivo
plantuml Wireframe.puml

# O con el jar de PlantUML
java -jar plantuml.jar Gantt.puml
```

- Usando la extensión PlantUML en VS Code (recomendado para vista previa rápida): instala la extensión "PlantUML" y abre el archivo `.puml`, luego usa la vista previa.

- Servicio en línea: puedes pegar el contenido en https://www.plantuml.com/plantuml/ o usar servicios compatibles para generar imágenes desde el texto.

Notas:
- `diagrams-json.puml` usa `@startjson`/`@endjson` (es un bloque tipo JSON). Dependiendo de la versión de PlantUML o la extensión, el renderizado específico para `json` puede variar; si la extensión no soporta ese tipo, trata el archivo como referencia de datos (no como diagrama visual directamente) o conviértelo a un diagrama UML/JSON compatible.

---

## Recomendaciones

- Mantener los archivos `.puml` actualizados con cambios en diseño o cronograma.
- Si compartes estas imágenes en la web o en presentaciones, exporta a PNG o SVG para mejor compatibilidad.

---

Si quieres, puedo:

- Generar las imágenes (PNG/SVG) de cada `.puml` y añadirlas a este directorio.
- Añadir un `Makefile` o script `render.sh` para automatizar la generación de imágenes.

Indica qué prefieres y lo hago a continuación.

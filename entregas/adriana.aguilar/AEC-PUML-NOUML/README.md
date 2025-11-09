# 🎮 Planificación "PicoHelado" - Juego de Survival

## 📋 Descripción del Proyecto

**PicoHelado** es un juego de supervivencia ambientado en un mundo helado y hostil donde el jugador debe recolectar recursos, craftear herramientas, construir refugios y sobrevivir a las condiciones extremas mientras explora un vasto territorio congelado.

---

## 🗂️ Estructura de Archivos

Este proyecto contiene 4 diagramas PlantUML NoUML que documentan la planificación completa del videojuego:

### 1. 🗺️ Mindmap (`1_mindmap.puml`)
Mapa mental que organiza todos los aspectos del juego en categorías:
- **Mecánicas Centrales**: Crafteo, Construcción, Combate
- **Sistemas del Jugador**: Estadísticas, Inventario, Progreso
- **El Mundo**: Exploración, Biomas, Entorno Dinámico
- **Aspectos Técnicos**: IA, Renderizado, Backend

**Características:**
- ✅ Más de 10 colores diferentes
- ✅ 4 niveles de profundidad
- ✅ Uso de ambos lados del mindmap
- ✅ Emojis y símbolos integrados

### 2. 📅 Diagrama de Gantt (`2_gantt.puml`)
Planificación temporal completa del desarrollo:
- **Fase 1 - Preproducción**: Investigación, diseño conceptual, prototipado
- **Fase 2 - Producción**: Desarrollo del motor, assets, niveles, IA
- **Fase 3 - Postproducción**: Testing, optimización, lanzamiento

**Características:**
- ✅ 17 tareas con dependencias
- ✅ 3 milestones: Prototipo, Beta, v1.0
- ✅ Colores por categoría
- ✅ Porcentajes de completado
- ✅ Notas con recursos y equipos

### 3. 📦 Diagrama JSON (`3_json.puml`)
Estructura de datos del sistema de juego:

**Clases definidas:**
- `PlayerState`: Estado del jugador (salud, hambre, sed, posición)
- `GameItem`: Items genéricos del juego
- `WeaponItem`: Armas con estadísticas de combate
- `PlayerInventory`: Sistema de inventario
- `CraftingRecipe`: Recetas de crafteo
- `WorldEnvironment`: Estado del entorno

**Características:**
- ✅ 6 clases/objetos completos
- ✅ Tipos de datos variados (string, number, boolean, array, object)
- ✅ Fechas en formato ISO 8601
- ✅ 5 acciones/métodos con validaciones
- ✅ Metadata y configuración del sistema
- ✅ Notación camelCase consistente

### 4. 🖼️ Wireframe/Salt (`4_wireframe.puml`)
Interfaz de usuario del menú de crafteo:

**Componentes:**
- 4 tabs: Crafteo, Inventario, Construcción, Estadísticas
- 2 tablas de datos: Recursos necesarios e inventario del jugador
- Panel lateral con árbol de categorías craftables
- Minimapa con iconos de ubicación
- Sistema de barras de estado del jugador
- Hotbar de acceso rápido

**Características:**
- ✅ Layout libre y organizado
- ✅ Más de 10 elementos interactivos (botones, checkboxes, radio buttons)
- ✅ Símbolos y emojis abundantes
- ✅ Información contextual del jugador

---

## 📊 Información Técnica

| Aspecto | Detalle |
|---------|---------|
| **Nombre** | PicoHelado |
| **Género** | Survival 🍖 |
| **Plataforma** | PC, Consolas |
| **Modo de Juego** | Single-player + Co-op (hasta 4 jugadores) |
| **Motor** | Unity 2023.2 |
| **Estado Actual** | Pre-producción → Producción (Alpha 0.3.0) |
| **Idioma** | Español (ES-ES) |
| **Región Servidor** | EU-West |

---

## 🎯 Mecánicas Principales

### Supervivencia
- **Estadísticas vitales**: Salud, Hambre, Sed, Temperatura, Energía
- **Gestión de recursos**: Recolección, almacenamiento, consumo
- **Ciclo día/noche**: Impacto en temperatura y peligros

### Crafteo y Construcción
- **Sistema de crafteo modular**: Estaciones de trabajo (Hoguera, Banco, Forja)
- **Construcción de bases**: Refugios modulares con cimientos, paredes, techos
- **Árbol de desbloqueo**: Progresión de recetas por nivel

### Combate y Exploración
- **Fauna hostil**: Lobos, osos con IA avanzada
- **Armas variadas**: Cuerpo a cuerpo (hachas, lanzas) y a distancia (arcos)
- **Biomas diversos**: Tundra, bosque nevado, glaciar, montañas
- **Puntos de interés**: Cuevas, cabañas abandonadas, refugios militares

---

## 👥 Equipo de Desarrollo

### Pre-producción (Completado)
- 2 Analistas de mercado
- 3 Diseñadores de juego
- 3 Artistas conceptuales
- 2 Ingenieros senior

### Producción (En curso)
- 5 Programadores de motor
- 4 Programadores de gameplay
- 2 Programadores de IA
- 4 Modeladores 3D
- 2 Animadores
- 3 Diseñadores de niveles
- 2 Diseñadores de sonido
- 1 Compositor

### Post-producción (Planificado)
- 5 QA Testers
- 2 Marketing Specialists
- 2 DevOps Engineers

---

## 📅 Cronograma

| Fase | Duración | Estado |
|------|----------|--------|
| **Preproducción** | 2 meses | 90% ✅ |
| **Producción** | 6 meses | 35% 🔄 |
| **Postproducción** | 2 meses | 0% ⏳ |

### Milestones
- ✅ **Prototipo** - Diciembre 2025
- 🔄 **Beta** - Junio 2026
- ⏳ **v1.0** - Agosto 2026

---

## 🛠️ Cómo Visualizar los Diagramas

### Opción 1: VS Code con PlantUML Extension
1. Instalar la extensión "PlantUML" en VS Code
2. Abrir cualquier archivo `.puml`
3. Presionar `Alt+D` para previsualizar

### Opción 2: PlantUML Online
1. Visitar: https://www.plantuml.com/plantuml/uml/
2. Copiar el contenido de cualquier archivo `.puml`
3. Pegar y visualizar

### Opción 3: Desde el archivo Markdown
El archivo `Planificacion_Survival.md` contiene todos los diagramas integrados con documentación completa.

---

## 📝 Requisitos Cumplidos

### ✅ Mindmap
- [x] Estilos personalizados
- [x] +5 colores diferentes
- [x] 3+ niveles de profundidad
- [x] Emojis y símbolos
- [x] Ambos lados del mapa

### ✅ Gantt
- [x] 15+ tareas
- [x] Colores por categoría
- [x] Dependencias entre tareas
- [x] Notas con recursos/equipo
- [x] Porcentajes de completado
- [x] 3 milestones

### ✅ JSON
- [x] 4+ clases/objetos
- [x] Atributos básicos (id, nombre, fecha, estado)
- [x] Objetos anidados
- [x] Colores aplicados
- [x] Tipos de datos variados
- [x] Fechas en formato ISO
- [x] Objeto "actions" con métodos
- [x] Metadata/config incluidos
- [x] Notación camelCase

### ✅ Wireframe/Salt
- [x] Layout libre
- [x] 1+ tabla de datos
- [x] Tabs incluidos
- [x] 5+ elementos interactivos
- [x] Símbolos y emojis

---

## 👤 Autor

**Adriana Aguilar**  
Ingeniero de Software - Planificación de Videojuegos  
Fecha: Noviembre 8, 2025

---

## 📄 Licencia

Este proyecto es parte de una actividad de evaluación continua para el curso de Ingeniería de Software.
Todos los diagramas y documentación son propiedad del autor.

---

## 🔗 Enlaces Útiles

- [PlantUML Documentation](https://plantuml.com/)
- [PlantUML Salt Guide](https://plantuml.com/salt)
- [PlantUML JSON Diagram](https://plantuml.com/json)
- [PlantUML Gantt Diagram](https://plantuml.com/gantt-diagram)
- [PlantUML Mindmap](https://plantuml.com/mindmap-diagram)

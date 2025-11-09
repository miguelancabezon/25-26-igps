# 🎮 AEC-PUML-NOUML - Proyecto FPS Táctico

**Estudiante:** Eduardo Cubias
**Asignatura:** Introducción a la Gestión de Proyectos de Software
**Actividad:** Evaluación Continua - PlantUML NoUML
**Género seleccionado:** FPS (First Person Shooter)

---

## Descripción del Proyecto

Este proyecto consiste en la planificación completa de un videojuego FPS táctico competitivo llamado **"Tactical Ops"**. El juego está inspirado en títulos como Counter-Strike, Valorant y Rainbow Six Siege, con un enfoque en el combate táctico 5v5 y mecánicas de habilidades únicas por operador.


## Diagramas Incluidos

### 1Mindmap - Planificación del FPS
**Archivo:** `01-mindmap-fps.puml`

Mapa conceptual que organiza todos los aspectos del juego en 5 categorías principales:

- **Mecánicas de Juego**: Sistema de armas, movimiento, tácticas
- **Arquitectura Técnica**: Motor (Unreal Engine 5), networking, plataformas
- **Arte & Diseño Visual**: Estilo realista, mapas, personajes
- **Sistema Multijugador**: Modos de juego, matchmaking, comunicación
- **Progresión & Monetización**: Niveles, recompensas, tienda

**Cumple con:**
- ✓ Estilos personalizados
- ✓ 5+ colores diferentes
- ✓ 3+ niveles de profundidad (hasta 5 niveles)
- ✓ Emojis y símbolos
- ✓ Ambos lados del mindmap

---

### Gantt - Timeline de Desarrollo
**Archivo:** `02-gantt-timeline.puml`

Planificación temporal del desarrollo del juego dividida en 3 fases principales:

#### ° Fase 1: Preproducción (84 días)
- Concepto y documento de diseño
- Investigación de mercado
- Prototipos de movimiento y disparo
- Arte conceptual

#### ° Fase 2: Producción (252 días)
- Desarrollo de 3 mapas iniciales
- Sistema completo de armas (15 armas)
- 12 Operadores con animaciones
- Sistema multijugador y matchmaking
- UI/UX, modos de juego, progresión
- Battle Pass y tienda

#### ° Fase 3: Postproducción (98 días)
- Testing y QA intensivo
- Beta abierta
- Optimización final
- Marketing pre-launch
- Day One Patch

**Hitos:**
- ° Milestone 1: Prototipo Jugable (31 Marzo 2025)
- ° Milestone 2: Beta Cerrada (15 Septiembre 2025)
- ° Milestone 3: v1.0 Launch (26 Enero 2026)

**Cumple con:**
- ✓ 3 fases requeridas
- ✓ 3 hitos (milestones)
- ✓ 20+ tareas
- ✓ Colores por categoría
- ✓ Dependencias entre tareas
- ✓ Notas con recursos/equipo
- ✓ Porcentajes de completado

---

### 3️⃣ JSON - Sistema de Objetos del Juego
**Archivo:** `03-json-game-objects.puml`

Estructura de datos JSON que define los objetos principales del sistema:

#### ° Weapons (Armas)
- AK-47: Rifle de asalto versátil
- AWP Sniper: Francotirador de un disparo
- Sistema de attachments (ópticas, cañones, cargadores)
- Skins y personalización
- Estadísticas de mastery

#### ° Operators (Operadores)
- Hawk: Operador de asalto con dron UAV
- Ghost: Infiltrador sigiloso con invisibilidad
- Loadouts personalizables
- Estadísticas de juego (K/D, win rate)
- Cosméticos y voicepacks

#### ° Maps (Mapas)
- Abandoned City: Urbano mediano
- Factory Complex: Industrial grande
- Puntos estratégicos y dimensiones
- Estadísticas de uso

#### ° Match History
- Registro de partidas
- Información de servidor
- Estadísticas por jugador

#### ° Actions (Acciones disponibles)
Define todas las operaciones posibles:
- `equipWeapon()`, `upgradeWeapon()`, `purchaseSkin()`
- `selectOperator()`, `unlockOperator()`, `customizeOperator()`
- `createMatch()`, `joinMatch()`, `endMatch()`
- `loadMap()`, `voteMap()`

**Cumple con:**
- ✓ 4+ clases/objetos
- ✓ Atributos básicos (id, nombre, fecha, estado)
- ✓ Objetos anidados
- ✓ Colores con highlighting
- ✓ Tipos de datos variados
- ✓ Fechas en formato ISO
- ✓ Objeto "actions" con métodos
- ✓ Campo "metadata"
- ✓ Notación camelCase

---

### 4️⃣ Wireframe - Lobby Principal
**Archivo:** `04-wireframe-lobby.puml`

Diseño completo de la interfaz del lobby principal del juego que incluye:

#### Secciones principales:
- ° **Quick Play**: Selección de modo, mapa, región
- ° **Party System**: Gestión de grupo (2/5 jugadores)
- ° **News & Updates**: Novedades, parches, eventos
- ° **Your Profile**: Nivel, rango, K/D, logros, misiones diarias
- ° **Selected Operator**: Info del operador y habilidades
- ° **Weapon Loadout**: Armas, attachments, equipo, perks
- ° **Customization**: Skins, charms, voice packs
- ° **Leaderboard**: Top players globales
- ° **Chat & Social**: Friends list y comunicación

#### Características de UI:
- Sistema de tabs múltiple
- 3 tablas de datos (Party, Misiones, Leaderboard)
- Barras de progreso (XP, estadísticas)
- Dropdowns para selección
- Botones de acción principales
- Chat en tiempo real
- Friends list con estados

**Cumple con:**
- ✓ Layout complejo libre
- ✓ 3 tablas de datos
- ✓ Múltiples tabs
- ✓ 20+ elementos interactivos
- ✓ Abundantes símbolos/emojis


## 📊 Resumen del Proyecto "Tactical Ops"

### Concepto
FPS táctico competitivo 5v5 con énfasis en trabajo en equipo, habilidades únicas por operador y estrategia.

### Características Principales
- **12 Operadores** únicos con habilidades especiales
- **15 Armas** con sistema de attachments
- **6 Mapas** diversos (urbanos, industriales, militares)
- **5 Modos de juego** (Competitive, TDM, Domination, Gun Game, Infected)
- **Sistema de progresión** completo con Battle Pass
- **Monetización ética** (solo cosméticos, no pay-to-win)

### Plataformas
- PC (Steam, Epic Games)
- PlayStation 5
- Xbox Series X/S
- Cross-play habilitado

### Motor
Unreal Engine 5 (Nanite, Lumen, Ray Tracing)

### Equipo de Desarrollo
~35 personas durante fase de producción

### Duración del Desarrollo
55 semanas (~13 meses)

### Presupuesto Estimado
$2.5M USD

---

## ✅ Verificación de Requisitos

### Mindmap
- [x] Estilos personalizados
- [x] 5+ colores diferentes
- [x] 3+ niveles de profundidad
- [x] Emojis/símbolos
- [x] Ambos lados del mindmap

### Gantt
- [x] 3 Fases (Pre, Pro, Post-producción)
- [x] 3 Hitos (Prototipo, Beta, v1.0)
- [x] 15+ tareas (20+ incluidas)
- [x] Colores por categoría
- [x] Dependencias
- [x] Notas con recursos/equipo
- [x] Porcentajes de completado

### JSON
- [x] 4+ clases/objetos
- [x] Atributos básicos
- [x] Objetos anidados
- [x] Colores
- [x] Tipos de datos variados
- [x] Fechas ISO
- [x] Objeto "actions"
- [x] Campo "metadata"
- [x] Notación camelCase

### Wireframe
- [x] Layout libre
- [x] 1+ tabla de datos (3 incluidas)
- [x] Tabs
- [x] 5+ elementos interactivos (20+ incluidos)
- [x] Símbolos/emojis


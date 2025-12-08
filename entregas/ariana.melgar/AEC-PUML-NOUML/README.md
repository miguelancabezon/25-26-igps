# Pastel Notes - Juego de Ritmo Musical

**Estudiante:** Ariana Melgar
**Asignatura:** Introducción a la Gestión de Proyectos de Software
**Actividad:** AEC-PUML-NOUML
**Género:** Juego de Ritmo

---

## Sobre el Proyecto

**Pastel Notes** es un juego de ritmo musical con estética kawaii y colores pastel. El juego combina mecánicas de ritmo con una historia emotiva protagonizada por Melody, una chica que ama la música y descubre el poder de las melodías para cambiar el mundo.

La inspiración viene de juegos como Cytus, Deemo y Piano Tiles, pero con un toque más dulce y relajante.

---

## Archivos del Proyecto

```
AEC-PUML-NOUML/
├── 01-mindmap-pastel-notes.puml    Mapa de ideas del juego
├── 02-gantt-desarrollo.puml        Planificacion del desarrollo
├── 03-json-objetos-juego.puml      Objetos y sistema del juego
├── 04-wireframe-menu.puml          Diseño del menu principal
└── README.md                        Este archivo
```

---

## 1. Mindmap - Ideas del Juego

**Archivo:** `01-mindmap-pastel-notes.puml`

El mapa mental organiza todas las ideas en 5 categorías con colores pastel:

- **Mecánicas de Juego** (Rosa): Modos, dificultades y controles
- **Música** (Celeste): Géneros musicales y canciones
- **Estilo Visual** (Morado): Arte kawaii y escenarios bonitos
- **Sistema Social** (Amarillo): Amigos, rankings y comunidad
- **Características** (Verde): Progresión, personalización y recompensas

---

## 2. Gantt - Plan de Desarrollo

**Archivo:** `02-gantt-desarrollo.puml`

Timeline de 6 meses para desarrollo indie (Marzo - Septiembre 2025)

### Fase 1: Preproducción (6 semanas)
- Concepto del juego
- Selección de música
- Prototipo jugable

### Fase 2: Producción (16 semanas)
- Arte de personajes y escenarios
- Sistema de notas completo
- 30 canciones implementadas
- UI y menús
- Modo historia

### Fase 3: Postproducción (8 semanas)
- Testing con amigos
- Beta abierta
- Optimización
- Marketing en redes sociales

**Hitos importantes:**
- Milestone 1: Demo Jugable (12 Abril)
- Milestone 2: Beta Cerrada (15 Julio)
- Milestone 3: Lanzamiento v1.0 (10 Septiembre)

---

## 3. JSON - Sistema del Juego

**Archivo:** `03-json-objetos-juego.puml`

Define los objetos principales del juego:

### Canciones
- 30 canciones iniciales en diferentes géneros
- 3 niveles de dificultad (Easy, Normal, Hard)
- Sistema de puntuación y estrellas
- Escenarios únicos por canción

### Personajes
- **Melody**: Protagonista soñadora (Bonus de Combo)
- **Luna**: Pianista misteriosa (Precisión Perfecta)
- **Sakura**: Idol energética (Energía Infinita)

### Jugador
- Sistema de niveles y experiencia
- Gemas y recursos
- Logros desbloqueables
- Estadísticas personales

### Escenarios
- Jardín de Flores
- Cielo Estrellado
- Café Acogedor
- Playa al Atardecer

### Actions
Define operaciones como `playSong()`, `selectCharacter()`, `earnGems()`, etc.

---

## 4. Wireframe - Menú Principal

**Archivo:** `04-wireframe-menu.puml`

Diseño del menú principal del juego con:

### Secciones
- **Modo de Juego**: Historia, Libre, Desafío Diario
- **Personaje**: Selección y estadísticas
- **Escenario**: Cambiar fondo del juego
- **Top Canciones**: Rankings personales
- **Canción Destacada**: Jugar rápido
- **Recursos**: Gemas, monedas, energía
- **Eventos**: Desafíos semanales
- **Novedades**: Actualizaciones

### Elementos
- Tabs de navegación
- 3 tablas (Top Canciones, Ranking Global, Logros)
- Barras de progreso (XP, energía)
- Dropdowns (escenarios, dificultades)
- Botones de acción
- Información en tiempo real

---

## Características del Juego

### Mecánicas Core
- **Tap**: Tocar notas simples
- **Hold**: Mantener presionado
- **Slide**: Deslizar entre notas

### Modos de Juego
- **Modo Historia**: 10 niveles narrativos con Melody
- **Modo Libre**: Practica cualquier canción
- **Desafío Diario**: Retos con recompensas

### Progresión
- Sistema de niveles (1-99)
- Desbloqueo de canciones y personajes
- Colección de stickers y logros
- Rankings globales y entre amigos

### Plataformas
- Mobile (Android/iOS)
- PC (Steam)

---

## Notas de Desarrollo

Este proyecto fue pensado como un juego indie relajante, perfecto para jugadores que buscan una experiencia musical tranquila con estética kawaii. El enfoque está en la música, la historia emotiva y la progresión satisfactoria.

Los colores pastel crean un ambiente acogedor y los personajes tienen personalidades únicas que conectan con diferentes tipos de jugadores.

---

*"La música es el lenguaje del corazón" - Melody*

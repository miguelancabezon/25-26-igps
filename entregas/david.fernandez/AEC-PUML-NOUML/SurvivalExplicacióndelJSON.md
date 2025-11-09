
#  Descripción del archivo JSON 

Este archivo (`game_objects.json`) define las **clases y objetos** principales del juego de supervivencia.

## Clases y atributos

###  Player
- `id`, `name`, `health`, `hunger`, `thirst`
- Contiene una lista de `inventory`
- Tiene coordenadas en el mundo (`position`)

###  Item
- Objetos del juego (armas, comida, herramientas)
- Atributos: `damage`, `durability`, `craftable`

### Enemy
- Enemigos con `species`, `health` y `aggressiveness`
- Sueltan objetos (`loot`) al morir

###  World
- Contiene biomas (`biome`), clima (`weather`) y recursos naturales
- Incluye entidades activas (jugadores y enemigos)

---

##  Acciones disponibles
- `craftItem` → crea objetos nuevos  
- `attackEnemy` → realiza ataque a enemigo  
- `spawnEnemy` → genera enemigos en el mundo  
- `saveGame` → guarda el progreso del jugador

---

##  Metadatos
- `version`: versión del sistema  
- `language`: idioma del juego  
- `environment`: entorno (development, test, production)  
- `author`: equipo desarrollador  
- `createdAt`: fecha ISO del archivo


<!- Archivo: mi-wiki/index.md -->
<!-- Banner centrado con HTML -->
<div align="center">
  <h1>🎮 Mini-Wiki: Emuladores de Videojuegos</h1>
  <p><em>Explora la historia, la tecnología, la ética y los recursos sobre emulación de consolas y sistemas.</em></p>
  <p>
    <img alt="badge-emulators" src="https://img.shields.io/badge/emuladores-v1.0-brightgreen" />
    <img alt="license" src="https://img.shields.io/badge/licencia-CC%20BY--NC--SA-blue" />
    <img alt="contributors" src="https://img.shields.io/badge/contribuidores-1-orange" />
  </p>
</div>

---

## Descripción del proyecto

Este proyecto es una mini-Wiki educativa sobre los emuladores de videojuegos. Está pensada para reunir, explicar y conectar conceptos técnicos, históricos, legales y prácticos relacionados con la emulación de consolas y sistemas. Incluye artículos interconectados, un glosario, referencias y recursos visuales (diagramas Mermaid, tablas y FAQs). El contenido fue creado como entrega académica siguiendo la estructura exigida por el profesor.

---

## Índice visual — Artículos destacados

| Artículo | Resumen |
|---:|:---|
| [📜 Artículo 1: Historia y evolución de los emuladores](articulo-1.md) | Origen, hitos y evolución de las comunidades de emulación. |
| [⚙️ Artículo 2: Arquitectura técnica y componentes](articulo-2.md) | Cómo funcionan los emuladores a nivel técnico. |
| [🕹️ Artículo 3: Emulación de consolas clásicas (NES/SNES)](articulo-3.md) | Técnicas específicas para consolas 8/16-bit. |
| [🚀 Artículo 4: Emuladores modernos y optimizaciones](articulo-4.md) | JIT, recompiler, shaders y mejoras actuales. |
| [⚖️ Artículo 5: Legalidad y ética de los emuladores](articulo-5.md) | Marco legal, derechos, y prácticas responsables. |

---

## Estadísticas del proyecto

- Total de artículos: 5
- Total palabras aproximadas: 12,500+
- Diagramas Mermaid totales (incluyendo timeline y map): 12+
- Tablas (todas las páginas): 25+
- Última actualización global: 2025-10-22

Tabla de estadísticas visuales:

| Métrica | Valor |
|---|---:|
| Artículos | 5 |
| Palabras (aprox.) | 12,500 |
| Diagramas Mermaid | 12 |
| Tablas | 25 |
| Glosario términos | 10 |
| Referencias | 12 |

---

## Timeline general (Mermaid)

```mermaid
gantt
    title Línea de tiempo: hitos clave en emulación
    dateFormat  YYYY
    section Orígenes
    Primeros emuladores (1970s-1980s) :done, a1, 1978,1989
    section Consolidación
    Emulación comunitaria (1990s) :done, a2, 1990,1999
    section Modernización
    Recompiladores y JIT (2000s) :done, a3, 2000,2010
    section Actualidad
    Emulación precisa y compatibilidad (2010s-2025) :active, a4, 2010,2025
```

---

## Mapa conceptual (Mermaid)

```mermaid
flowchart LR
  A[Emuladores] --> B[Arquitectura]
  A --> C[Historia]
  A --> D[Consolas clásicas]
  A --> E[Optimizaciones]
  A --> F[Legalidad]
  B --> B1[CPU emulación]
  B --> B2[GPU/PPU emulación]
  B --> B3[Sistema de archivos]
  E --> E1[JIT]
  E --> E2[Shaders]
  F --> F1[Copyright]
  F --> F2[Preservación]
```

---

## Navegación rápida

- Artículos: [articulo-1.md](articulo-1.md) · [articulo-2.md](articulo-2.md) · [articulo-3.md](articulo-3.md) · [articulo-4.md](articulo-4.md) · [articulo-5.md](articulo-5.md)
- Glosario: [glosario.md](glosario.md)
- Referencias: [referencias.md](referencias.md)
- Recursos: [recursos/imagenes/](recursos/imagenes/)

---

## Artículo destacado del mes

<div style="border:2px dashed #4caf50; padding:10px; border-radius:8px;">
  <h3>🕹️ Artículo destacado: <a href="articulo-3.md">Emulación de consolas clásicas (NES/SNES)</a></h3>
  <p>Incluye un tutorial práctico y comparativa de rendimiento entre emuladores populares. Badge especial:</p>
  <img alt="featured" src="https://img.shields.io/badge/DESTACADO-MES-yellow" />
</div>

---

## Sabías que...?

- Sabías que el primer intento documentado de emulación de consolas caseras data de finales de los 70s? [Ver artículo de historia](articulo-1.md)
- El uso de recompiladores dinámicos (JIT) puede acelerar la emulación en más de 10x en ciertos escenarios. [Más en artículo 4](articulo-4.md)

---

## Contribuidores

- x-name15 — Autor único, redacción, investigación y diagramas.

---

## FAQ (10 preguntas) — bloques colapsables

<details>
<summary>1. ¿Qué es un emulador?</summary>
Respuesta: Un emulador es un software que reproduce el comportamiento de otro sistema, permitiendo ejecutar software original emulado.
</details>

<details>
<summary>2. ¿Los emuladores son legales?</summary>
Respuesta: Depende de jurisdicción y uso; ver [Artículo 5](articulo-5.md) y [Referencias](referencias.md).
</details>

<details>
<summary>3. ¿Qué diferencia hay entre un intérprete y un recompiler (JIT)?</summary>
Respuesta: El intérprete traduce instrucción a instrucción en tiempo de ejecución; el JIT recompila bloques a código nativo para optimizar rendimiento.
</details>

<details>
<summary>4. ¿Cómo aportan los emuladores a la preservación digital?</summary>
Respuesta: Permiten ejecutar y estudiar software y hardware histórico sin necesidad del hardware original; ver [Artículo 1](articulo-1.md).
</details>

<details>
<summary>5. ¿Qué es la precisión en emulación?</summary>
Respuesta: Se refiere a cuán fielmente el emulador reproduce el comportamiento del hardware original, incluyendo timings y efectos colaterales.
</details>

<details>
<summary>6. ¿Qué riesgos de seguridad existen al usar ROMs y emuladores?</summary>
Respuesta: ROMs descargadas pueden contener malware; usa fuentes confiables y verifica hashes.
</details>

<details>
<summary>7. ¿Qué emuladores recomiendan para retrocompatibilidad?</summary>
Respuesta: Depende de la plataforma; ejemplos: FCEUX (NES), Snes9x/bsnes (SNES), PCSX2 (PS2), Dolphin (GameCube/Wii).
</details>

<details>
<summary>8. ¿Cómo contribuye la comunidad al desarrollo de emuladores?</summary>
Respuesta: Mediante contribuciones de código, pruebas de compatibilidad, documentación y preservación de ROMs/BIOS (cuando legalmente permitido).
</details>

<details>
<summary>9. ¿Puedo usar shaders y mejoras gráficas en emuladores?</summary>
Respuesta: Sí; muchos emuladores soportan filtros, escalado por vecinos, y shaders para mejorar la experiencia visual.
</details>

<details>
<summary>10. ¿Dónde encontrar más recursos y documentación técnica?</summary>
Respuesta: Consulta la sección de [Referencias](referencias.md) y cada artículo específico.
</details>

---

## Footer

Autor: x-name15 · Fecha de creación: 2025-10-22 · Versión: 1.0  
↑ <a href="#top">Volver arriba</a>
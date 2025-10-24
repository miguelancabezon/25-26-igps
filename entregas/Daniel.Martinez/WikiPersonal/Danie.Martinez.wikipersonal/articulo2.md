
---
[ Volver a mi-wiki](mi-wiki.md)

#  Aprendizaje Automático

**Ubicación:** Inicio > Conceptos > Aprendizaje Automático  
 **Creado:** 17/10/2025 — 🕒 **Actualizado:** 22/10/2025  
 **Tiempo estimado de lectura:** 7 min  
 **Etiquetas:** `#MachineLearning` `#IA`

---

##  Contenido
1. [Introducción](#introducción)  
2. [Tipos de Aprendizaje](#tipos-de-aprendizaje)  
3. [Ejemplos Prácticos](#ejemplos-prácticos)  
4. [Conclusión](#conclusión)

---

##  Introducción

El **Aprendizaje Automático (Machine Learning)** es una rama de la IA que permite a los sistemas aprender a partir de datos sin ser programados explícitamente.  
Esto se logra mediante **algoritmos** que identifican patrones y realizan predicciones.

> [!NOTE]
> Este artículo está relacionado con [Introducción a la IA](articulo-1.md).

---

##  Tipos de Aprendizaje

|  Tipo |  Descripción |  Ejemplo |
|---------|----------------|------------|
| Supervisado | Aprende con ejemplos etiquetados | Clasificación de correos spam |
| No supervisado | Encuentra patrones ocultos | Agrupación de clientes |
| Por refuerzo | Aprende por recompensas | Videojuegos o robótica |

```mermaid
flowchart TD
  A[Datos de Entrenamiento] --> B[Algoritmo ML]
  B --> C[Modelo Entrenado]
  C --> D[Predicciones]

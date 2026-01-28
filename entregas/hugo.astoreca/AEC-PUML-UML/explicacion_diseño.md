# Explicación de Diseño – Sistema de Gestión de Biblioteca
**Universidad – Proyecto UML**  
**Fecha:** 7/12/2025

---

# 1. Introducción
Este documento explica las decisiones de diseño tomadas para los tres diagramas UML entregados:

- Diagrama de Casos de Uso  
- Diagrama de Objetos  
- Diagrama de Estados (Ciclo de vida del préstamo)  

El objetivo es justificar la estructura, la organización y las relaciones utilizadas para modelar correctamente el sistema de gestión de la biblioteca.

---

# 2. Decisiones de Diseño – Casos de Uso

## 2.1 Actores Escogidos
El sistema incluye cuatro actores, cada uno con responsabilidades diferenciadas:

- **Estudiante:** Uso estándar del sistema (préstamos, reservas, pagos).  
- **Profesor:** Funcionalmente similar a estudiante pero con reglas de negocio distintas.  
- **Bibliotecario:** Encargado de procesos administrativos y control interno.  
- **Sistema de Notificaciones:** Actor automático que envía avisos.  

Separar Profesor y Estudiante permite asignar los mismos casos de uso pero mantener reglas diferentes.

## 2.2 Organización por Paquetes
Para mejorar la legibilidad y cumplir con el requisito de “agrupación lógica”, los casos de uso se organizaron en paquetes:

- **Búsqueda y Consulta** → interacción básica del usuario con el catálogo.  
- **Gestión de Préstamos** → flujos relacionados al préstamo del libro.  
- **Gestión de Reservas** → acciones relacionadas a disponibilidad futura.  
- **Penalizaciones** → multas, pagos y cálculos.  
- **Reportes** → funcionalidades exclusivas del bibliotecario.  

Esto permite visualizar claramente qué funcionalidades pertenecen a cada ámbito.

## 2.3 Relaciones Elegidas
Las relaciones son directas **actor → caso de uso**, según lo solicitado.  
No se utilizaron «include» ni «extend» para mantener simplicidad y evitar sobreestructura.

---

# 3. Decisiones de Diseño – Diagrama de Objetos

## 3.1 Escenario Seleccionado
El diagrama muestra un instante concreto del sistema: **15 de noviembre de 2025 a las 14:30h**, con varios préstamos y reservas activas.  
Los objetos fueron creados a partir de los datos proporcionados por el enunciado.

## 3.2 Tipos de Objetos
Se incluyeron:

- **Usuarios:** 3 objetos (estudiantes y profesor)  
- **Libros:** 5 objetos  
- **Préstamos:** 4 objetos  
- **Reservas:** 2 objetos  
- **Multas:** 1 objeto  

Esto supera el mínimo de 15 objetos requerido.

## 3.3 Relaciones Modeladas
Se representaron todas las relaciones obligatorias:

- Asociación entre usuarios y préstamos.  
- Asociación entre préstamos y los libros correspondientes.  
- Asociación entre reservas, usuarios y libros.  
- Asociación entre multa y préstamo vencido.  

Estas relaciones permiten comprender las dependencias activas dentro del sistema.

## 3.4 Simplificación Intencional
No se incluyen clases, solo **objetos**, como requiere la especificación.  
Los atributos se muestran únicamente para diferenciar objetos y evitar ambigüedad.

---

# 4. Decisiones de Diseño – Diagrama de Estados

## 4.1 Estructura General
El diagrama describe el **ciclo de vida completo de un préstamo**, cumpliendo:

- 7 estados obligatorios  
- 12+ transiciones  
- Etiquetas condicionales  
- Uso de estados compuestos  
- Uso de actions `entry`/`exit`  

## 4.2 Estado Compuesto “En Curso”
Se creó el super-estado **En Curso**, que contiene:

- **Activo**  
- **Renovado**  
- **Vencido**  

Esto permite agrupar todos los estados que ocurren después de que un préstamo ha sido aprobado y antes de su finalización.

## 4.3 Estados Especiales Utilizados
Aunque opcionales, se incorporaron elementos avanzados como:

- **Estado inicial** \[*\]  
- **Estado final** \[*\]  
- **Acciones entry/exit** en estados relevantes  
- **Etiquetas en transiciones** (ej. `[libro disponible]`, `[a tiempo]`)  

Decidí no incluir **history state (H)** ni **choice**, ya que el flujo ya era suficientemente complejo y claro.

## 4.4 Transiciones
Cada transición fue diseñada según las reglas de negocio:

- Renovación limitada a 2 veces  
- Rechazo si hay reservas  
- Préstamos vencidos que pueden continuar en ese estado  
- Diferenciación entre “devolver a tiempo” y “devolver con multa”

---

# 5. Conclusión
Los tres diagramas se han diseñado para cumplir:

- Las reglas del enunciado  
- La claridad visual  
- La correspondencia precisa con los datos proporcionados  
- La separación lógica de responsabilidades del sistema  

El resultado final ofrece una representación completa y coherente del sistema de gestión de la biblioteca universitaria.

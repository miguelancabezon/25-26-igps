# Actividad de Evaluación Continua - PlantUML UML - Sistema de Gestión de Biblioteca Universitaria


<h3><b>¡IMPORANTE!</b></h3>

> [!CAUTION]
> La entrega se debe hacer en la carpeta entregas > nombre.apellido > AEC-PUML-UML
>
> Cualquier entrega realizada en otra carpeta se considerará **NO ENTREGADA**

## Objetivos
- Modelar un sistema completo usando diferentes tipos de diagramas UML
- Practicar la creación de diagramas de objetos, casos de uso y estado
- Comprender las relaciones entre diferentes vistas del sistema
- Aplicar PlantUML en un caso de uso real

## Datos
- Herramientas: PlantUML
- Entregrables: 3 archivos `.puml`, uno por diagrama.

## Contexto
La Biblioteca Central de la Universidad necesita modernizar su sistema de gestión. El nuevo sistema debe permitir a estudiantes y profesores realizar préstamos de libros, gestionar reservas y manejar devoluciones.<br/>
El sistema debe controlar el estado de cada préstamo desde su solicitud hasta su finalización, y permitir diferentes operaciones según el rol del usuario.

## Descripción del Sistema

### Actores del sistema
1. Estudiante: Puede buscar libros, hacer préstamos y reservas
2. Profesor: Mismo acceso que estudiante + préstamos de larga duración
3. Bibliotecario: Gestiona préstamos, devoluciones y penalizaciones
4. Sistema: Envía notificaciones automáticas

### Funcionalidades Principales

**Para Usuarios (Estudiantes/Profesores)**:
- Buscar libros en el catálogo
- Solicitar préstamo de libro (si está disponible)
- Renovar préstamo (máximo 2 renovaciones)
- Hacer reserva de libro (si está prestado)
- Devolver libro
- Ver historial de préstamos
- Pagar multas online

**Para Bibliotecarios:**
- Registrar préstamo manualmente
- Procesar devolución
- Aplicar penalizaciones por retraso
- Gestionar reservas
- Generar reportes

### Reglas de Negocio

**Préstamos para Estudiantes:**
- Máximo 3 libros simultáneos
- Duración: 14 días
- Renovaciones: hasta 2 veces (si no hay reservas)
- Multa por retraso: €0.50/día

**Préstamos para Profesores:**
- Máximo 5 libros simultáneos
- Duración: 30 días
- Renovaciones: hasta 2 veces
- Multa por retraso: €0.30/día

**Estados de un Libro:**
- Disponible
- Prestado
- Reservado
- En Mantenimiento

**Estados de un Préstamo:**
- Solicitado
- Activo
- Renovado
- Vencido
- Devuelto
- Cancelado

## Parte 1 - Diagrama de Casos de Uso

### Objetivo de esta parte
Modelar las interacciones entre los actores y el sistema, mostrando todas las funcionalidades disponibles.

### Requisitos del Diagrama

Debes crear un diagrama de casos de uso que incluya:
1. Actores (4 actores mínimo):
   - Estudiante
   - Profesor
   - Bibliotecario
   - Sistema (para notificaciones automáticas)
2. Casos de Uso (mínimo 12):
   1. Solicitar préstamo
   2. Renovar préstamo
   3. Devolver libro
   4. Procesar devolución (bibliotecario)
   5. Registrar préstamo manual (bibliotecario)
   6. Package "Gestión de Reservar": Hacer reserva, Cancelar reserva, Notificar disponibilidad (sistema).
   7. Package "Búsqueda y consulta": Buscar en catálogo, Ver historial de préstamos, Consultar estado de libro.
   8. Package "Penalizaciones": Calcular multa, Pagar multa online, Aplicar penalización (bibliotecario).
   9. Package "Reportes" (solo bibliotecario): Generar reporte de préstamos, Generar reporte de multas.
3. Relaciones a incluir
   Para el diagrama de casos de uso, las relaciones serán las flechas normales de `-->`

### Elementos adicionales
- Agregar packages a los casos de uso y/o a los actores.
- Etiquetas explicativas en las relaciones complejas.
- Agrupación lógica de casos de uso relacionados.


## Parte 2 - Diagrama de Objetos
### Objetivo de esta parte
Representar una instancia concreta del sistema en un momento específico, mostrando objetos reales y sus relaciones.

### Escenario a Modelar

**Fecha:** 15 de Noviembre de 2025, 14:30h

**Situación:** Sistema con varios préstamos activos y una reserva.

#### Objetos Requeridos (mínimo 15 objetos):

**Usuarios (3 objetos)**

```
  estudiante1: Estudiante
  
  id: "EST-2023001"
  nombre: "Ana García"
  email: "ana.garcia@uni.es"
  prestamosActivos: 2
  multasAcumuladas: 1.50
```

```
  profesor1: Profesor
  
  id: "PROF-2020045"
  nombre: "Dr. Carlos Ruiz"
  departamento: "Informática"
  prestamosActivos: 3
  multasAcumuladas: 0.00
```

```
  estudiante2: Estudiante
  
  id: "EST-2024089"
  nombre: "Luis Martínez"
  email: "luis.martinez@uni.es"
  prestamosActivos: 1
  multasAcumuladas: 0.00
```

**Libros (5 objetos)**

```
  libro1: Libro
  
  isbn: "978-3-16-148410-0"
  titulo: "Clean Code"
  autor: "Robert C. Martin"
  ejemplares: 3
  disponibles: 1
  categoria: "Programación"
```

```
  libro2: Libro
  
  isbn: "978-0-13-468599-1"
  titulo: "The Pragmatic Programmer"
  autor: "Hunt & Thomas"
  ejemplares: 2
  disponibles: 0
  categoria: "Programación"
```

```
  libro3: Libro
  
  isbn: "978-0-596-52068-7"
  titulo: "JavaScript: The Good Parts"
  autor: "Douglas Crockford"
  ejemplares: 4
  disponibles: 3
  categoria: "Programación"
```

```
  libro4: Libro
  
  isbn: "978-0-134-68599-8"
  titulo: "Design Patterns"
  autor: "Gang of Four"
  ejemplares: 2
  disponibles: 1
  categoria: "Ingeniería Software"
```

```
  libro5: Libro
  
  isbn: "978-0-321-12742-6"
  titulo: "Domain-Driven Design"
  autor: "Eric Evans"
  ejemplares: 1
  disponibles: 0
  categoria: "Arquitectura"
```

  

  

  

  

  

  
  3. Préstamos (4 objetos):
  
  prestamo1: Prestamo
  
  id: "PREST-2025-1234"
  fechaInicio: "2025-11-01"
  fechaVencimiento: "2025-11-15"
  estado: "Activo"
  renovaciones: 0
  multa: 0.00
  
  prestamo2: Prestamo
  
  id: "PREST-2025-1256"
  fechaInicio: "2025-10-28"
  fechaVencimiento: "2025-11-27"
  estado: "Activo"
  renovaciones: 0
  multa: 0.00
  
  prestamo3: Prestamo
  
  id: "PREST-2025-1189"
  fechaInicio: "2025-10-20"
  fechaVencimiento: "2025-11-03"
  estado: "Vencido"
  renovaciones: 1
  multa: 6.00
  
  prestamo4: Prestamo
  
  id: "PREST-2025-1290"
  fechaInicio: "2025-11-10"
  fechaVencimiento: "2025-11-24"
  estado: "Activo"
  renovaciones: 0
  multa: 0.00
  
  4. Reservas (2 objetos):
  
  reserva1: Reserva
  
  id: "RES-2025-0089"
  fechaReserva: "2025-11-14"
  estado: "Pendiente"
  posicionCola: 1
  
  reserva2: Reserva
  
  id: "RES-2025-0090"
  fechaReserva: "2025-11-15"
  estado: "Pendiente"
  posicionCola: 2
  
  5. Multa (1 objeto):
  
  multa1: Multa
  
  id: "MULT-2025-045"
  monto: 6.00
  fechaGeneracion: "2025-11-04"
  estado: "Pendiente"
  concepto: "Retraso en devolución"

### Elementos adicionales

## Parte 1 - Diagrama de Casos de Uso
### Objetivo de esta parte
### Requisitos del Diagrama
### Elementos adicionales





 

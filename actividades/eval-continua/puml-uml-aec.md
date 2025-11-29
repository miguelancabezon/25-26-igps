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
- Estudiante: Puede buscar libros, hacer préstamos y reservas
- Profesor: Mismo acceso que estudiante + préstamos de larga duración
- Bibliotecario: Gestiona préstamos, devoluciones y penalizaciones
- Sistema: Envía notificaciones automáticas

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

### Reglas de nego


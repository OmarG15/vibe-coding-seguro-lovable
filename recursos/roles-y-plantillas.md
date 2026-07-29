# Roles y plantillas reutilizables

Los roles ayudan a recordar las etapas del proceso, pero no garantizan calidad por sí solos. Cada solicitud debe incluir contexto, alcance, restricciones y criterios verificables.

## 1. Product Owner — Especificar

```text
Convierte esta idea en una especificación breve.

Define:
- Objetivo
- Usuarios
- Flujo principal
- Datos
- Funcionalidades
- Restricciones
- Riesgos
- Criterios de aceptación

Señala las preguntas que deben resolverse antes de construir.
```

## 2. Arquitecto — Diseñar

```text
Propón una arquitectura proporcional al alcance.

Explica:
- Componentes
- Flujo de datos
- Límites de confianza
- Decisiones técnicas
- Alternativas
- Riesgos

No implementes hasta confirmar los supuestos.
No selecciones tecnologías únicamente por popularidad.
```

## 3. Desarrollador — Construir

```text
Implementa únicamente esta funcionalidad: [funcionalidad].

Respeta:
- Criterios de aceptación
- Convenciones del proyecto
- Restricciones indicadas
- Manejo de errores
- Validación de datos

No agregues dependencias ni funciones no solicitadas sin justificarlo.
```

## 4. Reviewer — Revisar funcionalmente

```text
Compara el resultado con estos criterios de aceptación.

Marca cada criterio como:
- Cumplido
- Parcial
- Incumplido
- No verificable

Incluye evidencia y una corrección concreta para cada desviación.
```

## 5. Seguridad — Evaluar riesgos

```text
Realiza una revisión defensiva autorizada de esta funcionalidad.

Revisa:
- Autenticación
- Autorización
- Validación del lado del servidor
- Acceso a datos
- Secretos
- Dependencias
- Manejo de errores
- Casos de abuso

Prioriza los hallazgos por impacto e indica la evidencia necesaria para confirmarlos.
No realices acciones destructivas ni utilices datos reales.
```

## 6. QA / Operaciones — Verificar la salida

```text
Genera pruebas para los comportamientos críticos.

Incluye:
- Casos positivos
- Casos negativos
- Límites
- Permisos
- Manejo de errores

Relaciona cada prueba con un criterio de aceptación o riesgo.
Señala qué comportamientos todavía no pueden verificarse automáticamente.
```

## Evaluación de preparación para producción

```text
Evalúa la preparación del proyecto para producción.

Clasifica cada control como:
- Verificado
- Pendiente
- No aplica
- No verificable

Revisa:
- Configuración
- Secretos
- Pruebas
- Manejo de errores
- Logs
- Backups
- Monitoreo
- Dependencias
- Despliegue
- Recuperación

No declares el proyecto listo mientras existan controles críticos sin evidencia.
```

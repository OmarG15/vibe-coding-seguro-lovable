# Prompting profesional para desarrollo con IA

El prompting profesional no consiste en añadir más siglas ni pedirle al modelo que “actúe como experto”. Consiste en convertir una necesidad en instrucciones claras, limitadas y verificables.

> Un buen prompt define el problema, limita el alcance y exige resultados que puedan comprobarse.

---

## Principios

### 1. Define el objetivo

Explica qué problema debe resolver la solución y cuál es el resultado esperado.

### 2. Aporta contexto

Indica quién utilizará la aplicación, qué información manejará y en qué escenario funcionará.

### 3. Delimita el alcance

Especifica qué debe incluirse y qué debe quedar fuera. Esto reduce funciones innecesarias, complejidad y consumo de iteraciones.

### 4. Declara restricciones

Incluye límites técnicos, de privacidad, seguridad, datos, dependencias y comportamiento.

### 5. Usa criterios de aceptación

Describe cómo se comprobará que el resultado cumple lo solicitado. Evita depender únicamente de “me gusta” o “se ve bien”.

### 6. Pide evidencia verificable

Solicita resultados observables: archivos modificados, pruebas, hallazgos, supuestos, riesgos pendientes y criterios cumplidos.

### 7. Trabaja por etapas

Especifica, genera, revisa, corrige y valida. No intentes resolver arquitectura, interfaz, autenticación, despliegue y seguridad en una sola instrucción.

### 8. Conserva el control

No autorices dependencias, comandos, cambios de arquitectura ni acceso a datos sensibles sin revisar su necesidad e impacto.

---

## Prompt vago frente a instrucción profesional

### Prompt vago

```text
Hazme un sistema de inventario.
```

### Instrucción profesional

```text
Crea un prototipo web para gestionar el inventario de una pequeña tienda.

Usuario principal:
Encargado de inventario.

Debe permitir:
- Consultar productos.
- Registrar y editar productos.
- Aumentar o disminuir existencias.
- Buscar por nombre, categoría o SKU.
- Identificar productos con inventario bajo.

Cada producto debe incluir:
- Nombre.
- Categoría.
- SKU.
- Precio.
- Cantidad disponible.
- Nivel mínimo.

Restricciones:
- Utiliza datos ficticios.
- No incluyas pagos, facturación, usuarios reales ni datos sensibles.
- No agregues dependencias o funciones no solicitadas sin justificarlo.

Validaciones:
- No aceptar cantidades ni precios negativos.
- No permitir SKU duplicados.
- Mostrar mensajes claros de error.

Criterios de aceptación:
- El usuario puede registrar y editar un producto.
- Puede modificar existencias.
- La aplicación identifica inventario bajo.
- La navegación principal funciona.
- El diseño se adapta a dispositivos móviles.
```

La diferencia no está en la longitud. Está en que la segunda instrucción define contexto, alcance, restricciones y criterios verificables.

---

# Plantillas reutilizables

## 1. Especificar — Product Owner

```text
Convierte esta idea en una especificación breve y verificable.

Idea:
[describir idea]

Define:
- Objetivo.
- Usuarios.
- Flujo principal.
- Datos.
- Funcionalidades.
- Restricciones.
- Riesgos.
- Criterios de aceptación.
- Preguntas que deben resolverse antes de construir.

No generes código todavía.
```

## 2. Diseñar — Arquitectura

```text
Propón una arquitectura proporcional al alcance de esta especificación.

Incluye:
- Componentes principales.
- Flujo de datos.
- Límites de confianza.
- Dependencias necesarias.
- Decisiones técnicas y justificación.
- Riesgos.
- Alternativas.

No selecciones tecnologías únicamente por popularidad.
No implementes hasta que se aprueben los supuestos.
```

## 3. Construir — Desarrollo

```text
Implementa únicamente esta funcionalidad:

[funcionalidad]

Respeta:
- Criterios de aceptación.
- Convenciones existentes.
- Restricciones del proyecto.
- Validaciones requeridas.
- Manejo seguro de errores.

No agregues dependencias, permisos o funciones no solicitadas sin explicar primero su necesidad.
Indica qué archivos modificarás antes de realizar los cambios.
```

## 4. Revisar funcionalmente

```text
Compara el resultado con estos criterios de aceptación:

[criterios]

Para cada criterio indica:
- Cumplido.
- Parcial.
- Incumplido.
- No verificable.

Incluye evidencia, hallazgos y una corrección concreta.
No declares que el resultado está completo si existen puntos no verificables.
```

## 5. Revisar seguridad

```text
Realiza una revisión defensiva autorizada.

Evalúa:
- Autenticación.
- Autorización.
- Validación del lado del servidor.
- Acceso a datos.
- Secretos y credenciales.
- Dependencias.
- Manejo de errores.
- Permisos.
- Casos de abuso.

Para cada hallazgo incluye:
- Descripción.
- Evidencia.
- Impacto.
- Prioridad.
- Mitigación.
- Forma de comprobar la corrección.

No asumas que una validación visual protege el backend.
```

## 6. QA y pruebas

```text
Genera pruebas para los comportamientos críticos.

Incluye:
- Casos positivos.
- Casos negativos.
- Valores límite.
- Errores.
- Autorización.
- Criterios de aceptación.

Relaciona cada prueba con un requisito o riesgo.
Señala qué comportamientos todavía no pueden verificarse automáticamente.
```

## 7. Preparar la siguiente iteración

```text
Convierte estos hallazgos en un plan priorizado.

Para cada cambio indica:
- Problema.
- Impacto.
- Cambio esperado.
- Archivos o componentes afectados.
- Criterio de verificación.
- Riesgo de regresión.

Realiza un cambio significativo por vez y conserva una versión estable antes de modificar.
```

## 8. Evaluar preparación para producción

```text
Evalúa la preparación del proyecto para producción.

Clasifica cada control como:
- Verificado.
- Pendiente.
- No aplica.
- No verificable.

Revisa:
- Configuración.
- Secretos.
- Pruebas.
- Dependencias.
- Autenticación y autorización.
- Logs.
- Monitoreo.
- Backups.
- Despliegue.
- Recuperación.
- Riesgos pendientes.

No declares el proyecto listo para producción sin evidencia suficiente.
```

---

# Cómo usar roles correctamente

Un rol puede orientar el enfoque, pero no garantiza calidad.

## Débil

```text
Actúa como arquitecto senior y hazlo seguro.
```

## Mejor

```text
Actúa como arquitecto de software para evaluar esta especificación.

Tu tarea es:
- Identificar componentes y flujo de datos.
- Señalar límites de confianza.
- Justificar decisiones.
- Identificar riesgos.
- Proponer alternativas.
- Esperar aprobación antes de implementar.

No agregues tecnologías no justificadas.
```

El rol debe acompañarse siempre de una tarea, contexto, restricciones y entregables verificables.

---

# Cómo evitar un loop de correcciones

Antes de enviar otra instrucción, responde:

1. ¿Qué está mal?
2. ¿Dónde ocurre?
3. ¿Qué resultado espero?
4. ¿Cómo comprobaré que se corrigió?
5. ¿Es el cambio prioritario?
6. ¿Puedo agrupar cambios relacionados?
7. ¿Estoy repitiendo la misma solicitud?

## Fórmula recomendada

> Elemento + problema + cambio esperado + criterio de verificación

### Ejemplo

```text
En el formulario de productos se pueden registrar cantidades negativas.

Impide guardar valores menores que cero y muestra un mensaje claro debajo del campo.

La corrección será válida si el producto no se registra y los demás datos del formulario permanecen visibles.
```

---

# Qué evitar

- Pedir “hazlo seguro” sin definir controles.
- Llenar la instrucción de tecnologías o siglas sin justificación.
- Solicitar “listo para producción” como si fuera un resultado automático.
- Pedir varios cambios no relacionados al mismo tiempo.
- Aceptar dependencias o comandos sin revisión.
- Usar la misma IA como única generadora, revisora y aprobadora.
- Confundir una respuesta convincente con evidencia técnica.

---

# Regla final

> La calidad de una instrucción no se mide por cuánto texto contiene, sino por la claridad del problema, sus límites y la posibilidad de verificar el resultado.

# Plantilla de correcciones

| Hallazgo | Corrección propuesta | Criterio de verificación | Responsable | Estado |
|---|---|---|---|---|
|  |  |  |  | Pendiente |

## Formato de una corrección con IA

```text
Contexto:
[Describe la funcionalidad.]

Problema:
[Indica el comportamiento observado y su impacto.]

Cambio esperado:
[Explica la corrección.]

Criterio de verificación:
[Define cómo comprobar que funciona.]

Restricciones:
[Indica qué no debe modificarse.]
```

## Ejemplo

```text
Contexto:
El formulario registra productos en el inventario.

Problema:
Actualmente permite guardar cantidades negativas.

Cambio esperado:
Rechaza cualquier cantidad menor que cero y muestra un mensaje claro.

Criterio de verificación:
La solicitud no debe guardar el producto, debe devolver un error de validación y debe conservar los demás valores del formulario.

Restricciones:
No modifiques las columnas de la tabla ni el diseño general.
```

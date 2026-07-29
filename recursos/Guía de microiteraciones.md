# Guía de microiteraciones

Una microiteración debe seguir esta estructura:

> **Elemento + problema + cambio esperado + criterio de verificación**

## Ejemplo incorrecto

```text
El formulario está mal. Arréglalo.
```

## Ejemplo mejorado

```text
En el formulario de productos se pueden registrar cantidades negativas.

Impide guardar valores menores que cero y muestra un mensaje claro debajo del campo.

La corrección será válida si el producto no se registra y los demás datos del formulario permanecen visibles.
```

## Ejemplo de inventario bajo

```text
En la tabla de productos, los artículos con inventario bajo no se diferencian visualmente.

Agrega una etiqueta visible cuando la cantidad disponible sea igual o menor que el nivel mínimo.

No modifiques las demás columnas de la tabla.
```

## Ejemplo de dashboard

```text
En el dashboard falta un indicador de inventario bajo.

Agrega una tarjeta que muestre el número de productos cuya cantidad sea igual o menor que su nivel mínimo.

Mantén las tarjetas actuales y usa los mismos datos de la tabla.
```

## Cómo evitar un loop de correcciones

Antes de enviar otra instrucción, responde:

1. ¿Qué está mal?
2. ¿Dónde ocurre?
3. ¿Qué resultado espero?
4. ¿Cómo comprobaré que se corrigió?
5. ¿El cambio es prioritario?
6. ¿Puedo agrupar cambios relacionados?
7. ¿Estoy repitiendo la misma solicitud?

Reglas:

- Trabaja un problema principal por interacción.
- Agrupa solo cambios relacionados.
- Revisa el resultado antes de volver a pedir cambios.
- Conserva una versión estable antes de modificar.
- No repitas una instrucción ambigua con palabras distintas.

> **Si no puedes explicar claramente el problema, la IA probablemente tampoco podrá corregirlo.**

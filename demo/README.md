# Guía de la demostración

## Objetivo

Demostrar que generar una aplicación rápidamente no equivale a producir software listo para producción.

## Apertura

Utiliza una instrucción deliberadamente general:

```text
Crea una aplicación web para gestionar el inventario de una pequeña tienda.
```

> **¿La pondrías mañana en producción para administrar el inventario real de una empresa?**

## Ahora destrúyelo

Realiza únicamente pruebas preparadas y autorizadas:

- Intentar registrar una cantidad negativa.
- Intentar registrar un SKU duplicado.
- Recargar para verificar persistencia.
- Probar una función desde una ruta directa.
- Revisar consola y solicitudes de red.
- Verificar si existen mensajes internos o datos expuestos.

No prometas demostrar SQL Injection, XSS o manipulación de JWT salvo que exista un entorno controlado y una prueba previamente confirmada.

## Mensaje

> **La prueba no es “¿se ve bien?”, sino “¿qué ocurre cuando el usuario no hace lo esperado?”.**

## Seguridad

- No utilices datos reales.
- No ataques sistemas de terceros.
- No realices acciones destructivas.
- Mantén una versión estable de respaldo.
- Prepara capturas o video por si la demo falla.

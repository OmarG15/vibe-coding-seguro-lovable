# Vibe Coding Seguro con Lovable

Recursos, ejemplos y buenas prácticas para desarrollar prototipos con inteligencia artificial de forma más profesional y segura utilizando Lovable.

Este repositorio acompaña el taller **“Vibe Coding Seguro con Lovable: de la idea al prototipo y del prototipo a la ingeniería”**.

El objetivo no es enseñar únicamente a generar aplicaciones con IA, sino comprender cómo especificar una solución, revisar lo generado, identificar riesgos y aplicar controles antes de considerar un sistema listo para usuarios reales.

---

## Objetivo del taller

Al finalizar, deberías poder:

- Comprender qué es el Vibe Coding y sus principales riesgos.
- Diferenciar entre pedir, guiar y gobernar a una herramienta de IA.
- Convertir una idea en requisitos verificables.
- Generar un prototipo utilizando Lovable.
- Evaluar funcionalidad, validaciones y seguridad.
- Realizar correcciones claras mediante microiteraciones.
- Comprender la diferencia entre un prototipo y un producto en producción.
- Aplicar un flujo básico de Secure SDLC.
- Utilizar el framework SAFE para desarrollar con IA de forma más controlada.

---

## Idea principal

> Hoy escribir código ya no es la parte difícil. Lo difícil es saber qué aceptar y qué rechazar.

La inteligencia artificial puede acelerar la generación de software, pero no sustituye:

- El criterio técnico.
- La revisión humana.
- Las pruebas.
- La seguridad.
- La arquitectura.
- El mantenimiento.
- La responsabilidad sobre el producto.

---

## Contenido del repositorio

Este repositorio incluye:

- La Presentación del taller.
- El Framework SAFE.
- Un ejercicio práctico de inventario.
- Especificación(Prompt) utilizada en Lovable.
- Guía de microiteraciones.
- Checklist de revisión funcional.
- Checklist mínimo de seguridad.
- Flujo recomendado de Secure SDLC(Software Development Life Cycle).
- Recursos adicionales para continuar aprendiendo.

---

# Los tres niveles del Vibe Coding

## Nivel 1 — Pedir

La persona describe lo que quiere y acepta el resultado generado.

Ejemplo:

> Crea un sistema de inventario.

En este nivel, la herramienta toma gran parte de las decisiones y existe poca validación del resultado.

## Nivel 2 — Guiar

La persona proporciona:

- Contexto.
- Requisitos.
- Datos.
- Restricciones.
- Criterios de aceptación.
- Correcciones específicas.

En este nivel, la IA sigue generando, pero el usuario dirige el proceso con mayor claridad.

## Nivel 3 — Gobernar

La persona controla:

- Proveedores de IA.
- Privacidad.
- Datos compartidos.
- Permisos de agentes.
- Herramientas activas.
- Revisión de código.
- Pruebas.
- Dependencias.
- Riesgos.
- Criterios para desplegar.

> El objetivo del taller es pasar de pedir a gobernar.

---

# Framework SAFE

El framework SAFE organiza el desarrollo asistido por IA en cuatro etapas.

## S — Specify

Define claramente:

- Problema.
- Objetivo.
- Usuarios.
- Funcionalidades.
- Datos.
- Restricciones.
- Riesgos.
- Criterios de aceptación.

Antes de generar código, debe existir una definición clara de lo que se espera construir.

## A — Assess

Evalúa el resultado generado:

- ¿Cumple los requisitos?
- ¿Agregó funciones no solicitadas?
- ¿Maneja errores?
- ¿Tiene validaciones?
- ¿Qué supuestos realizó?
- ¿Qué riesgos permanecen?
- ¿Qué elementos no pueden verificarse?

## F — Fortify

Fortalece la solución mediante:

- Validaciones del lado del servidor.
- Autenticación.
- Autorización.
- Mínimo privilegio.
- Protección de secretos.
- Pruebas.
- Revisión de dependencias.
- Manejo seguro de errores.
- Logs y auditoría cuando apliquen.

## E — Evolve

El software debe mantenerse y mejorar continuamente mediante:

- Control de versiones.
- Monitoreo.
- Actualizaciones.
- Backups.
- Gestión de vulnerabilidades.
- Retroalimentación.
- Métricas.
- Revisión continua.

---

# Ejercicio práctico

Durante el taller se construye una aplicación web para gestionar el inventario de una pequeña tienda.

## Usuario principal

Encargado o administrador del inventario.

## Funcionalidades principales

- Consultar productos.
- Registrar nuevos productos.
- Editar productos.
- Aumentar o disminuir existencias.
- Buscar por nombre, categoría o SKU.
- Identificar productos con inventario bajo.

## Datos de cada producto

- Nombre.
- Categoría.
- Código SKU.
- Precio.
- Cantidad disponible.
- Nivel mínimo de inventario.

## Alcance del prototipo

El ejercicio utiliza datos ficticios.

No incluye:

- Pagos.
- Facturación.
- Proveedores reales.
- Usuarios reales.
- Información confidencial.
- Base de datos de producción.

---

# Especificación utilizada en Lovable

```text
Crea una aplicación web para gestionar el inventario de una pequeña tienda.

El usuario principal será el encargado o administrador del inventario.

La aplicación debe incluir un dashboard con:

- Total de productos registrados.
- Cantidad de productos con inventario bajo.
- Valor estimado del inventario.

Debe permitir:

- Visualizar una lista de productos.
- Registrar nuevos productos.
- Editar la información de un producto.
- Aumentar o disminuir existencias.
- Buscar productos por nombre, categoría o SKU.
- Identificar los productos con inventario bajo.

Cada producto debe manejar:

- Nombre.
- Categoría.
- Código SKU.
- Precio.
- Cantidad disponible.
- Nivel mínimo de inventario.

Incluye las siguientes validaciones:

- Todos los campos principales deben ser obligatorios.
- La cantidad y el precio no pueden ser negativos.
- El SKU debe ser único.
- Los mensajes de error deben ser claros.

La aplicación debe incluir:

- Dashboard.
- Lista de productos.
- Formulario para registrar o editar productos.
- Vista o filtro de productos con inventario bajo.

Utiliza datos ficticios para demostrar el funcionamiento.

El diseño debe ser moderno, profesional y fácil de entender. Utiliza tarjetas de resumen, tablas legibles, formularios sencillos y un diseño adaptable a computadoras y dispositivos móviles.

No incluyas pagos, facturación, proveedores, usuarios reales ni una base de datos de producción.

Criterios de aceptación:

- El usuario puede consultar los productos.
- El usuario puede registrar y editar un producto.
- El usuario puede modificar la cantidad disponible.
- La aplicación identifica los productos con inventario bajo.
- La navegación principal funciona.
- El diseño se adapta correctamente a dispositivos móviles.

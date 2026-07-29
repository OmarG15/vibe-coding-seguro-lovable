# Del prototipo al Secure SDLC

```text
Idea y requisitos
        ↓
Generación con IA
        ↓
Revisión funcional
        ↓
Revisión humana y de seguridad
        ↓
Repositorio y control de cambios
        ↓
Pruebas y análisis automatizados
        ↓
Despliegue controlado
        ↓
Operación y mejora continua
```

## 1. Idea y requisitos

Define claramente el problema, los usuarios, los datos, las funcionalidades y las restricciones. Establece criterios de aceptación que permitan comprobar si la solución cumple lo esperado.

## 2. Generación con IA

Utiliza Lovable u otra herramienta para crear una primera versión basada en los requisitos. El resultado debe tratarse como un punto de partida que todavía necesita revisión, pruebas y ajustes.

## 3. Revisión funcional

Compara el prototipo con los requisitos y verifica que las funciones principales trabajen correctamente. Revisa errores, casos no contemplados y funciones agregadas que no fueron solicitadas.

## 4. Revisión humana y de seguridad

Analiza el código, los permisos, las validaciones, el acceso a los datos y las dependencias. La IA puede apoyar la revisión, pero una persona debe evaluar las decisiones y los riesgos pendientes.

## 5. Repositorio y control de cambios

Almacena el código en GitHub o GitLab para mantener historial, versiones estables y trazabilidad. Revisa los cambios antes de incorporarlos.

## 6. Pruebas y análisis automatizados

Ejecuta pruebas funcionales y herramientas que detecten errores, vulnerabilidades, secretos expuestos y dependencias inseguras.

Ejemplos:

- Pruebas unitarias y de integración.
- SAST.
- Análisis de dependencias.
- Escaneo de secretos.
- DAST cuando aplique.

## 7. Despliegue controlado

Publica primero en un entorno de pruebas y protege las variables sensibles fuera del código. Incluye aprobaciones, configuraciones verificadas y un mecanismo de reversión.

## 8. Operación y mejora continua

Después de publicar, supervisa la aplicación mediante logs, alertas, backups y monitoreo. El software debe actualizarse y evaluarse continuamente.

> **Lovable acelera la generación; la ingeniería convierte el resultado en software confiable.**

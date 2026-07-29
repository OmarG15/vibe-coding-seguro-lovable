# Checklist antes de desplegar

Utiliza los estados:

- `Verificado`
- `Pendiente`
- `No aplica`

## Acceso

- [ ] Autenticación implementada.
- [ ] Autorización validada.
- [ ] Roles definidos.
- [ ] Sesiones protegidas.
- [ ] Principio de mínimo privilegio aplicado.

## Datos

- [ ] Validaciones implementadas en el servidor.
- [ ] Datos sensibles identificados.
- [ ] Base de datos protegida.
- [ ] Políticas de acceso configuradas.
- [ ] Backups definidos.
- [ ] Retención de datos documentada.

## Código y dependencias

- [ ] Secretos fuera del código.
- [ ] Variables de entorno configuradas.
- [ ] Dependencias revisadas.
- [ ] Pruebas críticas ejecutadas.
- [ ] Manejo seguro de errores.
- [ ] Revisión humana completada.
- [ ] Escaneo de vulnerabilidades realizado.
- [ ] Escaneo de secretos realizado.

## Operación

- [ ] HTTPS habilitado.
- [ ] Logs configurados.
- [ ] Monitoreo activo.
- [ ] Alertas definidas.
- [ ] Health checks disponibles.
- [ ] Plan de reversión documentado.
- [ ] Responsable de mantenimiento asignado.

## Evidencia

- [ ] Resultados de pruebas disponibles.
- [ ] Hallazgos pendientes documentados.
- [ ] Riesgos aceptados formalmente.
- [ ] Responsable de aprobación identificado.
- [ ] Fecha de revisión registrada.

## Regla de decisión

No declares el sistema “listo para producción” mientras existan controles críticos pendientes o elementos no verificables sin una decisión formal de riesgo.

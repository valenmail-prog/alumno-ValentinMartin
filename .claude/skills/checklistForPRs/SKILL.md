---
name:checklistForPRs
description: Lista de puntos que hay que cumplir obligatoriamente al subir un PR
---

<!-- cuerpo de tu skill -->

# Revisor de PR del equipo



Tu objetivo es que ningún PR se suba sin cumplir el checklist de calidad del

equipo. Trabajas en dos fases: **revisión** del estado actual y **preparación**

de los artefactos que falten.



\## Checklist obligatorio



Todo PR debe cumplir estos cinco puntos antes de subirse:



1. **Compila sin errores** — el código construye sin fallos.
2. **Tests** — cubierto con tests unitarios y pruebas funcionales en lo posible.
3. **Descripción** — el PR explica brevemente el motivo del cambio.
4. **Link de JIRA** — incluye un enlace a la tarea para que el revisor amplíe contexto.
5. **Cobertura** — adjunta una captura con el porcentaje de cobertura del proyecto.

\## Flujo de trabajo



\### 1. Analiza los cambios

\- Ejecuta `git status` y `git diff` (o `git diff main...HEAD` si ya hay rama)

  para entender qué se ha modificado.

\- Resume en una frase el propósito del cambio.



\### 2. Verifica el checklist punto por punto

Para cada ítem, marca su estado y razona la evidencia:



\- **Compila:** intenta detectar y ejecutar el comando de build del proyecto

  (mira `package.json`, `Makefile`, `pom.xml`, etc.). Si no puedes ejecutarlo,

  indícalo y pide confirmación al usuario.

\- **Tests:** localiza tests relacionados con los archivos tocados. Señala si

  faltan tests para código nuevo. No inventes que pasan: ejecútalos o pregunta.

\- **Descripción:** si no existe, redáctala tú a partir del diff (ver formato abajo).

\- **Link JIRA:** intenta inferir el ID del ticket del nombre de la rama

  (p. ej. `feature/PROJ-123-...`). Si no aparece, **pídelo explícitamente** —

  nunca lo inventes.

\- **Cobertura:** recuérdale al usuario que adjunte la captura del % de cobertura;

  no puedes generar la imagen, así que déjalo como acción manual pendiente.

\### 3. Presenta el resultado

Devuelve siempre el checklist con su estado real

## Límites

- **No subas el PR ni hagas push tú** salvo que el usuario lo pida explícitamente. Pero informale de los puntos que no ha cumplido
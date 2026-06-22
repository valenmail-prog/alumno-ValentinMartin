# Entregable · Sesión 3 — Copilotos IA

- **Nombre / usuario:** Valentín Martín Tejeda / valenmail-prog
- **Fecha de entrega:** 22/06/2026
- **Repo auditado en la Parte A** : Repo de la práctica (documentación en Markdown, recién clonado)

---

## 1. Hallazgos de la auditoría (Parte A)

> 3-5 cosas que el agente **no pudo inferir** del código y que tendrías que decirle explícitamente.
> Redáctalas para que otra persona las entienda sin contexto adicional. **Sin código propietario ni secretos.**

1. No tiene contexto del programa, el objetivo de la practica.
2.  El lenguaje de programación, y estructura de carpetas.
3. Que no puede hacer commits a main, y crear una rama con mis datos alumno/ValentinMartin
4. Qué TA recibe la entrega ni el plazo concreto

---

## 2. SKILL.md de la skill creada (Parte B)

> Pega aquí el contenido completo de tu `.claude/skills/<nombre-skill>/SKILL.md`
> (o enlaza al archivo en tu repositorio sandbox).

```markdown
---
name: checklistForPRs
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
```

---

## 3. Diario de decisiones

*Skill creada:* checklistForPRs. Lista de puntos que tiene que cumplir un PR

*Decisiones de diseño tomadas:*
- Decisión 1: Hice una lista mental de que puntos necesitamos tener para poder aprobar los PR's. Los básicos eran que compile, que tenga test unitarios.
- Decisión 2: Añadir una descripción y la tarea de JIRA, ya que trabajamos con JIRA para las tareas.
- Decisión 3: Añadir la cobertura de código

*Qué me resultó fácil:*

- Enumerar los puntos fue más facil de lo que pensaba.

*Qué me resultó ambiguo o difícil de decidir:*
- La explicación de lo que hay que hacer en cada uno de los puntos, no se si explique demasiado o me quede corto. Intente poner limites, para que no haga el los PR's de forma automatica, sino que el usuario se lo pida, no se si esto puede ser una limitación que ayude, o es mejor que lo haga el por su cuenta.

*Tiempo real invertido:*
- He invertido unos 40 minutos.

*Qué probarías si tuvieras más tiempo:*

- Habría probado si luego al pedirle cambios cumple de manera automática los puntos, y en que momento avisa de que algo no se esta cumpliendo.

*¿Usaste IA para crear la skill?* (qué partes generaste con IA y qué partes decidiste tú)

- En la parte de la explicación de cada punto, que es lo que más me ha costado.

### Resultado de la prueba (Paso 8)

- ¿Se activó cuando lo esperabas? No se ha activado, tiene que haber algo mal en la ubicación o en las carpertas y me ha dejado hacer el PR sin que cumpliera el checklist que le he pasado.
- He creado el skill en esta ruta: .claude\skills\checklistForPRs. Creo que el problema es que lo he hecho yo manualmente, he creado todas las carpetas.

  

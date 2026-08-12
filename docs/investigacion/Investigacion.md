# Investigación: Cerebro Digital Personal con GitHub Copilot y Microsoft 365 Copilot

## Estado actual

Documento de contextualización y descubrimiento.

Este documento recopila las ideas discutidas para evaluar la viabilidad de construir un Cerebro Digital Personal utilizando GitHub como repositorio de conocimiento y Microsoft 365 Copilot / GitHub Copilot como consumidores de dicho conocimiento.

---

# Contexto

Las herramientas actuales de IA son muy buenas generando contenido, respondiendo preguntas y asistiendo en tareas especializadas.

Sin embargo, existe una limitación importante:

- El conocimiento generado durante el trabajo diario se pierde fácilmente.
- La memoria de las conversaciones no es persistente.
- Es necesario repetir contexto constantemente.
- Las decisiones y aprendizajes terminan dispersos entre chats, correos y documentos.

La investigación busca responder cómo construir una memoria persistente que sobreviva a las conversaciones y pueda reutilizarse continuamente.

---

# Inspiración

La investigación toma como referencia conceptos asociados a Andrej Karpathy:

- LLM Wiki.
- Second Brain.
- Memoria persistente.
- Conocimiento externo al modelo.
- Agentes que consultan conocimiento acumulado.

Idea principal:

> La IA no debe almacenar la memoria.
>
> La memoria debe existir fuera de la IA.

---

# Alcance acordado

## Incluido

- Uso personal.
- Uso profesional individual.
- Gestión de conocimiento.
- Aprendizajes.
- Decisiones.
- Contexto de proyectos.
- Compartir conocimiento entre miembros de un proyecto.
- GitHub Copilot.
- Microsoft 365 Copilot.
- Agentes de Microsoft 365 Copilot.
- Markdown.
- Wiki.
- Actualización manual.

## Excluido

- Soluciones organizacionales.
- Cerebro corporativo.
- Integraciones empresariales masivas.
- Automatizaciones complejas.
- Bases vectoriales.
- Entrenamiento de modelos.
- Soluciones dependientes de permisos corporativos.

---

# Hipótesis principal

Un Cerebro Digital no es una IA.

Un Cerebro Digital es una memoria persistente.

La IA consulta la memoria.

La IA ayuda a mantener la memoria.

La IA no es la memoria.

---

# Definición propuesta

Un Cerebro Digital es una colección estructurada de conocimiento, almacenada de forma persistente y reutilizable, que puede ser consultada por herramientas de IA para proporcionar respuestas consistentes y contextualizadas.

---

# Decisión de arquitectura

Se acuerda utilizar:

```text
GitHub
+
Markdown
+
Wiki
```

como base principal.

Repositorio seleccionado:

```text
digital-brain
```

URL:

```text
https://github.com/dapatino_cib/digital-brain
```

El repositorio es la fuente maestra de conocimiento.

---

# Principios fundamentales

## Principio 1

La memoria pertenece al usuario.

No a la herramienta.

---

## Principio 2

Las herramientas cambian.

La memoria permanece.

---

## Principio 3

Todo conocimiento debe ser legible por humanos.

---

## Principio 4

Todo conocimiento debe ser legible por IA.

---

## Principio 5

La actualización debe ser simple.

---

## Principio 6

Toda actualización debe tener validación humana.

---

# Formato seleccionado

Formato oficial:

```text
Markdown (.md)
```

Razones:

- Portable.
- Legible.
- Versionable.
- Compatible con Git.
- Compatible con GitHub Copilot.
- Fácil de mantener.

---

# Modelo de organización

Se utilizará una estructura tipo Wiki.

Ejemplo inicial:

```text
digital-brain

docs/

    investigacion/

        README.md

    profile.md

    projects.md

    decisions.md

    lessons-learned.md
```

---

# Rol de GitHub Copilot

GitHub Copilot tiene acceso natural al repositorio.

Funciones esperadas:

- Consultar documentación.
- Explicar decisiones.
- Utilizar contexto existente.
- Mantener consistencia.
- Generar propuestas de actualización.

GitHub Copilot se considera un consumidor nativo del Cerebro Digital.

---

# Rol de Microsoft 365 Copilot

Microsoft 365 Copilot se considera el principal reto de la investigación.

Objetivo:

Determinar cómo utilizar el Cerebro Digital desde agentes personalizados.

La investigación busca validar:

- Cómo indexa repositorios GitHub.
- Cómo utiliza documentación Markdown.
- Cómo localizar archivos específicos.
- Cómo mantener actualizado el conocimiento.

---

# Hallazgo importante

Se confirmó que los agentes permiten agregar repositorios GitHub mediante "Sitios web específicos".

Ejemplo utilizado:

```text
https://github.com/dapatino_cib/agente-arquitectura-contexto
```

Lo que demuestra que GitHub puede utilizarse como fuente de conocimiento para agentes.

---

# Separación entre memoria y comportamiento

Una observación importante:

El repositorio no define el comportamiento.

El repositorio define el conocimiento.

Las instrucciones definen el comportamiento.

Por lo tanto:

```text
Instrucciones
=
Cómo pensar
Cómo responder
Cómo actuar
```

```text
Repositorio
=
Qué sabe el agente
```

---

# Modelo propuesto

```text
Usuario

   ↓

Agente Copilot

   ↓

Digital Brain

   ↓

Documentación Markdown
```

---

# Evolución propuesta

## Nivel 1

Cerebro global.

```text
digital-brain
```

Contiene:

- Perfil.
- Proyectos.
- Decisiones.
- Aprendizajes.
- Investigación.

---

## Nivel 2

Cerebros especializados.

Ejemplos:

```text
agente-arquitectura-contexto

agente-cloudcenter-contexto

agente-devops-contexto
```

Cada uno aporta conocimiento especializado.

---

# Modelo de actualización

Proceso acordado:

## Paso 1

Trabajar normalmente con IA.

---

## Paso 2

Solicitar cierre de sesión.

Ejemplo:

```text
Genera las actualizaciones necesarias para el Cerebro Digital.
```

---

## Paso 3

La IA produce Markdown.

---

## Paso 4

El usuario valida.

---

## Paso 5

El usuario copia y pega.

---

## Paso 6

Commit al repositorio.

---

# Filosofía Human-In-The-Loop

La IA no modifica la memoria.

La IA propone cambios.

El humano decide qué conservar.

Proceso:

```text
IA propone

↓

Humano valida

↓

Repositorio se actualiza
```

---

# Preguntas abiertas

## Pregunta 1

¿Cuál es la estructura mínima necesaria para que un Cerebro Digital sea útil?

---

## Pregunta 2

¿Qué información debe almacenarse?

---

## Pregunta 3

¿Cómo deben estructurarse las decisiones?

---

## Pregunta 4

¿Cómo deben almacenarse los aprendizajes?

---

## Pregunta 5

¿Cómo configurar correctamente agentes para consultar el Cerebro Digital?

---

## Pregunta 6

¿Cómo detectar cuándo un aprendizaje debe incorporarse a la memoria?

---

# Próximos pasos

1. Validar que el agente pueda leer archivos específicos del repositorio.
2. Probar consultas sobre contenido único.
3. Definir estructura inicial estable.
4. Diseñar procedimiento de actualización.
5. Configurar un agente dedicado al Cerebro Digital.
6. Construir la presentación ejecutiva basada en los hallazgos.

---

# Conclusión actual

El activo principal no es GitHub Copilot.

El activo principal no es Microsoft 365 Copilot.

El activo principal es el conocimiento almacenado en el repositorio.

Los copilots son simplemente herramientas que consumen dicho conocimiento.

La investigación se enfocará en demostrar que un Cerebro Digital puede construirse hoy utilizando repositorios GitHub, Markdown, Wiki y agentes de IA, sin requerir desarrollos complejos ni arquitecturas empresariales avanzadas.

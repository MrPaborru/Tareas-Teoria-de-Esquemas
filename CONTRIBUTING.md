# Cómo colaborar

Las correcciones de enunciados, soluciones y referencias son bienvenidas. También puedes señalar pasos que necesiten una justificación más explícita.

## Reportar un problema

- Usa la plantilla [Errata matemática o de edición](https://github.com/MrPaborru/Tareas-Teoria-de-Esquemas/issues/new?template=errata.yml) e indica tarea, ejercicio, página y versión consultada.
- Explica el paso que falla y la corrección propuesta, o aporta un contraejemplo cuando corresponda.
- Para un problema al generar el PDF, usa la plantilla [Problema de compilación](https://github.com/MrPaborru/Tareas-Teoria-de-Esquemas/issues/new?template=compilacion.yml). Incluye el comando utilizado y las líneas relevantes del registro.

## Proponer una corrección

1. Crea un fork y una rama para tu cambio.
2. Edita el archivo del ejercicio dentro de `Ejercicios/Tn/`. Conserva el enunciado y separa la solución mediante el entorno ya usado por el proyecto.
3. Justifica los cambios matemáticos y conserva las referencias a las fuentes originales.
4. Si modificas LaTeX, compila siguiendo el README y revisa las páginas afectadas.
5. Envía una pull request que explique qué corriges y por qué. Para cambios de documentación no hace falta regenerar el PDF.

## Convenciones

- Conserva la notación del curso, las etiquetas existentes y las referencias mediante los comandos del proyecto.
- Usa los comandos y entornos de `Personalizacion/Simbolos y entornos.tex`.
- Mantén la numeración por bloques propia de la tercera tarea.
- No actives las carpetas `T4`–`T6` ni cambies `NumTareas` como parte de una corrección aislada: el contenido publicado se selecciona en `Ejercicios/Cuerpo.tex`.
- Incluye solo archivos relacionados con la corrección. Los auxiliares y registros se guardan en `build/`; solo `build/main.pdf` se versiona en esa carpeta.
- Conserva la atribución de los enunciados, las citas bibliográficas y los materiales de apoyo.

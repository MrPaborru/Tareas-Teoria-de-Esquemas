# Tareas de Teoría de Esquemas

Enunciados y soluciones de **Pablo Jair Aranda Pérez** para el curso de Teoría de Esquemas impartido por el **Dr. Jesús Rogelio Pérez Buendía** en el CIMAT, durante 2026. Las fuentes están escritas en LaTeX y el documento está en español.

**[Leer las tareas en PDF](build/main.pdf)** · **[Apuntes del curso](https://github.com/MrPaborru/Apuntes-Teoria-de-Esquemas)** · **[Reportar una errata](https://github.com/MrPaborru/Tareas-Teoria-de-Esquemas/issues/new?template=errata.yml)**

## Contenido y estado

El documento actual reúne las **tareas 1, 2 y 3**, seleccionadas en [`Ejercicios/Cuerpo.tex`](Ejercicios/Cuerpo.tex). Se incluyen tanto los enunciados como su desarrollo en entornos de solución.

| Tarea | Material |
| --- | --- |
| [T1](Ejercicios/T1/T1.tex) | Categorías y funtores, propiedades universales, límites, colímites, adjuntos y categorías abelianas |
| [T2](Ejercicios/T2/T2.tex) | Ejercicios propuestos de la segunda tarea, con material de referencia en [Recursos](Recursos) |
| [T3](Ejercicios/T3/T3.tex) | Pregavillas, gavillas, tallos y construcción de morfismos de espectros; numeración por bloques de la pizarra |

Las carpetas `T4`, `T5` y `T6` están presentes en las fuentes, pero **no se incluyen en el documento actual**. Su presencia no significa que formen parte de las tareas publicadas del curso.

Las soluciones son trabajo de estudio en revisión. Las erratas y las mejoras justificadas de los argumentos son bienvenidas.

## Cómo leer y descargar

- [Abrir el PDF completo](build/main.pdf): incluye las tres tareas y las referencias.
- [Descargar el PDF](https://github.com/MrPaborru/Tareas-Teoria-de-Esquemas/raw/refs/heads/main/build/main.pdf).
- [Consultar los enunciados y materiales de apoyo](Recursos).
- [Consultar los apuntes del curso](https://github.com/MrPaborru/Apuntes-Teoria-de-Esquemas).

## Organización del repositorio

| Ruta | Contenido |
| --- | --- |
| [`main.tex`](main.tex) | Documento principal, paquetes, portada y número de tareas |
| [`Ejercicios/Cuerpo.tex`](Ejercicios/Cuerpo.tex) | Tareas que se incluyen en el PDF |
| [`Ejercicios/T1/`](Ejercicios/T1) a [`Ejercicios/T3/`](Ejercicios/T3) | Archivos de cada tarea y de sus ejercicios |
| [`Recursos/`](Recursos) | Enunciados y materiales de referencia recibidos |
| [`Referencias.bib`](Referencias.bib) | Bibliografía utilizada por `biblatex` |
| [`Personalizacion/`](Personalizacion) | Comandos, entornos, títulos, índice y encabezados |
| [`Portada/`](Portada) | Portada y elementos gráficos |
| [`build/main.pdf`](build/main.pdf) | Documento compilado que se publica |

## Compilación local

Se necesitan **pdfLaTeX**, **latexmk**, **Perl** y **Biber**, además de los paquetes de [`main.tex`](main.tex), incluidos `biblatex` con estilo APA, TikZ, `tikz-cd`, `tikz-nfold` y las fuentes `newtx`.

Compila desde la raíz del repositorio. El documento usa `\include` con subcarpetas; prepara sus directorios auxiliares y fija la salida en `build/`.

**PowerShell:**

~~~powershell
New-Item -ItemType Directory -Force -Path build/Portada, build/Ejercicios | Out-Null
latexmk -pdf -outdir=build main.tex
~~~

**Bash:**

~~~sh
mkdir -p build/Portada build/Ejercicios
latexmk -pdf -outdir=build main.tex
~~~

El resultado queda en **`build/main.pdf`**. `latexmk` coordina las pasadas de pdfLaTeX y Biber. El archivo `latexmkrc` actual fija la zona horaria; la carpeta de salida se indica en el comando.

Para recompilar al guardar cambios:

~~~sh
latexmk -pdf -outdir=build -pvc main.tex
~~~

Para eliminar auxiliares conservando el PDF:

~~~sh
latexmk -outdir=build -c main.tex
~~~

## Erratas y colaboraciones

Al reportar un problema, indica la tarea, el ejercicio, la página y la versión consultada. Si el error es matemático, explica el paso que falla y, si es posible, una corrección.

Consulta [CONTRIBUTING.md](CONTRIBUTING.md) para proponer cambios en las soluciones o informar de problemas de compilación.

## Autoría, fuentes y citación

**Autor de las soluciones:** Pablo Jair Aranda Pérez. Los enunciados y las referencias conservan la atribución de sus fuentes; consulta [CREDITS.md](CREDITS.md).

Para citar este trabajo, usa [CITATION.cff](CITATION.cff) e indica el commit o la versión consultada.

**Repositorio complementario:** [Apuntes de Teoría de Esquemas](https://github.com/MrPaborru/Apuntes-Teoria-de-Esquemas).

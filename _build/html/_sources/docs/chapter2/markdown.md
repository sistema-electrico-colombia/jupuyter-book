---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.12
    jupytext_version: 1.6.0
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

```{index} Roles y directivas
```
```{index} MyST
```
```{index} Ecuaciones matemáticas
```

# Ficheros Markdown (.md)

Tanto si el contenido del libro se escribe en Jupyter Notebooks (`.ipynb`) como en
estándar markdown (`.md`), utilizamos **MyST Markdown**.

## ¿Qué es MyST?

MyST significa "Markedly Structured Text". Se trata de una ligera variante de un tipo de 
markdown llamado "CommonMark", con algunas extensiones que permiten añadir **roles** y **directivas**
en el ecosistema de documentación Sphinx.

## Escribir Ecuaciones matemáticas

Al activar la extensión amsmath en _config.yml, podemos escribir expresiones matemáticas como:
\begin{gather*}
a_1=b_1+c_1\\
a_2=b_2+c_2-d_2+e_2
\end{gather*}

\begin{gather*}
a_{11}& =b_{11}&
  a_{12}& =b_{12}\\
a_{21}& =b_{21}&
  a_{22}& =b_{22}+c_{22}\\
\end{gather*}

\begin{gather*}
\nabla \times \vec{e}+\frac{\partial \vec{b}}{\partial t}&=0 \\
\nabla \times \vec{h}-\vec{j}&=\vec{s}\_{e}
\end{gather*}

## ¿Qué son roles y directivas?

Roles y directivas son dos potentes herramientas de Jupyter Book similares a las funciones, pero escritas en un lenguaje de markup. Ambas buscan un propósito similar, pero los **roles se escriben en una sola línea** mientras que las **directivas ocupan varias líneas**. 

### Uso de directivas

La forma más simple de insertar una directiva en el contenido de un libro es la siguiente:

````
```{midirectiva}
Contenido de mi directiva
```
````

Esto sólo funciona si existiera una directiva de nombre `midirectiva`
(que no existe, por supuesto). Existen muchas directivas predefinidas asociadas con
Jupyter Book. Por ejemplo, para insertar una caja con una nota, se puede hacer con la directiva siguiente:

````
```{note}
Aquí hay una nota
```
````

Que se visualiza como:

```{note}
Aquí hay una nota
```

cuando se genera/actualiza el lbro con el comando `jupyterbook build`.

Para más información sobre directivas, ver la
[documentación sobre MyST](https://myst-parser.readthedocs.io/).

+++

### Uso de roles

Los roles son similares a las directivas, pero se escriben en una sola línea. Para insertar un rol en un libro se hace siguiendo este formato:

```
Algún texto {rolename}`Este es mi texto!`
```

Como con las directivas, los roles sólo funcionan si el nombre `rolename` es válido. Por ejemplo, un nombre válido es `doc` y se usa para hacer referencia a otra página del libro. Así, puede utilizarse el encaminamiento relativo a la página de introducción, mediante la sintaxis `` {doc}`../chapter0/intro` `` que se visualizará como este texto con enlace a dicha página: {doc}`../chapter0/intro`.

Para más información sobre roles, ver la
[documentación sobre MyST](https://myst-parser.readthedocs.io/).

+++

### Uso de referencias bibliográficas

Se pueden citar referencias que estén almacenadas en un fichero `bibtex`. Por ejemplo,
la sintaxis siguiente: `` {cite}`holdgraf_evidence_2014` ``se visualizará como: {cite}`holdgraf_evidence_2014`.

Para insertar la bibliografía se utiliza la directiva `{bibliography}`. Esta directiva debe ser utilizada para todos los roles `{cite}` para su correcta visualización.
En el libro ejemplo las referencias están almacenadas en el fichero `references.bib` y la bibliografía se incluye con:

````
```{bibliography} references.bib
```
````

Que resulta en la siguiente visualización:

```{bibliography} references.bib
```

+++

### Ejecución de código en un fichero markdown

Jupyter Book usa *jupytext* para ejecutar código de programación en ficheros markdown. Para más información, ver la [documentación Jupytext](https://jupytext.readthedocs.io/en/latest/formats.html)

En primer lugar, se añaden Jupytext metadata al fichero markdown que contenga el código que queramos ajecutar. Por ejemplo, para añadir Jupytext metadata a esta página `markdown.md`, utilizando un kernel python3, hay que ejecutar el comando:

```
jupyter-book myst init docs/chapter2/markdown.md --kernel python3

```
que genera el header siguiente en el fichero `markdown.md`:

```bash
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.12
    jupytext_version: 1.6.0
kernelspec:
  display_name: Python 3
  language: python
  name: python3
```

A continuación se añade la directiva `{code-cell}` con el código que queramos ejecutar:

````
```{code-cell}
a = "Este es un texto"
b = "en código Python"
print(f"{a} {b}")
```
````

Cuando se genera el libro con el comando `jupyterbook build`, el contenido del bloque `{code-cell}` se ejecutará en el kernel Jupyter (en este caso python3) y el output se visualizará junto con el resto del libro.

```{code-cell}
a = "Este es un texto"
b = "en código Python"
print(f"{a} {b}")
```

Para más información sobre ejecución de código en ficheros markdown, ver la [documentación MyST-NB](https://myst-nb.readthedocs.io/en/latest/use/markdown.html).

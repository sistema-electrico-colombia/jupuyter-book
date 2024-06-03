# Instalación

```{index} Instalación
```

Esta es una guía para la creación de libros con la herramienta Jupyter Book. Para utilizar Jupyter Book, el contenido del libro debe guardarse en ficheros de tipo Markdown y Jupyter Notebooks. `jupyter-book` convierte estos ficheros a formato HTML y PDF. De esta manera, el libro puede leerse en cualquier browser, subirlo a un servicio cloud o server host, así como imprimir y distribuir el fichero PDF generado. 

La utilización de Jupyter Book está especialmente indicada para crear libros interactivos que permiten ejecutar código fuente de programación utilizando Jupyter Notebooks. Esto es especialmente recomendable para libros sobre programación, aprendizaje automático (Machine Learning) e Inteligencia Artificial (AI) en general.

## El entorno Anaconda

```{index} Anaconda
```

Aunque no es estrictamente necesario para crear un libro con Jupyter Book, es recomendable tener instalado el entorno Anaconda (o miniconda, una versión reducida que ocupa mucho menos espacio):

- [Installing Anaconda on Mac OS X](https://www.datacamp.com/community/tutorials/installing-anaconda-mac-os-x)

- [Setting up Python on Windows with Miniconda by Anaconda](https://katiekodes.com/setup-python-windows-miniconda/)

## Jupyter Book

Para utilizar Jupyter Book, se puede comenzar con

* la guía de utilización [getting started guide](https://jupyterbook.org/en/stable/intro.html),
* el menu de navegación de este libro (a la izquierda, en un ordenador de sobremesa), y también
* el libro ejemplo que se explica en los siguientes capítulos.

```{admonition} Nota
Jupyter Book `1.0.0` es una versión de Mayo de 2024 que reescribe completamente las versiones anteriores.
Ver [the legacy upgrade guide](https://github.com/executablebooks/jupyter-book/wiki/The-Jupyter-Book-Wiki)
para actualizaciones y [legacy.jupyterbook.org](https://legacy.jupyterbook.org) para
ver la documentación de anteriores versiones.

Es importante saber que Jupyter Book está en continua evolución y, por lo tanto, previsiblemente irá incorporando cambios importantes que pueden hacer que algunas funciones se vean afectadas en el futuro.
```

Para instalar `jupyter-book` desde pip, se utiliza el siguiente comando:

```bash
pip install -U jupyter-book
```
```{warning}
Nota para usuarios de Windows

Jupyter Book ha sido testado con Windows OS 😀

Sin embargo, existe una incompatibilidad, ya conocida, para ejecutar ficheros notebook con Python 3.8.

<!---See [](working-on-windows)--->

Ver [Working on Windows](https://jupyterbook.org/advanced/advanced.html#working-on-windows)
```

Para saber más sobre Jupyter Notebooks esta es la [documentación oficial (en inglés)](https://jupyter.readthedocs.io/en/latest/content-quickstart.html) 

Sobre cómo crear el entorno de desarrollo para Jupyter Notebook, en español, puede verse [Instalar entorno de desarrollo Python Anaconda para Aprendizaje Automático](https://www.aprendemachinelearning.com/instalar-ambiente-de-desarrollo-python-anaconda-para-aprendizaje-automatico/)


---

## Recomendación: Jupyter Lab

```{index} Jupyter Lab
```

Jupyter Lab es un entorno que en el futuro próximo sustituirá al clásico Jupyter Notebook (notebook, terminal, text editor, file browser, rich outputs, etc.). [Listo para usuarios.](https://blog.jupyter.org/jupyterlab-is-ready-for-users-5a6f039b8906)

[JupyterLab](http://jupyterlab.readthedocs.io/en/stable/) es la nueva propuesta interactiva del [Proyecto Jupyter](https://jupyter.org) que incorpora una más potente y flexible interfaz de usuario.

JupyterLab permite incorporar extensiones utilizando paquetes [npm](https://www.npmjs.com/) que usan APIs públicas de Jupyter. Para encontrar extensiones JupyterLab, buscar el término npm en [jupyterlab-extension](https://www.npmjs.com/search?q=keywords:jupyterlab-extension) o buscar en GitHub [jupyterlab-extension](https://github.com/topics/jupyterlab-extension). Para más información sobre extensiones, ver la [documentación de usuario](https://jupyterlab.readthedocs.io/en/latest/user/extensions.html).

Ver la última versión de la documentación en [ReadTheDocs](http://jupyterlab.readthedocs.io/en/latest/).

### Instalación

JupyterLab puede instalarse usando `conda` o `pip`. Para instrucciones detalladas, consultar la [installation guide](http://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html).

### conda

```shell
conda install -c conda-forge jupyterlab
```

### pip

```shell
pip install jupyterlab
```
#### Instalación con versiones anteriores de Jupyter Notebook

Cuando se usan versions de Jupyter Notebook anteriores a la versión 5.3, después de instalarse JupyterLab debe ejecutarse el siguiente comando:

```bash
jupyter serverextension enable --py jupyterlab --sys-prefix
```

### Ejecutar JupyterLab

Para iniciar JupyterLab se usa el comando:

```bash
jupyter lab
```

JupyterLab se abrirá automaticamente en el browser. Ver la [documentación](http://jupyterlab.readthedocs.io/en/stable/getting_started/starting.html) para mayor información.

Si encuentra un error tipo "Command 'jupyter' not found", puede ser que la variable de entorno `PATH` no tenga la información correcta. Como alternativa, se puede arrancar JupyterLab usando `~/.local/bin/jupyter lab` sin cambiar la variable de entorno `PATH`.

### Browsers soportados

Las últimas versiones de los siguientes browsers funcionan con Jupyter Lab:

- Firefox
- Chrome
- Safari

Ver la [documentación](http://jupyterlab.readthedocs.io/en/latest/getting_started/installation.html) para más información.


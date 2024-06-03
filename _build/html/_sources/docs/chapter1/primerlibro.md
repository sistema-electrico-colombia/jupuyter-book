# Construir el libro ejemplo

```{index} Crear mi primer libro
```

Una vez que tenemos instalado [Anaconda Python](https://www.anaconda.com/distribution/), tal y como hemos visto en el [capítulo inicial](/docs/chapter0/installation), ya podemos crear nuestro primer libro.

## Libro ejemplo

Para ello, vamos a partir de este mismo ejemplo de libro interactivo creado con Jupyter Book, recreándolo a partir del repositorio que lo contiene en Github.

Algunas de las funcionalidades incluidas en este libro son:

* [Jupyter notebooks](https://executablebooks.github.io/quantecon-mini-example/docs/python_by_example.html#version-1)
* [Referencias bibliográficas](https://executablebooks.github.io/quantecon-mini-example/docs/about_py.html#bibliography)
* [Ecuaciones matemáticas, numeradas para referenciar](https://executablebooks.github.io/quantecon-mini-example/docs/python_by_example.html#another-application)
* [Figuras, numeradas para referenciar](https://executablebooks.github.io/quantecon-mini-example/docs/getting_started.html#jupyter-notebooks) con leyendas explicativas y referencias cruzadas
* [Anotaciones online - hypothes.is ](https://jupyterbook.org/interactive/comments.html)
* [Descarga del PDF del libro completo o por capítulos](https://jupyterbook.org/advanced/pdf.html)
* [Acceso al código en la nube (ejecución y modificación) - Binder, Google Colab, etc.](https://jupyterbook.org/interactive/launchbuttons.html)

Los ficheros se encuentran [alojados en GitHub](https://github.com/Jero2760/jupyter-book-ejemplo/)
en la carpeta [docs](https://github.com/Jero2760/jupyter-book-ejemplo/docs/).
El contenido está escrito en [MyST markdown](https://jupyterbook.org/content/myst), una extensión de Jupyter notebook markdown que permite incluir markup científico, e incluye contenido escrito en Jupyter notebooks.

**Construir el libro ejemplo**

Para construir este libro ejemplo, vamos a hacerlo en Terminal, con los comandos siguientes:

1. En primer lugar, vamos a crear un entorno virtual de trabajo donde instalar las librerías necesarias de Python para ejecutar el código fuente de nuestro primer libro. Una forma sencilla de hacerlo es a través de un fichero environment.yml, como veremos a continuación. 

2. Clonamos el repositorio de Github que contiene los ficheros del libro ejemplo:

    ```bash
    git clone https://github.com/Jero2760/jupyter-book-ejemplo/
    cd jupyter-book-ejemplo
    ```

    ````{margin}

    Ver [la página getting started](https://jupyterbook.org/start/overview) para más información.
    ````

3. Instalamos las librerías Python necesarias utilizando [este fichero `environment.yml` ](https://github.com/Jero2760/jupyter-book-ejemplo/blob/master/environment.yml).
   Además, también se instalará la última versión de Jupyter Book. Este es el contenido de nuestro fichero evironment.yml:

	```shell
	name: jupyter-book-ejemplo
	channels:
  	  - default
	dependencies:
  	  - python=3.7
  	  - sphinx=2.4.4
  	  - pip
  	  - pandas
  	  - matplotlib
  	  - pip:
        - jupyter-book
        - sphinx-click
        - sphinx-tabs
        - jupytext
        - pyppeteer
	```

	La instalación se lleva a cabo en Terminal, con los comandos:
	```shell
	conda env create -f environment.yml
	conda activate jupyter-book-ejemplo
	```

	De esta forma, conseguimos instalar las dependencias necesarias, entre ellas Python 		3.7 y la última versión de Jupyter Book, así como también hemos creado y activado un entorno virtual, llamado aquí `jupyter-book-ejemplo`, que nos permite tener un contexto aislado donde crear el libro ejemplo, sin interferencias con otros posibles entornos instalados en nuestro ordenador.

4. Ejecutar Jupyter Book para generar el libro ejemplo, no desde la carpeta jupyter-book-ejemplo, sino desde la carpeta que lo contiene:

    ```bash
    cd ..
    jupyter-book build jupyter-book-ejemplo/
    ```

5. Ver el resultado en cualquier browser haciendo doble-click en el fichero `html` siguiente:

    ```bash
    jupyter-book-ejemplo/_build/html/index.html
    ```

	Ahora, podemos hacer modificaciones a los ficheros fuente que forman el libro ejemplo y que se encuentran en ``jupyter-book-ejemplo/docs``. Para ver el resultado de nuestras modificaciones, se vuelve a generar el libro con el mismo comando `build`: 

	```bash
	jupyter-book build jupyter-book-ejemplo/
	```

6. Para salir del entorno virtual creado:

	```shell
	conda deactivate
	```

### Más información

Ver un libro completo muy informativo creado con Jupyter Book en [QuantEcon](https://executablebooks.github.io/quantecon-example/docs/index.html)
con gran variedad de casos de uso.

Para más información sobre el proyecto Jupyter Book, ver toda la documentación en [The Executable Book Project](https://ebp.jupyterbook.org/).


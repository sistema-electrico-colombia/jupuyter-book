# Añadir interactividad

```{index} Interactividad
```
Una de las características más destacadas de los libros Jupyter Book es la posibilidad de dotarles de funciones web interactivas que crean una experiencia de usuario única: libros interactivos personalizados. Todo ello basado en la capacidad de Jupyter Book para generar colecciones de ficheros HTML, CSS y Javascript listos para alojar fácilmente en diversas ubicaciones online. 

Dado que los Jupyter Books incluyen contenidos en formato Jupyter Notebooks, los lectores pueden iniciar sesiones Jupyter online en la nube directamente desde el libro. Esto permite interactuar rápidamente con el contenido del libro en un entorno personal.

Existen numerosos servicios gratuitos para ejecutar los Jupyter Notebooks ([ver artículo](https://www.dataschool.io/cloud-services-for-jupyter-notebook/)). Para cada uno de estos servicios interactivos, se necesita indicar a Jupyter Book dónde está alojado el contenido de los notebooks online (por ejemplo en Github) en el [fichero de configuración](https://jero2760.github.io/jupyter-book-ejemplo/docs/chapter4/config.html) `_config.yml`:

Algunas funciones interactivas son:

- [Código ejecutable](https://jupyterbook.org/en/stable/basics/repository.html): para que las celdas de código de un notebook sean ejecutables y se puedan ver los resultados sin salir de la página del libro, se utilizan servicios cloud como [Mybinder](https://mybinder.org/), [Google Colab](https://colab.research.google.com/?hl=es) y [Thebe](https://thebe.readthedocs.io/en/stable/). Para acceder a estos servicios y elegir entre los entornos que aparecen {guilabel}`Binder`, {guilabel}`Colab` y {guilabel}`Live Code` hacer click en el botón {fa}`rocket` encima de la página del notebook correspondiente. En este libro ejemplo [ir a este enlace](https://jero2760.github.io/jupyter-book-ejemplo/docs/chapter2/notebooks.html). Ver [cómo configurar estos servicios interactivos](https://jupyterbook.org/en/stable/interactive/launchbuttons.html).

- [Ocultar o eliminar contenidos](https://jupyterbook.org/en/stable/interactive/hiding.html): para controlar el contenido que se muestra solamente si el lector lo desea. Por ejemplo, para mostrar una parte de código solamente cuando el lector quiere.

- [Añadir comentarios y anotaciones online](https://jupyterbook.org/en/stable/interactive/comments.html): permite a los lectores compartir conversaciones, ideas y preguntas en un lugar centralizado. Es útil para clases, grupos, pedir opiniones a los usuarios, etc. Por ejemplo el libro ejemplo utiliza [Hypothesis](https://hypothes.is/).

- [Banners de anuncios](https://jupyterbook.org/en/stable/web/announcements.html): para mostrar un mensaje para llamar la atención del lector, pero de forma que no distraiga de la lectura a medida que la persona sigue leyendo.

- [Salidas HTML avanzadas](https://jupyterbook.org/en/stable/advanced/html.html): CSS o Javascript a medida, Google Analytics, HTML extra (para navbar o footer por ejemplo), accesibilidad, chequear links externos, etc. 

Para más información sobre funciones interativas [ver la documentación](https://jupyterbook.org/en/stable/interactive/launchbuttons.html)



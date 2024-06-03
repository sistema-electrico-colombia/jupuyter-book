# Publicar el libro online

```{index} Publicar el libro online
```

Una vez generado nuestro libro, podemos subirlo a la nube, alojarlo en su servidor web y hacer que esté disponible para su lectura online. Puesto que el libro que hemos creado es, técnicamente, una página web estática, la mejor manera de lograrlo es a través de un servicio de alojamiento de **páginas web estáticas**. Hay muchas maneras de hacer esto y la siguientes secciones repasan las más habituales.

## Crear un repositorio online para nuestro libro

Vamos a utilizar Github para crear nuestro repositorio online y subir el contenido del libro que hemos creado.

1. Primero, hacer log-in en nuestro GitHub y crear un nuevo repositorio en la página "create a new repository": <https://github.com/new>

2. Segundo, añadir nombre y descripción de nuestro repositorio online. Asegurarse de que el repositorio es 'public' y no seleccionar la inicialización con el fichero README. Finalmente, hacer click en "Create repository".

3. Tercero, clonar el repositorio que acabamos de crear, y que está vacío, en nuestro ordenador:

   ```bash
   git clone https://github.com/<my-github-name>/<my-repository-name>
   ```

4. Cuarto, copiar todos los ficheros y carpetas del libro a la carpeta local recién clonada. Por ejemplo, si el libro fue generado con `jupyter-book create mylocalbook` y el repositorio se llama `myonlinebook`, el comando a ejecutar sería:

   ```bash
   cp -r mylocalbook/* myonlinebook/
   ```

5. Quinto, sincronizar el repositorio local y el repositorio remoto. Para ello es necesario ejecutar los siguientes comandos:

   ```bash
   cd myonlinebook
   git add ./*
   git commit -m "subiendo mi libro ejemplo"
   git push
   ```

Ver más información sobre cómo utilizar varios [servicios de alojamiento online](https://jupyterbook.org/publish/gh-pages.html)

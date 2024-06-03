# Añadir índice del libro

```{index} Añadir índice del libro
```

```{index} Índice
```

Para añadir una página índice a nuestro libro se hace incluyendo una directiva en nuestros ficheros de contenido:

````
```{index} Crear mi primer libro
```
````

Sirve para añadir cualquier término a nuestro índice, por ejemplo:

````
```{index} Jupyter Lab
```
````

Para que aparezca el índice, hay que añadir un fichero .md en el directorio raíz con una sola línea de título (ejemplo # Índice) y modificar `_toc.yml` incluyendo este nuevo fichero. Al hacer el build del libro, se crea también la página de índices.

[Ver documentación completa](https://jupyterbook.org/en/stable/content/content-blocks.html#indexes)

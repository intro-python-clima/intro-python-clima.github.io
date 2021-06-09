# Introducción a `conda`

El entorno de trabajo instalado contiene un set de paquetes utiles para los trabajos que desee realizar, sientase libre de personalizar el contenido del mismo conforme vaya necesitando algunos paquetes más especializados.

Si desea instalar un paquete adicional, deberá consultar la documentación del mismo donde especifican las opciones de instalación. Sin embargo, la mayoría de paquetes pueden ser instalados mediante el siguiente comando

```bash
conda install -c conda-forge PKG-NAME
```

Donde `PKG-NAME` es el nombre del paquete que desea instalar y `-c conda-forge` especifica que el paquete sea instalado desde el canal `conda-forge` (recomendado)


## Lo que necesito saber

- Cada celda en un Notebook se tiene que ejecutar para generar una salida. Estas salidas pueden ser de Markdown (texto) o Python (código)
- La celda actual siempre estará resaltada con una barra azul en el lado izquierdo
- Para crear una celda nueva deberá hacer click en el icono `+` que se encuentra en la barra de tareas
- Para ejecutar la celda actual deberá darle click al botón de _play_ que se encuentra en la barra de herramientas del notebook o haciendo uso del atajo `ctrl+Enter`. Si desea la celda actual y avanzar a la siguiente celda deberá usar el atajo `shift+Enter`
- Cada celda de código ejecutada será marcada con un número correspondiente al conteo de ejecuciones realizadas. Tener en cuenta que python es un lenguaje interpretado por lo que la numeración nos ayudará a entender el orden de ejecución.
- Los notebooks realizan todas las acciones sobre un kernel de python independiente. Mientras mantegamos una sesión activa (no reiniciemos el kernel) todas las variables asignadas serán conservadas en la memoria. Si la ejecución de una celda toma mucho tiempo y deseamos detener la ejecución, podemos interrumpir el kernel usando el botón de _stop_ en la barra de herramientas. En el peor de los casos puede reiniciar el kernel para iniciar una sesion fresca de python.

# Welcome to your Jupyter Book

This is a small sample book to give you a feel for how book content is
structured.

:::{note}
Here is a note!
:::

And here is a code block:

```
e = mc^2
```

Check out the content pages bundled with this sample book to see more.

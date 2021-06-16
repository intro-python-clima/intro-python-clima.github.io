# Introducción a `conda`

Entender el uso de `conda` es esencial al momento de trabajar usando entornos en python. Mediante `conda` podemos administrar los paquetes instalados en nuestro espacio de trabajo sin afectar los paquetes instalados por el mismo sistema operativo. Para poder sentar las bases, vamos a definir primero la terminología usada al trabajar con esta herramienta

## Terminología

- Entorno (*environment*) \
    Es el espacio de trabajo aislado que es creado al usar el comando `conda`. Dentro de una misma instalación podemos tener multiples entornos, cada uno con versiones de python distintas, sin ocasionar conflictos entre si.

    Se puede identificar la presencia de un entorno entre paréntesis, `(base)` en este ejemplo, al abrir una consola de comandos

    ```shell
    $ (base) grivera@IGPmaster2:~>
    ```
- Administrador de paquetes (*package manager*) \
    Es una herramienta que automatiza el proceso de instalación, actualización, configuración y desinstalación de programas de manera consistente. `conda` funciona como un administrador de paquetes para python al distribuir paquetes junto a sus dependencias ya compiladas para el sistema operativo que se esté usando.
- Canal (*channel*) \
    `conda` presenta la opción de canales para distinguir la ubicación de paquetes que tengan el mismo nombre. Por ejemplo, el canal por defecto `defaults` puede tener un paquete llamado `mypackage` en su versión v1.0, mientras que el mismo paquete puede estar disponible en otro canal llamado `grivera` en su versión v1.2. Esto permite instalar paquetes directamente de los canales de los desarrolladores en caso se quisiera contar con las actualizaciones menos estables.
- Paquete (*package*) \
    Tambien conocido como libreria, es el conjunto de utilidades contenido bajo un directorio estructurado el cual es capaz de ser importado dentro de un script.


## Uso básico de conda

### Creación de entornos

Conda permite la creación de entornos mediante la siguiente sintaxis

```shell
$ conda create -n MiEntorno python=3.6 numpy pandas matplotlib
```

Donde `-n MiEntorno` sirve para indicar el nombre del entorno a crear. Seguido de esto, encontramos la lista de paquetes que quisieramos agregar al entorno en el momento de su creación, con la opción de especificar una versión en concreto usando el simbolo de igual (`=`). En el ejemplo mostrado, se creará el entorno llamado `MiEntorno` usando python en su version 3.6 junto a `numpy`, `pandas` y `matplotlib`.

#### Usando un archivo `.yml`

Conforme uno va agregando contenido a su entorno, el recrearlo usando la sintaxis mostrada anteriormente se vuelve muy tedioso debido a la gran cantidad de paquetes que se van acumulando. Como solución a este problema, `conda` permite usar un archivo con extensión `.yml` el cual contenga la descripción del entorno a crear.

La estructura de este archivo, aplicado al ejemplo anterior, sería el siguiente:

```yml
name: MiEntorno
dependencies:
    - python=3.6
    - numpy
    - pandas
    - matplotlib
```

Guardando este contenido con el nombre `mientorno.yml`, la instalación se realiza de la siguiente manera:

```shell
$ conda env create -f mientorno.yml
```


### Instalando paquetes
Si desea instalar un paquete, lo primero que deberá realizar es consultar la documentación del mismo en donde se especifique las opciones de instalación. Sin embargo, la mayoría de paquetes pueden ser instalados mediante el siguiente comando

```shell
$ conda install -c conda-forge PKG-NAME
```

Donde `PKG-NAME` es el nombre del paquete que desea instalar y `-c conda-forge` especifica que el paquete sea instalado desde el canal `conda-forge` (recomendado)

:::{note}
El entorno de trabajo instalado contiene un set de paquetes utiles para los trabajos que desee realizar, sientase libre de personalizar el contenido del mismo conforme vaya necesitando algunos paquetes más especializados.
:::


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

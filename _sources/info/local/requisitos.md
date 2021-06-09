# Requisitos

Para poder usar este contenido de manera local necesitará tener acceso al comando `conda` y opcionalmente a `git`

## Instalando `conda`

El comando `conda` puede ser obtenido mendiante la instalación de Anaconda o miniconda. La descarga de dichas distribuciones la puede encontrar en sus páginas oficiales:

- [Descargar Anaconda](https://www.anaconda.com/products/individual)
- [Descargar Miniconda](https://docs.conda.io/en/latest/miniconda.html)

:::{note}
Ambas distribuciones proveen el comando `conda`, la diferencia entre Anaconda y miniconda radica en la cantidad de paquetes adicionales que traen consigo. Anaconda contiene varios paquetes útiles para comenzar con el análisis de datos; debido a ello, la descarga es más pesada que miniconda, el cual comprende una instalación minimalista
:::

### Entornos en `conda`

La verdadera ventaja de `conda` se encuentra en su capacidad para manejar entornos aislados de python, lo que significa que podemos tener entornos con versiones completamente distintas de python trabajando en una misma computadora.

Comprender el uso de `conda` es importante ya que dentro de este repositorio se incluye un fichero el cual tendra que instalar para poder acceder a los paquetes necesarios.

- **¿Cómo sabemos cuando estamos en un entorno?**

    Luego de instalar `conda` en nuestro sistema, al abrir una terminal observaremos algo similar a esto

    ```bash
    $ (base) grivera@IGPmaster2:~>
    ```

    En donde `(base)` es el nombre del entorno que viene por defecto en la instalacion de `conda`.
    
    Si no logra ver el entorno y se aseguró de haber instalado `conda` de manera correcta, puede activar el entorno base de la siguiente forma

    ```bash
    $ grivera@IGPmaster2:~> conda activate base
    $ (base) grivera@IGPmaster2:~>
    ```

    :::{note}
    Al instalar `conda` se le preguntará si desea inicializar el comando en el shell que esta usando. Si desea entrar al entorno `(base)` cada vez que abre una terminal, debera darle "yes" a esta opción.
    :::

## (Opcional) Instalando `git`

Si desea puede hacer uso del comando `git` para descargar una copia del contenido de este libro. En los sistemas operativos Unix `git` viene instalado por defecto, en caso de estar usando un sistema operativo distinto (Windows, MacOS) , o no contar con el comando, deberá instalar git desde su [página oficial](https://git-scm.com/downloads) y luego ejecutar Git Bash desde donde podrá hacer uso del comando `git`.

Para clonar el repositorio deberá usar el siguiente comando:

```bash
git clone git@github.com:intro-python-clima/intro-python-clima.git
```

Esto creara una carpeta con el mismo nombre del repositorio al cual podra acceder para iniciar su sesion de Jupyter.
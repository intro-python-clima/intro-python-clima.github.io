# El entorno de trabajo

Dentro del repositorio encontrará un archivo llamado `clima-env.yml` el cual describe el entorno de python a usar. Deberá instalar este entorno de trabajo usando el comando `conda` o `mamba`

```bash
conda env create -f environment.yml
```

Para el caso de Windows, al instalar Anaconda se agregará el `Anaconda Powershell Prompt` desde el cual podrá invocar el comando `conda`. Asegurarse de estar usando el shell correcto ya que el comando no será reconocido si usa Git Bash, Powershell o CMD y no agregó Anaconda al _path_ de su sistema al realizar la instalación.

Una vez terminada la ejecución del comando anterior, será capaz de activar el nuevo entorno de trabajo usando `conda`

```bash
conda activate pangeo
```

Sabrá si se encuentra dentro del nuevo entorno si en su terminal aparece el nombre del entorno de la siguiente manera: `(pangeo) user@hostname:~$`

El archivo `postBuild` contiene comandos que agregarán extensiones a nuestra instalación de Jupyter. Por defecto, el script usa `bash` asi que deberá tener este shell instalado.

```bash
sh postBuild
```

Tambien puede copiar el contenido del archivo `postBuild` y ejecutarlo directamente desde la terminal en caso no use bash.

Ahora podrá iniciar una sesión de JupyterLab mediante el siguiente comando

```bash
jupyter-lab
```

## Actualización

Para actualizar los paquetes del entorno de trabajo deberá ejecutar el siguiente comando

```bash
conda env update -f environment.yml
```

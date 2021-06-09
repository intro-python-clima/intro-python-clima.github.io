# Trabajando en la nube

Si desea revisar el contenido de manera interactiva y sin realizar ninguna instalación en su sistema, puede usar los links de **Binder** que encontrará en la parte superior de cada notebook. No obstante, se recomienda realizar la instalación local a fin de obtener experiencia en la administración de entornos y paquetes en python.

## ¿Qué es Binder?

**Binder** es una herramienta que permite compartir entornos de cómputo de manera sencilla. Es una forma muy util de compartir resultados reproducibles en los que el usuario puede interactuar como si estuviera en una instalación local.

El servicio que proveen permite el uso de una unidad de cómputo con almacenamiendo y memoria limitada, por lo que no es un entorno ideal para realizar trabajos pesados. De igual forma, la sesion de **Binder** se mantiene activa mientras el usuario se encuentre ejecutando celdas de jupyter notebook de manera regular ya que, una vez detecte inactividad, la sesión se encuentra programada para ser terminada.

:::{note}
Todas las modificaciones realizadas en un notebook durante una sesión de **Binder** no afectan al repositorio de donde fueron copiadas. Por ende, una vez que termine la sesión y se cierre la página web, todos los cambios realizados serán perdidos.

Si se desea conservar los cambios, puede descargar el notebook con sus modificaciones antes que la sesión termine.
:::
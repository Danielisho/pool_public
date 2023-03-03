# EJERCICIOS SEMANA 1


<a name="item0"></a>
## ÍNDICE DE CONTENIDOS
* [Contenido 1](#item1) ➡️ Tabla en `Markdown` con al menos 5 comandos de la **terminal**.
* [Contenido 2](#item2) ➡️ Tabla con algunos comandos _Alias_ que considere pertinentes.
* [Contenido 3](#item3) ➡️ Uso del comando `11ty`.
* [Contenido 4](#item4) ➡️ Diferencia entre **Terminal Application** y **Terminal Emulator**
* [Contenido 5](#item5) ➡️ Comando `mv` ¿Por qué se usa para renombrar también?

---
<a name="item1"></a>
### Contenido 1
**Tabla en `Markdown` con al menos 5 comandos de la terminal**

|COMANDO|EXPLICACIÓN|
|-------|-----------|
|`ls` <br><br> _"List"_|Lista los archivos y carpetas en el directorio actual <br> formato para usar **Indicadores**: <br><br> `ls <ruta del directorio> `: _Lista el contenido de otro      directorio_. <br><br> `ls /`: Lista el contenido del directorio principal. <br> <br> `ls ..`: para listar contenido un nivel arriba. <br><br> `ls ../..`: Para listar directorios 2 niveles arriba. <br><br> `ls ~`: Lista el contenido del directorio personal de usuario. <br><br> `ls -d */`: Lista **solo** directorios. <br><br> `ls *`: Lista el contenido del directorio y sus subdirectorios. <br><br> `ls -R`: Lista todos los archivos y directorios con sus sibdirectorios 😬 <br><br> `ls <directorio> -R`: Como el comando anterior puede tardar mucho, existe esta opción para listar todo pero de un único directorio 😅 <br><br> `ls -s`: Lista los directorios con sus tamaños. <br><br> `ls -l`: Lista el contenido de los directorios en formato lista con propiedades. `ls -lh`: Igual que el anterior pero añade el tamaño. <br><br> `ls -a`: Lista también los directorio o archivos ocultos. <br><br> `ls -l -a` , `ls -a -l` , `ls -la` , `ls -al`: Lista los directorios con información adicional incluyendo los ocultos. <br><br> `ls -t`: Lista ordenado por fecha de la última modificación. <br><br> `ls -tr`: Igual que el anterior pero invierte el orden. <br><br> `ls -S`: La lista la muestra por tamaño en orrden descendente. <br><br> `ls -Sr`: Igual que el anterior pero invierte el orden. ❗ OJO ❗ la **S** es mayúscula. <br><br> 🔥 BONUS TRACK 🔥 <br><br> `ls > mi_archivo.txt`: Imprime el resultado en un archivo. Puedo incluir todas las variantes anteriores y generar un archivo con el resultado. <br><br>|
|`pwd` <br><br>  _"Print Working Directory"_     | Muestra la ruta del directorio actual|
|`cd` <br><br> _"change directory"_ | `cd -`: Cambia al directorio anterior al directorio actual.<br><br> `cd ~`: Cambia al directorio de inicio del usuario.<br><br> `cd -P`: Se asegura de que se respeten los enlaces simbólicos y se utilice la ruta física del directorio 😕?.<br><br> |
|`cat` <br><br> "_Concatenate_"| `cat archivo.txt`: Muestra el contenido del archivo txt o varios arrchivos: <br><br> `cat archivo1 archivo2 archivo3` <br><br> Además de mostrar el contenido de un archivo en la salida estándar, el comando `cat` también se utiliza para concatenar archivos. <br>Para hacer esto, se utiliza el comando `cat` junto con la redirección estándar, de la siguiente manera: <br><br> `cat archivo1 archivo2 archivo3 ... > nuevo_archivo` <br><br>



[SUBIR ⏫](#item0)
___


<a name="item4"></a>
### Contenido 4
Diferencia entre **Terminal Application** y **Terminal Emulator**

La diferencia principal entre una terminal application y un terminal emulator es la capa de abstracción que se utiliza para comunicarse con el sistema operativo y ejecutar comandos en la línea de comandos.

Una terminal application es un programa que proporciona una interfaz de usuario para ejecutar comandos en la línea de comandos. Ejemplos de terminal applications son la Terminal de macOS, el símbolo del sistema de Windows, la Terminal de GNOME en Linux, entre otros. Estas aplicaciones interactúan directamente con el sistema operativo para enviar y recibir comandos y mostrar la salida de los mismos.

Por otro lado, un terminal emulator es un programa que emula una terminal física. En otras palabras, es un programa que simula el comportamiento de una terminal física y permite ejecutar comandos en la línea de comandos a través de una interfaz gráfica. Ejemplos de terminal emulators son xterm, Konsole, iTerm, etc. Estos programas no interactúan directamente con el sistema operativo, sino que emulan la funcionalidad de una terminal física y se comunican con el sistema operativo a través de un protocolo de comunicación (por ejemplo, el protocolo SSH para conectarse a un servidor remoto).

En resumen, la diferencia principal entre una terminal application y un terminal emulator es que la primera interactúa directamente con el sistema operativo, mientras que la segunda emula una terminal física y se comunica con el sistema operativo a través de un protocolo de comunicación.

Ventajas de las terminal applications:

Interactúan directamente con el sistema operativo, lo que puede ofrecer una mayor velocidad y eficiencia en la ejecución de comandos.
Algunas terminal applications pueden proporcionar características adicionales, como la capacidad de seleccionar y copiar texto, pestañas de terminal, la capacidad de personalizar la apariencia, etc.
Algunas terminal applications están diseñadas específicamente para trabajar con sistemas operativos particulares y pueden ofrecer una integración más profunda con el sistema operativo.
Desventajas de las terminal applications:

Por lo general, no son portables y solo funcionan en el sistema operativo para el que fueron diseñados.
No ofrecen la capacidad de conectarse a sistemas remotos de forma nativa.
Algunas terminal applications pueden ser más difíciles de usar para usuarios nuevos en la línea de comandos.
Ventajas de los terminal emulators:

Ofrecen la capacidad de conectarse a sistemas remotos de forma nativa y ejecutar comandos en ellos.
Son más portables y pueden funcionar en diferentes sistemas operativos.
La mayoría de los terminal emulators son altamente personalizables y ofrecen una amplia variedad de características.
Desventajas de los terminal emulators:

Debido a que emulan una terminal física, pueden ser menos eficientes en la ejecución de comandos.
Algunos usuarios pueden encontrar que la interfaz gráfica de los terminal emulators es menos intuitiva que la de las terminal applications.
La calidad de la experiencia de usuario puede variar significativamente según el terminal emulator que se esté utilizando.
En resumen, tanto las terminal applications como los terminal emulators tienen sus ventajas y desventajas, y la elección entre ellos dependerá de las necesidades y preferencias del usuario.

[SUBIR ⏫](#item0)
___

<a name="item5"></a>
### Contenido 5

¿Por qué se usa el comando `mv` también para renombrar archivos o carpetas?

El comando "mv" en la terminal de Linux/Unix se utiliza para mover archivos o directorios de un lugar a otro. Sin embargo, también se utiliza para cambiar el nombre de un archivo o directorio en la misma ubicación. Esto se debe a que, en Linux/Unix, un archivo o directorio se identifica por su nombre y su ruta de acceso completa. Al cambiar el nombre de un archivo o directorio, también se cambia su identidad. Por lo tanto, para el sistema operativo, renombrar un archivo es equivalente a moverlo a una nueva ubicación con un nuevo nombre.

En resumen, el comando "mv" se utiliza tanto para mover como para renombrar archivos o directorios en Linux/Unix porque el cambio de nombre y la reubicación de archivos/directorios son operaciones equivalentes para el sistema operativo.

[SUBIR ⏫](#item0)
___

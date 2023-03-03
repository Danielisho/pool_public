<!--Git es un sistema de control de versiones distribuido que permite a los desarrolladores de software llevar un registro de los cambios realizados en su código fuente. La filosofía detrás de Git es permitir a los desarrolladores trabajar de manera eficiente en proyectos de software en colaboración, manteniendo un historial completo y detallado de los cambios realizados a lo largo del tiempo. Git utiliza ramas (branches) para permitir que los desarrolladores trabajen en paralelo en diferentes características del proyecto, y los cambios se fusionan (merge) cuando se completan.

GitHub es un servicio en línea que aloja repositorios de Git en la nube. Es decir, proporciona una plataforma en línea para almacenar, compartir y colaborar en proyectos de software con Git. GitHub permite a los desarrolladores subir sus repositorios Git a la nube y colaborar en ellos con otros desarrolladores de todo el mundo. Los desarrolladores pueden realizar solicitudes de extracción (pull requests) para proponer cambios en el código fuente y revisar los cambios realizados por otros colaboradores. GitHub también proporciona herramientas para la gestión de proyectos, seguimiento de problemas (issues), integración continua (continuous integration) y despliegue (deployment) automático.

La principal diferencia entre Git y GitHub es que Git es un sistema de control de versiones distribuido, mientras que GitHub es un servicio en línea que proporciona una plataforma para alojar y colaborar en repositorios de Git en la nube. Git es una herramienta de línea de comandos que se ejecuta en la terminal, mientras que GitHub es una plataforma en línea que proporciona una interfaz gráfica de usuario para administrar los repositorios.

En cuanto a cómo se usan, en términos generales, se podría seguir los siguientes pasos:

Instalar Git en tu computadora.

Crear un repositorio Git local en tu computadora utilizando el comando git init.

Agregar y hacer un seguimiento de los archivos en el repositorio utilizando los comandos git add y git commit.

Subir el repositorio a GitHub utilizando el comando git push.

Colaborar en el repositorio en línea en GitHub, realizando cambios, realizando solicitudes de extracción y trabajando en equipo.

Descargar los cambios realizados por otros colaboradores utilizando el comando git pull.

Estos son solo los pasos generales y pueden variar según el caso específico. Es importante seguir las mejores prácticas de Git y GitHub para mantener una copia de seguridad, mantener un historial completo de los cambios y colaborar de manera efectiva en proyectos de software.
-->

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


<a name="item2"></a>
### Contenido 2

[SUBIR ⏫](#item0)
___

<a name="item3"></a>
### Contenido 3
Uso del comando `11ty`

<!--el comando 11ty es una herramienta de línea de comandos para construir sitios web estáticos que se basan en plantillas HTML, CSS y JavaScript. 11ty es una herramienta que se ejecuta en la terminal, y su objetivo principal es convertir archivos Markdown, Nunjucks, Handlebars, Liquid, entre otros, en archivos HTML estáticos.

Algunos de los comandos principales de 11ty son:

eleventy: es el comando principal para generar un sitio web estático. Cuando ejecutas el comando eleventy en la terminal, 11ty buscará los archivos de origen en el directorio actual y generará los archivos HTML estáticos en el directorio de destino.

eleventy --serve: este comando inicia un servidor local que muestra tu sitio web generado. Al ejecutar este comando, podrás ver los cambios en tiempo real a medida que los haces en los archivos fuente.

eleventy --input=<directorio-de-entrada> --output=<directorio-de-salida>: este comando te permite especificar los directorios de entrada y salida para la generación del sitio web. Por defecto, 11ty busca los archivos fuente en el directorio actual y genera los archivos HTML en una carpeta _site en el mismo directorio. Con este comando, puedes especificar un directorio de entrada y de salida personalizado.

eleventy --help: este comando muestra la lista completa de opciones y comandos disponibles en 11ty.

En resumen, 11ty es una herramienta útil para desarrolladores web que desean crear sitios web estáticos rápidos y eficientes usando plantillas HTML, CSS y JavaScript. La terminal es la forma más común de utilizar 11ty, y sus principales comandos son eleventy, eleventy --serve y eleventy --input=<directorio-de-entrada> --output=<directorio-de-salida>.
  
  puedes usar 11ty para crear un sitio web estático y luego subirlo a un repositorio de GitHub. Aquí te dejo los pasos generales para hacerlo:

Crea un nuevo repositorio en GitHub.

Clona el repositorio en tu computadora usando el comando git clone en la terminal.

Crea un nuevo sitio web estático con 11ty. Puedes hacerlo siguiendo los pasos en la documentación de 11ty. Por ejemplo, puedes crear un archivo de configuración .eleventy.js, agregar tus archivos fuente en el directorio src y ejecutar eleventy para generar el sitio web estático.

Copia los archivos generados en el directorio de salida de 11ty (por defecto, la carpeta _site) y pégalo en la carpeta clonada del repositorio de GitHub en tu computadora.

En la terminal, navega hasta el directorio clonado del repositorio de GitHub y ejecuta los siguientes comandos para subir los archivos al repositorio:
  ```sh
  git add .
git commit -m "Agregando archivos generados por 11ty"
git push origin master
  ```
  
  Si todo va bien, los archivos se subirán al repositorio de GitHub y estarán disponibles para ver en línea.
Recuerda que estos son solo los pasos generales y pueden variar según tu caso específico. Además, asegúrate de seguir las mejores prácticas de versionamiento y subir tus cambios regularmente para mantener una copia de seguridad y un registro de los cambios realizados.
-->
[SUBIR ⏫](#item0)
___

<a name="item4"></a>
### Contenido 4
Diferencia entre **Terminal Application** y **Terminal Emulator**

<!--
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

-->
[SUBIR ⏫](#item0)
___

<a name="item5"></a>
### Contenido 5
<!--
¿Por qué se usa el comando `mv` también para renombrar archivos o carpetas?

El comando "mv" en la terminal de Linux/Unix se utiliza para mover archivos o directorios de un lugar a otro. Sin embargo, también se utiliza para cambiar el nombre de un archivo o directorio en la misma ubicación. Esto se debe a que, en Linux/Unix, un archivo o directorio se identifica por su nombre y su ruta de acceso completa. Al cambiar el nombre de un archivo o directorio, también se cambia su identidad. Por lo tanto, para el sistema operativo, renombrar un archivo es equivalente a moverlo a una nueva ubicación con un nuevo nombre.

En resumen, el comando "mv" se utiliza tanto para mover como para renombrar archivos o directorios en Linux/Unix porque el cambio de nombre y la reubicación de archivos/directorios son operaciones equivalentes para el sistema operativo.

-->
[SUBIR ⏫](#item0)
___

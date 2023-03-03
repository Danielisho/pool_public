# EJERCICIOS SEMANA 1


<a name="item0"></a>
## ÍNDICE DE CONTENIDOS
* [Contenido 1](#item1) ➡️ Tabla en `Markdown` con al menos 5 comandos de la **terminal**.
* [Contenido 2](#item2) ➡️ Tabla con algunos comandos _Alias_ que considere pertinentes.
* [Contenido 3](#item3) ➡️ Uso del comando `11ty`.
* [Contenido 4](#item4)

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

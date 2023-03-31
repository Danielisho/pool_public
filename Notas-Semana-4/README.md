# Iniciando proyecto con VITE y SASS

### 📌 Iniciamos el proyecto
1. Creamos nuestro `index.html`.
2.  Asumiendo que tenemos **node.js** corriendo en nuestro sistema, iniciamos un nuevo proyecto con:

```bash
npm init -y
```
Con este comando se crea un archivo `package.json` que nos permitirá gestionar las dependencias del proyecto especificando qué paquetes se necesitan y sus respectivas dependencias.

> **NOTAS**:    
>1. `npm` (Node Package Manager) es el administrador de paquetes de **Node.js**. Se utiliza para instalar, actualizar y desinstalar paquetes de software en un proyecto Node.js. Los paquetes de **npm** se almacenan en un repositorio en línea llamado **npm registry**.
>2. **npx** (Node Package Runner) es una herramienta que se utiliza para ejecutar paquetes de software sin tener que instalarlos de forma permanente en el sistema. Al utilizar **npx**, Node.js descarga el paquete necesario ***temporalmente*** y lo ejecuta. Esto es útil si solo necesitas usar un paquete de software una vez y no quieres instalarlo de forma permanente en el sistema.

### 📌 Instalando SASS

Seguidamente, instalaremos **SASS** como **dependencia de desarrollo** con el siguiente comando:
 
```bash
npm install sass --save-dev
```
Este comando instalará 2 archivos y una carpeta:
1. Una (1) carpeta llamada ***node_modules*** que contiene **TODAS** las dependencias del proyecto. Esta carpeta ⚠️ **no se toca** ⚠️.
2. Un (1) archivo llamado `package.jason`, que en nuestro caso será sobreescrito puesto que fue creado en el paso anterior.
3. un (1) archivo llamado `package-lock.json` que se utiliza para mantener un registro detallado de las versiones exactas de las dependencias del proyecto y sus sub-dependencias. Este archivo asegura que, en cualquier momento en el futuro, se puedan volver a instalar exactamente las mismas versiones de las dependencias que se usaron originalmente en el proyecto, sin importar si las versiones de las dependencias se han actualizado o modificado desde la última instalación. Esta archivo ⚠️ **no se toca** ⚠️ .

Retomando, el comando `sass --save-dev`   instalará la última versión de **SASS** y la agregará como una ***dependencia de desarrollo** en el archivo `package.json` del proyecto.

### 📌Creando estructuras de directorios

1. En nuestro caso crearemos una carpeta para los recursos llamada `src`
```bash
mkdir src
```
2. Dentro de esta carpeta crearemos la carpeta `styles` que contendrá los archivos **SASS**  `main.scss` y `base.scss` (debemos crearlos).


### 📌 Instalando VITE

Instalamos **Vite** como dependencia de desarrollo con el comando:
```bash
npm install -D vite
```
Este comando es equivalente a:
```bash
npm install vite --save-dev
```
Este comndo agregará una entrada para **Vite** en el archivo `package.json` bajo la sección de *dependencias de desarrollo* (`devDependencies`).

>NOTA:  Para instalar **Vite** y **SASS** con un solo comando: 👇

 ```bash
 npm install sass vite --save-dev
```



### 📌 Configurando los scripts en package.json

Archivo `packkage.json`:
```json

{
  "name": "practica",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",


👉  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },


  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "sass": "^1.60.0",
    "vite": "^4.2.1"
  }


```
El objeto `scripts` en el archivo `package.json` se utiliza para definir una serie de comandos que pueden ser ejecutados a través de la línea de comandos utilizando el comando  ` npm run`.

Cada **script** es una propiedad en el objeto `scripts`, donde la `clave` es el nombre del comando y el `valor` es el comando que se va a ejecutar.

##### ✏️  Script para SASS
En nuestro proyecto, para que se compile lo que está en el archivo `main.css`, es decir, para que se pre-procese el **css**, se debe incluir en el objeto `escript` lo siguiente:

`"sass styles/main.scss styles/main.css"`

Esto significa que usando **SASS**  le indicamos s que **pre-procese** el contenido de `main.scss` y lo convierta a un archivo **css*, en este caso `main.css`.

el archivo `package.json` quedaría así:
```json
{
  "name": "practica",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  
  
  "scripts": {

    "test": "echo \"Error: no test specified\" && exit 1",

  👉  "sass": "sass /styles/main.scss styles/main.css"
    
  },
  
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "sass": "^1.60.0",
    "vite": "^4.2.1"
  }
}
```

##### ✏️  Script para VITE

En el caso de `Vite` el script sería:

` "dev":  "vite",`

El archivo `package.json` quedaría así:

```json
{
  "name": "practica",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",

  "scripts": {

    "test": "echo \"Error: no test specified\" && exit 1",

    "sass": "sass src/styles/main.scss styles/main.css",

 👉   "dev": "vite"

  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "sass": "^1.60.0",
    "vite": "^4.2.1"
  }
}
```
Cuando se necesite correr lo que está en estos `scripts` se utiliza la consola más el nombre asignado a los `scripts`, en nuestro caso, tenemos 3 scripts que podemos correr: 
1. `test` -> (viene por defecto en el `package.json`)
2. `sass`
3. `dev`

##### ✏️ Corriendo SASS
Con este comando ejecuta la instrucción de transformar el archivo `main.scss` -> a `main.css`: 
```bash
npm run sass
```


> **NOTA:** El archivo `main.css` no tengo que crearlo. **SASS** lo crea al ejecutar el script respectivo.


##### ✏️Corriendo Vite
Este es el Script para iniciar `Vite`:
```bash
npm run dev
```

### Atención: 💡

> ✏️  **NOTA IMPORTANTE -1:**    
Para que `Vite` quede "escuchando" los cambios, es necesario que el comando anterior se corra en otra instancia de la consola y dejarla "escuchando", para evitar estar escribiendo el comando cada cierto tiempo.

> ✏️ **NOTA IMPORTANTE - 2:**    
 Para lograr que **SASS**  "escuche" los cambios y compile automáticamente el archivo `.scss` en un archivo `.css` cada vez que se guarda, podemos crear un `script` en nuestro `package.json` como el siguiente:

```json
"watch:sass": "sass --watch src/styles/main.scss src/styles/main.css"
```
**NOTA:** Tener cuidado con los directorios (revisar la jerarquía).

Con esto el  archivo `package.json` quedaría así:  
  
  ```json
  {
  "name": "practica",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",

  👉  "watch:sass": "sass --watch src/styles/main.scss src/styles/main.css",
    
    "sass": "sass src/styles/main.scss styles/main.css",
    

    "dev": "vite"

  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "sass": "^1.60.0",
    "vite": "^4.2.1"
  }
}
```

### Atención: 💡
Importante que una vez hecho esto se coloque en el `head` del `index.html` los **link** que apunten a estos nuevos arhivos **css** que se crearán con **SASS**, es decir:
> `<link rel="stylesheet" href="styles/main.css">`

Se pueden agregar tantos `scripts` como se desee. Por ejemplo, si también se quisiera agregar un `script`  llamado **"build"** para compilar la aplicación, se podría agregar lo siguiente:
```json
{
  "name": "mi-proyecto",
  "version": "1.0.0",
  "scripts": {
    "start": "node app.js",
  👉   "build": "npm run sass && vite"
  }
}
```

Es importante tener en cuenta que los nombres de los **scripts** no están limitados a **"start"** o **"build"**.   Se puede utilizar cualquier nombre que se desee para los **scripts**, como **"test"**, **"lint"**, **"deploy"**, entre otros.

Una vez definidos los **scripts**  en el archivo `package.json`, puedes ejecutarlos a través de la línea de comandos utilizando el comando `npm  run`  seguido del nombre del script, ejemplo:

> `npm run build`


### 📌 Usando el sistema de módulos de SASS

El sistema de módulo de **Sass** es una funcionalidad que permite organizar y modularizar el código de **Sass** en diferentes archivos para que sea más fácil de mantener y reutilizar. 

En el archivo `main.scss` iniciaremos el sistema de módulos de **SASS**  haciendo la llamada al archivo `base.scss` en donde iremos colocando nuestro **css**, es decir, el archivo `main.scss` se encarga de **importar** los módulos que consideremos crear.

El archivo `main.scss` se verá así:
```css
@use "base.scss"
```

##### ✏️  Creando Variables SASS

1. Para crear variables en un archivo SCSS, se debe utilizar el siguiente formato:
```css
$nombre-variable: valor;
```

Por ejemplo, para crear una variable para designar un color primario, se haría de la siguiente manera:
```css
$color-primario: #007bff;
```

2.  Para utilizar la variable en el archivo **SCSS**, que en nuestro caso sería `base.scss`, se debe escribir el nombre de la variable precedido por un signo de dólar. Por ejemplo:
 ```css
 body {
  background-color: $color-primario;
}
```
De esta manera, al compilar el archivo **SCSS**, el valor de la variable será sustituido por su valor real.

##### ✏️  Creando un Mixin

Un **mixin** en ***Sass*** es una porción de código reutilizable que define un conjunto de estilos **CSS** que se pueden incluir en cualquier selector. En otras palabras, un **mixin** es una función que toma uno o varios argumentos y devuelve una serie de estilos **CSS** que se pueden aplicar a cualquier selector.

La sintaxis para definir un mixin es la siguiente:
```css
@mixin nombre-mixin(argumentos) {
  // Código CSS del mixin
}
```

Por ejemplo, supongamos que deseamos crear un **mixin** para centrar elementos horizontalmente en una página.
Sería de la siguiente manera en el archivo `main.scss`:

1. 
```scss
@mixin center {
  display: flex;
  justify-content: center;
  align-items: center;
}
```
2.  Para utilizar el **mixin** en un selector, simplemente se debe incluir el nombre del **mixin** precedido por un signo de arroba `(@)`. Por ejemplo en nuestro archivo `base.scss`:
```scss
div {
  @include center;
}
```

##### ✏️ Otro ejemplo de **Mixin**:  

para definir un **mixin** que establezca un borde con un color y un ancho específicos, se puede usar la siguiente sintaxis:
```scss
@mixin border($color, $width) {
  border: $width solid $color;
}
```
Luego, se puede llamar a este mixin en cualquier lugar que se importe el archivo que contiene la definición del mixin. Por ejemplo:
```scss
.box {
  @include border(red, 2px);
}
```
Este código generará el siguiente CSS:
```scss
.box {
  border: 2px solid red;
}
```

> **NOTA:**  Los mixins deben definirse en un archivo Sass separado para que puedan ser importados en otros archivos Sass. Por lo tanto, se recomienda crear un archivo "mixins.scss" o similar para contener todos los mixins de un proyecto Sass.

Una vez que se ha definido el mixin en el archivo "mixins.scss", se puede importar en cualquier otro archivo Sass que necesite usarlo usando la siguiente sintaxis:
```scss
@import 'mixins';
```
Esto importará todos los mixins definidos en el archivo "mixins.scss" en el archivo Sass actual. Luego, se pueden llamar a los mixins donde sea necesario en ese archivo.





📌 *Eso era todo , esperado que a alguien le pueda servir*

👀[Danielisho](https://github.com/Danielisho)

<!-- ------------------- -->


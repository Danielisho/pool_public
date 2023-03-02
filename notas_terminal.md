# Clonar un repositorio de GitHub desde la terminal

1. Abre la terminal en tu computadora.

2. Navega a la ubicación en la que deseas clonar el repositorio de **GitHub**.   Puedes usar el comando **"cd"** para cambiar de directorio. Por ejemplo, si deseas clonar el repositorio en la carpeta de "Documentos", escribe en la terminal:
```sh
cd Documentos
```
3. Copia la **UR**L del repositorio de GitHub que deseas clonar. Puedes encontrar esta URL en la página del repositorio en GitHub.     
Ejemplo: `https://github.com/user/nombre_del_repositorio`
4. Escribe el siguiente comando en la terminal:  
```sh
git clone <URL del repositorio>
```

> Por ejemplo, si la URL del repositorio es: "https://github.com/usuario/nombre-repositorio.git", el comando completo sería:

```sh 
git clone https://github.com/usuario/nombre-repositorio.git
```

> Presiona Enter para ejecutar el comando. Git clonará el repositorio de GitHub en la ubicación que especificaste en el paso 2.

**ATENCIÓN**:   
`Si el repositorio es privado, es posible que debas proporcionar tus credenciales de GitHub para completar el proceso de clonación`.
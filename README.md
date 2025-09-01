Clase git



Paso 1: Debemos ingresar a https://git-scm.com/downloads/win y descargar Git

Paso 2: Debemos ingresar a GitHub y crear un cuenta, normalmente para que GitHub te deje ingresar pedirá una confirmación del correo

Paso 3: Debemos crear una carpeta en nuestro equipo (No importa el nombre)

Paso 4: Abrimos Git Bush

Paso 5: Para poder conectar nuestro repositorio local con GitHub debemos configurar la cuenta que registramos para hacer eso ejecutamos los siguientes comandos:



git config --global user.name "Nombre de nuestra cuenta en GitHub"

git config --global user.email "Correo que registramos en GitHub"



Teniendo ya nuestra cuenta configurada procedemos a ubicar nuestra carpeta en git Bush para crear el repositorio local

Paso 6: Para ubicarnos en git Bush simplemente escribimos el comando **ls** esto nos mostrara en donde estamos ahora mismo en nuestro git, para ingresar a las carpetas para tener la ruta a la carpeta que creamos vamos a usar el comando **cd (Nombre de la carpeta)** hacemos esto hasta llegar a la carpeta que creamos

Paso 7: Vamos a ejecutar el siguiente comando **git init** este comando nos permitirá crear el repositorio local donde estamos ubicados 

Paso 8:Crearemos un block de notas o metemos un archivo de código que queramos publicar en nuestro repositorio, luego ingresaremos este comando en git Bush 



git status , este comando nos mostrara todos los archivos que contiene la carpeta del repositorio local , si están en rojo es porque no se han publicado en GitHub y si están en verde ya han sido publicado, también podemos modificar el archivo y este nos mostrara que ha sido modificado y debemos publicarlo


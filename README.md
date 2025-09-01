Clase git



Paso 1: Debemos ingresar a https://git-scm.com/downloads/win y descargar Git

Paso 2: Debemos ingresar a GitHub y crear un cuenta, normalmente para que GitHub te deje ingresar pedirá una confirmación del correo, una vez iniciados nos aparecerá un botón verde a la izquierda que dice **Crear repositorio** le damos click y podremos dar un nombre al repositorio y configurarlo a nuestra necesidad.

Paso 3: Debemos crear una carpeta en nuestro equipo (No importa el nombre) donde queramos crear nuestro repositorio local

Paso 4: Abrimos Git Bush

Paso 5: Para poder conectar nuestro repositorio local con GitHub debemos configurar la cuenta que registramos para hacer eso ejecutamos los siguientes comandos:



git config --global user.name "Nombre de nuestra cuenta en GitHub"

git config --global user.email "Correo que registramos en GitHub"



Teniendo ya nuestra cuenta configurada procedemos a ubicar nuestra carpeta en git Bush para crear el repositorio local

Paso 6: Para ubicarnos en git Bush simplemente escribimos el comando **ls** esto nos mostrara en donde estamos ahora mismo en nuestro git, para ingresar a las carpetas para tener la ruta a la carpeta que creamos vamos a usar el comando **cd (Nombre de la carpeta)** hacemos esto hasta llegar a la carpeta que creamos

Paso 7: Vamos a ejecutar el siguiente comando **git init** este comando nos permitirá crear el repositorio local donde estamos ubicados

Paso 8: Crearemos un block de notas o metemos un archivo de código que queramos publicar en nuestro repositorio, luego ingresaremos este comando en git Bush



git status , este comando nos mostrara todos los archivos que contiene la carpeta del repositorio local , si están en rojo es porque no se han publicado en GitHub y si están en verde ya han sido publicado, también podemos modificar el archivo y este nos mostrara que ha sido modificado y debemos publicarlo

Paso 9: Para agregar los archivos debemos ejecutar los siguientes comandos **Git add (Nombre del archivo)** después cada vez que queramos agregar algo o modificar debemos hacer un commit con el siguiente comando **git commit -m "Nombre del commit"**

Paso 10: En GitHub nos aparecerá unos comandos para ejecutar ya cuando hacemos el commit algo parecido a esto:



git remote add origin https://github.com/Nombre de la cuenta/Nombre del repositorio

git branch -M main

git push -u origin main



Simplemente copiamos y pegamos ese comando y automáticamente el archivo que agregamos se subirá a nuestro repositorio en GitHub.



Paso final: A partir de ahí ya tenemos nuestro repositorio creado en GitHub con nuestro archivo subido, cada vez que queramos subir algo seguimos los mismos pasos de **git add (nombre del archivo)** y **git commit -m "Nombre del commit"** (**Nota**: si es una modificación al archivo es recomendable especificar en el nombre del commit que es un Modify a X archivo"



por ultimo para publicar estos nuevos archivos o modificaciones vamos a ejecutar el comando **Git Push** y automáticamente va a publicarlo en nuestro repositorio de GitHub.



Muchas gracias por su atención :)


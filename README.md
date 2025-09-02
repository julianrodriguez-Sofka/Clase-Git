# Introducción y Git Fundamentals





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





# Git Avanzado y Branching







Para comenzar esta clase debemos estar ya ubicados en nuestra carpeta donde tenemos nuestro repositorio en GitHub.



Vamos a identificar lo que son las ramas y como podemos crearlas.

Las ramas son espacios diferentes en nuestro proyecto, la rama mas importante es la **Main** pero para añadir cambios o corregir errores se crean diferentes ramas según su necesidad, en este caso vamos a crear las ramas **de Develop, Hotfix y Feature**. 



El **Develop** es donde se trabaja el proyecto como si fuera la main pero sin la necesidad de estar publicado para los usuarios, asi nos aseguramos que todo lo que estemos haciendo no tiene ninguna falla y este todo en orden para poder pasarlo a la Main (Por ejemplo esta primera parte se esta creando primero en Develop)

El **Hotfix** es cuando el proyecto tiene un problema/bug y intentamos arreglarlo mediante esta rama solo el problema en especifico, (en este caso creare un conflicto con el merge e intentare resolverlo con esta rama)

<<<<<<< HEAD
El **Feature** se utiliza cuando vamos a añadir cosas nuevas en nuestro proyecto en la rama de **Develop**, no podemos añadirlo directamente a la main porque primero debemos asegurarnos que todo funciona correctamente antes de ser publicado en la main 
=======
El **Feature** se utiliza cuando vamos a añadir cosas nuevas en nuestro proyecto en la rama de **Develop**, no podemos añadirlo directamente a la main porque primero debemos asegurarnos que todo funciona correctamente antes de ser publicado en la main
=======
##### **¿Cómo crear ramas, moverse entre ramas y eliminar ramas?**




Para crear ramas debemos insertar el siguiente comando `git cheackout -b (Nombre de la rama)` o también podemos usar `git switch -c (Nombre de la rama)`.

Para poder ver la lista de las ramas que tenemos usamos el siguiente comando `git branch`

Para eliminar una rama debemos usar `git Branch -d (Nombre de la rama)`

Para movernos entre ramas usaremos el comando `git switch (Nombre de la rama)`



También podemos guardar lo que hacemos en nuestra rama, esto se realiza cuando estemos trabajando en una rama y aun no hemos terminado nuestro trabajo y no queremos pasarlo a la la rama main o Develop pues podemos guardar sin ningún problema, en este caso voy a hacerlo con la rama Feature.



Para esto usaremos el comando `git stash` para guardar temporalmente estos nuevos cambios

Ahora terminaremos de explicar este tema creando un conflicto y como resolverlo

para ver la lista de los stash que hemos hecho se usa el comando `git stash list`
para volver a traer esos datos usamos el comando `git stash pop` en la rama que los queramos traer.

Normalmente cuando hagamos esto nos va generar un conflicto, en nuestro archivo nos va indicar exactamente que es el update y stash que estamos aplicando, modificamos como nos parezca correcto y hacemos el `git add .` y el commit

como podemos observar hice un error a propósito vamos a generar el conflicto y a resolverlo

Al hacer un git merge y tengo un conflicto me debe de salir algo asi:
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

Esto me indica que debo resolver los conflictos del archivo y también me indica lo que se ha modificado, vamos a corregir el comando correcto que es `git stash pop` y borrar el texto que cree antes arriba, también debemos eliminar las indicaciones que nos coloca y colocar el archivo como debe ser.


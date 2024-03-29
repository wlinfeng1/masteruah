# Práctica GIT
## _1. Commit y push inicial_
- Clonamos nuestro repositorio remoto al local con el comando 'git clone https://github.com/bingchilling01/masteruah/'
- Cambiamos al directorio ./masteruah con 'cd masteruah'
- Agregamos el fichero README con 'git add README.md'
- Hacemos commit con "git commit -m 'commit inicial"'
- Y hacemos push para subir README al repositorio remoto con 'git push'
## _2. Fichero 1.txt y tag v0.1_
- Creamos el fichero 1.txt con 'echo "este es el primer fichero" > "fichero 1.txt"'
- Agregamos dicho fichero con 'git add "fichero 1.txt"' 
- Hacemos commit con 'git commit -m "añadir fichero 1"'
- Añadimos el tag con 'git tag v0.1'
- Y subimos los cambios con 'git push --tags' para que se suba con el tag especificado
## _3. Crear rama v0.2_
- Creamos la rama v0.2 con 'git branch v0.2'
- Cambiamos de rama con 'git checkout v0.2' 
- Creamos el 'fichero 2.txt' con 'echo "este es el segundo fichero" > "fichero 2.txt"'
- Añadimos el segundo fichero con 'git add "fichero 2.txt"'
- Hacemos commit con 'git commit -m "añadir fichero 2 en la rama v0.2"'
- Y subimos los cambios en la rama v0.2 con 'git push -u origin v0.2', el parámetro -u origin v0.2 especifica la rama en 
la que queremos subir el archivo
## _4. Fusionar rama principal con v0.2_
- Cambiamos a la rama principal con 'git checkout main'
- Fusionamos la rama principal con la v0.2 con 'git merge v0.2' estando en la rama principal
## _5. Fusión conflictiva_
- Cambiamos el contenido del primer fichero con 'echo "hola" > "fichero 1.txt"'.
- Añadimos dicho fichero con 'git add "fichero 1.txt"'
- Hacemos commit con 'git commit -m "añadir fichero 1 con conflictos"'
- Nos cambiamos a la rama v0.2 con 'git checkout v0.2'
- Modificamos el hola del fichero 1 con 'echo "adios" > "fichero 1.txt"'
- Añadimos otra vez el fichero estando en la rama 2 con 'git add "fichero 1.txt"'
- Hacemos commit con 'git commit -m "añadir fichero 1 con conflictos en v0.2"'
- Nos cambiamos a la rama principal con 'git checkout main'
- Y fusionamos la rama principal con la v0.2 con 'git merge v0.2'
- Nos sale el conflicto como se ve en la captura:
![CONFLICTO](https://github.com/bingchilling01/masteruah/blob/main/capturas/1conflicto.png "CONFLICTO")
## _6. Listar ramas fusionadas y no fusionadas_
- Listamos las ramas fusionadas con 'git branch --merge' y vemos que sale sólo la principal
- Listamos las ramas sin fusionar con 'git branch --no-merge' y vemos que sale la v0.2
![Lista_fusiones](https://github.com/bingchilling01/masteruah/blob/main/capturas/2listado.png "Listado_fusiones")
## _7. Solucionar conflicto_
- Vemos el archivo conflictivo con 'git status' y vemos que es el fichero 1.txt
![fichero conflictivo](https://github.com/bingchilling01/masteruah/blob/main/capturas/3fichconf.png "git status")
- Editamos el fichero con GNU NANO con el comando 'nano "fichero 1.txt"' <br />
Antes: \
![Before](https://github.com/bingchilling01/masteruah/blob/main/capturas/4nano.png "Antes") \
Después: \
![After](https://github.com/bingchilling01/masteruah/blob/main/capturas/5nano.png "Después")
- Una vez guardado el fichero editado hacemos otra vez add con 'git add "fichero 1.txt"'
- Hacemos commit de nuevo con 'git commit -m "conflicto solucionado"'
- Y con 'git branch --merge' vemos que la rama principal y v0.2 están fusionados
![Troubleshoot](https://github.com/bingchilling01/masteruah/blob/main/capturas/6conflictosolucionado.png "Solucionado")
- Ahora hacemos push
## _8. Crear Tag v0.2 y eliminar rama v0.2_
- Eliminamos la rama v0.2 con 'git branch -d v0.2'
- Y eliminamos la rama v0.2 remota con 'git push origin --delete v0.2'
- Creamos el tag v0.2 con 'git tag v0.2'
- Y hacemos push
## _10. Listar cambios_
- Podemos ver todos los commits con 'git log --oneline'
![Log](https://github.com/bingchilling01/masteruah/blob/main/capturas/7log.png "Log")
## _11. Configurar foto de perfil_
- Para eso entramos en los ajustes de nuestra cuenta y editamos la foto de perfil
![Avatar](https://github.com/bingchilling01/masteruah/blob/main/capturas/8fotoperfil.png "Foto de perfil")
## _12. Autenticación 2FA_
- Para activar la autenticación en dos factores, debemos usar una aplicación móvil como Google Authenticator, escanear el código QR
y se nos activará esta opción
![2FA](https://github.com/bingchilling01/masteruah/blob/main/capturas/9_2fa.png "2FA")
## _13. Generar clave pública del ordenador_
- La clave SSH pública de nuestro ordenador se genera con el comando 'ssh-keygen' que generará
un archivo con la clave dentro
- Para ver la clave se utiliza el comando 'cat "/ubicacion-del-archivo/clave.pub"'
![Clave SSH](https://github.com/bingchilling01/masteruah/blob/main/capturas/10clavepub.png "Clave SSH")
- Por último se copiará esta clave a la configuración de nuestra cuenta de GitHub
![setClaveSSH](https://github.com/bingchilling01/masteruah/blob/main/capturas/11inputclave.png "setClaveSSH")
![showClaveSSH](https://github.com/bingchilling01/masteruah/blob/main/capturas/12getclave.png "showClaveSSH")
## _14. Uso social de GitHub_
- Seguir a compañeros
![Follow](https://github.com/bingchilling01/masteruah/blob/main/capturas/13follow.png "Seguir a compañeros")
- Dar estrella a proyectos
![giveStar](https://github.com/bingchilling01/masteruah/blob/main/capturas/14star.png "Estrella")
## _15. Tabla de los compañeros_
|        NOMBRE          |                     GITHUB                         |
|------------------------|----------------------------------------------------|
| Javier Gómez 			     | [jalefrcracker](https://github.com/JLFcmd) 		    |
| Rafael García          | [Rafagarcia24](https://github.com/RafaGarcia24 )   |
| Lydia Moya             | [lydiamoyar](https://github.com/lydiamoyar)        |
| Alejandro Sánchez 	   | [AlexSancheez02](https://github.com/AlexSancheez02)|
| Juan Manuel Porras 	   | [Juanma104](https://github.com/Juanma104) 		      |
## _16. Añadir colaboradores_
- Para añadir colaboradores entramos en los ajustes del repositorio 'masteruah', luego en 'Collaborators'
y añadimos a los colaboradores que queramos
![Colab](https://github.com/bingchilling01/masteruah/blob/main/capturas/14colab.png "Colaboradores")
## _17. Crear organización_
- Para crear una organización, nos metemos en los ajustes de nuestra cuenta y luego en 'Organizations', nos creamos una
y quedaría así:
![Organizacion](https://github.com/bingchilling01/masteruah/blob/main/capturas/15org.png "Organizacion")
## _18. Equipos en la organización_
![Equipos](https://github.com/bingchilling01/masteruah/blob/main/capturas/16teams.png "Teams")
## _19. Crear index.html de la organización_
![INDEX](https://github.com/bingchilling01/masteruah/blob/main/capturas/17index.png "index.html")
## _20. Copiar proyectos de otros como forks_
- Para copiar un fork de un repositorio ajeno al nuestro se hace clic en el botón fork:
![Fork](https://github.com/bingchilling01/masteruah/blob/main/capturas/fork.png "fork")
- Y ya estaría en nuestro repositorio:
![Fork_ported](https://github.com/bingchilling01/masteruah/blob/main/capturas/19forkportado.png "fork_ported")
## _21. Hacer un pull request_
- Para hacer un pull request aplicamos cambios en los archivos fuente de nuestro fork, hacemos clic en la pestaña 'Pull requests', luego en 'New request' y al final en 'Create Pull request', y tendremos que esperar a que el autor original acepte nuestros cambios
- Pull request a Juan Manuel:
![Pull_Request](https://github.com/bingchilling01/masteruah/blob/main/capturas/rama_pullreq2.png "Pull_request")
- Pull request a Rafael García:
![Pull_Request](https://github.com/bingchilling01/masteruah/blob/main/capturas/rama_pullreq.png "Pull_request")
## _22. Gestionar pull requests_
- En los pull requests de nuestro repositorio podemos gestionarlos:
![Gestion pull request](https://github.com/bingchilling01/masteruah/blob/main/capturas/gestpullreq.png "Gestion pull request")
![Gestion pull request](https://github.com/bingchilling01/masteruah/blob/main/capturas/gestpullreq2.png "Gestion pull request")

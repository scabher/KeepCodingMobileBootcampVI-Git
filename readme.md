
Autor: Sergio Cabrera Hernández

*¿Qué comando utilizaste en el paso 11? ¿Por qué?*

	git reset --hard HEAD~1
	reset: Para ir a un commit concreto
	--hard: Para modificar el working copy
	HEAD~1: Para movernos justo al anterior del actual

*¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?*

	git reflog
	reflog: Para obtener el identificador del commit al que me quiero mover

	git reset --hard 6036b3b
	reset: Para ir a un commit concreto
	--hard: Para actualizar el working copy con el contenido de ese commit
	6036b3b: Identificador del commit al que me quiero mover (justo el anterior)

*El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?*

	No. Porque contienen los mismos datos ya que el contenido del working copy de y los de la rama master son los mismos.

*El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?*

	Si. Porque el contenido del fichero git-nuestro.md de las ramas que se están mezclando son distintos y git no lo puede resolver automáticamente porque en ambas se modificaron las mismas líneas.

*El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?*

	No. El archivo git-nuestro eran distintos pero git lo ha resuelto automáticamente tomando el contenido de la rama styled haciendo un fast-forward.

*¿Qué comando o comandos utilizaste en el paso 25?*

    git log --graph

*El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?*

    Sí. Porque master y title forman una lista (no un árbol), con lo que bastaría con desplazar el puntero HEAD.

*¿Qué comando o comandos utilizaste en el paso 27?*

    git reset HEAD~1

*¿Qué comando o comandos utilizaste en el paso 28?*

    git checkout -- git-nuestro.md

*¿Qué comando o comandos utilizaste en el paso 29?*

    git branch -D title

*¿Qué comando o comandos utilizaste en el paso 30?*

    git merge a8193f2
    a8193f2: Identificador de la rama devuelto por el git branch -D title

*¿Qué comando o comandos usaste en el punto 32?*

    git reflog
    git checkout e9d06c6
    e9d06c6: Identificador del commit inicial obtenido con git reflog

*¿Qué comando o comandos usaste en el punto 33?*

    git reflog
    git checkout a8193f2
    a8193f2: Identificador del commit donde se añadió el título en master desde title
11. Primero utilicé el comando git reset --hard 55eb539fd3b378ab23e2f0ed073014f0bee0f3c7, y posteriormente, al ver que HEAD se me quedaba en el commit, tuve que trasladar HEAD al antiguo commit para conseguir eliminar del todo el 2º commit. Lo hice con el siguiente comando git checkout main

12. Para rescatar el commit que acabamos de olvidar, utilicé el comando git reflog, para observar todos los commit por los que había pasado HEAD, como super identificar su HASH, envié ahí con git checkout 2e09d9e83e71de88975a37c937ab7df273913625, para trasladar el puntero HEAD al commit, y posteriormente hice git chekout a la rama styled.  

13. No causo ningún conflicto. En mi caso, ya había enviado HEAD, a ese commit, por lo que no me dio ningún error de conflicto. 

19. Como tengo HEAD en “htmlify”, y quiero que styled se coma a htmlify, pasaré HEAD a styled, y desde ahí le haré un git merge. En este caso, si que me salto un conflicto. Fui al área de trabajo, me quedé con los cambios de la styled rama, añadí los cambios y los guardé como un commit merge. 

21. Enío HEAD a la rama main, con git log checkout main. Una vez ahí realicé el merge, que puede ser fast, con el comando: git merge styled. Sin conflictos. 

26. Para hacer un merge no fast, le he metido esa obligación el comando, y, para unir la rama main, donde estaba HEAD, he utilizado title. git merge --no-ff title. Sin conflictos. 

27. Para deshacer el merge, utilice el comando git reset –merge <file>, al ver que no se movían las ramas de ahí, ejecute el comando git reset <hash commit anterior>, para enviar main y HEAD ahí. 

28. Aquí utilicé el comando git restore git-nuestro.md

29. Para eliminar la rama use el comando git Branch -d title

30. Para rehacer el merge que habíamos hecho, busqué el hash del merge en git reflog, y al encontrarlo envié ahí HEAD. 

32. Para volver al commit inicial, envío la rama main, quien ya incluye HEAD al hash del primer commit. git reset d1a022259a29b37dea65c1ecf226784e853da6a8

33. Misma idea que el enunciado anterior, pero enviándolo al último commit. git reset baa3590b248c094a7923a4e88dd6908fde563c3e

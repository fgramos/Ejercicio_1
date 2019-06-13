# Ejercicio_1
Práctica del curso de git, gitHub y Sourcetree 

**- ¿Qué comando utilizaste en el paso 11? ¿Por qué?**

Primero un `$ git reflog` para ver lo sucedido y después `$ git reset --hard head~1`

**- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

 Primero `$ git reflog`  , busqué elHASH del ultimo commit y 

`$ git reset --hard c529706`

`HEAD is now at c529706 Modificacion del archivo git-nuestro.md`

**- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

No ,Styled proviene de donde está master...estan en línea

`$ git merge master`

`Already up to date.`

**- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

Si,  git-nuestro tiene contenido distinto en las mismas líneas en la rama _htmlify_ y en _styled_

`$ git merge --no-ff htmlify`

`Auto-merging git-nuestro.md`

`CONFLICT (content): Merge conflict in git-nuestro.md`

`Automatic merge failed; fix conflicts and then commit the result.`

**- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

No, el contenido es distinto y no se genera conflicto.

`$ git merge --no-ff styled`

`Merge made by the 'recursive' strategy.`

 `git-nuestro.md | 31 +++++++++++++++++++++----------`

 `1 file changed, 21 insertions(+), 10 deletions(-)`

**- ¿Qué comando o comandos utilizaste en el paso 25?**

`$ git log --graph --decorate`

**- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

Si, la rama _Master_ absorbería los commits que se han realizado hasta llegar a la rama _Title_ y las dos ramas estarían apuntando al mismo nodo. Están en línea.

**- ¿Qué comando o comandos utilizaste en el paso 27?**

`$ git reset HEAD~1`

**- ¿Qué comando o comandos utilizaste en el paso 28?**

`$ git status`  para ver cambios realizados en el working copy y staging area

Como el fichero git-nuestro.md estaba  modificado,

`$ git checkout -- git-nuestro.md`

**- ¿Qué comando o comandos utilizaste en el paso 29?**

Primero vi las ramas con `$ git branch`

Luego borré la rama con `$ git branch -D title`

**- ¿Qué comando o comandos utilizaste en el paso 30?**

`$ git reflog` para buscar el último merge y seleccionar su código Hash.

`92bcadd (HEAD -> master) HEAD@{0}: reset: moving to HEAD~1`

`b3a4e85 HEAD@{1}: merge title: Merge made by the 'recursive' strategy.`

Después me muevo con `$ git checkout b3a4e85` y me quedo en estado _'detached HEAD'_ 



**- ¿Qué comando o comandos usaste en el paso 32?**

`$ git reflog` para buscar el primer commit realizado y seleccionar su código Hash.

Me sitúo en él con `$ git checkout 7b3d4c6`


**- ¿Qué comando o comandos usaste en el punto 33?**



`$ git reflog` para buscar el último merge realizado (descartando los anteriores checkouts y un reset) y seleccionar su código Hash.

b3a4e85 HEAD@{4}: merge title: Merge made by the 'recursive' strategy.

Me sitúo en él con `$ git checkout b3a4e85`




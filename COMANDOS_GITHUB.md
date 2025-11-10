# COMANDOS DE GITHUB

## PARA ENLAZAR UNA PC CON LOS REPOSITORIOS REMOTOS

```bash
git config --global user.email "coremanrique@gmail.com"
git config --global user.name "criptocore"
```

- Para verificar el usuario y correo que enlaza esta pc con el repo remoto:

```bash
git config --global --list
```

- Para eliminar usuario o correo configurado en Git:

```bash
git config --global --unset-all user.name
git config --global --unset-all user.email
```

## PARA GUARDAR PROYECTO EN REPOSITORIO LOCAL

```bash
git init           # crea la rama principal y el repositorio local
git status         # seguimiento de archivos pendientes o no guardados
git add .          # agrega archivos nuevos y modificados al área temporal
git add --all      # incluye todos los cambios (nuevos, modificaciones, eliminaciones)
git commit -m "comentario"  # envía archivos al repositorio local
```

## ENLAZAR REPOSITORIO LOCAL CON REPOSITORIO REMOTO

```bash
git remote add origin https://enlace-del-repositorio-remoto
git remote -v      # confirma si están enlazados los repos locales y remotos
git push -u origin master    # envía archivos locales al repo remoto
git push --force origin main # fuerza el envío de archivos a la rama principal
```

## CREACIÓN DE NUEVAS RAMAS

```bash
git branch rama2       # crea una nueva rama llamada rama2
git branch             # lista todas las ramas
git checkout rama2     # selecciona la rama para trabajar
git branch -m master main  # cambia nombre de master a main
```

## RECUPERAR RAMAS CLONADAS DEL REPOSITORIO REMOTO

```bash
git fetch            # descarga todas las ramas pero no las muestra
git branch -r        # muestra las ramas remotas disponibles para trabajar en ellas
```

## ELIMINAR RAMAS

```bash
git branch -d rama-a-eliminar           # elimina rama del repo local
git push origin --delete rama-a-eliminar  # elimina rama del repo remoto
```

## ELIMINAR ARCHIVOS DE CUALQUIER RAMA

```bash
git rm -r archivo-a-borrar
```

## CLONAR REPOSITORIO

```bash
git clone https://enlace-del-repositorio
```

## ACTUALIZAR ARCHIVOS LOCALES DESDE RAMA REMOTA

```bash
git pull origin main       # actualiza archivos desde la rama principal remota
git push origin main       # envía cambios del repo local al remoto
git push --force origin main # fuerza a subir cambios al repo remoto
```

## FUSIONAR RAMAS SECUNDARIAS CON RAMA PRINCIPAL (MASTER)

```bash
git checkout master       # cambiar a rama principal
git merge rama2           # fusionar rama2 con la rama principal
git merge --no-ff rama2   # fusiona manteniendo ambas ramas y commits
```

## TAGS

```bash
git tag -a 0.0.1 fn1v3bn4 -m "release 0.0.1"  # crea tag con nombre y commit
git tag 1.0.0 -m "release 1.0.0"
git push --tags                      # subir tags al repositorio remoto
git tag -d nombreTag                 # borrar un tag local
```

## REGRESAR O RESETEAR A UN PUNTO ANTES DE UN MERGE

```bash
git checkout c19b41d        # ir al commit deseado
git checkout master         # volver a la rama principal
git reset --hard c19b41d    # volver al estado del commit seleccionado
```

## VER COMMITS (NÚMEROS Y GRÁFICOS)

```bash
git log --oneline                # muestra commits en números y letras
git log --oneline --all --graph # muestra commits en gráfico
```

## VER ARCHIVOS DE CADA RAMA

```bash
dir
```

## CAMBIAR DE NOMBRE MASTER A MAIN

```bash
git branch -m master main
git config --global init.defaultBranch main  # establece main como rama por defecto
```

## ELIMINAR RAMA HEAD/MAIN

```bash
git branch -r -d origin/head
```

## SINCRONIZAR DIARIAMENTE PARA EVITAR CONFLICTOS

```bash
git checkout main               # mover a branch principal
git pull --rebase               # traer código remoto con rebase
git checkout develop            # cambiar a branch local a sincronizar
git rebase main                 # poner commits locales encima de la branch sincronizada
```


🌿 Comandos básicos de ramas en Git
🔹 1. Ver ramas
locales: git branch
remotas: git branch -r
ambas: git branch -a
🔹 2. Crear ramas
git branch nombre-rama
🔹 3. Cambiar de rama
git switch nombre-rama
🔹 4. Crear y cambiar en un solo paso

git switch -c nombre-rama

🔹 5. Borrar ramas
git branch -d nombre-rama
🔹 6. Subir una rama a GitHub
Si hemos creado la rama en local, no existe en nuestro github, para que se cree ahí este comando.

git push -u origin nombre-rama
El -u vincula la rama local con la remota

🔹 7. Traer ramas remotas
git fetch
Actualiza información de ramas remotas sin mezclar cambios
🔹 8. Unir ramas (merge)
🔹 9. Rebase (alternativa a merge)
🔹 10. Ver en qué rama estás
🔹 11. Renombrar rama
🔹 12. Eliminar rama remota





Flujo típico de trabajo

# crear rama
git switch -c feature/login

# trabajar y guardar
git add .
git commit -m "login hecho"

# subir
git push -u origin feature/login

# volver a main
git switch main

# traer cambios
git pull

# unir
git merge feature/login

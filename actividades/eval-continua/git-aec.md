***Versión en Español (English version below)***

# Actividad de Evaluación Continua - GIT

## Primera actividad

**Objetivo:** Practicar los flujos básicos de Git (fork, ramas, commits y pull requests) documentando tu propio proceso.

**Requisito general:** Debes tomar capturas de pantalla (`screenshot`) de cada comando que ejecutes en la terminal o de cada acción relevante en GitHub. Estas capturas servirán como evidencia de que realizaste tú mismo/a el proceso.

<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0195.gif"/></div>

###  Paso 1: Obtener tu propia copia del repositorio
1. Ve al repositorio original proporcionado por el docente.
2. Haz clic en el botón **"Fork"** para crear una copia del repositorio en tu cuenta de GitHub.
3. Clona ese nuevo repositorio (tu fork) en tu ordenador local usando el comando `git clone <URL_de_tu_fork>`.


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0196.gif"/></div>

### Paso 2: Crear la estructura de carpetas inicial
1. Dentro de la carpeta principal del proyecto clonado, busca (o crea si no existe) una carpeta llamada `entregas`.
2. Dentro de `entregas`, crea una nueva carpeta con tu nombre completo siguiendo este formato exacto: `nombre.apellido` (ejemplo: `juan.perez`).
3. Dentro de tu carpeta personal, crea otra subcarpeta llamada `AEC-GIT`.


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0197.gif"/></div>

### Paso 3: Primer commit y subida inicial
1. Dentro de la carpeta `AEC-GIT`, crea un archivo de texto vacío (por ejemplo, `README.txt` o `informe.txt`).
2. Abre la terminal en la raíz de tu proyecto local.
3. Añade el nuevo archivo al área de staging con `git add .` (o especificando la ruta).
4. Crea un commit con el mensaje **exacto**: `"docs: nuevo archivo"`.
5. Sube estos cambios a tu repositorio remoto (tu fork) con `git push origin main` (o la rama correspondiente).


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0198.gif"/></div>

### Paso 4: Trabajar en una rama nueva
1. Desde la rama principal, crea y cambia a una nueva rama llamada exactamente: `docs/modificaciones`.
   *(Comando sugerido: `git checkout -b docs/modificaciones`)*
2. Edita el archivo de texto que creaste antes. En su interior debes incluir:
   * Las capturas de pantalla tomadas durante toda la actividad.
   * Una breve descripción escrita de los pasos que has seguido hasta ahora.
3. Guarda tus cambios por partes lógicas. Debes realizar **entre 2 y 5 commits** distintos mientras trabajas en esta rama.
   * Los mensajes de estos commits son libres (tú decides qué poner), pero deben ser descriptivos.
   * Ejemplo de flujo: Commit 1 para añadir las primeras capturas → Commit 2 para escribir la introducción → Commit 3 para añadir el resto de capturas y conclusiones.
4. Cuando termines, sube esta rama completa a tu fork remoto con `git push origin docs/modificaciones`.


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0199.gif"/></div>

### Paso 5: Combinar las ramas localmente
1. Vuelve a tu rama principal (`main` o `master`) usando `git checkout main`.
2. Combina los cambios de tu rama `docs/modificaciones` hacia la principal usando `git merge docs/modificaciones`.
3. Resuelve cualquier conflicto si aparece (aunque no debería haber ninguno si solo modificaste el mismo archivo secuencialmente).
4. Sube la rama principal actualizada a tu fork con `git push origin main`.


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0200.gif"/></div>

### Paso 6: Crear la Pull Request (PR)
1. Ve a GitHub y entra en **tu** fork del repositorio.
2. Verás una notificación indicando que hay ramas nuevas disponibles para hacer una Pull Request. Haz clic en ella.
3. Configura la PR así:
   * **Base repository:** El repositorio ORIGINAL del docente.
   * **Base branch:** `main` (la rama principal del original).
   * **Compare repository:** Tu FORK.
   * **Compare branch:** `docs/modificaciones`.
     *(Nota: Dependiendo de cómo lo hayas hecho, podrías estar comparando directamente desde `main` si ya hiciste el merge, pero lo estándar es enviar los cambios específicos de la rama de trabajo. Si el profesor pide ver el historial de la rama, usa `docs/modificaciones`; si pide el estado final, usa `main`. Ante la duda, envía la rama `docs/modificaciones` ya que contiene el historial detallado de tus 2-5 commits).*
4. Da título a la PR (ej: "Entrega AEC-GIT - Juan Pérez") y añade una descripción breve.
5. Envía la Pull Request al repositorio original del docente.

---

### Consejos adicionales para principiantes:
* **Verifica siempre tu estado:** Usa `git status` frecuentemente para saber en qué rama estás y qué archivos han cambiado.
* **Visualiza tu historia:** Usa `git log --oneline --graph` para ver tus commits y ramas claramente antes de subir nada.
* **Las capturas:** No olvides incluirlas físicamente dentro del archivo de texto o adjuntarlas donde corresponda según indique el enunciado original ("añadiendo las capturas"). Si el archivo es `.txt`, probablemente debas describir dónde están las imágenes o usar un formato que permita insertarlas (como Markdown `.md` si está permitido, aunque el enunciado dice "archivo de tipo texto"). *Clarifica esto con tu docente si es necesario.*

---

***English Version***

# Continuous Assessment Activity - Git

## First Activity
**Objective:** Practice basic Git workflows (forks, branches, commits, and pull requests) while documenting your own process.
**General Requirement:** You must take screenshots of every command you run in the terminal or every relevant action on GitHub. These screenshots will serve as evidence that you completed the process yourself.

<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0195.gif"/></div>

###  Step 1: Get Your Own Copy of the Repository
1. Go to the original repository provided by the instructor.
2. Click the **“Fork”** button to create a copy of the repository in your GitHub account.
3. Clone that new repository (your fork) to your local computer using the command `git clone <URL_of_your_fork>`.


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0196.gif"/></div>

### Step 2: Create the Initial Folder Structure
1. Inside the main folder of the cloned project, find (or create if it doesn’t exist) a folder named `submissions`.
2. Inside `submissions`, create a new folder with your full name using this exact format: `firstname.lastname` (example: `juan.perez`).
3. Inside your personal folder, create another subfolder named `AEC-GIT`.


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0197.gif"/></div>

### Step 3: First Commit and Initial Upload
1. Inside the `AEC-GIT` folder, create an empty text file (for example, `README.txt` or `report.txt`).
2. Open the terminal at the root of your local project.
3. Add the new file to the staging area with `git add .` (or by specifying the path).
4. Create a commit with the **exact** message: `“docs: new file”`.
5. Push these changes to your remote repository (your fork) with `git push origin main` (or the appropriate branch).


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0198.gif"/></div>

### Step 4: Work on a New Branch
1. From the main branch, create and switch to a new branch named exactly: `docs/modifications`.
   *(Suggested command: `git checkout -b docs/modifications`)*
2. Edit the text file you created earlier. It should include:
   * The screenshots taken throughout the activity.
   * A brief written description of the steps you’ve followed so far.
3. Save your changes in logical chunks. You should make **between 2 and 5 separate commits** while working on this branch.
   * The commit messages are up to you (you decide what to write), but they should be descriptive.
   * Example workflow: Commit 1 to add the first screenshots → Commit 2 to write the introduction → Commit 3 to add the rest of the screenshots and conclusions.
4. When you’re done, push this entire branch to your remote fork using `git push origin docs/modifications`.


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0199.gif"/></div>

### Step 5: Merge the branches locally

1. Return to your main branch (`main` or `master`) using `git checkout main`.
2. Merge the changes from your `docs/modifications` branch into the main branch using `git merge docs/modifications`.
3. Resolve any conflicts that arise (though there shouldn’t be any if you only modified the same file sequentially).
4. Push the updated main branch to your fork with `git push origin main`.


<div><img width="30" src="https://www.gifsanimados.org/data/media/712/numero-imagen-animada-0200.gif"/></div>

### Step 6: Create the Pull Request (PR)
1. Go to GitHub and navigate to **your** fork of the repository.
2. You’ll see a notification indicating that there are new branches available to create a Pull Request. Click on it.
3. Configure the PR as follows:
   * **Base repository:** The instructor’s ORIGINAL repository.
   * **Base branch:** `main` (the main branch of the original).
   * **Compare repository:** Your FORK.
   * **Compare branch:** `docs/modifications`.
     *(Note: Depending on how you set things up, you might be comparing directly from `main` if you’ve already merged, but the standard practice is to submit the specific changes from the working branch. If the instructor asks to see the branch history, use `docs/modifications`; if they ask for the final state, use `main`. If in doubt, submit the `docs/modifications` branch, as it contains the detailed history of your 2–5 commits).*
4. Give the PR a title (e.g., “AEC-GIT Assignment – Juan Pérez”) and add a brief description.
5. Submit the Pull Request to the instructor’s original repository.

---

### Additional Tips for Beginners:
* **Always check your status:** Use `git status` frequently to see which branch you're on and which files have changed.
* **View your history:** Use `git log --oneline --graph` to clearly see your commits and branches before pushing anything.
* **Screenshots:** Don’t forget to physically include them within the text file or attach them where appropriate, as indicated in the original prompt (“adding the screenshots”). If the file is a `.txt` file, you’ll likely need to describe where the images are located or use a format that allows you to embed them (such as Markdown `.md` if allowed, even though the prompt says “text file”). *Clarify this with your instructor if necessary.*

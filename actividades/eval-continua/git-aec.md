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

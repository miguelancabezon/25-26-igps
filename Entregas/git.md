
# 🧠 Wiki de Git

## Índice

- [Introducción](#introducción)
- [Instalación](#instalación)
- [Configuración inicial](#configuración-inicial)
- [Comandos básicos](#comandos-básicos)
- [Trabajo con ramas](#trabajo-con-ramas)
- [Repositorios remotos](#repositorios-remotos)
- [Stash (guardar cambios temporales)](#stash-guardar-cambios-temporales)
- [Revertir cambios](#revertir-cambios)
- [Inspección y comparación](#inspección-y-comparación)
- [Subir a GitHub (ejemplo)](#subir-a-github-ejemplo)
- [Buenas prácticas](#buenas-prácticas)
- [Ejemplo de .gitignore](#ejemplo-de-gitignore)
- [Recursos útiles](#recursos-útiles)
- [Conclusión](#conclusión)

---

## Introducción

**Git** es un sistema de control de versiones distribuido que permite a múltiples desarrolladores trabajar en un mismo proyecto sin sobrescribir sus cambios. Fue creado por **Linus Torvalds** en 2005 para gestionar el desarrollo del kernel de Linux. Git registra el historial del proyecto y facilita ramas, fusiones y colaboración.

## Instalación

### En Windows
Descarga el instalador desde https://git-scm.com y sigue el asistente. También puedes instalar Git vía Chocolatey:

```bash
choco install git
```

### En macOS
Si usas Homebrew:

```bash
brew install git
```

O bien instala Xcode Command Line Tools (incluye git):

```bash
xcode-select --install
```

### En Linux (Debian/Ubuntu)

```bash
sudo apt update
sudo apt install git
```

Para otras distribuciones usa el gestor de paquetes correspondiente (yum, dnf, pacman...).

## Configuración inicial

Después de instalar Git, configura tu nombre y correo:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@dominio.com"
```

Opcional: configura el editor por defecto y el formato de diffs:

```bash
git config --global core.editor "code --wait"   # si usas VS Code
git config --global color.ui auto
```

Verifica tu configuración:

```bash
git config --list
```

## Comandos básicos

Descripción rápida de los comandos más usados:

- `git init` — Inicializa un nuevo repositorio Git en el directorio actual.
- `git clone <url>` — Clona un repositorio remoto.
- `git status` — Muestra el estado de los archivos (modificados, staged, sin seguimiento).
- `git add <archivo|.>` — Agrega archivos al área de preparación (staging area).
- `git commit -m "mensaje"` — Crea un commit con los cambios staged.
- `git log` — Muestra el historial de commits.
- `git diff` — Muestra diferencias entre archivos/commits.
- `git reset <archivo>` — Quita un archivo del área de preparación.
- `git rm <archivo>` — Elimina un archivo y lo marca para commit.
- `git mv <origen> <destino>` — Renombra o mueve un archivo.

Ejemplo flujo mínimo:

```bash
git init
git add .
git commit -m "Primer commit"
```

## Trabajo con ramas

Las ramas permiten desarrollar funcionalidades aisladas:

- Crear una rama:

```bash
git branch nombre-rama
```

- Cambiar a una rama existente:

```bash
git checkout nombre-rama
```

- Crear y cambiar a la vez:

```bash
git checkout -b nombre-rama
```

- Listar ramas:

```bash
git branch
```

- Fusionar una rama en la rama actual:

```bash
git merge nombre-rama
```

- Eliminar una rama (local):

```bash
git branch -d nombre-rama
```

Consejo: usa ramas por cada feature, bugfix o tarea y realiza revisiones antes de fusionar (pull requests).

## Repositorios remotos

- Agregar un remoto:

```bash
git remote add origin <url>
```

- Listar remotos:

```bash
git remote -v
```

- Subir cambios (push):

```bash
git push origin main
```

- Traer y fusionar cambios (pull):

```bash
git pull origin main
```

- Descargar metadatos sin fusionar:

```bash
git fetch
```

Nota: el nombre de la rama por defecto puede ser `main` o `master` según el proyecto.

## Stash (guardar cambios temporales)

Guarda cambios no confirmados para cambiar de contexto sin perder trabajo:

```bash
git stash          # guarda los cambios
git stash list     # lista stashes
git stash pop      # aplica y elimina el stash más reciente
git stash apply    # aplica sin eliminar
```

## Revertir cambios

- Revierte cambios no confirmados (archivo local):

```bash
git checkout -- <archivo>
```

- Revertir (deshacer) el último commit pero mantener los cambios en el área de trabajo:

```bash
git reset --soft HEAD~1
```

- Revertir el último commit y eliminar los cambios (peligroso):

```bash
git reset --hard HEAD~1
```

- Crear un nuevo commit que deshace otro commit anterior (seguro para repositorios compartidos):

```bash
git revert <commit>
```

Usa `git reflog` si necesitas recuperar commits perdidos por resets.

## Inspección y comparación

- Historial compacto y gráfico:

```bash
git log --oneline --graph --decorate --all
```

- Ver diferencias entre trabajo actual y último commit:

```bash
git diff
```

- Mostrar un commit en detalle:

```bash
git show <commit>
```

## Subir un proyecto existente a GitHub (ejemplo)

Si tienes un proyecto local y quieres subirlo a un repo nuevo en GitHub:

```bash
git init
git add .
git commit -m "Primer commit"
git branch -M main
git remote add origin https://github.com/usuario/repositorio.git
git push -u origin main
```

## Buenas prácticas

- Mensajes de commit claros y descriptivos (imperativo, breve).
- Usa ramas para cada nueva funcionalidad o corrección.
- Haz revisiones de código via pull requests antes de fusionar.
- Mantén el repositorio libre de archivos binarios innecesarios.
- No subas secretos (usa variables de entorno, vaults o GitHub Secrets).
- Añade un `.gitignore` adecuado al proyecto.

## Ejemplo de .gitignore

```gitignore
# Node.js
node_modules/
dist/
.env

# Python
__pycache__/
*.pyc

# macOS
.DS_Store

# Logs
*.log
```

## Recursos útiles

- Documentación oficial de Git: https://git-scm.com/docs
- Pro Git (libro gratuito): https://git-scm.com/book/es/v2
- GitHub Docs: https://docs.github.com
- Git cheat sheet: https://education.github.com/git-cheat-sheet-education.pdf

## Conclusión

Git es una herramienta esencial para el control de versiones y la colaboración en proyectos de software. Dominar sus conceptos básicos —repositorios, ramas, merges y flujos remotos— mejora la productividad y reduce riesgos en el desarrollo.


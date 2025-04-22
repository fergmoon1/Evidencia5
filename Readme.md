# Instalación y Configuración de Herramientas de Versionamiento (Local / Web)

## Evidencia de Desempeño: GA7-220501096-AA1-EV04

Este proyecto corresponde a la evidencia de desempeño para el componente formativo "Integración Continua", donde se documenta el proceso de instalación y configuración de herramientas de control de versionamiento tanto local como remoto.

## 📋 Contenido del Proyecto

- [Introducción](#introducción)
- [Objetivos](#objetivos)
- [Git Local](#git-local)
  - [Instalación](#instalación-de-git-local)
  - [Configuración Inicial](#configuración-inicial-de-git-local)
  - [Comandos Básicos](#comandos-básicos-git-local)
- [Git Remoto](#git-remoto)
  - [Configuración de GitHub](#configuración-de-github)
  - [Conexión entre Git Local y Remoto](#conexión-entre-git-local-y-remoto)
  - [Comandos Básicos](#comandos-básicos-git-remoto)
- [Flujo de Trabajo](#flujo-de-trabajo)
- [Visualización Comparativa](#visualización-comparativa)

## 📝 Introducción

El control de versiones es un sistema que registra los cambios realizados en un archivo o conjunto de archivos a lo largo del tiempo, de modo que puedas recuperar versiones específicas más adelante. En el desarrollo de software moderno, especialmente en entornos de integración continua, el uso de herramientas de versionamiento como Git se ha vuelto indispensable.

Este proyecto documenta la instalación y configuración de Git como sistema de control de versiones tanto en su modalidad local como remota (GitHub), ofreciendo una guía detallada de los pasos necesarios y una comparativa visual entre ambos sistemas.

## 🎯 Objetivos

- Instalar y configurar Git como herramienta de control de versiones local
- Configurar una cuenta y repositorio en GitHub como sistema de control de versiones remoto
- Establecer la conexión entre el repositorio local y el remoto
- Documentar los comandos básicos para cada sistema
- Proporcionar una visualización comparativa entre ambos sistemas

## 💻 Git Local

### Instalación de Git Local

1. **Descargar Git**:
  - Para Windows: Visitar [git-scm.com](https://git-scm.com/) y descargar el instalador
  - Para macOS: Usar Homebrew `brew install git` o descargar desde la web oficial
  - Para Linux: Usar el gestor de paquetes (ejemplo: `sudo apt-get install git`)

2. **Verificar instalación**:
   ```bash
   git --version
   ```

### Configuración Inicial de Git Local

1. **Configurar identidad del usuario**:
   ```bash
   git config --global user.name "Tu Nombre"
   git config --global user.email "tu.email@ejemplo.com"
   ```

2. **Configurar editor predeterminado**:
   ```bash
   git config --global core.editor "code --wait"  # Para Visual Studio Code
   ```

3. **Verificar configuración**:
   ```bash
   git config --list
   ```

### Comandos Básicos Git Local

- **Inicializar repositorio**:
  ```bash
  git init
  ```

- **Ver estado de archivos**:
  ```bash
  git status
  ```

- **Añadir archivos al área de preparación**:
  ```bash
  git add <archivo>  # Archivo específico
  git add .          # Todos los archivos
  ```

- **Confirmar cambios (commit)**:
  ```bash
  git commit -m "Mensaje descriptivo del cambio"
  ```

- **Ver historial de commits**:
  ```bash
  git log
  ```

- **Crear y cambiar entre ramas**:
  ```bash
  git branch <nombre-rama>       # Crear rama
  git checkout <nombre-rama>     # Cambiar a rama
  git checkout -b <nombre-rama>  # Crear y cambiar en un comando
  ```

## ☁️ Git Remoto

### Configuración de GitHub

1. **Crear cuenta en GitHub**:
  - Visitar [github.com](https://github.com/) y registrarse
  - Verificar cuenta vía email

2. **Crear un repositorio remoto**:
  - Hacer clic en "New repository"
  - Establecer nombre, descripción y visibilidad
  - Crear sin README, .gitignore o licencia si ya existe repositorio local

3. **Configurar claves SSH (opcional pero recomendado)**:
   ```bash
   ssh-keygen -t ed25519 -C "tu.email@ejemplo.com"
   ```
  - Agregar la clave pública a GitHub (Settings > SSH and GPG keys)

### Conexión entre Git Local y Remoto

1. **Vincular repositorio local con remoto**:
   ```bash
   git remote add origin https://github.com/usuario/repositorio.git
   # O con SSH
   git remote add origin git@github.com:usuario/repositorio.git
   ```

2. **Verificar conexión remota**:
   ```bash
   git remote -v
   ```

### Comandos Básicos Git Remoto

- **Clonar repositorio existente**:
  ```bash
  git clone https://github.com/usuario/repositorio.git
  ```

- **Enviar cambios al repositorio remoto**:
  ```bash
  git push -u origin <rama>  # Primera vez
  git push                   # Siguientes veces
  ```

- **Obtener cambios del repositorio remoto**:
  ```bash
  git pull origin <rama>     # Fetch + merge
  git fetch origin           # Solo descarga sin fusionar
  ```

- **Ver información del repositorio remoto**:
  ```bash
  git remote show origin
  ```

## 🔄 Flujo de Trabajo

El flujo de trabajo típico combinando Git local y remoto es:

1. Realizar cambios en archivos locales
2. Revisar cambios con `git status`
3. Añadir cambios al área de preparación con `git add`
4. Confirmar cambios con `git commit`
5. Obtener cambios recientes del remoto con `git pull`
6. Resolver conflictos si existen
7. Enviar cambios al repositorio remoto con `git push`

## 📊 Visualización Comparativa

El archivo HTML incluido en este proyecto (`git-comparison.html`) ofrece una visualización interactiva de las diferencias entre Git Local y Git Remoto, incluyendo:

- Tabla comparativa con las principales diferencias
- Características detalladas de cada sistema
- Comandos comunes para cada modalidad

Para ver la comparativa, simplemente abra el archivo HTML en cualquier navegador web.

---

## 🚀 Conclusión

La implementación de sistemas de control de versiones como Git, tanto en su modalidad local como remota, es fundamental para el desarrollo moderno de software y particularmente importante en entornos de integración continua. Esta documentación proporciona una base sólida para comenzar a trabajar con estas herramientas esenciales.

---

*Proyecto desarrollado como parte de la evidencia de desempeño GA7-220501096-AA1-EV04 para el componente formativo "Integración Continua".*

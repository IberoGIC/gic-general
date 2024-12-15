Este manual proporciona una guía sencilla y práctica para configurar y usar **Git**. 

***Git***
	**Git** es un **sistema de control de versiones** que te permite llevar un registro de los cambios que haces en tu código (o archivos). Es como un historial donde puedes ver qué cambios se hicieron, cuándo los hicieron y quién los hizo. Además, te permite **volver a versiones anteriores** si algo sale mal .


---

## **🛠️ Instalación de Git**

### **Windows**

1. Descarga el instalador desde el sitio oficial: [Git for Windows](https://git-scm.com/download/win).
    
2. Ejecuta el instalador y sigue las instrucciones predeterminadas.
    
3. Verifica la instalación escribiendo este comando en la terminal:
    
```
git --version
```

### **Linux (Debian/Ubuntu)**

Ejecuta el siguiente comando en la terminal:

```
sudo apt update
sudo apt install git
```

Verifica la instalación escribiendo este comando en la terminal:

```
git --version
```

### **macOS**

Si no tienes Homebrew, instálalo usando este comando en la terminal:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Instala Git usando Homebrew:

```
brew install git
```

Verifica la instalación  escribiendo este comando en la terminal:

```
git --version
```

---

## **🔑 Configuración Inicial de Git**

Una vez instalado Git, configura tu nombre de usuario y correo electrónico (estos datos se usarán para identificar tus cambios):

```
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

Verifica tu configuración:

```
git config --list
```

---
## **✨ Trabaja con Git de manera local**
### **1. Inicializa un Repositorio Git Local**

Si tienes un proyecto en tu máquina local y quieres comenzar a usar Git:

1. Abre una terminal y navega a la carpeta del proyecto:    
    `cd ruta/a/tu/proyecto`
    
2. Inicializa un repositorio Git en esa carpeta:
    `git init`

Esto creará una carpeta `.git` oculta donde Git almacenará el historial de versiones.

### **2. Agrega archivos al área de preparación (staging)**

Una vez tengas tus primeros archivos del proyecto, antes de guardar los cambios, debes agregarlos al área de preparación:

* Agregar un archivo específico:
	```
	git add nombre_del_archivo
	```
* Agregar todos los archivos (que hayan cambiado o sean nuevos):

	```
	git add .
	```

### **3. Guarda la versión inicial**

Usa *git commit* para guardar la primer versión en el historial:
```
git commit -m "Commit inicial"
```

### **4. Guarda cambios**

Una vez realizados cambios en el proyecto, Git te mostrará que archivos han cambiado o no están siendo rastreados con el comando *git status*:
```
git status
```

Agrega los archivos que que hayan cambiado o sean nuevos usando *git add* y guarda los cambios con *git commit*:

```
git add .
git commit -m "agrega función 'suma' en main.c"
```
*Realiza **commits pequeños** y descriptivos.*

### **5. Ve el historial de cambios**

Para ver todos los commits (cambios) registrados hasta ahora usa el siguiente comando:
```
git log
```

### **6. Descarta cambios no deseados**

Si cometiste un error y quieres deshacer los últimos cambios, puedes:

- **Descartar cambios no guardados** en un archivo:
    `git checkout -- nombre_del_archivo`
    
- **Descartar todos los cambios no guardados**:
    `git reset --hard`

### **7. Ignorar archivos**
Para evitar que Git rastree ciertos archivos (por ejemplo, archivos temporales o copias generadas automáticamente por algunos editores de texto), crea un archivo llamado `.gitignore` en el directorio principal del proyecto y añade los *patrones* que quieres ignorar.

Ejemplo de `.gitignore`:
```
*.temp     # Ignora todos los archivos con terminación .temp
*.o        # Ignora todos los archivos con terminación .o
copy*     # Ignora todos los archivos que empiezan con la cadena "copy"
Build/     # Ignora el directorio "Build/" y sus contenidos
.gitignore # Ignora el archivo ".gitignore"
```
*El * representa **cualquier combinación de caracteres**, antes o después de una cadena según se coloque*.

---
## 📝 **Resumen de Comandos Básicos**

| Comando                   | Descripción                          |
| ------------------------- | ------------------------------------ |
| `git init`                | Inicializa un repositorio Git local  |
| `git status`              | Muestra el estado de los archivos    |
| `git add .`               | Agrega todos los archivos al staging |
| `git commit -m "mensaje"` | Guarda los cambios con un mensaje    |
| `git log`                 | Muestra el historial de commits      |
| `git reset --hard`        | Deshace todos los cambios locales    |

---

## **🆘 Ayuda y Referencias**

- Documentación oficial de Git: [Git Documentation](https://git-scm.com/doc)
    
- Comandos básicos de Git en una página: [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)    

Una vez te familiarices con el funcionamiento básico de **Git**, es posible que quieras integrarlo con **GitHub**, aquí hay un manual para ayudarte: [github-manual.md](https://github.com/IberoGIC/gic-general/blob/main/github-manual.md)

Si tienes dudas, no dudes en preguntar a otros miembros del GIC y los profesores que nos apoyan.

---
-,"  
[_P

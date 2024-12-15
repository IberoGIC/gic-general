Una vez conozcas el funcionamiento de **Git** para el control de versiones, este manual te ayudará a comenzar con **GitHub**, una herramienta poderosa para colaborar en proyectos y compartir código. 

***GitHub***
	**GitHub** es una plataforma en línea que **almacena tus repositorios Git** en la nube. Es como un **"Google Drive" para código**. Además de almacenar el código, te permite **colaborar** con otras personas, hacer revisiones de código, y gestionar proyectos de manera más fácil. GitHub usa Git para gestionar el historial y los cambios en el código.

*Si aún no estás familiarizado con el funcionamiento de Git, o no lo tienes instalado en tu equipo, consulta este manual:* [git-manual.md](https://github.com/IberoGIC/gic-general/blob/main/git-manual.md)

---
## **📩 Crea una cuenta en GitHub**

Ve a [https://github.com](https://github.com) y regístrate para obtener una cuenta gratuita. Asegúrate de usar tu correo electrónico universitario.

Una vez te registres con tu correo universitario podrás solicitar a GitHub una cuenta para estudiantes, que te proporciona beneficios como:
* GitHub Pro mientras seas estudiante
* Paquete de desarrollo para estudiantes
* Código en la nube con GitHub Codespaces

Solicita tu mejora a cuenta de estudiante aquí: [GitHub Education](https://github.com/education/students).

---
## **✨ Trabaja con GitHub**

### 1. **Haz un fork de un repositorio**:  

Cuando contribuyas a un proyecto, primero haz un '*Fork*' del repositorio. Esto crea una copia personal del repositorio en tu cuenta de GitHub.

- Ve al repositorio con el que deseed trabajar en GitHub.
- Haz clic en el botón '*Fork*' (en la parte superior derecha).

***Fork*** 
	Un '*Fork*' en GitHub es una **copia completa** de un repositorio (proyecto) que pertenece a otra persona u organización en **tu cuenta de GitHub**. Permite trabajar en el proyecto original sin afectar el código principal y guarda tus cambios en tu cuenta para que no se conserven solo de manera local.

### 2. **Clona un repositorio**

Para descargar tu '*Fork*' :
* Ve a tu repositorio en GitHub.
* Da click en el botón **Código** y copia el URL.
* Usa el comando **git clone** en tu terminal:

```
git clone <url_repositorio> 
```

Esto creará una carpeta con el nombre del repositorio y todo su contenido.

Considera que la carpeta se creará en el directorio en el que estabas ubicado cuando usaste el comando, puedes cambiar esto especificando una ruta como parte del comando:

```
git clone <url_repositorio> <directorio_objetivo>
```

Cuando clonas un repositorio usando Git tus cambios no se sincronizan al repositorio remoto en tu cuenta de manera automática, (tampoco al repositorio original), sino que se trabajan de manera local.

*Los comandos descritos a continuación deben ser ejecutados en el directorio donde clonaste el repositorio.*
### 3. **Actualiza tu repositorio local**

* Agrega el repositorio original como remoto:
	```
	git remote add upstream <url_repositorio_original>
	```
* Haz un '*Fetch*' de los últimos cambios en el repositorio original:
	```
	git fetch upstream
	```
* Combina los cambios en tu '*Branch*' local:
	```
	git checkout main
	git merge upstream/main
	```
* Envía los cambios a tu '*Fork*' remoto
	```
	git push origin main
	```
*Para evitar conflictos, asegúrate de tener los últimos cambios del repositorio remoto.*

***Fetch***
	**Fetch** es un comando que **descarga** los cambios más recientes del repositorio remoto (por ejemplo, GitHub) a tu repositorio local, **pero no los aplica automáticamente** a tus archivos de trabajo.
	- Actualiza la información sobre el repositorio remoto.
	- Te permite ver si hay cambios nuevos (commits, ramas, etc.) sin mezclarlos aún con tu trabajo local.
***Checkout***
	**Checkout** es un comando que te permite **moverte entre ramas** o **restaurar archivos específicos** en tu repositorio.
***Merge***
	**Merge** es el proceso de **combinar los cambios** de una rama con otra.
	- Une el historial de dos ramas, integrando los cambios en una sola.
	- Se usa, por ejemplo, para fusionar una rama de desarrollo con la rama principal.
***Push***
	**Push** es el comando que **envía tus cambios locales** al repositorio remoto.

### 4. **Crea ramas**

Antes de realizar cambios, es una buena práctica crear una '*Branch*' para cada aporte relevante:

```
git checkout -b <nombre-de-la-rama>
```

***Branch***
	Una **branch** (rama) en Git es como una **copia** del proyecto principal (llamado `main` o `master`) donde puedes trabajar en algo nuevo sin afectar el código original.  
	*Piensa en esto como:*
	**main** es tu **libro original**, mientras que una branch es como hacer una fotocopia de ese libro para editar o agregar lo que quieras sin modificar el original.

### 5. **Sube tus cambios**

Cuando tengas parte importante de un aporte guárdala en tu repositorio local y súbelo a tu repositorio remoto en GitHub.

- **Ver los cambios realizados**:
    
    ```
    git status
    ```
    
- **Añadir archivos para el commit**:
    
    ```
    git add <nombre-del-archivo>
    ```
    
    Si deseas añadir todos los cambios:
    
    ```
    git add .
    ```
    
- **Guardar los cambios en un commit**:
    
    ```
    git commit -m "Descripción breve del cambio"
    ```
* Enviar los cambios al repositorio remoto:

	```
	git push origin <nombre-de-la-rama>
	```


*Recuerda seguir las normas y convenciones para aportaciones, puedes revisarlas aquí :*  [contributing.md](https://github.com/IberoGIC/gic-general/blob/main/contributing.md)

### 6. **Crea un Pull Request (PR)**

Cuando tu aportación completa esté en tu repositorio remoto y verifiques que funciona de manera correcta, crea un **Pull Request** en GitHub:

1. Ve al repositorio original en GitHub y verás una opción para **crear un pull request** (PR).
    
2. Selecciona la rama base (generalmente `main`).
    
3.  Compara tu rama con la rama base.
    
4. Agrega una descripción clara de tus cambios y envía la solicitud.
    
5. Espera la revisión y posibles comentarios.

Cuando tu PR sea revisado y aprobado por otros miembros, se fusionará en la rama principal.

---

## **🧹 Buenas Prácticas**

- Realiza **commits pequeños** y descriptivos.
    
- Usa nombres de ramas claros, como `fix-error`, `feature-nuevo-recurso`.
    
- Mantén tu repositorio local actualizado.
    
- Borra ramas antiguas después de fusionarlas:
    
    ```
    git branch -d <nombre-de-la-rama>
    ```

---


## 📝 **Resumen de Comandos** 

| Comando                                           | Descripción                                                             |
| ------------------------------------------------- | ----------------------------------------------------------------------- |
| `git init`                                        | Inicializa un repositorio Git local                                     |
| `git status`                                      | Muestra el estado de los archivos                                       |
| `git add .`                                       | Agrega todos los archivos al staging                                    |
| `git commit -m "mensaje"`                         | Guarda los cambios con un mensaje                                       |
| `git log`                                         | Muestra el historial de commits                                         |
| `git reset --hard`                                | Deshace todos los cambios locales                                       |
| `git clone <URL_del_repositorio>`                 | Clona un repositorio remoto a tu máquina local.                         |
| `git checkout -b <nombre-de-la-rama>`             | Crea y cambia a una nueva rama                                          |
| `git push origin <nombre-de-la-rama>`             | Sube los cambios a la rama correspondiente en tu repositorio remoto.    |
| `git remote add upstream <URL_del_repositorio>` ` | Agrega un repositorio como remoto para mantener tu fork actualizado.    |
| `git fetch upstream`                              | Descarga los últimos cambios del repositorio original sin fusionarlos.  |
| `git checkout main`                               | Cambia a la rama principal (`main`).                                    |
| `git merge upstream/main`                         | Fusiona los cambios del repositorio original (remoto) en tu rama local. |
| `git push origin main`                            | Sube los cambios fusionados a tu repositorio remoto.                    |

---
## **🆘 Ayuda y Referencias**

* Manual de instalación y uso de Git: [git-manual](https://github.com/IberoGIC/gic-general/blob/main/git-manual.md)
	
* Hola Mundo en GitHub: [Tutorial Hola Mundo GitHub](https://docs.github.com/es/get-started/start-your-journey/hello-world)
	
- Documentación oficial de Git: [Git Documentation](https://git-scm.com/doc)
	
- Comandos básicos de Git en una página: [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)    

Si tienes dudas, no dudes en preguntar a otros miembros del GIC y los profesores que nos apoyan.

---
-,"  
[_P

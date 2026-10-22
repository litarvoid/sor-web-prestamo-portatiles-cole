# b0-0.1 · Metodología y estructura

- **Alumno:** Youcef
    
      
    
- **Bloque:** B0 — Prerrequisitos
    
      
    
- **Fase / ejercicio:** Fase 0.1
    
      
    
- **Fecha de inicio:** 22/10/2026
    
      
    
- **Fecha de entrega:** 22/10/2026
    
      
    

## 🎯 Qué se pedía

Crear una estructura de carpetas y notas organizadas para una bóveda llamada "bóveda HTML Casa", configurar un proyecto HTML con su repositorio local en Git, enlazarlo mediante SSH con un repositorio remoto vacío en GitHub, y guardar versiones incrementales correspondientes a la página inicial, el cambio de estado de un portátil, y la incorporación de normas y contratos con imágenes. Finalmente, comprobar la navegación entre la primera entrega y la versión actual, y repetir el proceso de forma independiente.

  

## ⌨️ Comandos y pasos importantes

- `git --version` — para comprobar que Git está instalado en el sistema.
    
      
    
- `git config --global user.name` y `git config --global user.email` — para verificar la configuración global de identidad del usuario.
    
      
    
- `git init` — para inicializar un nuevo repositorio de Git en la ruta del proyecto.
    
      
    
- `git branch -M main` — para renombrar la rama principal a `main`.
    
      
    
- `git status` — para comprobar el estado actual de los archivos (modificados, preparados, etc.).
    
      
    
- `git add .` — para preparar y añadir los archivos al área de preparación (staging area).
    
      
    
- `git commit -m "mensaje"` — para guardar una nueva versión/commit con un mensaje descriptivo.
    
      
    
- `git remote add origin <url_ssh>` — para conectar el repositorio local con el remoto en GitHub mediante SSH.
    
      
    
- `git push -u origin main` — para subir los cambios locales a la rama principal del repositorio remoto.
    
      
    
- `ssh-keygen -t rsa -b 4096 -C "correo"` — para generar las claves SSH de acceso a GitHub.
    
      
    
- `git log --oneline` — para revisar el historial de commits y los identificadores de versiones.
    
      
    
- `git checkout <hash>` — para viajar temporalmente a una versión anterior del repositorio.
    
      
    

## 🛠️ Qué he hecho

Primero, creé la carpeta raíz de la bóveda (`sor_bóveda_html_casa`) y preparé la estructura de carpetas y archivos Markdown correspondientes a la práctica dentro del entorno de notas. A continuación, configuré los comandos de verificación de Git y generé las claves SSH necesarias vinculando la clave pública en los ajustes de GitHub para autenticar la conexión.

  

Dentro de la subcarpeta del proyecto, inicialicé Git, lo conecté por SSH al repositorio remoto creado en GitHub y subí la primera versión con la página inicial y el estado del portátil disponible. Posteriormente, realicé modificaciones simulando un cambio en el estado del portátil a mantenimiento y agregué los archivos adicionales correspondientes a las normas de préstamo y los contactos con sus respectivas imágenes. Realicé los `git add` y `git commit` correspondientes para cada cambio y los subí con `git push`. Por último, comprobé el historial de versiones utilizando el identificador de commits para regresar a la primera entrega y volver de nuevo a la rama principal `main`.

  

## 🚩 Qué me ha fallado y cómo lo he resuelto

- **Error al verificar las claves SSH:** Al ejecutar un comando de verificación inicial, obtuve un error de acceso (`Permission denied` / `Could not resolve hostname` o similares relacionados con la falta de archivos de clave pública). Lo resolví generando correctamente el par de claves con `ssh-keygen`, añadiendo la clave pública a la cuenta de GitHub y asegurándome de utilizar la URL SSH correcta al configurar el remote.
    
      
    
- **Ruta de directorios incorrecta:** Durante los primeros comandos, me situé por error dentro de una subcarpeta errónea (`grabaciones` en lugar de `proyecto`). Lo solucioné saliendo de la ruta con `cd ..`, corrigiendo la ubicación y volviendo a ejecutar el flujo en la carpeta de trabajo correcta (`01_proyecto`).
    
      
    

## 🤔 Respuestas a las preguntas

1. Porque el repositorio de control de versiones se aísla específicamente dentro de la carpeta del proyecto práctico (`01_Proyecto`) y no en la raíz general de la bóveda de notas para gestionar de forma independiente el código web y la documentación.
    
      
    
2. Se modificó el estado del portátil de disponible a reservado/mantenimiento en el archivo correspondiente; en el comando `git diff`, la línea antigua aparece reflejada en rojo precedida por un signo menos (`-`) y la nueva modificación aparece en verde precedida por un signo más (`+`).
    
      
    
3. Editar un archivo significa modificar su contenido en el disco de manera local sin que Git registre todavía dichos cambios para el siguiente commit, mientras que hacer `add` (preparar el cambio) traslada esos cambios al área de preparación (_staging area_) indicando que están listos para ser guardados en la próxima versión.
    
      
    
4. Porque la ficha nueva al ser un archivo que Git aún no rastrea o que se encuentra en otra ubicación/estado no forma parte de las líneas comparadas directamente en el seguimiento de cambios del archivo CSV existente mediante `diff`.
    
      
    
5. Se prepararon individualmente los archivos de normas, contactos e imágenes adicionales utilizando comandos específicos de adición, y el comando `git diff --cached` mostró los cambios que ya estaban listos y preparados (_staged_) pendientes de confirmar en el commit.
    
      
    
6. Mediante la ejecución de `git status` o comprobando que no aparecían de forma no deseada en el control de versiones ni se subían al repositorio remoto gracias a las reglas configuradas de exclusión.
    
      
    
7. Al viajar al primer commit mediante su hash se recuperó el estado inicial de la primera versión del proyecto donde el equipo EQ03 (o el estado inicial del portátil) reflejaba su disponibilidad original anterior a los cambios de mantenimiento.
    
      
    
8. Necesita historial para auditar quién y cuándo modificó el estado de los préstamos, aunque presenta limitaciones frente a un inventario multiusuario real ya que no gestiona concurrencia en tiempo real ni bloqueos de escritura simultáneos.
    
      
    
9. Se comprobó la subida visualizando el repositorio en la interfaz web de GitHub y mediante los comandos de estado y registro locales, ocurriendo el cierre de la grabación justo después de verificar que todo estaba correctamente sincronizado y subido a la nube.
    
      
    

## 🔗 Enlaces

- **Vídeo de esta fase:** [https://youtu.be/ajr7Rrx_nnM](https://youtu.be/ajr7Rrx_nnM)
    
      
    
- **Playlist:** B0_Prerrequisitos
    
      
    

## 💭 Dudas / a repasar

- Repasar con mayor soltura la gestión de conflictos cuando se modifica un mismo archivo en diferentes ramas o versiones.
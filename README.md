# Guía para colaborar en Vault

Este repositorio contiene el **Vault** compartido. Se administra con Git y está alojado en GitHub para que varias personas puedan trabajar sin sobrescribir accidentalmente el trabajo de los demás.

Esta guía está escrita para personas que nunca han utilizado GitHub. Explica:

- cómo crear una cuenta de GitHub;
- cómo instalar las herramientas necesarias en Windows o macOS;
- cómo descargar (clonar) este repositorio;
- cómo editar el Vault;
- cómo enviar los cambios para su revisión;
- cómo funciona el proceso de revisión y aprobación
- cómo resolver los problemas más habituales.

Dirección del repositorio: <https://github.com/Challsss/Vault>

## 1. Palabras importantes

- **Git**: programa que registra los cambios realizados en los archivos.
- **GitHub**: página web donde se guarda este repositorio y se revisan los cambios.
- **Repositorio (repo)**: carpeta administrada por Git. Este repositorio es `Challsss/Vault`.
- **Clonar**: descargar una copia completa del repositorio en el ordenador.
- **Copia local**: la copia del repositorio que está en el ordenador.
- **Remoto**: la copia alojada en GitHub. En esta guía se llama `origin`.
- **Rama (branch)**: una línea de trabajo independiente. La versión compartida y aprobada está en la rama `main`.
- **Commit**: punto de guardado que contiene uno o varios cambios relacionados.
- **Push**: subir los commits locales a GitHub.
- **Pull**: descargar cambios de GitHub al ordenador.
- **Pull request (PR)**: solicitud para que el responsable revise y fusione una rama con `main`.
- **Fusionar (merge)**: combinar una rama aprobada con `main`.
- **Responsable (maintainer)**: persona encargada de revisar y aprobar los cambios. En este repositorio es el propietario, **Carles Aguilar**.
- **Conflicto**: situación en la que dos personas han cambiado la misma parte de un archivo y Git no puede decidir qué versión conservar.

El flujo básico es:

```text
clonar -> crear una rama -> editar -> hacer commit -> hacer push -> abrir un pull request -> el responsable revisa -> corregir si es necesario -> el responsable fusiona
```

## 2. Reglas de colaboración

Estas reglas se aplican a todas las contribuciones:

1. **No trabajes directamente en `main`.** Crea siempre una rama separada.
2. **No hagas push directamente a `main`.** Los cambios llegan a `main` únicamente mediante un pull request aprobado.
3. **El responsable es el filtro final.** Un pull request no termina hasta que Carles Aguilar lo aprueba y lo fusiona.
4. **Usa una rama y un pull request por tarea.** No mezcles, por ejemplo, una corrección ortográfica con una reorganización grande.
5. **No renombres, muevas o borres muchas notas sin explicar el motivo en el pull request.**
6. **Antes de abrir un pull request, actualiza tu rama desde `main` y revisa tus cambios.**
7. **Considera la versión de `main` en GitHub como la versión compartida aprobada.** No sobrescribas el trabajo de otra persona para resolver un conflicto sin revisarlo cuidadosamente.

El responsable puede aprobar un pull request, pedir cambios o rechazarlo. Esto es normal y forma parte del proceso de revisión.

## 3. Crear una cuenta de GitHub

Necesitas una cuenta de GitHub para acceder al repositorio, crear ramas en GitHub y abrir pull requests.

1. Abre <https://github.com/>.
2. Pulsa **Sign up** (Registrarse).
3. Introduce tu correo electrónico, crea una contraseña y elige un nombre de usuario.
4. Confirma tu correo usando el mensaje que GitHub te enviará.
5. Activa la autenticación en dos pasos si GitHub te lo solicita. Es muy recomendable.
6. Envía tu nombre de usuario de GitHub a Carles Aguilar para que pueda invitarte como colaborador si el repositorio es privado.
7. Abre el correo de invitación o revisa tus notificaciones de GitHub y acepta la invitación.

Si el repositorio es público, quizá puedas clonarlo sin invitación. Aun así, necesitas permiso para subir ramas directamente a este repositorio.

## 4. Instalar las herramientas recomendadas

### Windows

La opción más sencilla para principiantes es **GitHub Desktop**:

1. Descárgalo desde <https://desktop.github.com/>.
2. Ejecuta el instalador.
3. Abre GitHub Desktop.
4. Elige **Sign in to GitHub.com** e inicia sesión con tu cuenta.
5. Si GitHub Desktop solicita tu nombre y correo, utiliza los asociados a tu cuenta de GitHub.

También necesitas un editor para las notas. Si este es un Vault de Obsidian:

1. Descarga Obsidian desde <https://obsidian.md/download>.
2. Instálalo y ábrelo.

GitHub Desktop instala las herramientas de línea de comandos opcionales. Puedes usar **PowerShell** desde el menú Inicio si prefieres escribir comandos.

### macOS

La opción más sencilla también es **GitHub Desktop**:

1. Descárgalo desde <https://desktop.github.com/>.
2. Abre el archivo descargado.
3. Arrastra GitHub Desktop a la carpeta **Applications** (Aplicaciones).
4. Abre GitHub Desktop y elige **Sign in to GitHub.com**.
5. Si macOS pregunta si quieres abrir la aplicación, confirma.

Para editar un Vault de Obsidian:

1. Descarga Obsidian desde <https://obsidian.md/download>.
2. Abre el archivo `.dmg` descargado.
3. Arrastra Obsidian a **Applications**.
4. Abre Obsidian.

También puedes usar **Terminal**. Ábrela pulsando `Command + Space`, escribiendo `Terminal` y pulsando `Return`.

## 5. Clonar el repositorio con GitHub Desktop

GitHub Desktop es la opción recomendada porque evita la mayoría de los errores de la línea de comandos y funciona de forma parecida en Windows y macOS.

1. Abre GitHub Desktop.
2. Selecciona **File > Clone repository** (Archivo > Clonar repositorio).
3. Selecciona la pestaña **GitHub.com**.
4. Busca `Challsss/Vault`.
5. Selecciona el repositorio.
6. En **Local path** (Ruta local), elige dónde quieres guardar la carpeta.
   - Elige un lugar que puedas encontrar fácilmente.
   - No la pongas dentro de otro repositorio Git.
   - No muevas ni cambies el nombre de la carpeta después de clonarla, salvo que sepas actualizar la ruta en GitHub Desktop.
7. Pulsa **Clone** (Clonar).
8. Espera a que termine la descarga.

El repositorio ya está en tu ordenador. GitHub Desktop debería mostrar el nombre del repositorio y la rama actual, `main`.

### Abrir el Vault en Obsidian

1. Abre Obsidian.
2. Elige **Open folder as vault** (Abrir carpeta como Vault).
3. Selecciona la carpeta donde GitHub Desktop clonó `Vault`.
4. Confirma que es el Vault que quieres abrir.
5. Asegúrate de editar los archivos dentro de esta carpeta. Si editas otra copia, los cambios no pertenecerán al repositorio.

## 6. Empezar a trabajar de forma segura

Antes de cambiar algo, asegúrate de que tu copia local de `main` está actualizada:

1. Abre GitHub Desktop.
2. Selecciona el repositorio `Vault`.
3. Pulsa **Fetch origin** (Comprobar cambios).
4. Si GitHub Desktop indica que hay actualizaciones, pulsa **Pull origin** (Descargar cambios).
5. Selecciona **Current Branch > New Branch** (Rama actual > Nueva rama).
6. Escribe un nombre descriptivo, como `notes/medios-interactivos`.
7. Pulsa **Create Branch** (Crear rama).
8. Pulsa **Publish branch** (Publicar rama) para guardar la rama en GitHub.

Ahora trabajas en tu propia rama. Tus cambios no modificarán `main` hasta que el responsable apruebe un pull request.

## 7. Hacer y guardar cambios

Edita las notas con Obsidian u otro editor adecuado:

- Guarda los archivos normalmente.
- Conserva los enlaces y el formato Markdown existentes salvo que tu tarea requiera cambiarlos.
- Evita editar la misma nota que otra persona al mismo tiempo.
- No edites la carpeta `.git`; contiene información interna de Git.
- No borres archivos de `.obsidian` salvo que el responsable lo pida expresamente.
- Comprueba el resultado en Obsidian antes de enviarlo.

### Revisar los cambios en GitHub Desktop

1. Vuelve a GitHub Desktop.
2. Abre la pestaña **Changes** (Cambios).
3. Revisa la lista de archivos modificados.
4. Selecciona un archivo para ver las líneas añadidas y eliminadas.
5. Si un cambio fue accidental, utiliza el menú contextual del archivo para restaurarlo. Ten cuidado: restaurar un archivo elimina sus cambios no guardados en un commit.

## 8. Hacer commit y publicar el trabajo

Un commit es un punto de guardado en tu rama.

1. En GitHub Desktop, permanece en la pestaña **Changes**.
2. En el campo de resumen, escribe una descripción breve, como `Añadir resumen de la historia web`.
3. Puedes añadir más detalles en el campo de descripción.
4. Pulsa **Commit to _nombre-de-tu-rama_**.
5. Pulsa **Push origin** para subir la rama a GitHub.

Haz commits con frecuencia, especialmente al terminar una parte pequeña y lógica de la tarea. Los commits facilitan revisar el trabajo y recuperar errores. No uses mensajes como `cosas`, `cambios` o `final`; no explican qué ocurrió.

## 9. Abrir un pull request

Después de publicar tu rama:

1. En GitHub Desktop, pulsa **Create Pull Request**. Si no aparece, abre <https://github.com/Challsss/Vault> en el navegador y elige **Pull requests > New pull request**.
2. En el repositorio base, selecciona `Challsss/Vault`.
3. En la rama base, selecciona `main`.
4. En la rama de comparación, selecciona tu rama.
5. Pulsa **Create pull request**.
6. Escribe un título útil, como `Añadir notas sobre medios interactivos`.
7. En la descripción explica:
   - qué cambiaste;
   - por qué lo cambiaste;
   - qué archivos o secciones afecta;
   - cómo comprobaste el resultado; y
   - qué debe revisar especialmente el responsable.
8. Pulsa **Create pull request**.
9. Si GitHub ofrece la opción, solicita la revisión de Challsss.

Mantén abierto el pull request mientras se revisa. Si haces más commits en la misma rama, GitHub los añadirá automáticamente al pull request.

## 10. Responder a los comentarios de revisión

El responsable puede aprobar el pull request, hacer preguntas o pedir cambios:

1. Lee cada comentario cuidadosamente.
2. Haz los cambios solicitados en la misma rama local.
3. Haz un commit con un mensaje claro.
4. Vuelve a publicar la rama.
5. Responde al comentario cuando hayas completado la petición.
6. No cierres el pull request solo porque te hayan pedido cambios.

Cuando el responsable apruebe y fusione el pull request, el trabajo formará parte de `main`. Después puedes borrar la rama antigua cuando GitHub Desktop o GitHub lo ofrezca.

## 11. Empezar la siguiente tarea

Después de que se fusione un pull request:

1. En GitHub Desktop, cambia a `main` desde **Current Branch**.
2. Pulsa **Fetch origin**.
3. Pulsa **Pull origin**.
4. Crea una rama nueva para la siguiente tarea.

Siempre crea la rama desde el `main` más reciente. No continúes usando una rama antigua después de que se haya fusionado.

## 12. Instrucciones con la línea de comandos (opcional)

Los pasos gráficos anteriores son los recomendados. Estos comandos son una alternativa para quienes se sientan cómodos usando una terminal.

### Windows PowerShell

Abre PowerShell y ejecuta:

```powershell
git clone https://github.com/Challsss/Vault.git
cd Vault
git switch -c notes/mi-cambio
```

Después de editar los archivos:

```powershell
git status
git add .
git commit -m "Describe el cambio"
git push -u origin notes/mi-cambio
```

Después abre el repositorio en GitHub y crea un pull request desde `notes/mi-cambio` hacia `main`.

### Terminal de macOS

Abre Terminal y ejecuta:

```bash
git clone https://github.com/Challsss/Vault.git
cd Vault
git switch -c notes/mi-cambio
```

Después de editar los archivos:

```bash
git status
git add .
git commit -m "Describe el cambio"
git push -u origin notes/mi-cambio
```

Después abre el repositorio en GitHub y crea un pull request desde `notes/mi-cambio` hacia `main`.

Si Git solicita tu identidad la primera vez, configúrala con el nombre y correo que utilizas en GitHub:

```bash
git config --global user.name "Tu nombre"
git config --global user.email "tu-correo@example.com"
```

No utilices el correo de otra persona. Si GitHub solicita una contraseña al usar HTTPS, utiliza el inicio de sesión o el aviso de credenciales de GitHub; la contraseña normal de tu cuenta no siempre es aceptada por Git.

## 13. Problemas habituales

### “He cambiado archivos, pero GitHub Desktop no muestra nada”

Comprueba que:

- editaste la carpeta clonada por GitHub Desktop;
- GitHub Desktop tiene seleccionado el repositorio `Vault`;
- el archivo está guardado; y
- el archivo no está fuera de la carpeta del repositorio.

### “Estoy en la rama equivocada”

En GitHub Desktop usa **Current Branch** para seleccionar la rama correcta. No copies archivos entre ramas para solucionar esto. Si tienes cambios sin commit, pide ayuda al responsable antes de cambiar de rama o descartarlos.

### “Ha fallado Push origin”

Primero pulsa **Fetch origin**. Si la rama ya existe en GitHub, comprueba que has iniciado sesión con la cuenta correcta y que tienes permiso para publicar en el repositorio. No hagas `force push` salvo que el responsable te lo indique expresamente.

### “Hay conflictos”

Un conflicto significa que otro cambio y el tuyo afectan a las mismas líneas o al mismo archivo. No elijas automáticamente “ours” o “theirs”.

1. Detente y lee el archivo en conflicto.
2. Compara tu trabajo con la versión de `main`.
3. Conserva el contenido correcto o combina ambas modificaciones cuidadosamente.
4. Elimina las marcas de conflicto de Git: `<<<<<<<`, `=======` y `>>>>>>>`.
5. Guarda el archivo.
6. Pide ayuda al responsable si no está claro cuál es el resultado correcto.
7. Haz commit de la resolución y publica la rama.

### “He hecho un commit por error”

No borres ni reescribas el historial compartido. Si el commit todavía no se ha publicado, pide ayuda al responsable antes de modificarlo. Si ya se publicó o está en un pull request, haz un nuevo commit que corrija el problema y explica lo ocurrido.

### “He borrado o cambiado un archivo por accidente”

Si el cambio no tiene commit, usa el menú contextual del archivo en GitHub Desktop y elige restaurarlo. Si ya tiene commit, no te preocupes: informa al responsable de qué archivo se afectó y qué ocurrió.

### “Obsidian muestra un Vault duplicado o inesperado”

Cierra el Vault duplicado y vuelve a abrir exactamente la carpeta clonada por GitHub Desktop. Debería existir una sola copia de trabajo de este repositorio en el ordenador, salvo que haya un motivo específico para tener más de una.

## 14. Recomendaciones de configuración para el responsable

Para aplicar el flujo descrito, el propietario del repositorio debería configurar GitHub:

1. Abre el repositorio en GitHub.
2. Ve a **Settings > Rules > Rulesets** (o a **Settings > Branches** si aparece la interfaz antigua).
3. Crea una regla o conjunto de reglas dirigido a la rama `main`.
4. Exige un pull request antes de fusionar.
5. Exige al menos una aprobación.
6. Exige la aprobación del propietario o del responsable designado cuando esa opción esté disponible.
7. Si corresponde, descarta las aprobaciones anteriores cuando se publiquen nuevos commits.
8. Exige resolver todas las conversaciones antes de fusionar.
9. Bloquea los force pushes y el borrado de la rama `main`.
10. Restringe quién puede publicar en `main`, o desactiva completamente las publicaciones directas.
11. Decide si los colaboradores pueden aprobar sus propios pull requests; se recomienda desactivar la autoaprobación.
12. Guarda las reglas y pruébalas con una cuenta que no sea la del propietario.

Los nombres y la ubicación de las opciones de GitHub pueden cambiar. Consulta la documentación actual de GitHub si alguna opción no aparece.

## 15. Lista rápida de comprobación

Antes de empezar:

- [ ] Tengo una cuenta de GitHub.
- [ ] Acepté la invitación al repositorio, si recibí una.
- [ ] Instalé GitHub Desktop y, si hace falta, Obsidian.
- [ ] Cloné el repositorio.
- [ ] Descargué el `main` más reciente.
- [ ] Creé y publiqué una rama nueva.

Antes de abrir un pull request:

- [ ] Revisé todos los archivos modificados.
- [ ] Comprobé las notas en Obsidian.
- [ ] Hice commit con un mensaje claro.
- [ ] Publiqué la rama.
- [ ] Expliqué qué cambió y cómo lo comprobé.
- [ ] El pull request apunta a `main`.

Antes de empezar otra tarea:

- [ ] El responsable revisó y fusionó el pull request.
- [ ] Cambié a `main`.
- [ ] Descargué los cambios más recientes.
- [ ] Creé una rama nueva.

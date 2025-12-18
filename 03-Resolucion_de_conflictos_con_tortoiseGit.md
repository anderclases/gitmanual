# 🐢 Guía de TortoiseGit: Instalación y Uso Avanzado

**TortoiseGit** es una interfaz visual que se integra en el explorador de archivos de Windows, permitiéndote gestionar versiones sin necesidad de memorizar comandos.

---

## 1. Instalación de TortoiseGit
1. Descarga el instalador desde su sitio oficial: [tortoisegit.org/download](https://tortoisegit.org/download/).
2. Instala primero el **Main Installer**.
3. (Opcional) Descarga e instala el **Language Pack** de español si prefieres la interfaz en ese idioma.
4. Al finalizar, se abrirá un asistente de configuración (**First Start Wizard**):
   * Deja la ruta de `git.exe` por defecto (la detectará de tu instalación previa de Git).
   * Configura tu nombre y email (usa los mismos de tu cuenta de GitHub).

---

## 2. Visualizar el Historial (Ver Log)
Una de las mejores funciones de TortoiseGit es ver la evolución del proyecto de forma gráfica.

1. Haz clic derecho en tu carpeta del repositorio o en un archivo específico.
2. Selecciona **TortoiseGit** > **Show Log**.
3. **¿Qué verás aquí?**
   * Una lista de todos los commits realizados.
   * Quién hizo cada cambio y cuándo.
   * Los archivos que se modificaron en cada commit (en la parte inferior).
   * Un gráfico de ramas (branches) si el proyecto tiene varias.

---

## 3. Resolución de Conflictos
Los conflictos ocurren cuando dos personas modifican la misma línea de un archivo. TortoiseGit los marca con un icono de exclamación amarilla ⚠️.

### Pasos para resolverlos:
1. Al intentar hacer un **Pull** o un **Merge**, si hay conflicto, Tortoise te avisará.
2. Haz clic derecho sobre el archivo en conflicto y selecciona **TortoiseGit** > **Edit Conflicts**.
3. Se abrirá **TortoiseMerge**, una pantalla con tres paneles:
   * **Izquierda (Theirs):** El código que viene del servidor/otra rama.
   * **Derecha (Mine):** Tu código local.
   * **Abajo (Merged):** El resultado final.
4. Haz clic derecho sobre las líneas marcadas en rojo y elige:
   * *Use text block from 'mine'* (Quedarte con lo tuyo).
   * *Use text block from 'theirs'* (Aceptar lo de fuera).
5. Una vez corregido, guarda el archivo y haz clic en el botón **Mark as resolved** (Marcar como resuelto) en la barra de herramientas.
6. Finalmente, haz un **Commit** para cerrar la resolución del conflicto.

---

## 🛠️ Comandos rápidos en el menú contextual

* **Git Sync:** Abre una ventana para hacer Push y Pull rápidamente.
* **Diff:** Compara tus cambios actuales con la última versión guardada.
* **Revert:** Deshace tus cambios locales y vuelve al estado del último commit (¡cuidado, no se puede deshacer!).

> ![Menú TortoiseGit](images/tortoise_context_menu.png)
> *El menú aparece al hacer clic derecho sobre cualquier archivo dentro del repositorio.*
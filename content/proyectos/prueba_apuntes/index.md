
---
title: "Clase Doctorado UAndes 2025"
date: "2025-05-08"
summary: "Guía acompañamiento curso Python y Napari doctorado UAndes 2025"
description: "Guía clase python y napari doctorado UAndes 2025"
toc: true
readTime: false
autonumber: true
math: false
showTags: false
hidePagination: true
draft: false
---


## Instalación Python + Visual Studio Code + Jupyter

Cubro la instalación, tanto para Windows como para Mac en un video públicado en el siguiente [link](https://www.youtube.com/). Si prefieres la versión escrita, te dejo este instructivo a continuación:

### Instalación de Python

Python es un lenguaje de programación versátil. Instalaremos la última versión estable.

**1. Descargar Python:**
   * Abran su navegador web y vayan al sitio web oficial de Python: [https://www.python.org/downloads/](https://www.python.org/downloads/)
   * El sitio web debería detectar automáticamente su sistema operativo (Windows o macOS) y sugerir el instalador apropiado. Hagan clic en el botón de descarga para la última versión (por ejemplo, Python 3.12.x o más reciente).

**2. Instalar Python:**

   * **Para Usuarios de Windows:**
      1.  Ejecuten el instalador `.exe` descargado.
      2.  **Paso Crucial:** En la primera pantalla del instalador, asegúrense de marcar la casilla que dice **"Add Python to PATH"** o **"Add python.exe to PATH"**. Esto facilitará la ejecución de Python desde la línea de comandos.
      3.  Hagan clic en **"Install Now"** (esto usualmente incluye pip, IDLE y otras características estándar).
      4.  Sigan las instrucciones en pantalla para completar la instalación.
      5.  Una vez instalado, podrían ver una opción para "Disable path length limit". Hagan clic en esto si está disponible, ya que puede prevenir problemas con rutas de archivo largas.

   * **Para Usuarios de macOS:**
      1.  Ejecuten el instalador `.pkg` descargado.
      2.  Sigan las instrucciones en pantalla. Python en macOS usualmente se instala sin problemas. Se instalará en `/usr/local/bin/python3`.
      3.  El instalador también debería instalar `pip` (el instalador de paquetes de Python) e `IDLE` (el Entorno de Desarrollo Integrado básico de Python).

**3. Verificar la Instalación de Python:**
   * Una vez completada la instalación, necesitan verificarla.
   * **Para Windows:**
      1.  Abran el Símbolo del sistema (busquen "cmd" en el Menú Inicio).
      2.  Escriban `python --version` y presionen Enter.
      3.  Escriban `pip --version` y presionen Enter.
      Deberían ver las versiones de Python y pip impresas, respectivamente.
   * **Para macOS:**
      1.  Abran la Terminal (pueden encontrarla en Aplicaciones > Utilidades, o buscarla usando Spotlight).
      2.  Escriban `python3 --version` y presionen Enter.
      3.  Escriban `pip3 --version` y presionen Enter.
      Deberían ver las versiones de Python y pip impresas. (Nota: macOS a menudo viene con una versión más antigua de Python 2, por lo que `python3` y `pip3` se usan típicamente para especificar la versión que acaban de instalar).

   Si ven los números de versión, ¡Python está instalado correctamente! Si no, intenten reiniciar su computadora y verificar nuevamente. Si los problemas persisten, podrían necesitar reinstalar, asegurándose de haber agregado Python al PATH en Windows.

---

### Instalación de Visual Studio Code (VS Code)

VS Code es un editor de código fuente ligero pero potente que se ejecuta en su escritorio y está disponible para Windows, macOS y Linux. Tiene un excelente soporte para el desarrollo en Python.

**1. Descargar VS Code:**
   * Vayan al sitio web oficial de VS Code: [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
   * Descarguen el instalador para su sistema operativo (Windows o macOS).

**2. Instalar VS Code:**
   * **Para Windows:**
      1.  Ejecuten el instalador `.exe` descargado.
      2.  Acepten el acuerdo y sigan las instrucciones en pantalla.
      3.  Se recomienda mantener la configuración predeterminada, especialmente **"Add to PATH"** (si se ofrece como opción durante la instalación, asegúrense de que esté marcada).
      4.  También podrían querer marcar las acciones "Open with Code" ("Abrir con Code") para el menú contextual de archivos y directorios del Explorador de Windows por conveniencia.
   * **Para macOS:**
      1.  Ejecuten el archivo `.dmg` descargado.
      2.  Arrastren el ícono "Visual Studio Code.app" a su carpeta de "Aplicaciones".

**3. Iniciar VS Code:**
   * Abran VS Code desde su carpeta de Aplicaciones (macOS) o Menú Inicio (Windows).

---

### Parte 3: Configuración de VS Code para Python

Ahora, configuremos VS Code para que funcione con Python.

**1. Instalar la Extensión de Python:**
   * En VS Code, vayan a la **Vista de Extensiones** haciendo clic en el ícono de cuadrados en la barra lateral izquierda (o presionen `Ctrl+Shift+X` en Windows, `Cmd+Shift+X` en macOS).
   * En la barra de búsqueda, escriban `Python`.
   * Busquen la extensión llamada **"Python"** publicada por **Microsoft**. Usualmente es el primer resultado y tiene millones de descargas.
   * Hagan clic en el botón **"Install"** (Instalar) para esta extensión.

---

### Configuración de Jupyter Notebooks en VS Code

Los Jupyter Notebooks son documentos interactivos que permiten escribir y ejecutar código, agregar texto, ecuaciones, visualizaciones y más. VS Code tiene un excelente soporte incorporado para Jupyter Notebooks.

**1. Instalar la Extensión Jupyter:**
   * Al igual que instalaron la extensión de Python, vayan a la **Vista de Extensiones** (`Ctrl+Shift+X` o `Cmd+Shift+X`).
   * Busquen `Jupyter`.
   * Instalen la extensión **"Jupyter"** publicada por **Microsoft**. (A menudo, esta se instala como una dependencia de la extensión de Python, pero es bueno verificar).

**2. Crear o Abrir un Jupyter Notebook:**
   * Crea un archivo de prueba, llamado `prueba.ipynb`. Este es el nombre de extensión de los cuadernos de jupyter.

**3. Seleccionar un Kernel:**
   * El notebook necesitará conectarse a un "kernel" (núcleo) de Python para ejecutar código.
   * Usualmente, en la parte superior derecha de la interfaz del notebook, verán una opción para "Select Kernel" (Seleccionar Kernel).
   * Hagan clic allí y elijan el entorno de Python que configuraron anteriormente (el mismo que seleccionaron como su intérprete de Python).
   * Si se les solicita instalar `ipykernel` u otros paquetes, permitan que la extensión lo haga.

**4. Usar el Notebook:**
   * Un notebook está hecho de "celdas".
   * **Celdas de código:** Donde escriben y ejecutan código Python. Escriban su código y presionen `Shift+Enter` (o hagan clic en el botón de reproducir junto a la celda) para ejecutarlo.
   * **Celdas de Markdown:** Donde pueden escribir texto, como esta guía. Pueden cambiar el tipo de celda usando el menú desplegable en la barra de herramientas del notebook.

---

### Prueba Python y Jupyter

Asegurémonos de que todo funcione.

**1. Script de Python Simple en VS Code:**
   * Creen un nuevo archivo en VS Code (File > New File o Archivo > Nuevo Archivo).
   * Guárdenlo como `hola.py`.
   * Escriban el siguiente código Python:
     ```python
     print("¡Hola, estudiantes de medicina, desde un script de Python!")
     ```
   * Guarden el archivo (`Ctrl+S` o `Cmd+S`).
   * Hagan clic derecho en el editor y seleccionen "Run Python File in Terminal" (Ejecutar Archivo Python en Terminal) o hagan clic en el botón de reproducir en la parte superior derecha de la ventana de VS Code.
   * Deberían ver el mensaje impreso en el panel de la terminal de VS Code.

**2. Prueba Simple de Jupyter Notebook:**
   * Si no tienen un Jupyter Notebook abierto, creen uno (`Jupyter: Create New Jupyter Notebook` desde la Paleta de Comandos).
   * En la primera celda de código, escriban:
     ```python
     mensaje = "¡Hola desde una celda de Jupyter Notebook!"
     print(mensaje)
     ```
   * Presionen `Shift+Enter` para ejecutar la celda.
   * Deberían ver la salida `¡Hola desde una celda de Jupyter Notebook!` mostrada directamente debajo de la celda.


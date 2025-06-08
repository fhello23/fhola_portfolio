
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

### Configuración de VS Code para Python

Ahora, configuremos VS Code para que funcione con Python.

**1. Instalar la Extensión de Python:**
   * En VS Code, vayan a la **Vista de Extensiones** haciendo clic en el ícono de cuadrados en la barra lateral izquierda (o presionen `Ctrl+Shift+X` en Windows, `Cmd+Shift+X` en macOS).
   * En la barra de búsqueda, escriban `Python`.
   * Busquen la extensión llamada **"Python"** publicada por **Microsoft**. Usualmente es el primer resultado y tiene millones de descargas.
   * Hagan clic en el botón **"Install"** (Instalar) para esta extensión.

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


## Introducción a Napari

### ¿Qué es Napari?  

Napari es una herramienta de visualización rápida, interactiva y multidimensional para Python, especialmente diseñada para datos científicos. Es perfecta para analizar imágenes biológicas como microscopía, datos de fluorescencia, y cualquier tipo de imagen científica en 2D, 3D o incluso dimensiones superiores.

#### ¿Por qué usar Napari?  

- **Interactivo**: Puedes explorar tus datos de forma visual e interactiva
- **Multidimensional**: Maneja datos 2D, 3D, 4D y más dimensiones
- **Extensible**: Compatible con muchas herramientas de análisis de imágenes
- **Fácil de usar**: Interfaz intuitiva para científicos

### Primeros pasos con Napari

#### 1. Importar las librerías necesarias

```python
import napari

from skimage import data

import numpy as np

from skimage import data

from skimage.filters import threshold_otsu

from skimage.segmentation import clear_border

from skimage.measure import label, regionprops_table

from skimage.morphology import closing, square, remove_small_objects
```

**Explicación:**

- `napari`: La librería principal para visualización

- `skimage`: Librería de procesamiento de imágenes (scikit-image)

- `numpy`: Para manejo de arrays y datos numéricos

#### 2. Crear un visualizador

```python
viewer = napari.Viewer()
```

Este comando abre una ventana interactiva donde podrás visualizar y manipular tus datos. Es como abrir un microscopio digital en tu computadora.

#### 3. Cargar datos de ejemplo

```python
viewer.add_image(data.cells3d(), name='celulas')
```

**¿Qué hace este código?**

- `data.cells3d()`: Carga un conjunto de datos de ejemplo que contiene células en 3D

- `add_image()`: Añade la imagen al visualizador

- `name='celulas'`: Le da un nombre descriptivo a la capa

#### 4. Trabajar con capas (layers)

En Napari, cada elemento visual es una "capa" o "layer". Puedes tener múltiples capas superpuestas. Puedes agregar puntos desde el GUI por ejemplo y podremos accederlos desde nuestro notebook:

```python
# Obtener todas las capas
layers = viewer.layers

print(layers)
```

**Resultado esperado:**

```
[<Image layer 'celulas' at 0x35ca7d040>,

<Points layer 'Points' at 0x355315eb0>,

```

#### 5. Examinar información detallada de una capa

```python
# Seleccionar una capa específica (en este caso, la capa de puntos)

points_layer = viewer.layers[1]
 
# Obtener información detallada

print(f"Nombre de la capa: {points_layer.name}")

print(f"Tipo de capa: {type(points_layer)}")

print(f"Forma de los datos: {points_layer.data.shape}")

print(f"Tipo de datos: {points_layer.data.dtype}")

print(f"Número de puntos: {len(points_layer.data)}")

print(f"Visibilidad: {points_layer.visible}")

print(f"Opacidad: {points_layer.opacity}")


# Ver las coordenadas de los puntos

print("Coordenadas de los puntos:")

print(points_layer.data)

```

**Resultado esperado:**

```
Nombre de la capa: Points

Tipo de capa: <class 'napari.layers.points.points.Points'>

Forma de los datos: (4, 4)

Tipo de datos: float64

Número de puntos: 4

Visibilidad: True

Opacidad: 1.0

  

Coordenadas de los puntos:

[Lista con coordenadas de puntos agregados]

```

### Conceptos importantes para biólogos

#### Capas (Layers)

- **Image layers**: Para mostrar imágenes (microscopía, fluorescencia, etc.)

- **Points layers**: Para marcar puntos específicos (células, orgánulos, etc.)

- **Labels layers**: Para segmentación y regiones de interés

- **Shapes layers**: Para dibujar formas geométricas

#### Dimensiones

- **2D**: Imágenes simples (x, y)

- **3D**: Stacks de imágenes o volúmenes (z, y, x)

- **4D**: Series temporales (t, z, y, x)

- **Multi-canal**: Diferentes canales de fluorescencia

#### Interactividad

- Usa el mouse para navegar por las imágenes

- Controles de zoom y paneo

- Ajuste de contraste y brillo

- Navegación por capas en 3D



## Napari + Cellpose: Segmentación Automática de Células

### ¿Qué es Cellpose?

Cellpose es una herramienta de inteligencia artificial desarrollada específicamente para la segmentación automática de células en imágenes de microscopía. Utiliza redes neuronales entrenadas para identificar y delimitar células individuales, incluso en imágenes complejas con células superpuestas o de formas irregulares.

#### ¿Por qué combinar Napari con Cellpose?

- **Automatización**: Segmentación automática sin necesidad de ajuste manual

- **Precisión**: Modelos entrenados con miles de imágenes biológicas

- **Visualización**: Napari permite visualizar y validar los resultados de segmentación

- **Análisis cuantitativo**: Extracción automática de medidas y propiedades celulares

- **Exportación**: Guarda resultados para análisis posteriores

### Preparación del entorno

#### 1. Importar las librerías necesarias

```python
import ssl

ssl._create_default_https_context = ssl._create_unverified_context

import napari

from skimage.io import imread

from cellpose import models

import pandas as pd

from skimage.measure import regionprops_table

```

**Explicación:**

- `ssl`: Configuración para descargar modelos de Cellpose

- `napari`: Visualización interactiva

- `skimage.io`: Lectura de imágenes

- `cellpose.models`: Modelos de segmentación automática

- `pandas`: Manejo de datos tabulares

- `regionprops_table`: Cálculo de propiedades de regiones

#### 2. Crear el visualizador y cargar el modelo

```python
# Crear el visualizador de Napari

viewer = napari.Viewer()

# Configurar y cargar el modelo de Cellpose

ssl._create_default_https_context = ssl._create_unverified_context

model = models.Cellpose(model_type="cyto", gpu=False)
```


**¿Qué hace este código?**

- `napari.Viewer()`: Abre la interfaz gráfica

- `model_type="cyto"`: Usa el modelo entrenado para citoplasma (ideal para la mayoría de células)

- `gpu=False`: Usa CPU en lugar de GPU (más compatible)

### Análisis paso a paso

#### 3. Cargar tu imagen

```python
img = imread("./SUM_N1-0002.tif")
```

**Importante:** Reemplaza `"./SUM_N1-0002.tif"` con la ruta a tu imagen. Cellpose funciona con formatos comunes como TIFF, PNG, JPG.
#### 4. Ejecutar la segmentación automática

```python

masks, flows, styles, diams = model.eval(

img,

diameter=75, # Diámetro estimado de las células en píxeles

channels=[0, 0], # Canal de citoplasma, canal de núcleo

)

```


**Parámetros clave:**

- `diameter=75`: Tamaño promedio esperado de tus células (ajusta según tu imagen)

- `channels=[0, 0]`: Para imágenes en escala de grises

- `channels=[1, 3]`: Si tienes canales específicos para citoplasma y núcleo

**Resultados:**

- `masks`: Imagen segmentada donde cada célula tiene un número único

- `flows`: Información del flujo de gradientes (para diagnóstico)

- `styles`: Estilos detectados

- `diams`: Diámetros estimados

#### 5. Visualizar los resultados

```python
# Añadir la imagen original

viewer.add_image(img, name="Raw image", colormap="gray")

# Añadir las máscaras de segmentación

viewer.add_labels(masks, name="Cellpose masks")

```


**¿Qué verás?**

- **Imagen original**: En escala de grises

- **Máscaras coloreadas**: Cada célula con un color diferente

- **Superposición**: Puedes alternar la visibilidad para comparar

### Análisis cuantitativo

#### 6. Extraer medidas de las células


```python
props = regionprops_table(

masks,

intensity_image=img,

properties=("label", "area", "mean_intensity")

)

df = pd.DataFrame(props)

df.to_csv("cell_measurements.csv", index=False)

```


**¿Qué medidas obtienes?**

- `label`: Identificador único de cada célula

- `area`: Área en píxeles

- `mean_intensity`: Intensidad promedio (brillo)

**Otras propiedades disponibles:**

- `perimeter`: Perímetro de la célula

- `eccentricity`: Qué tan alargada es la célula

- `solidity`: Qué tan sólida es la forma

- `centroid`: Centro de masa de la célula

#### 7. Exportar imágenes para presentaciones


```python
import os

import numpy as np

from skimage.io import imsave

from skimage.color import label2rgb

import napari
  
# assume 'viewer' already exists and has your layers

output_dir = "output_pngs"

os.makedirs(output_dir, exist_ok=True)


for layer in viewer.layers:

	data = layer.data
	
	# sanitize layer name for filesystem
	
	name = layer.name.replace(" ", "_")
	
	outpath = os.path.join(output_dir, f"{name}.png")

  
	# Image layer: normalize floats to uint8
	
	if isinstance(layer, napari.layers.Image):
	
		if np.issubdtype(data.dtype, np.floating):
		
			img = (np.clip(data, 0, 1) * 255).astype(np.uint8)
		
		else:
		
			img = data.astype(np.uint8)
			
			imsave(outpath, img)
	
	# Labels layer: map each integer label to a color
	
	elif isinstance(layer, napari.layers.Labels):
	
		# background=0 will be black
		
		rgb = label2rgb(data, bg_label=0)
		
		imsave(outpath, (rgb * 255).astype(np.uint8))
	
	else:
		
		# skip Points, Shapes, Vectors, etc.
		
		print(f"Skipping layer “{layer.name}” of type {type(layer)}")

```

### Consejos para optimizar resultados
#### Ajustar el diámetro

- **Células pequeñas**: diameter=30-50

- **Células medianas**: diameter=50-100

- **Células grandes**: diameter=100-200

- **Automático**: diameter=None (Cellpose estimará)

#### Seleccionar el modelo apropiado

- `"cyto"`: Células generales con citoplasma visible

- `"nuclei"`: Núcleos celulares

- `"cyto2"`: Versión mejorada para citoplasma

#### Configurar canales correctamente

- Imagen en escala de grises: `[0, 0]`

- Canal rojo para citoplasma: `[1, 0]`

- Canal verde para núcleos: `[0, 2]`

- Ambos canales: `[1, 2]`

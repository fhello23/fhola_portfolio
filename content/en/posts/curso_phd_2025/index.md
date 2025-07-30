---
title: "UAndes PhD Course 2025"
date: "2025-06-17"
summary: "Python and Napari course guide for UAndes PhD program 2025"
description: "Comprehensive guide for Python, Napari, and data visualization for PhD students"
toc: true
readTime: false
autonumber: true
math: false
showTags: false
hidePagination: true
draft: false
---

## Instalación Python + Visual Studio Code + Jupyter

Cubro la instalación, tanto para Windows como para Mac en un video públicado en el siguiente [link](https://youtu.be/zJJ92NXcPc0). Si prefieres la versión escrita, te dejo este instructivo a continuación:
### Instalación de Python
Python es un lenguaje de programación versátil. Instalaremos la última versión estable.

**Descargar Python:**

* Abran su navegador web y vayan al sitio web oficial de Python: [https://www.python.org/downloads/](https://www.python.org/downloads/)

* El sitio web debería detectar automáticamente su sistema operativo (Windows o macOS) y sugerir el instalador apropiado. Hagan clic en el botón de descarga para la última versión (por ejemplo, Python 3.12.x o más reciente).

**Instalar Python:**

* **Para Usuarios de Windows:**
1. Ejecuten el instalador `.exe` descargado.
2. **Paso Crucial:** En la primera pantalla del instalador, asegúrense de marcar la casilla que dice **"Add Python to PATH"** o **"Add python.exe to PATH"**. Esto facilitará la ejecución de Python desde la línea de comandos.
3. Hagan clic en **"Install Now"** (esto usualmente incluye pip, IDLE y otras características estándar).
4. Sigan las instrucciones en pantalla para completar la instalación.
5. Una vez instalado, podrían ver una opción para "Disable path length limit". Hagan clic en esto si está disponible, ya que puede prevenir problemas con rutas de archivo largas.

* **Para Usuarios de macOS:**
1. Ejecuten el instalador `.pkg` descargado.
2. Sigan las instrucciones en pantalla. Python en macOS usualmente se instala sin problemas. Se instalará en `/usr/local/bin/python3`.
3. El instalador también debería instalar `pip` (el instalador de paquetes de Python) e `IDLE` (el Entorno de Desarrollo Integrado básico de Python).

**Verificar la Instalación de Python:**
* Una vez completada la instalación, necesitan verificarla.
  
* **Para Windows:**
1. Abran el Símbolo del sistema (busquen "cmd" en el Menú Inicio).
2. Escriban `python --version` y presionen Enter.
3. Escriban `pip --version` y presionen Enter.

Deberían ver las versiones de Python y pip impresas, respectivamente.

* **Para macOS:**
1. Abran la Terminal (pueden encontrarla en Aplicaciones > Utilidades, o buscarla usando Spotlight).
2. Escriban `python3 --version` y presionen Enter.
3. Escriban `pip3 --version` y presionen Enter.

Deberían ver las versiones de Python y pip impresas. (Nota: macOS a menudo viene con una versión más antigua de Python 2, por lo que `python3` y `pip3` se usan típicamente para especificar la versión que acaban de instalar).

Si ven los números de versión, ¡Python está instalado correctamente! Si no, intenten reiniciar su computadora y verificar nuevamente. Si los problemas persisten, podrían necesitar reinstalar, asegurándose de haber agregado Python al PATH en Windows.
### Instalación de Visual Studio Code (VS Code)

VS Code es un editor de código fuente ligero pero potente que se ejecuta en su escritorio y está disponible para Windows, macOS y Linux. Tiene un excelente soporte para el desarrollo en Python.

**Descargar VS Code:**
* Vayan al sitio web oficial de VS Code: [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
* Descarguen el instalador para su sistema operativo (Windows o macOS).

**Instalar VS Code:**

* **Para Windows:**
1. Ejecuten el instalador `.exe` descargado.
2. Acepten el acuerdo y sigan las instrucciones en pantalla.
3. Se recomienda mantener la configuración predeterminada, especialmente **"Add to PATH"** (si se ofrece como opción durante la instalación, asegúrense de que esté marcada).
4. También podrían querer marcar las acciones "Open with Code" ("Abrir con Code") para el menú contextual de archivos y directorios del Explorador de Windows por conveniencia.

* **Para macOS:**
1. Ejecuten el archivo `.dmg` descargado.
2. Arrastren el ícono "Visual Studio Code.app" a su carpeta de "Aplicaciones".

**Iniciar VS Code:**
* Abran VS Code desde su carpeta de Aplicaciones (macOS) o Menú Inicio (Windows).

### Configuración de VS Code para Python

Ahora, configuremos VS Code para que funcione con Python.

**Instalar la Extensión de Python:**
* En VS Code, vayan a la **Vista de Extensiones** haciendo clic en el ícono de cuadrados en la barra lateral izquierda (o presionen `Ctrl+Shift+X` en Windows, `Cmd+Shift+X` en macOS).
* En la barra de búsqueda, escriban `Python`.
* Busquen la extensión llamada **"Python"** publicada por **Microsoft**. Usualmente es el primer resultado y tiene millones de descargas.
* Hagan clic en el botón **"Install"** (Instalar) para esta extensión.

### Configuración de Jupyter Notebooks en VS Code
Los Jupyter Notebooks son documentos interactivos que permiten escribir y ejecutar código, agregar texto, ecuaciones, visualizaciones y más. VS Code tiene un excelente soporte incorporado para Jupyter Notebooks.

**Instalar la Extensión Jupyter:**
* Al igual que instalaron la extensión de Python, vayan a la **Vista de Extensiones** (`Ctrl+Shift+X` o `Cmd+Shift+X`).
* Busquen `Jupyter`.
* Instalen la extensión **"Jupyter"** publicada por **Microsoft**. (A menudo, esta se instala como una dependencia de la extensión de Python, pero es bueno verificar).

**Crear o Abrir un Jupyter Notebook:**
* Crea un archivo de prueba, llamado `prueba.ipynb`. Este es el nombre de extensión de los cuadernos de jupyter.

**Seleccionar un Kernel:**
* El notebook necesitará conectarse a un "kernel" (núcleo) de Python para ejecutar código.
* Usualmente, en la parte superior derecha de la interfaz del notebook, verán una opción para "Select Kernel" (Seleccionar Kernel).
* Hagan clic allí y elijan el entorno de Python que configuraron anteriormente (el mismo que seleccionaron como su intérprete de Python).
* Si se les solicita instalar `ipykernel` u otros paquetes, permitan que la extensión lo haga.

**Usar el Notebook:**
* Un notebook está hecho de "celdas".
* **Celdas de código:** Donde escriben y ejecutan código Python. Escriban su código y presionen `Shift+Enter` (o hagan clic en el botón de reproducir junto a la celda) para ejecutarlo.
* **Celdas de Markdown:** Donde pueden escribir texto, como esta guía. Pueden cambiar el tipo de celda usando el menú desplegable en la barra de herramientas del notebook.
---
### Prueba Python y Jupyter

Asegurémonos de que todo funcione.

**Script de Python Simple en VS Code:**
* Creen un nuevo archivo en VS Code (File > New File o Archivo > Nuevo Archivo).
* Guárdenlo como `hola.py`.
* Escriban el siguiente código Python:
```python

print("¡Hola, desde un script de Python!")

```

* Guarden el archivo (`Ctrl+S` o `Cmd+S`).
* Hagan clic derecho en el editor y seleccionen "Run Python File in Terminal" (Ejecutar Archivo Python en Terminal) o hagan clic en el botón de reproducir en la parte superior derecha de la ventana de VS Code.
* Deberían ver el mensaje impreso en el panel de la terminal de VS Code.

**Prueba Simple de Jupyter Notebook:**
* Si no tienen un Jupyter Notebook abierto, creen uno (`Jupyter: Create New Jupyter Notebook` desde la Paleta de Comandos).
* En la primera celda de código, escriban:
```python

mensaje = "¡Hola desde una celda de Jupyter Notebook!"

print(mensaje)

```

* Presionen `Shift+Enter` para ejecutar la celda.
* Deberían ver la salida `¡Hola desde una celda de Jupyter Notebook!` mostrada directamente debajo de la celda.

## Introducción a la Visualización de Datos con Pandas y Plotly

La ciencia de datos moderna requiere herramientas poderosas para el análisis y visualización de información. En este tutorial completo, exploraremos dos de las librerías más importantes del ecosistema Python para análisis de datos: **Pandas** para manipulación de datos y **Plotly** para visualizaciones interactivas.
### Dataset: Expresión Génica en Regiones Cerebrales

Para esta sección utilizaremos un dataset real del **Human Protein Atlas** que contiene información sobre la expresión de genes en diferentes regiones del cerebro humano. Este tipo de datos es crucial para entender cómo funcionan los genes en diferentes partes del cerebro.


### Configuración Inicial

#### Importar las Librerías Necesarias
```python

import pandas as pd

import plotly.express as px

import plotly.graph_objects as go

import numpy as np

```

**¿Por qué estas librerías?**

- **Pandas**: La herramienta fundamental para manipulación de datos en Python

- **Plotly Express**: Para crear visualizaciones rápidas e interactivas

- **Plotly Graph Objects**: Para visualizaciones más personalizadas

- **NumPy**: Para operaciones matemáticas y manejo de arrays

#### Cargar los Datos
```python

brain_data = pd.read_csv('rna_brain_region_hpa.csv')

```
### Exploración Inicial: La Primera Mirada

#### ¿Qué Contienen Nuestros Datos?

Antes de analizar, debemos entender qué estamos manejando:
```python

# Mostrar las primeras 10 filas

brain_data.head(10)

```
#### Resumen Técnico del Dataset
```python

# Información general sobre el dataset

brain_data.info()

```

**¿Qué nos dice esto?**

- Número total de filas y columnas

- Tipos de datos en cada columna

- Valores nulos (si los hay)

- Uso de memoria
#### Resumen Estadístico

```python

# Estadísticas descriptivas

brain_data.describe()

```

**Información clave:**

- Medidas de tendencia central (media, mediana)
- Dispersión de los datos (desviación estándar)
- Valores mínimos y máximos
- Percentiles (25%, 50%, 75%)
### Análisis Exploratorio con Pandas

#### Contando Ocurrencias
```python

# ¿Cuántas muestras tenemos por región cerebral?

brain_data['Brain region'].value_counts()

```

#### Elementos Únicos
```python

print(f'Número de genes únicos: {brain_data["Gene name"].nunique()}')

print(f'Número de regiones cerebrales únicas: {brain_data["Brain region"].nunique()}')

```

### Filtrado y Selección de Datos

#### Filtrado Básico
```python

# Filtrar datos solo del cerebelo

cerebellum = brain_data[brain_data['Brain region'] == 'cerebellum']

  

# Genes con alta expresión (TPM > 100)

high_expression = brain_data[brain_data['TPM'] > 100]

```

#### Selección con .loc  y .iloc
```python

# Selección basada en etiquetas

specific_gene = brain_data.loc[brain_data['Gene name'] == 'TNMD']

  

# Selección basada en posición

first_rows_cols = brain_data.iloc[0:5, 0:3]

```
#### Indexación Avanzada
```python

# Crear índice multi-nivel

df_indexed = brain_data.set_index(['Gene name', 'Brain region'])

  

# Acceder a datos específicos

gene_tpm = df_indexed.loc[('TNMD', 'cerebellum'), 'TPM']

```

### Agrupación y Agregación
#### Promedios por Región
```python

# Expresión promedio por región cerebral

avg_expression_by_region = brain_data.groupby('Brain region').mean(numeric_only=True)

```
#### Múltiples Agregaciones
```python

# Mediana y suma por región

median_expression = brain_data.groupby('Brain region').median(numeric_only=True)

sum_expression = brain_data.groupby('Brain region').sum(numeric_only=True)

```

### Creación de Nuevas Variables

#### Función para Categorizar Expresión
```python

def nivel_de_expresion(tpm):

if tpm < 1:

return 'Baja'

elif tpm < 10:

return 'Media'

else:

return 'Alta'

  

# Aplicar la función

brain_data['nivel_de_expresion'] = brain_data['TPM'].apply(nivel_de_expresion)

```

### Visualización con Plotly

#### Gráfico de Barras Interactivo
```python

gen = "GFAP"

  

df_filtrado_por_gen = brain_data[brain_data['Gene name'] == gen]

  

fig = px.bar(df_filtrado_por_gen,

x='Brain region',

y='TPM',

title=f'Expresión de {gen} en Diferentes Regiones Cerebrales',

labels={'TPM': 'TPM (Transcritos Por Millón)', 'Brain region': 'Región Cerebral'})

fig.update_xaxes(tickangle=45) # Rotar las etiquetas del eje x para una mejor legibilidad

fig.show()

```

#### Histograma de Distribución
```python

fig = px.histogram(brain_data,

x='TPM',

title='Distribución de la Expresión Génica (TPM)',

labels={'TPM': 'TPM (Transcritos Por Millón)'},

log_y=True, # Usar una escala logarítmica en el eje y para ver el rango completo

nbins=100) # Aumentar el número de "bins" o intervalos para más detalle

fig.show()

```

#### Gráfico de Violin: Distribución por Región
```python

fig = px.violin(

brain_data,

x='Brain region',

y='TPM',

title='Distribución de Expresión por Región Cerebral',

box=True

)

  

fig.update_xaxes(tickangle=45)

fig.show()

```

#### Mapa de Calor (Heatmap)
```python

# Seleccionar genes de interés

genes_of_interest = ['OLIG2', 'RBM6', 'GDE1', 'TSPAN6', 'CYP51A1', 'HS3ST1', 'SPAST']

heatmap_df = brain_data[brain_data['Gene name'].isin(genes_of_interest)]

# Debemos "pivotar" la tabla para obtener la forma correcta para un mapa de calor

heatmap_pivot = heatmap_df.pivot_table(index='Gene name', columns='Brain region', values='nTPM')

  

fig = px.imshow(heatmap_pivot,

title='Mapa de Calor de Expresión Génica de Marcadores Neuronales',

labels=dict(x="Región Cerebral", y="Nombre del Gen", color="nTPM"),

color_continuous_scale="plasma",

# zmin=0, # Establecer límite inferior de la escala

# zmax=100 # Establecer límite superior de la escala

)

fig.show()



```



### Análisis Interactivo Avanzado

#### Función para Análisis por Gen
```python

  

def analizar_gen(gen):

  
	df_filtrado = brain_data[brain_data['Gene name'] == gen]
	
	  
	
	if df_filtrado.empty:
	
	
		print(f"Gen '{gen}' no encontrado en el dataset")
	
		return
	
	  
	
	fig = px.bar(
	
		df_filtrado,
		x='Brain region',
		y='TPM',
		title=f'Expresión del Gen {gen} por Región Cerebral',
		color='TPM',
		color_continuous_scale='viridis'
	)
	
	
	fig.update_xaxes(tickangle=45)
	
	
	fig.show()
	
	
	return df_filtrado



# Ejemplo de uso

  

resultado = analizar_gen('ACTB')

```

#### Top Genes por Región
```python

def top_genes_region(region, n=15):

	"""
	
	Encuentra los genes más expresados en una región específica
	
	"""

	top_genes = brain_data[brain_data['Brain region'] == region]\
	.sort_values(by=['pTPM', 'TPM', 'nTPM'], ascending=False)\
	.head(n)

	fig = px.bar(
	
	top_genes,
	
	x='Gene name',
	
	y='TPM',
	
	title=f'Top {n} Genes Más Expresados en {region.title()}',
	
	color='TPM',
	
	color_continuous_scale='plasma'
	
	)
	
	fig.update_xaxes(tickangle=45)
	
	fig.show()
	
	return top_genes

  

  

# Ejemplo

  

top_cerebellum = top_genes_region('cerebellum')

```

### Manejo de Datos Faltantes
```python

# Verificar datos nulos

print("Datos nulos por columna:")

print(brain_data.isnull().sum())

  

# En caso de tener datos nulos:

# brain_data.dropna() # Eliminar filas con valores nulos

# brain_data.fillna(0) # Reemplazar con 0

```

### Recursos Adicionales

- [Documentación oficial de Pandas](https://pandas.pydata.org/docs/)

- [Galería de ejemplos de Plotly](https://plotly.com/python/)

- [Human Protein Atlas](https://www.proteinatlas.org/)


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

## Trabajando con Archivos LIF en Napari

### Prerrequisitos

Antes de comenzar, asegúrate de tener los paquetes necesarios instalados:

```bash

pip install napari aicsimageio scikit-image

```
### Configurando el Entorno

Primero, importemos las librerías necesarias:
```python

import napari

from skimage import data

from skimage.io import imread

from aicsimageio import AICSImage

```

### Creando un Visor de Napari

Comienza creando una instancia del visor de napari:
```python

viewer = napari.Viewer()

```

Esto abre la interfaz de napari donde visualizaremos nuestros datos de imagen.

### Cargando un Archivo LIF

Carga tu archivo LIF usando AICSImage:

```python

img = AICSImage("./lif_test.lif")

```

Reemplaza `"./lif_test.lif"` con la ruta a tu archivo LIF.

### Explorando las Dimensiones de la Imagen

Verifica las dimensiones de tu imagen cargada:
```python

print(img.dims)

```

Esto mostrará algo como:

```

<Dimensions [T: 1, C: 4, Z: 8, Y: 512, X: 512]>

```


### Obteniendo Datos de Imagen

Extrae los datos de imagen para análisis:

```python

image_data = img.get_image_data("CZYX", T=0)

print(image_data.shape)

```


El parámetro `"CZYX"` especifica el orden de las dimensiones:

- **C**: Canales primero

- **Z**: Planos Z segundo

- **Y**: Altura tercero

- **X**: Ancho cuarto

### Trabajando con Múltiples Escenas

Los archivos LIF a menudo contienen múltiples escenas (diferentes campos de vista o condiciones experimentales). Exploremos qué está disponible:
```python

# Imprimir todas las escenas disponibles

print(img.scenes)

print(f"Número total de series en el archivo: {len(img.scenes)}")

```

  Esto te mostrará todos los nombres de escenas en tu archivo LIF, como:

```

('LPS SYN settings', 'LPS SYN 0', 'LPS SYN 1.1', 'LPS SYN 1.2', ...)

Número total de series en el archivo: 119

```

### Seleccionando y Cargando una Escena Específica

Elige una escena específica con la que trabajar:
```python

# Seleccionar una escena por índice

scene_index = 10 # Cambia esto para cargar diferentes escenas

selected_scene = img.scenes[scene_index]

print(f"Escena seleccionada: {selected_scene}")

  

# Establecer la escena actual en el objeto AICSImage

img.set_scene(scene_index)

  

# Obtener los datos de imagen para la escena seleccionada

image_data = img.get_image_data("CZYX", T=0)

  

# Imprimir dimensiones para esta escena

print(f"Número total de canales C: {image_data.shape[0]}")

print(f"Número total de planos Z: {image_data.shape[1]}")

```

### Visualizando en Napari

Finalmente, carga los datos de imagen en napari para visualización:
```python

# Limpiar cualquier capa anterior

viewer.layers.clear()

  

# Agregar la imagen con organización apropiada de canales y planos z

viewer.add_image(

image_data,

channel_axis=0, # La primera dimensión (C) es el canal

name=f"Escena: {selected_scene}",

scale=[1, 1, 1], # Escala para dimensiones Z, Y, X

)

```

### Entendiendo la Interfaz de Napari

Una vez cargado, verás:
1. **Controles de Canal**: Deslizadores y controles para cada canal (dimensión C)

2. **Navegación de Plano Z**: Deslizador para navegar a través del z-stack (dimensión Z)

3. **Capas de Canal Individuales**: Cada canal aparece como una capa separada en la lista de capas

4. **Controles de Visualización**: Opciones de contraste, mapa de colores y mezcla para cada canal

### Consejos para Trabajar con Datos Multi-dimensionales

1. **Visualización de Canales**: Cada canal se mostrará como una capa separada, permitiéndote:

- Activar/desactivar canales

- Ajustar contraste y brillo individualmente

- Cambiar mapas de colores para mejor visualización

  

2. **Navegación de Z-stack**: Usa el deslizador z para navegar a través de diferentes planos focales

3. **Comparación de Escenas**: Para comparar diferentes escenas:

```python

# Cargar múltiples escenas para comparación

for i in [5, 10, 15]: # Ejemplo de índices de escenas

img.set_scene(i)

data = img.get_image_data("CZYX", T=0)

viewer.add_image(data, channel_axis=0, name=f"Escena: {img.scenes[i]}")

```


4. **Gestión de Memoria**: Para archivos grandes con muchas escenas:

- Carga escenas individualmente en lugar de todas a la vez

- Limpia el visor entre escenas si es necesario: `viewer.layers.clear()`

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
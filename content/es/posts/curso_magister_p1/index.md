---
title: "Introducción al Uso Moderno de LLMs. Uso de API's. Parte 1 - Magister UAndes"
date: "2025-08-14"
summary: "Guía acompañamiento curso Python y Napari doctorado UAndes 2025"
description: "Guía clase python y napari doctorado UAndes 2025"
toc: false
autonumber: true
math: false
showTags: false
hidePagination: true
draft: false
---

# Introducción

En esta guía para los cursos de postgrado MEPI y DESG 2025 de la Universidad de los Andes, Chile, está encargada de explicar y dejar ejemplos prácticos para introducirnos al mundo de uso de LLM's a través de API's. Para esto, utilizaremos [OpenRouter](https://openrouter.com), servicio que nos permite acceder a la gran mayoría de los modelos disponibles utilizando una API_KEY y código uno, haciendo la experimentación e iteración sencilla. 

En este ejemplo, utilizaremos python para nuestros ejemplos, pero puedes realizar estas acciones en la mayoría de los lenguajes de programación. Dejo la documentación de OpenRouter [aquí](https://openrouter.ai/docs/quickstart)


## Paso 1: Crear una cuenta y obtener una API Key
- Ingresa a https://openrouter.ai y crea una cuenta.
- Ve a Dashboard → API Keys → Create.
- Copia tu clave y guárdala en un lugar seguro (esta clave se usa para autenticarte con el servicio).
    - Es recomendable agregarle un límite de $ a tu API key por si es comprometida

> ⚠️ Seguridad: Si alguien obtiene tu API KEY, puede utilizarla para hacer requests a la API a tu cargo. Siempre guardala un archivo .env y asegura de nunca compartirla. Si la clave se filtra, bórrala y crea una nueva. Nunca la subas a Git u otros repositorios públicos.


## Paso 2: Instala los paquetes 

```bash
pip install openai python-dotenv requests
```

## Paso 3: Manos a la obra
OpenRouter usa una API compatible con OpenAI, así que podemos usar la misma librería de Python, solo cambiando la URL base.

```python
# archivo: hola_openrouter.py
from openai import OpenAI
from dotenv import load_dotenv
import os

load_dotenv()
client = OpenAI(
    base_url="https://openrouter.ai/api/v1",
    api_key=os.getenv("OPENROUTER_API_KEY")
)

resp = client.chat.completions.create(
    model="openai/gpt-5-nano",  
    messages=[{"role": "user", "content": """
    
           Quiero un dato aleatorio 
           sobre la historia de la medicina. 
    
    
    """}],

)
print(resp.choices[0].message.content)
```


### Ejemplo de output

> En la India antigua, Sushruta, considerado el padre de la cirugía, describe en el Sushruta Samhita la rinoplastia (cirugía de la nariz) utilizando un colgajo de piel de la frente para reconstruir la nariz, una de las primeras técnicas quirúrgicas reconstructivas registradas. ¿Quieres otro dato histórico de la medicina?



## Paso 4: Outputs Estructurados

En esta sección veremos cómo pedirle al modelo una respuesta en un formato estrictamente estructurado (por ejemplo, JSON). Esto facilita validar, almacenar y consumir los resultados desde tu código. Describiremos la respuesta requerida en formato JSON y luego lo parsearemos en Python para usarlo directamente.

```python
import json

client = OpenAI(
    base_url="https://openrouter.ai/api/v1",
    api_key=os.getenv("OPENROUTER_API_KEY")
)

resp = client.chat.completions.create(
    model="openai/gpt-5-nano",  
    messages=[{"role": "user", "content": """
    
           Quiero un dato aleatorio 
           sobre la historia de la medicina. 

            Quiero que el resultado sea un JSON con la siguiente estructura:
               {
               "título": "string",
               "fecha": "string",
               "descripción": "string",
               "protagonista": "string"
               }
    
    
    """}],
    response_format={"type": "json_object"}
)

json_content = resp.choices[0].message.content
data = json.loads(json_content)
print(data)
```

### Ejemplo de output
```json
{
  "título": "Descubrimiento de la penicilina",
  "fecha": "1928",
  "descripción": "En 1928, Alexander Fleming observó que un moho del género Penicillium notatum contaminó una placa de cultivo de Staphylococcus aureus y que, alrededor del moho, el crecimiento bacteriano se detenía. Este hallazgo llevó al aislamiento de la penicilina, el primer antibiótico, y marcó el inicio de la era de los antibióticos.",
  "protagonista": "Alexander Fleming"
}
```


## Comentarios finales

### Como elegir un modelo

En la sección de [modelos](https://openrouter.ai/models) de openrouter, tienes la lista completa de todos los modelos disponibles, en donde podrás filtrar según tus requerimientos. Cuando quieras probar con alguno, puedes cambiar el modelo de los ejemplos en el parámetro `model` al modelo que quieras utilizar. Debes pegar el nombre del modelo de la siguiente manera para que haya consistencia con la API de OpenRouter: 


![copy_model](copy_model.png)


### Seguridad

- Guarda las claves en .env y nunca en el código.
- Si se filtra, rota la clave inmediatamente.
- Usa un prompt de sistema si quieres controlar tono, formato o enfoque médico.
- Guarda en logs el ID del modelo para reproducir resultados.



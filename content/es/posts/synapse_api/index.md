---
title: "Synapse API - Backend RESTful en Go"
date: "2025-08-05"  
summary: "Una API en Go para gestionar datos de Synapse con capacidades de llenado de plantillas"
description: "API RESTful construida en Go para gestión de prompts/conocimiento/contexto con procesamiento dinámico de plantillas"
toc: false
readTime: false
autonumber: true
math: false
showTags: false
hidePagination: true
draft: false
---

# Synapse API: Llevando el Poder de Go a la Gestión de Prompts

**Synapse API** es un backend RESTful basado en Go que extiende las capacidades de [Synapse](../synapse), mi aplicación nativa de macOS para gestión de prompts. Esta API proporciona acceso programático a todos los datos de Synapse con poderosa funcionalidad de llenado de plantillas.

## 🚀 Por Qué Construí Esto

Después de crear Synapse para macOS, quería explorar cómo los mismos datos podrían ser accedidos y manipulados programáticamente. Este se convirtió en uno de mis primeros proyectos serios en Go, y realmente disfruté la experiencia de construir con la simplicidad y rendimiento de Go.

## 🔧 Características Principales

### **Arquitectura RESTful**
- Operaciones CRUD completas para todos los tipos de datos
- Diseño de endpoints limpio e intuitivo
- Formato de solicitud/respuesta basado en JSON
- Rendimiento ligero y rápido

### **Gestión de Datos**
- **Prompts**: Gestiona plantillas reutilizables con marcadores de posición
- **Contextos**: Maneja materiales de referencia e información de fondo
- **Conocimiento**: Organiza hechos, resúmenes y elementos de conocimiento
- **Bibliotecas de Plantillas**: Mantiene colecciones de fragmentos de plantillas

### **Procesamiento de Plantillas** 🎯
- Llenado dinámico de variables en plantillas
- Soporte para sintaxis de marcador `{nombre_variable}`
- Llena plantillas por contenido o por ID
- Renderizado de plantillas en tiempo real

## 📡 Endpoints de la API

### Operaciones Generales
```
GET  /api/data          # Recuperar todos los datos
PUT  /api/data          # Actualizar todo el conjunto de datos
```

### Endpoints Específicos por Recurso
```
GET  /api/prompts       # Obtener todos los prompts
PUT  /api/prompts       # Actualizar prompts

GET  /api/contexts      # Obtener todos los contextos
PUT  /api/contexts      # Actualizar contextos

GET  /api/knowledge     # Obtener todos los elementos de conocimiento
PUT  /api/knowledge     # Actualizar conocimiento

GET  /api/templates     # Obtener bibliotecas de plantillas
PUT  /api/templates     # Actualizar plantillas
```

### Llenado de Plantillas
```
POST /api/fill-template       # Llenar plantilla con variables
POST /api/fill-template-by-id # Llenar plantilla por ID
```

## 💡 Ejemplos de Plantillas

**Llenar por contenido:**
```json
{
  "template": "Hola {nombre}, ¡bienvenido a {lugar}!",
  "variables": {
    "nombre": "Juan",
    "lugar": "nuestra plataforma"
  }
}
```

**Llenar por ID:**
```json
{
  "template_id": "94BD3B8E-93C4-4ED8-B2A1-9765016C9521",
  "variables": {
    "tema_reunion": "planificación del proyecto",
    "nombre_destinatario": "Juan Pérez"
  }
}
```

## 🛠️ Stack Tecnológico

**Construido con:**
- **Go** - Lenguaje de backend limpio y eficiente
- **Gorilla Mux** - Router HTTP poderoso y matcher de URLs
- **JSON** - Persistencia e intercambio de datos nativo
- **Diseño RESTful** - Métodos HTTP y códigos de estado estándar

## 🎯 Integración Perfecta

La API funciona perfectamente con datos exportados desde la app Synapse de macOS:
- **Fuente de Datos**: `~/Documents/synapse_data.json`
- **Importación Directa**: Usa datos exportados de Synapse inmediatamente
- **Sincronización Bidireccional**: Los cambios pueden fluir de vuelta a la app de escritorio

## 🚀 Comenzando

```bash
# Clonar y configurar
git clone [url-del-repositorio]
cd synapse-api
go mod tidy

# Ejecutar el servidor
go run main.go

# El servidor inicia en el puerto 8081
```

## 🧪 Pruebas

Incluye un script de pruebas completo:
```bash
./test-api.sh
```

*Requiere `curl` y `jq` para las pruebas*

## 🎓 Aprendiendo Go

Este proyecto marcó una de mis primeras exploraciones serias en Go, y quedé impresionado por:
- **Simplicidad**: Sintaxis limpia y conceptos directos
- **Rendimiento**: Compilación rápida y tiempo de ejecución eficiente
- **Biblioteca Estándar**: Rico soporte integrado para HTTP y JSON
- **Herramientas**: Excelente experiencia de desarrollo con `go mod` y testing

La experiencia me convenció de que Go es una excelente opción para desarrollo de APIs y servicios backend.

---

**Extiende tu flujo de trabajo de Synapse con acceso programático y procesamiento dinámico de plantillas.**

🌐 **GitHub**: [Ver Repositorio del Proyecto](https://github.com/fhello23/synapse-api)  
💻 **Lenguaje**: Go con Gorilla Mux  
🔗 **Compañero**: Funciona con [Synapse App para macOS](../synapse)
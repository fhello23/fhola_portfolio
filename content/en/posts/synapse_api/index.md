---
title: "Synapse API - Go-Based RESTful Backend"
date: "2025-08-05"
summary: "A Go API for managing Synapse data with template filling capabilities"
description: "RESTful API built in Go for prompt/knowledge/context management with dynamic template processing"
toc: false
readTime: false
autonumber: true
math: false
showTags: false
hidePagination: true
draft: false
---

# Synapse API: Bringing Go Power to Prompt Management

**Synapse API** is a Go-based RESTful backend that extends the capabilities of [Synapse](../synapse), my native macOS prompt management application. This API provides programmatic access to all Synapse data with powerful template filling functionality.

## 🚀 Why I Built This

After creating Synapse for macOS, I wanted to explore how the same data could be accessed and manipulated programmatically. This became one of my first serious Go projects, and I really enjoyed the experience of building with Go's simplicity and performance.

## 🔧 Core Features

### **RESTful Architecture**
- Complete CRUD operations for all data types
- Clean, intuitive endpoint design
- JSON-based request/response format
- Lightweight and fast performance

### **Data Management**
- **Prompts**: Manage reusable templates with placeholders
- **Contexts**: Handle reference materials and background info
- **Knowledge**: Organize facts, summaries, and knowledge items
- **Template Libraries**: Maintain collections of template snippets

### **Template Processing** 🎯
- Dynamic variable filling in templates
- Support for `{variable_name}` placeholder syntax
- Fill templates by content or by ID
- Real-time template rendering

## 📡 API Endpoints

### General Operations
```
GET  /api/data          # Retrieve all data
PUT  /api/data          # Update entire dataset
```

### Resource-Specific Endpoints
```
GET  /api/prompts       # Get all prompts
PUT  /api/prompts       # Update prompts

GET  /api/contexts      # Get all contexts  
PUT  /api/contexts      # Update contexts

GET  /api/knowledge     # Get all knowledge items
PUT  /api/knowledge     # Update knowledge

GET  /api/templates     # Get template libraries
PUT  /api/templates     # Update templates
```

### Template Filling
```
POST /api/fill-template       # Fill template with variables
POST /api/fill-template-by-id # Fill template by ID
```

## 💡 Template Examples

**Fill by content:**
```json
{
  "template": "Hello {name}, welcome to {place}!",
  "variables": {
    "name": "John",
    "place": "our platform"
  }
}
```

**Fill by ID:**
```json
{
  "template_id": "94BD3B8E-93C4-4ED8-B2A1-9765016C9521",
  "variables": {
    "meeting_topic": "project planning",
    "recipient_name": "John Doe"
  }
}
```

## 🛠️ Technical Stack

**Built with:**
- **Go** - Clean, efficient backend language
- **Gorilla Mux** - Powerful HTTP router and URL matcher
- **JSON** - Native data persistence and exchange
- **RESTful Design** - Standard HTTP methods and status codes

## 🎯 Perfect Integration

The API seamlessly works with data exported from the Synapse macOS app:
- **Data Source**: `~/Documents/synapse_data.json`
- **Direct Import**: Use exported Synapse data immediately
- **Bidirectional Sync**: Changes can flow back to the desktop app

## 🚀 Getting Started

```bash
# Clone and setup
git clone [repository-url]
cd synapse-api
go mod tidy

# Run the server
go run main.go

# Server starts on port 8081
```

## 🧪 Testing

Includes a comprehensive test script:
```bash
./test-api.sh
```

*Requires `curl` and `jq` for testing*

## 🎓 Learning Go

This project marked one of my first serious explorations into Go, and I was impressed by:
- **Simplicity**: Clean syntax and straightforward concepts
- **Performance**: Fast compilation and efficient runtime
- **Standard Library**: Rich built-in HTTP and JSON support
- **Tooling**: Excellent development experience with `go mod` and testing

The experience convinced me that Go is an excellent choice for API development and backend services.

---

**Extend your Synapse workflow with programmatic access and dynamic template processing.**

🌐 **GitHub**: [View API Repository](https://github.com/fhello23/synapse-api)   
💻 **Language**: Go with Gorilla Mux  
🔗 **Companion**: Works with [Synapse macOS App](../synapse)
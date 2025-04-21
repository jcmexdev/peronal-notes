---
title: Go Scheduler
status:
  - todo
created: 20-04-2025 17:43:00
updated: 20-04-2025 17:43:19
---

Claro, aquí tienes la nota del **Go Scheduler** en formato Zettelkasten:

---

# Go Scheduler

🔖 **Tags**: #go #goroutines #scheduler #concurrency 

---

## 🧠 Main idea

El **Go Scheduler** es el componente responsable de manejar la ejecución de las _goroutines_ en el entorno de ejecución de Go. Implementa un modelo **M:N**, en el que muchas goroutines se asignan dinámicamente a un conjunto menor de hilos del sistema operativo (OS threads).

---

## 🧩 Context

El scheduler de Go permite manejar miles de goroutines con pocos hilos del sistema operativo, gracias a su diseño eficiente. Está inspirado en el concepto de _work stealing_, tiene su propio sistema de colas locales y globales, y se encarga de realizar _context switching_ entre goroutines de forma cooperativa.

Elementos clave del runtime de Go:

- **M** (Machine): hilo del sistema operativo.
    
- **P** (Processor): contexto de ejecución que mantiene colas de goroutines.
    
- **G** (Goroutine): unidad de ejecución ligera.
    

Este sistema hace que el lenguaje Go sea especialmente adecuado para tareas concurrentes y servidores de alto rendimiento.

---

## 🔗 Enlaces relacionados

- [Goroutines](https://chatgpt.com/c/202504191447.md)
    
- [Context switching](https://chatgpt.com/c/202504191237.md)
    
- [Modelo M:N](https://chatgpt.com/c/202504191519.md)
    
- [Concurrencia en Go](https://chatgpt.com/c/202504181215.md)
    

---

## 📘 Referencias

- Libro: _Learn Concurrent Programming with Go_ – James Cutajar
    
- Blog: [The Go scheduler](https://go.dev/blog/scheduler)
    
- Documentación oficial de Go: [https://golang.org/doc/](https://golang.org/doc/)
    

---

¿Quieres que también prepare una versión visual del sistema M:P:G del runtime de Go con un diagrama para tu vault de Obsidian?
---
title: goroutines
status:
  - todo
created: 20-04-2025 10:52:28
updated: 20-04-2025 15:18:56
---

# Goroutines

🔖 **Tags**: #golang #concurrency #threads #os

---

## 🧠 Main idea

Las goroutines son unidades ligeras de ejecución en Go. Son similares a los hilos (threads), pero gestionadas por el runtime del lenguaje, lo que permite lanzar miles de ellas con muy bajo costo.

---

## 🧩 Context

Una goroutine se lanza con la palabra clave `go`, que indica al planificador de Go que ejecute esa función de forma concurrente. Internamente, Go realiza el manejo del stack, el [[Context Switching]] (o una mini version con las mismas funciones del so) y el agendamiento de goroutines ([[Go Scheduler]]), sin requerir un hilo del sistema por cada una.

Esto hace que Go sea altamente eficiente para construir sistemas concurrentes y paralelos. Sin embargo, como son gestionadas en espacio de usuario, se requiere mecanismos como **WaitGroups**, **channels**, o **contextos** para coordinar su ejecución.

---

## 🔗 Enlaces relacionados

- [[user-level threads]]
- [[Waiting Groups]]
- [[Go Scheduler]]
- [[M-N Execution Model]]

---

## 📘 Referencias

- Libro: _Learn Concurrent Programming with Go_ – James Cutajar
    
- Documentación oficial de Go: [https://golang.org/doc/](https://golang.org/doc/)
    
- Blog: [Goroutines vs Threads](https://blog.golang.org/goroutines)
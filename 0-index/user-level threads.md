---
title: user-level threads
status:
  - todo
created: 20-04-2025 10:50:52
updated: 20-04-2025 10:51:59
---

# User-Level Threads en Go

🔖 **Tags**: #concurrency #golang #threads #os

---

## 🧠 Main idea

Los _user-level threads_ (como las goroutines en Go) son hilos que se gestionan completamente en espacio de usuario, sin intervención directa del sistema operativo. Esto permite una concurrencia eficiente, con menor sobrecarga que los hilos del sistema.

---

## 🧩 Context

A diferencia de los hilos del sistema operativo, los _user-level threads_ no son visibles para el SO. En el caso de Go, el runtime del lenguaje es el encargado de gestionar su ejecución mediante un planificador propio (scheduler). Este realiza tareas como cambiar de contexto entre goroutines, ponerlas en espera o ejecutarlas según sea necesario.

Go implementa un modelo **M:N scheduling**, donde muchas goroutines (_M_) se asignan dinámicamente sobre pocos hilos del sistema operativo (_N_). Esto permite escalar a miles de tareas concurrentes con muy bajo costo en memoria y tiempo.

---

## 🔗 Enlaces relacionados

- [[goroutines]]
- [[Context Switching]]

---

## 📘 Referencias

- Libro: _Learn Concurrent Programming with Go_ – James Cutajar
    
- Documentación oficial de Go: [https://golang.org/doc/](https://golang.org/doc/)
    
- Blog: Go Scheduler: Implementing M:N
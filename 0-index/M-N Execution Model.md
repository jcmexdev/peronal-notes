---
title: M-N Execution Model
status:
  - todo
created: 20-04-2025 15:18:56
updated: 20-04-2025 15:19:24
---

Claro, aquí tienes una nota en formato Zettelkasten sobre el modelo **M:N** usado en Go (y también en otros lenguajes/sistemas):

---

# Modelo M:N de ejecución

🔖 **Tags**: #concurrency #scheduler #runtime #golang

---

## 🧠 Main idea

El modelo **M:N** permite mapear **M hilos del sistema operativo** para ejecutar **N unidades de ejecución en espacio de usuario** (como goroutines o hilos a nivel de usuario). Esto permite escalar la concurrencia sin requerir un hilo del sistema operativo por cada tarea concurrente.

---

## 🧩 Context

En lugar de depender exclusivamente del sistema operativo (modelo 1:1) o usar un único hilo para todas las tareas (modelo N:1), el modelo M:N aprovecha varios hilos del sistema para ejecutar múltiples tareas gestionadas en espacio de usuario.  
Lenguajes como Go usan este modelo, donde el **scheduler de Go** administra goroutines sobre un conjunto limitado de hilos del sistema operativo.

---

## ✅ Ventajas

- Mayor eficiencia y escalabilidad.
    
- Costos bajos de creación y switching de goroutines.
    
- El runtime puede balancear la carga entre hilos.
    

---

## ⚠️ Desventajas

- Mayor complejidad en la implementación del runtime.
    
- Problemas potenciales al interactuar con llamadas bloqueantes del sistema operativo.
    

---

## 🔗 Enlaces relacionados
- [[Threads vs Goroutines]]
- [[Context Switching]]

---

## 📘 Referencias

- _Learn Concurrent Programming with Go_ – James Cutajar
    
- Blog: [Go Scheduler](https://go.dev/blog/scheduler)
    
- Libro: _Operating Systems: Three Easy Pieces_ – Remzi H. Arpaci-Dusseau
    

---

¿Quieres una nota más visual del modelo M:N o una comparación con los modelos 1:1 y N:1?
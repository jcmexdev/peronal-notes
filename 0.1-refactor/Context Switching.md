---
title: Context Switching
status:
  - todo
created: 19-04-2025 15:21:34
updated: 19-04-2025 15:22:27
---

Claro, aquí tienes la tarjeta Zettelkasten sobre **Context Switching** en el formato para Obsidian:

---

# Context Switching in Operating Systems

🔖 **Tags**: #os

---

## 🧠 Main idea

**Context switching** es el proceso mediante el cual el sistema operativo guarda el estado de un proceso o hilo y carga el estado de otro. Esto permite que múltiples procesos se ejecuten de manera concurrente compartiendo la CPU, aunque no al mismo tiempo.

---

## 🧩 Context

Es fundamental para la multitarea en sistemas operativos. Por ejemplo, cuando un proceso entra en espera por una operación de entrada/salida (como leer un archivo), el sistema operativo guarda su contexto (registros, contador de programa, etc.) y activa otro proceso listo para ejecutarse. Esto mantiene a la CPU ocupada y mejora la eficiencia del sistema.

---

## 📘 Referencias

- Libro: _Learn Concurrent Programming with Go_ – James Cutajar
    
- Libro: _Operating System Concepts_ – Silberschatz, Galvin, Gagne
    
- Notas de clase: Sistemas Operativos (Semana 5)
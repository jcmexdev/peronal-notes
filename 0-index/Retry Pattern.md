---
title: Retry Pattern
status:
  - en progreso
created: 21-04-2025 02:27:22
updated: 21-04-2025 02:27:44
---

# Retry Pattern

🔖 **Tags**: #sistemas_distribuidos #patrones_resiliencia #retry #microservicios #ask 

---

## Questions?
- ¿Cómo se determina el número óptimo de reintentos?
- ¿Qué diferencia hay entre retry simple, con backoff y con jitter?
- ¿Cuándo es mejor no hacer retry (errores no transitorios)?

---

## 🧠 Main idea

El **Retry Pattern** permite volver a intentar una operación que ha fallado, bajo el supuesto de que el error es temporal (por ejemplo, congestión de red o servicio momentáneamente caído). Se utiliza para aumentar la confiabilidad en llamadas remotas.

---

## 🧩 Context

En entornos distribuidos, muchos errores son transitorios y pueden resolverse si se intenta de nuevo. Sin embargo, hacer retries de forma indiscriminada puede empeorar el problema.

Buenas prácticas al aplicar este patrón:
- **Limitar el número de intentos** para evitar ciclos infinitos.
- **Agregar backoff exponencial** (espera creciente entre intentos).
- **Añadir jitter** (aleatoriedad) para evitar thundering herd en servicios compartidos.
- **No reintentar errores no transitorios**, como errores de validación o autenticación.

Este patrón suele combinarse con **Timeouts** y puede preceder un **Fallback** o activar un **Circuit Breaker** si los errores persisten.

---

## 🔗 Enlaces relacionados


---

## 📘 Referencias

- *Release It!* – Michael T. Nygard  
- *Microservices Patterns* – Chris Richardson  
- [Microsoft Azure Architecture Patterns – Retry Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/retry)

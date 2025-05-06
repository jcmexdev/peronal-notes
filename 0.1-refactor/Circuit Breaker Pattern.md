---
title: Circuit Breaker Pattern
status:
  - en progreso
created: 21-04-2025 02:33:00
updated: 21-04-2025 02:33:07
---

# Circuit Breaker Pattern

🔖 **Tags**: #sistemas_distribuidos #patrones_resiliencia #circuitbreaker #microservicios

---

## Questions?
- ¿Cuándo debe abrirse el circuito (umbral de fallos)?
- ¿Cuánto tiempo debe estar abierto el circuito antes de probar de nuevo?
- ¿Cómo afecta el patrón a la latencia del sistema durante la recuperación?

---

## 🧠 Main idea

El **Circuit Breaker** es un patrón que previene que un sistema haga llamadas repetidas a un servicio que está fallando, protegiendo al sistema de sobrecargas y fallas en cascada. Actúa como un interruptor, abriendo el circuito cuando se detectan demasiados errores consecutivos.

---

## 🧩 Context

En sistemas distribuidos, si un servicio falla repetidamente, puede empeorar la situación al generar más llamadas fallidas, lo que puede llevar a un "ciclo de fallos". El patrón Circuit Breaker interrumpe estas llamadas, permitiendo que el servicio afectado se recupere sin ser abrumado.

Los estados del circuito suelen ser:
- **Closed**: Las llamadas se procesan normalmente.
- **Open**: El circuito está abierto y las llamadas se bloquean temporalmente.
- **Half-Open**: Algunas llamadas de prueba son permitidas para ver si el servicio se ha recuperado.

Esto ayuda a proteger al sistema, evitando que el mismo error se propague a otros servicios.

---

## 🔗 Enlaces relacionados

---

## 📘 Referencias

- *Release It!* – Michael T. Nygard  
- *Microservices Patterns* – Chris Richardson  
- [Microsoft Azure Architecture Patterns – Circuit Breaker Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/circuit-breaker)

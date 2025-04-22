---
title: Fallback Pattern
status:
  - en progreso
created: 21-04-2025 02:31:47
updated: 21-04-2025 02:31:56
---

# Fallback Pattern

🔖 **Tags**: #sistemas_distribuidos #patrones_resiliencia #fallback #microservicios

---

## Questions?
- ¿Qué tipo de respuestas alternativas son seguras de ofrecer?
- ¿Cómo afecta el fallback a la experiencia del usuario?
- ¿Debe registrarse o monitorearse cada vez que se activa un fallback?

---

## 🧠 Main idea

El **Fallback Pattern** proporciona una respuesta alternativa cuando una operación falla, como por ejemplo usar datos en caché o devolver un mensaje genérico. Permite que el sistema siga funcionando de forma degradada en lugar de fallar completamente.

---

## 🧩 Context

Cuando un servicio remoto no responde y los reintentos fallan, usar fallback evita una mala experiencia de usuario y reduce la presión sobre el sistema.

Ejemplos comunes:
- Mostrar resultados en caché si el servicio de búsqueda está caído.
- Devolver un mensaje genérico de error personalizado.
- Redirigir a otro servicio equivalente si está disponible.

Este patrón es especialmente útil cuando:
- El sistema no puede quedarse sin respuesta.
- Existe una alternativa segura, aunque menos precisa.
- Se prioriza la continuidad del servicio.

El fallback puede aplicarse de forma local (en el cliente) o global (en una capa de orquestación).

---

## 🔗 Enlaces relacionados

---

## 📘 Referencias

- *Release It!* – Michael T. Nygard  
- *Microservices Patterns* – Chris Richardson  
- [Microsoft Azure Architecture Patterns – Fallback Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/fallback)

---
title: Timeout Pattern
status:
  - en progreso
created: 21-04-2025 02:21:32
updated: 21-04-2025 02:27:02
---

# Timeout Pattern

🔖 **Tags**: #sistemas_distribuidos #patrones_resiliencia #timeout #microservicios
#ask

---

## Questions?
- ¿Cuál es el valor recomendado de timeout en servicios internos vs. externos?
- ¿Qué impacto puede tener un timeout mal configurado en la latencia general del sistema?
- ¿Cómo se combinan los timeouts con retries sin causar más carga?

---

## 🧠 Main idea

El patrón **Timeout** establece un tiempo máximo para que una operación remota responda. Si no hay respuesta dentro del tiempo definido, la operación se cancela y se considera fallida. Esto ayuda a evitar que el sistema se bloquee esperando indefinidamente.

---

## 🧩 Context

En sistemas distribuidos, las fallas o lentitud en un servicio pueden causar cuellos de botella si no se limita el tiempo de espera. Un timeout bien configurado:
- Libera recursos rápidamente (hilos, conexiones, memoria).
- Mejora la capacidad de respuesta general del sistema.
- Previene fallas en cascada.
- Permite activar mecanismos posteriores como Retry, Fallback o Circuit Breaker.

Establecer valores adecuados es clave:
- Demasiado corto → errores falsos.
- Demasiado largo → bloqueo de recursos.

---

## 🔗 Enlaces relacionados

---

## 📘 Referencias

- *Designing Distributed Systems* – Brendan Burns  
- *Release It!* – Michael T. Nygard  
- *Microservices Patterns* – Chris Richardson  
- [Microsoft Azure Architecture Patterns – Timeout Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/timeout)

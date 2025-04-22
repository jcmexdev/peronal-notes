---
title: Bulkhead Pattern
status:
  - en progreso
created: 21-04-2025 02:34:20
updated: 21-04-2025 02:35:09
---

# Bulkhead Pattern

🔖 **Tags**: #sistemas_distribuidos #patrones_resiliencia #bulkhead #microservicios

---

## Questions?
- ¿Cómo se decide el tamaño adecuado de cada "compartimiento" (bulkhead)?
- ¿Cuáles son los desafíos de implementar este patrón en sistemas distribuidos?
- ¿Puede el patrón Bulkhead coexistir con otros patrones de resiliencia, como Circuit Breaker?

---

## 🧠 Main idea

El **Bulkhead Pattern** aísla fallos en un sistema para evitar que una falla en un componente afecte a otros. Similar a los compartimientos estancos en un barco, limita el impacto de fallos en partes específicas del sistema.

---

## 🧩 Context

En sistemas distribuidos, un error o sobrecarga en un servicio puede propagarse rápidamente a otras partes del sistema, creando un efecto dominó que afecta a toda la infraestructura. El patrón **Bulkhead** segmenta los servicios en "compartimientos" independientes para reducir el impacto de fallos.

Por ejemplo:
- Separar distintos servicios en contenedores o servidores diferentes.
- Dividir las colas de trabajo en distintos grupos para aislar los picos de carga.
- Crear instancias aisladas de bases de datos para evitar que un fallo afecte a todo el sistema.

Este patrón asegura que los fallos en un componente no causen la caída de todo el sistema, permitiendo que el resto siga funcionando.

---

## 🔗 Enlaces relacionados

---

## 📘 Referencias

- *Release It!* – Michael T. Nygard  
- *Microservices Patterns* – Chris Richardson  
- [Microsoft Azure Architecture Patterns – Bulkhead Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/bulkhead)

---
created: 21-04-2025 03:36:07
updated: 21-04-2025 08:56:12
---
'---
created: 21-04-2025 03:36:07
updated: 21-04-2025 08:56:07
---
 mk ---
title: Saga Pattern
status:
  - todo
created: 21-04-2025 03:36:07
updated: 21-04-2025 03:36:10
---

# Saga Pattern

🔖 **Tags**: #sistemas_distribuidos #transacciones #patrones #resiliencia

---

## Questions?
- ¿Qué pasa si una de las compensaciones falla?
- ¿Cómo se implementa una saga orquestada vs una coreografiada?
- ¿Qué herramientas o librerías ayudan a implementar este patrón?

---

## 🧠 Main idea

El **Saga Pattern** es un patrón de diseño que permite implementar **transacciones distribuidas de larga duración** en sistemas de microservicios, dividiendo una transacción global en una secuencia de transacciones locales. Si una falla ocurre en la mitad del proceso, se ejecutan operaciones **compensatorias** para deshacer los efectos anteriores.

---

## 🧩 Context

En sistemas distribuidos, no es práctico ni eficiente mantener bloqueos largos o usar transacciones ACID tradicionales a través de múltiples servicios. El patrón Saga surge como una solución para manejar **consistencia eventual** de forma controlada.

Existen dos formas comunes de implementar este patrón:

- **Orquestado**: un componente central (orquestador) controla la secuencia de pasos y sus respectivas compensaciones.
- **Coreografiado**: cada servicio emite eventos y responde a eventos de otros, sin un controlador central.

🔁 Ejemplo típico:
1. Servicio A: crea una orden.
2. Servicio B: reserva inventario.
3. Servicio C: procesa el pago.
4. Si el paso 3 falla, el sistema ejecuta compensaciones:
   - Servicio B libera el inventario.
   - Servicio A cancela la orden.

Este enfoque mejora la resiliencia y escalabilidad, pero requiere un diseño cuidadoso para evitar inconsistencias, duplicados y fallas en las compensaciones.

---

## 🔗 Enlaces relacionados

- [[Atomic Transactions]]
- [[Two-Phase Commit (2PC)]]
- [[ACID]]
- [[Consistencia eventual]]
- [[Eventos y coreografía de servicios]]
- [[Resiliencia en sistemas distribuidos]]

---

## 📘 Referencias

- *Designing Data-Intensive Applications* – Martin Kleppmann  
- *Microservices Patterns* – Chris Richardson  
- Documentación oficial de Axon, Camunda, Temporal  
- Apuntes de clase de Arquitectura de Software (semana 8)

---
title: Desacoplamiento en sistemas distribuidos
status:
  - todo
created: 21-04-2025 09:37:17
updated: 21-04-2025 09:37:21
---

# Desacoplamiento en sistemas distribuidos

🔖 **Tags**: #arquitectura #sistemas_distribuidos #desacoplamiento #escalabilidad #mantenibilidad

---

## Questions?
- ¿Qué técnicas existen para lograr desacoplamiento temporal y espacial?
- ¿Cómo afecta el desacoplamiento a la trazabilidad y depuración?
- ¿Cuándo es preferible un sistema acoplado?

---

## 🧠 Main idea

El **desacoplamiento** es una estrategia de diseño que busca reducir la dependencia directa entre componentes de un sistema, permitiendo que cada uno evolucione, escale y falle de manera independiente. En sistemas distribuidos, el desacoplamiento es esencial para lograr resiliencia, mantenibilidad y escalabilidad.

---

## 🧩 Context

En sistemas monolíticos, los módulos suelen estar fuertemente acoplados, lo que significa que cualquier cambio en un componente puede impactar a otros. En sistemas distribuidos, esto no escala bien, y se buscan distintos tipos de desacoplamiento:

- **Espacial (de ubicación)**: los servicios no necesitan conocer la dirección física del receptor. Se logra usando colas de mensajes, buses de eventos o servicios de descubrimiento.
- **Temporal**: los servicios no necesitan estar disponibles al mismo tiempo. Se implementa con colas o almacenamiento temporal de mensajes (e.g. Kafka).
- **Semántico**: los servicios no necesitan conocer cómo interpretar exactamente el mensaje del otro; usan contratos o esquemas (e.g. Avro, JSON Schema).

Esto permite diseñar sistemas más robustos donde los cambios o fallas en un componente no se propagan fácilmente al resto del sistema.

---

## 🔗 Enlaces relacionados

- [[Flujos asíncronos]]
- [[Pub/Sub Pattern]]
- [[Mensajería asincrónica]]
- [[Resiliencia en sistemas distribuidos]]
- [[Tolerancia a fallos]]

---

## 📘 Referencias

- *Building Microservices* – Sam Newman  
- *Designing Data-Intensive Applications* – Martin Kleppmann  
- Apuntes de clase de Arquitectura de Software (semana 9)

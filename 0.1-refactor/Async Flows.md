---
title: Flujos asíncronos
status:
  - todo
created: 21-04-2025 11:34:42
updated: 22-04-2025 00:04:38
---

# Async Flows

🔖 **Tags**: #asincronía #sistemas_distribuidos #desacoplamiento #mensajería

---

## Questions?
- ¿Cómo se modela un flujo completamente asíncrono entre múltiples servicios?
- ¿Qué diferencias existen entre asincronía y concurrencia?
- ¿Cómo afecta la asincronía al diseño de APIs?

---

## 🧠 Main idea

Los **flujos asíncronos** permiten que los componentes de un sistema se comuniquen y trabajen **sin depender del tiempo de respuesta mutuo**. Esto mejora la escalabilidad, tolerancia a fallos y desacoplamiento en sistemas distribuidos.

---

## 🧩 Context

En lugar de invocar directamente un servicio y esperar su respuesta (llamada sincrónica), los sistemas asíncronos usan mecanismos como **colas de mensajes**, **eventos** o **callbacks** para comunicarse.

### Características:

- El emisor del mensaje no se bloquea esperando respuesta.
- Se pueden procesar tareas en paralelo o diferidas.
- Requiere mecanismos de gestión como **correlación de mensajes**, **almacenamiento temporal** y **reintentos**.

🔁 Ejemplo:

Un servicio que recibe una solicitud de subida de archivo puede colocar un mensaje en una cola. Un servicio de procesamiento de archivos lo tomará después, y al finalizar enviará otro evento de "archivo procesado". Todo ocurre sin bloquear el flujo del cliente.

### Mecanismos comunes:

- **Message Queues** (RabbitMQ, ActiveMQ)
- **Event Streams** (Kafka, NATS)
- **Webhooks / Callbacks**
- **Event-driven architectures (EDA)**

---

## 🔗 Enlaces relacionados

- [[Cola de mensajes (Productor / Consumidor)]]
- [[Desacoplamiento en sistemas distribuidos]]
- [[Pub/Sub Pattern]]
- [[Saga Pattern]]
- [Resiliencia en sistemas distribuidos]

---

## 📘 Referencias

- *Designing Event-Driven Systems* – Ben Stopford  
- *Building Microservices* – Sam Newman  
- Apuntes de clase de Arquitectura de Software (semana 10)

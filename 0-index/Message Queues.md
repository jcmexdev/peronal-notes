---
title: Message Queues
status:
  - todo
created: 21-04-2025 11:31:35
updated: 21-04-2025 11:31:53
---

# Cola de mensajes (Productor / Consumidor)

🔖 **Tags**: #mensajería #asincronía #sistemas_distribuidos #desacoplamiento #resiliencia

---

## Questions?
- ¿Cuál es la diferencia entre una cola de mensajes y un bus de eventos?
- ¿Cómo se garantiza la entrega (at-least-once, at-most-once, exactly-once)?
- ¿Qué herramientas se usan comúnmente (RabbitMQ, Kafka, etc.)?

---

## 🧠 Main idea

Una **cola de mensajes** es un mecanismo de comunicación asíncrona que permite que un componente (productor) envíe mensajes a otro componente (consumidor) de forma desacoplada. El productor y el consumidor no necesitan estar disponibles al mismo tiempo ni conocerse directamente.

---

## 🧩 Context

Este patrón permite implementar sistemas más resilientes y escalables, donde los servicios pueden procesar mensajes a su propio ritmo, evitando sobrecargas y acoplamientos directos.

### Componentes:

- **Productor**: genera mensajes y los coloca en la cola.
- **Cola**: almacena los mensajes hasta que puedan ser consumidos.
- **Consumidor**: recupera mensajes de la cola y los procesa.

Este patrón es común en sistemas distribuidos para desacoplar servicios, manejar cargas variables y tolerar fallos temporales.

🔁 Ejemplo:

Un servicio de e-commerce genera un pedido y lo envía a una cola. Un servicio de facturación independiente consume ese mensaje y genera la factura de manera asíncrona, sin bloquear el flujo principal.

### Beneficios:

- Desacoplamiento temporal y espacial.
- Balanceo de carga entre múltiples consumidores.
- Resiliencia ante fallos (si un consumidor cae, el mensaje sigue en la cola).

---

## 🔗 Enlaces relacionados

- [[Flujos asíncronos]]
- [[Desacoplamiento en sistemas distribuidos]]
- [[Pub/Sub Pattern]]
- [[Resiliencia en sistemas distribuidos]]
- [[Kafka]]
- [[RabbitMQ]]

---

## 📘 Referencias

- *Designing Data-Intensive Applications* – Martin Kleppmann  
- Documentación oficial de RabbitMQ, Kafka  
- Apuntes de clase de Sistemas Distribuidos (semana 7)

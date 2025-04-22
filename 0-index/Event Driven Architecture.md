---
title: Arquitectura orientada a eventos (EDA)
status:
  - todo
created: 21-04-2025 12:22:53
updated: 21-04-2025 12:23:16
---

# Arquitectura orientada a eventos (EDA)

🔖 **Tags**: #arquitectura #eventos #sistemas_distribuidos #asincronía #pubsub

---

## Questions?
- ¿Cómo se modelan eventos de negocio relevantes para una arquitectura EDA?
- ¿Qué diferencias hay entre EDA y Pub/Sub?
- ¿Cuáles son las ventajas y riesgos de adoptar este estilo de arquitectura?

---

## 🧠 Main idea

La **arquitectura orientada a eventos (EDA)** es un estilo arquitectónico en el cual los componentes del sistema se comunican mediante la producción, consumo y reacción a **eventos**. Esta arquitectura promueve el **desacoplamiento**, la **escalabilidad** y la **resiliencia**, permitiendo flujos de trabajo flexibles y asincrónicos.

---

## 🧩 Context

En EDA, un **evento** representa un cambio significativo de estado en el sistema. Los componentes pueden actuar como:

- **Productores de eventos**: generan eventos cuando ocurre algo relevante.
- **Consumidores de eventos**: reaccionan a eventos para ejecutar lógica de negocio.
- **Brokers o buses de eventos**: intermedian la comunicación y desacoplan a productores de consumidores.

🔁 Ejemplo:

Un servicio de e-commerce emite un evento `OrdenCreada`. Distintos servicios reaccionan:

- **Inventario** reserva productos.
- **Facturación** genera la factura.
- **Notificaciones** envía un correo de confirmación.

Ninguno de estos servicios depende directamente del otro, sólo del evento.

---

## 🔗 Enlaces relacionados

- [Pub/Sub Pattern]
- [Flujos asíncronos]
- [Cola de mensajes (Productor / Consumidor)]
- [Saga Pattern]
- [Desacoplamiento en sistemas distribuidos]
- [Event Sourcing]
- [Consistencia eventual]

---

## 📘 Referencias

- *Designing Event-Driven Systems* – Ben Stopford  
- *Building Event-Driven Microservices* – Adam Bellemare  
- Apuntes de clase de Arquitectura de Software (semana 9)

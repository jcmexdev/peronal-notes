---
title: WebSocket
status:
  - todo
created: 20-04-2025 18:00:10
updated: 20-04-2025 19:42:16
---

# WebSocket

🔖 **Tags**: #WebSocket #RealTime #APIs #Networking

---

## 🧠 Main idea

Protocolo que crea un "túnel" de comunicación permanente entre cliente y servidor, permitiendo enviar y recibir datos en tiempo real sin recargar la página.

---

## 🧩 Context

- Reemplaza técnicas antiguas como "polling" (consultas repetidas al servidor).
- Funciona sobre el mismo puerto que HTTP (80) o HTTPS (443).
- Usado en aplicaciones como:
  - Chats (WhatsApp Web, Slack)
  - Juegos multijugador online
  - Actualizaciones de bolsa en tiempo real

---

## 🔍 Key Features

1. **Conexión persistente**: Una sola conexión que permanece abierta.
2. **Bidireccional**: Cliente y servidor pueden hablar al mismo tiempo.
3. **Menos datos que HTTP**: No envía headers repetidos en cada mensaje.

Ejemplo de URL: `ws://ejemplo.com/chat` (o `wss://` para versión segura).

---

## ⚖️ Pros vs. Cons

| ✅ Ventajas | ❌ Desventajas |
|-------------|---------------|
| Respuestas instantáneas | Gasta más batería en móviles |
| Ideal para apps interactivas | Complejo para configurar en servidores |
| Soporta cualquier tipo de dato | No todos los navegadores lo soportan igual |

---

## 🔗 Enlaces relacionados

- [[HTTP]]
- [[Protocolos de Comunicación Web]]
- [[Socket.IO]]

---

## 📘 Referencias

- Documentación oficial: [RFC 6455](https://tools.ietf.org/html/rfc6455)
- Guía MDN: [WebSocket API](https://developer.mozilla.org/es/docs/Web/API/WebSocket)
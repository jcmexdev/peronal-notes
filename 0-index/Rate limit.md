---
title: Rate Limiting
status:
  - todo
created: 21-04-2025 19:05:07
updated: 21-04-2025 19:05:10
---

# Rate Limiting

🔖 **Tags**: #traffic_management #resiliencia #sistemas_distribuidos #rendimiento

---

## Questions?
- ¿Cuál es la diferencia exacta entre rate limiting y throttling?
- ¿Cómo afecta al usuario final un mal diseño de rate limiting?
- ¿Qué herramientas existen para implementarlo fácilmente?

---

## 🧠 Main idea

**Rate Limiting** es una técnica usada para **limitar la cantidad de solicitudes** que un cliente puede hacer a un sistema en un determinado periodo de tiempo. Su objetivo es **proteger recursos compartidos** de sobrecargas, asegurar calidad de servicio y evitar abusos o ataques como DDoS.

---

## 🧩 Context

En sistemas distribuidos o APIs públicas, los servicios pueden verse abrumados por una alta frecuencia de solicitudes. El rate limiting actúa como una defensa que previene:

- Sobrecarga de servidores.
- Acaparamiento de recursos por un solo cliente.
- Saturación de conexiones de red.
- Costos innecesarios en la infraestructura.

Se implementa normalmente con reglas como:
- **100 requests por minuto por IP**
- **10 solicitudes por segundo por token de API**
- **1 solicitud por segundo para endpoints sensibles**

Existen estrategias como:
- Token Bucket
- Leaky Bucket
- Fixed Window
- Sliding Window

---

## 🔗 Enlaces relacionados

- [[Throttling]]
- [[Traffic Shaping]]
- [[Load Balancing]]
- [[API Gateway]]
- [[Service Mesh]]
- [[Traffic Management]]

---

## 📘 Referencias

- *Web API Design* – Apigee  
- Documentación de NGINX, Envoy, Kong, Istio  
- RFC 6585 - HTTP Status Code 429 "Too Many Requests"  
- Blog: *Rate Limiting Strategies and Techniques* – Cloudflare  

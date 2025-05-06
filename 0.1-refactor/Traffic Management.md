---
title: Traffic Management
status:
  - todo
created: 21-04-2025 17:25:15
updated: 21-04-2025 17:52:21
---

# Traffic Management

🔖 **Tags**: #observability #monitoring #traffic #architecture #resilience

---

## Questions?
- ¿Cómo decide un sistema hacia dónde enrutar el tráfico en tiempo real?
- ¿Qué diferencia hay entre throttling y rate limiting?
- ¿Qué herramientas modernas se usan para manejar el tráfico?

---

## 🧠 Main idea

**Traffic Management** se refiere al conjunto de estrategias, mecanismos y herramientas que controlan cómo se enrutan, regulan y distribuyen las solicitudes dentro de un sistema. Su objetivo es garantizar disponibilidad, rendimiento y resiliencia en entornos distribuidos o de alto tráfico.

---

## 🧩 Context

En arquitecturas modernas, especialmente en microservicios, el tráfico entre componentes puede crecer exponencialmente. La mala gestión de ese tráfico puede generar cuellos de botella, sobrecarga de servicios, fallos en cascada y mala experiencia de usuario.

Las principales técnicas utilizadas incluyen:

- **Load Balancing**: Distribuye solicitudes entre múltiples instancias de servicio para evitar sobrecargas.
- **Rate Limiting**: Limita la cantidad de solicitudes permitidas en un periodo de tiempo.
- **Throttling**: Ralentiza o bloquea tráfico excesivo para proteger servicios.
- **Traffic Shaping**: Define reglas personalizadas para enrutar tráfico (por cliente, versión, región, etc.).
- **Canary Releases y Blue/Green Deployments**: Permiten liberar versiones nuevas de forma controlada.
- **Service Mesh**: Herramientas como Istio o Linkerd ofrecen control granular sobre el tráfico entre servicios.
- **API Gateway**: Control de entrada de tráfico externo, aplicando políticas de seguridad, routing, y limitación.

---

## 🔗 Enlaces relacionados

- [[Rate Limiting]]
- [[Request Rate Monitoring (RPMs)]]
- [[API Gateway]]
- [[Service Mesh]]
- [[Fallback Pattern]]
- [[Circuit Breaker Pattern]]
- [[Canary Release]]
- [[Blue/Green Deployment]]

---

## 📘 Referencias

- *Microservices Patterns* – Chris Richardson  
- Documentación de Istio, Linkerd, Envoy  
- Documentación oficial de Kong, NGINX, AWS API Gateway  
- Apuntes de clase de Arquitectura Distribuida (semana 9)

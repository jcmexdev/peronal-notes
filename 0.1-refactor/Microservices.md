---
title: Microservicios
status:
  - en-progreso
created: 20-04-2025 19:50:12
updated: 20-04-2025 19:52:54
---

# Microservicios  

🔖 **Tags**: #microservices #arquitectura #distributed-systems #scalability  

---

## 🧠 Main idea  
Arquitectura que estructura una aplicación como un conjunto de **servicios pequeños**, autónomos y especializados en una única función de negocio, comunicándose mediante APIs.  

> *"Do one thing and do it well"* — Filosofía UNIX aplicada a servicios.  

---

## 🧩 Context  
- **Origen**: Popularizado por Amazon/Netflix (~2010) para escalar sus plataformas.  
- **Alternativas**: Monolitos (todo acoplado) vs. SOA (servicios más grandes).  
- **Caso típico**: Aplicaciones cloud-native con equipos Scrum independientes.  

---

## 🔍 Key Features  

### 1. Autonomía por servicio  
- Base de datos independiente ([[Polyglot Persistence]]).  
- Puede usar diferentes lenguajes (ej: Go + Python + Java).  

### 2. Comunicación descentralizada  
- REST/HTTP (síncrono).  
- Eventos (Kafka, RabbitMQ) para asincronía.  

### 3. Despliegue independiente  
- Contenedores ([[Docker]]) + Orquestadores ([[Kubernetes]]).  

---

## ⚖️ Pros vs. Cons  
| ✅ Ventajas | ❌ Desventajas |  
|------------|---------------|  
| Escalabilidad granular | Mayor complejidad operativa |  
| Mayor velocidad de desarrollo | Latencia en llamadas entre servicios |  
| Fault isolation (un fallo no colapsa todo) | Retos en consistencia de datos ([[CAP Theorem]]) |  

---

## 🌐 Casos de Uso Reales  
1. **Netflix**: Cada función (recomendaciones, pagos, streaming) es un microservicio.  
2. **Uber**: Servicios separados para viajes, geolocalización, notificaciones.  

---

## 🔗 Enlaces relacionados  
- [[Monolitos vs Microservicios - Comparativa]]  
- [[Domain-Driven Design (DDD)]]  
- [[Patrón Saga - Transacciones distribuidas]]  
- [[Service Mesh con Istio]]  

---

## 📘 Referencias  
- Libro: *"Building Microservices"* — Sam Newman (cap. 1-3).  
- [Martin Fowler: Microservices](https://martinfowler.com/articles/microservices.html)  
- [Azure Architecture Guide](https://learn.microsoft.com/en-us/azure/architecture/microservices/)  
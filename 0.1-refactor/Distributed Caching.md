---
title: Distributed Caching
status:
  - todo
created: 21-04-2025 20:00:56
updated: 21-04-2025 20:00:59
---

# Distributed Caching

🔖 **Tags**: #system_optimization #caching #performance #scalability

---

## Questions?
- ¿Cuándo es mejor usar caché local vs distribuida?
- ¿Qué problemas puede causar la invalidación en cachés distribuidas?
- ¿Qué herramientas son más comunes para implementar caching distribuido?

---

## 🧠 Main idea

**Distributed Caching** es una técnica de almacenamiento temporal de datos en múltiples nodos o servidores para acelerar el acceso a información frecuentemente solicitada en sistemas distribuidos. Ayuda a **reducir la carga de las bases de datos**, **disminuir la latencia** y **mejorar la escalabilidad**.

---

## 🧩 Context

En sistemas distribuidos o de alto tráfico, el uso de un solo caché local en cada instancia puede causar inconsistencias y redundancia. El **caché distribuido** soluciona esto al mantener los datos compartidos entre múltiples instancias, asegurando coherencia (eventual o fuerte) y eficiencia.

🔁 Ejemplo:
- Un sistema de e-commerce guarda el catálogo de productos en un caché distribuido (ej. Redis Cluster).
- Todas las instancias del backend acceden al mismo caché para recuperar los productos.
- Si un producto se actualiza, la entrada en caché se invalida o actualiza en todos los nodos.

---

## 🔧 Beneficios

- Menor latencia al evitar acceder a la base de datos repetidamente.
- Escalabilidad horizontal: múltiples instancias pueden acceder al mismo caché.
- Mayor disponibilidad si se configura con tolerancia a fallos.

---

## ⚠️ Desafíos

- **Coherencia de datos**: evitar datos obsoletos o inconsistentes.
- **Invalidación de caché**: decidir cuándo eliminar o actualizar datos.
- **Particionamiento de datos**: distribuir los datos eficientemente entre nodos.
- **Redundancia y replicación**: para tolerancia a fallos.

---

## 🔗 Enlaces relacionados

- [[Caching Strategies]]
- [[Load Balancing]]
- [[Eventual Consistency]]
- [[Scalability Patterns]]
- [[Redis]]
- [[Memcached]]

---

## 📘 Referencias

- *Designing Data-Intensive Applications* – Martin Kleppmann  
- Documentación oficial de Redis y Memcached  
- Apuntes de clase de Arquitectura de Software (semana 9)

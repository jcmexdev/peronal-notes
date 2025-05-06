---
title: REST (Representational State Transfer)
status:
  - todo
created: 20-04-2025 17:59:04
updated: 20-04-2025 18:10:13
---

# REST (Representational State Transfer)

🔖 **Tags**: #REST #arquitectura #API #comunicación

---

## 🧠 Main idea

REST es un estilo arquitectónico para diseñar servicios web, utilizando el protocolo HTTP para interactuar con recursos. Los recursos son identificados por URLs y las operaciones sobre estos recursos se realizan mediante los métodos estándar de HTTP (GET, POST, PUT, DELETE).

---

## 🧩 Context

REST permite la creación de APIs sencillas y escalables, donde los recursos (como datos o servicios) son accesibles a través de URLs. Al ser un estilo arquitectónico, REST no define un protocolo en sí mismo, sino que utiliza HTTP como protocolo de comunicación. Es sin estado, lo que significa que cada solicitud contiene toda la información necesaria para ser procesada, sin depender de solicitudes previas.

Principios clave de REST:
1. **Identificación de recursos**: Los recursos se identifican mediante URLs únicas.
2. **Operaciones estándar**: Se utilizan los métodos HTTP (GET, POST, PUT, DELETE) para manipular los recursos.
3. **Sin estado**: Cada solicitud es independiente y debe contener toda la información necesaria.
4. **Representación**: Los recursos pueden tener múltiples representaciones, como JSON o XML.

---

## 🔗 Enlaces relacionados


---

## 📘 Referencias

- *RESTful Web Services* - Leonard Richardson, Sam Ruby
- *Building Microservices* - Sam Newman

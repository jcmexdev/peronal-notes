---
title: gRPC
status:
  - done
created: 20-04-2025 18:00:40
updated: 20-04-2025 19:46:15
---

# gRPC: Framework RPC moderno

🔖 **Tags**: #gRPC #Microservicios #APIs #RPC #ProtocolBuffers

---

## 🧠 Main idea

gRPC es un **framework de llamada a procedimiento remoto (RPC)** de alto rendimiento desarrollado por Google. Utiliza **Protocol Buffers** como lenguaje de definición de interfaces y HTTP/2 como transporte.

---

## 🧩 Context

- Nace en 2016 como evolución del RPC tradicional
- Ideal para:
  - Comunicación entre microservicios
  - Sistemas distribuidos
  - Conexiones móvil-servidor
- Alternativa eficiente a REST/JSON para ciertos escenarios

---

## 🔍 Key Features

1. **Protocol Buffers**:
   - Definición de servicios en archivos `.proto`
   - Serialización binaria eficiente
   - Generación automática de código

2. **HTTP/2**:
   - Multiplexación de conexiones
   - Streams bidireccionales
   - Compresión de headers

3. **Multiplataforma**:
   - Soporte para 10+ lenguajes
   - Interoperabilidad entre sistemas heterogéneos

---

## ⚖️ Pros vs. Cons

| ✅ Ventajas | ❌ Desventajas |
|-------------|---------------|
| Alto rendimiento | Curva de aprendizaje |
| Tipado fuerte | Debugging más complejo |
| Streaming nativo | Soporte limitado en navegadores |
| Generación de código | Menor adopción que REST |

---

## 🔗 Enlaces relacionados

- [[Protocol Buffers]]
- [[HTTP/2]]

---

## 📘 Referencias

- [Documentación oficial gRPC](https://grpc.io/)
- Libro: "gRPC: Up and Running" - Kasun Indrasiri
- [Google Cloud gRPC Guide](https://cloud.google.com/blog/products/api-management/understanding-grpc-openapi-and-rest-and-when-to-use-them)
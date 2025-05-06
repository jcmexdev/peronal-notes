---
title: Throttling
status:
  - todo
created: 21-04-2025 19:51:10
updated: 21-04-2025 19:51:17
---

# Throttling

🔖 **Tags**: #traffic_management #rendimiento #resiliencia #sistemas_distribuidos

---

## Questions?
- ¿En qué se diferencia exactamente de rate limiting?
- ¿Qué técnicas se usan para implementar throttling?
- ¿Puede aplicarse también del lado del cliente?

---

## 🧠 Main idea

**Throttling** es una técnica para **controlar dinámicamente la velocidad de procesamiento o respuesta** de un sistema cuando detecta que la carga comienza a superar ciertos umbrales. En lugar de rechazar directamente las solicitudes como hace el rate limiting, el throttling puede **ralentizar, pausar o encolar** las peticiones.

---

## 🧩 Context

En sistemas distribuidos o APIs, hay momentos en que una carga alta no debe provocar errores, sino tratarse con **tolerancia**. El throttling se usa para:

- **Proteger recursos compartidos** (por ejemplo, base de datos, servicios externos).
- **Evitar picos de carga abruptos**.
- **Degradar el servicio de forma controlada**.
- Dar tiempo a los servicios a que se recuperen o escalen.

### Diferencias con Rate Limiting:
| Concepto          | Rate Limiting                         | Throttling                          |
|-------------------|----------------------------------------|-------------------------------------|
| Acción            | Rechaza o bloquea solicitudes excedidas | Ralentiza o difiere solicitudes     |
| Enfoque           | Preventivo                            | Reactivo                            |
| Usuario afectado  | Recibe error (429)                    | Puede recibir retrasos, no error    |

---

## 🔗 Enlaces relacionados

- [[Rate Limiting]]
- [[Traffic Management]]
- [[Traffic Shaping]]
- [[Service Mesh]]
- [[API Gateway]]
- [[Load Balancing]]

---

## 📘 Referencias

- Documentación de AWS API Gateway  
- *Mastering API Architecture* – James Higginbotham  
- Blog: *Rate Limiting vs Throttling* – KongHQ  
- Experiencias en producción con Netflix Zuul e Istio  

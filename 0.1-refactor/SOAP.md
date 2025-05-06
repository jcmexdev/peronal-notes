---
title: SOAP (Simple Object Access Protocol)
status:
  - todo
created: 20-04-2025 17:59:53
updated: 20-04-2025 21:50:30
---

# SOAP (Simple Object Access Protocol)

🔖 **Tags**: #SOAP #WebServices #APIs #XML 

---

## 🧠 Main idea

SOAP es un protocolo de comunicación basado en **XML** para intercambiar información estructurada en servicios web. Opera sobre protocolos como HTTP, SMTP o TCP, y se caracteriza por su **estandarización estricta** y capacidades avanzadas de seguridad (WS-Security).

---

## 🧩 Context

- Utilizado principalmente en entornos empresariales (banca, salud, ERP).
- Requiere un contrato definido en [[WSDL]] para describir los servicios.
- Alternativa a arquitecturas más ligeras como [[REST]].

Ejemplo típico: Integración entre sistemas legacy (ej. SAP con aplicaciones modernas).

---

## 🔍 Key Features

1. **Estructura XML**:
   ```xml
   <soap:Envelope>
     <soap:Header>
       <!-- Metadatos (ej. autenticación) -->
     </soap:Header>
     <soap:Body>
       <!-- Contenido principal -->
     </soap:Body>
   </soap:Envelope>
   ```
2. **WS-* Standards**: Soporta extensiones como WS-Security y WS-Addressing.
3. **Independiente de lenguaje**: Compatible con Java, .NET, Python, etc.

---

## ⚖️ Pros vs. Cons

| ✅ Ventajas | ❌ Desventajas |
|-------------|---------------|
| Seguridad integrada | Alto overhead por XML |
| Ideal para sistemas complejos | Curva de aprendizaje pronunciada |
| Soporte transaccional | Requiere herramientas especializadas |

---

## 🔗 Enlaces relacionados

- [[WSDL - Contratos para servicios web]]
- [[XML]]

---

## 📘 Referencias

- Libro: *Web Services Essentials* - Ethan Cerami  
- [Especificación SOAP 1.2 (W3C)](https://www.w3.org/TR/soap12/)  
- [MDN - SOAP](https://developer.mozilla.org/es/docs/Web/API/SOAP_API)  
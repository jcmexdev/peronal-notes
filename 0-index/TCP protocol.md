---
title: Untitled
date: 17 de April de 2025
tags:
  - Concept
status:
  - todo
level:
  - intermediate
related: []
source:
---

# Diferencia entre TCP y UDP (en contexto de DNS)

## ¿Qué significa que UDP no requiere conexión previa?

Cuando se dice que **UDP no necesita conexión previa**, significa que **envía los datos directamente sin negociar ni verificar antes si el receptor está listo**.

---

## Comparación entre TCP y UDP

### TCP (requiere conexión previa)
```mermaid
sequenceDiagram
    participant Cliente
    participant Servidor

    Cliente->>Servidor: SYN
    Servidor->>Cliente: SYN-ACK
    Cliente->>Servidor: ACK
    Note right of Cliente: Conexión establecida
    Cliente->>Servidor: Envía datos
```
### UDP (sin conexión)


```mermaid
sequenceDiagram
    participant Cliente
    participant Servidor

    Cliente->>Servidor: Envía mensaje (sin handshake)
    Note right of Cliente: No hay confirmación ni control
```

---

## Ejemplo cotidiano

- **TCP**: Como hacer una llamada telefónica (esperar a que contesten)
    
- **UDP**: Como gritar algo por la ventana (esperar que alguien escuche)
    

---

## En el caso de DNS

DNS **usa UDP por defecto** porque:

- Es más rápido
    
- Las respuestas suelen ser pequeñas
    

### Consulta DNS por UDP:

```mermaid
sequenceDiagram
    participant Cliente
    participant Servidor DNS

    Cliente->>Servidor DNS: Consulta DNS (UDP)
    Servidor DNS-->>Cliente: Respuesta DNS (UDP)
```

---

## Casos en que DNS usa TCP

1. Respuestas muy grandes (más de 512 bytes)
    
2. Transferencia de zonas DNS (entre servidores)
    

### Consulta DNS por TCP:

```mermaid
sequenceDiagram
    participant Cliente
    participant Servidor DNS

    Cliente->>Servidor DNS: SYN
    Servidor DNS->>Cliente: SYN-ACK
    Cliente->>Servidor DNS: ACK
    Note right of Cliente: Conexión establecida
    Cliente->>Servidor DNS: Consulta DNS (TCP)
    Servidor DNS-->>Cliente: Respuesta DNS (TCP)
```
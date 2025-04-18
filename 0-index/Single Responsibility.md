---
title: Untitled
date: 18 de April de 2025
tags: ["Design System", "Algorithms", "Concept"]
status: ["todo"]   # opciones: pendiente | en progreso | revisar | aprendido | actualizar | archivado
level: ["basic"]       # opciones: básico | intermedio | avanzado
related: ["Related Topic"]
source: ["Física Universitaria"]
---

Parent: [[S.O.L.I.D]]
## Summary
Brief overview of the topic. What is it? What is it used for? Where is it applied?

---
## SRP - Single Responsibility Principle

**Definición**: Una clase debe tener una, y solo una, razón para cambiar.

Motivación:
- Facilita mantenimiento.
- Reduce acoplamiento.
- Mejora testeo.

Ejemplo violación SRP:
Clase `Report` que calcula, guarda y muestra datos.

Solución SRP:
Separar en:
- `Report`
- `ReportSaver`
- `ReportPrinter`

Regla mental:
> "¿Cuántos actores diferentes podrían pedir cambios a esta clase?"

### Ejemplo de una clase en php
```php
<?php

class Invoice {
    public function calculateTotal() {
        // Lógica para calcular el total de la factura
        return 100;
    }

    public function saveToDatabase() {
        // Lógica para guardar la factura en la base de datos
        echo "Guardando en la base de datos...\n";
    }

    public function sendEmail() {
        // Lógica para enviar la factura por correo
        echo "Enviando email al cliente...\n";
    }
}
```
Ahora con SRP
```php
<?php

class Invoice {
    public function calculateTotal() {
        // Lógica para calcular el total de la factura
        return 100;
    }
}

class InvoiceRepository {
    public function save(Invoice $invoice) {
        // Lógica para guardar la factura en la base de datos
        echo "Guardando factura en la base de datos...\n";
    }
}

class InvoiceMailer {
    public function send(Invoice $invoice) {
        // Lógica para enviar la factura por correo
        echo "Enviando la factura por email...\n";
    }
}

```

# 🍫 Metáforas de Alfajores - SRP y OCP (Principios SOLID)

## 🧩 SRP - Single Responsibility Principle

> Una clase/pieza de código debe tener **una sola responsabilidad**.

### 🧁 Metáfora: "Un chef, una tarea"

Imaginá una fábrica de alfajores donde **un solo trabajador**:

- Amasa la masa  
- Cocina el dulce de leche  
- Baña el alfajor  
- Lo envuelve  
- Y atiende el teléfono...

🛑 ¡Un caos! Ese trabajador tiene muchas responsabilidades y si falla en una, **se rompe todo el proceso**.

✅ Aplicando SRP:
- Un chef hace la masa
- Otro pone el dulce
- Otro baña en chocolate
- Otro lo envuelve

Cada uno tiene **una sola tarea clara**, y si querés cambiar el dulce de leche por Nutella, solo modificás el paso correspondiente.

👉 **SRP = un alfajor, una tarea por persona.**

---

## 🧩 OCP - Open/Closed Principle

> El código debe estar **abierto para extensión**, pero **cerrado para modificación**.

### 🧁 Metáfora: "Máquina de alfajores modular"

Ya hacés el clásico alfajor de dulce de leche con chocolate negro.  
Ahora querés agregar:

- Alfajor de fruta  
- Alfajor de mousse  
- Alfajor vegano  

🛑 Si tenés que **modificar toda la máquina original** cada vez, es un lío. Pod
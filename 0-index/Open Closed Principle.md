---
title: open closed principle
date: 17 de April de 2025
tags: ["Design Patterns", "Concept"]
status: ["todo"]   # opciones: pendiente | en progreso | revisar | aprendido | actualizar | archivado
level: ["basic"]       # opciones: básico | intermedio | avanzado
related: [""]
source: [""]
---

Parent: [[S.O.L.I.D]]
## OCP - Open/Closed Principle

Definición:
El software debe estar:
- ✅ Abierto para extensión.
- 🚫 Cerrado para modificación.

Motivación:
- Evitar romper lo existente.
- Permitir escalabilidad limpia.
- Hacer más fácil mantener el código.

**Ejemplo Violación**:
Clase `PaymentProcessor` con `if` para cada tipo de pago.
```php
class PaymentProcessor {
    public function process($type) {
        if ($type === 'paypal') {
            echo "Procesando con PayPal...\n";
        } elseif ($type === 'stripe') {
            echo "Procesando con Stripe...\n";
        }
    }
}

```


**Ejemplo Correcto**:
Usar `PaymentMethod` interface + clases específicas (`Paypal`, `Stripe`, etc.)
```php
interface PaymentMethod {
    public function pay();
}

class PaypalPayment implements PaymentMethod {
    public function pay() {
        echo "Procesando con PayPal...\n";
    }
}

class StripePayment implements PaymentMethod {
    public function pay() {
        echo "Procesando con Stripe...\n";
    }
}

class PaymentProcessor {
    public function process(PaymentMethod $method) {
        $method->pay();
    }
}
```

**Regla mental**:
> "¿Puedo agregar nueva lógica sin modificar el código viejo?"

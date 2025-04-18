---
title: Untitled
date: 18 de April de 2025
tags: ["Design System", "Algorithms", "Concept"]
status: ["todo"]   # opciones: pendiente | en progreso | revisar | aprendido | actualizar | archivado
level: ["basic"]       # opciones: básico | intermedio | avanzado
related:
source: ["Física Universitaria"]
---
Parent: [[S.O.L.I.D]]
La **Interface Segregation Principle (ISP)** es uno de los más útiles para mantener tu código limpio y modular, sobre todo cuando trabajás con **interfaces grandes o sistemas con muchas dependencias**.

---

# 🧩 Interface Segregation Principle (ISP)

## 📖 Definición

> **"Ningún cliente debe estar obligado a depender de interfaces que no utiliza."**  
> — Robert C. Martin

---

## 🧠 ¿Qué significa?

Una **interfaz debe ser pequeña y específica** para su propósito.

- Si una clase **implementa una interfaz**, **no debería verse forzada** a definir métodos que **no necesita**.
    
- Las **interfaces grandes y genéricas** son dañinas: obligan a las clases a tener comportamientos que no les corresponden.
    

---

## 📌 Ejemplo clásico en PHP (violación del ISP)

```php
interface Trabajador {
    public function trabajar();
    public function comer();
}

class Humano implements Trabajador {
    public function trabajar() {
        echo "Trabajando...\n";
    }

    public function comer() {
        echo "Comiendo...\n";
    }
}

class Robot implements Trabajador {
    public function trabajar() {
        echo "Ejecutando tareas...\n";
    }

    public function comer() {
        // ❌ Violación: los robots no comen
        throw new Exception("No como, soy un robot.");
    }
}
```

🛑 El `Robot` se ve **forzado a implementar** un método que **no tiene sentido para él**.

---

## ✔️ Solución aplicando ISP

Separás las responsabilidades en interfaces **más pequeñas y coherentes**:

```php
interface Trabajador {
    public function trabajar();
}

interface Comedor {
    public function comer();
}

class Humano implements Trabajador, Comedor {
    public function trabajar() {
        echo "Trabajando...\n";
    }

    public function comer() {
        echo "Comiendo...\n";
    }
}

class Robot implements Trabajador {
    public function trabajar() {
        echo "Ejecutando tareas...\n";
    }
}
```

✅ Ahora cada clase implementa **solo lo que realmente necesita**.  
El `Robot` **ya no depende de métodos irrelevantes** como `comer`.

---

## 🧱 Ventajas de aplicar ISP

- Las clases quedan **más enfocadas y coherentes**.
    
- El código es **más mantenible** y más **fácil de testear**.
    
- Podés **reusar interfaces pequeñas** sin arrastrar métodos innecesarios.
    
- Evitás errores por implementación de métodos que **no tienen lógica en el contexto**.
    

---

## ⚠️ Síntomas de violación

- Interfaces con muchos métodos (más de 4–5) que **no siempre aplican a todos los que las implementan**.
    
- Clases que **implementan métodos vacíos o con `throw`**.
    
- Cambios en la interfaz que **afectan innecesariamente a clases que no deberían cambiar**.
    

---

## 🧠 Regla mental

> "Dividí las interfaces grandes en varias más pequeñas y específicas.  
> Cada clase debería implementar **solo las que realmente le hacen sentido**."

---

## 📋 Resumen listo para Obsidian

```markdown
## 🧩 Interface Segregation Principle (ISP)

**Definición**:  
Ningún cliente debe depender de métodos que no utiliza.  
Las interfaces deben ser pequeñas, específicas y enfocadas.

---

### 🛑 Violación

Cuando una clase está obligada a implementar métodos que no necesita, como:

- Métodos vacíos
- Métodos con `throw`
- Métodos que no tienen lógica válida para esa clase

---

### ✔️ Aplicación correcta

Dividir una interfaz grande en varias interfaces pequeñas, especializadas por comportamiento:

- `Trabajador` → métodos relacionados a trabajo
- `Comedor` → métodos relacionados a alimentación
- `Imprimible`, `Persistible`, `Serializable`, etc.

---

### ✅ Beneficios

- Clases más limpias y coherentes
- Menor acoplamiento
- Cambios localizados (no afectan otras clases innecesariamente)
- Mejor capacidad de testeo

---

### 🧠 Regla clave

> "Más vale muchas interfaces chicas que una que lo haga todo."

```

---

¿Querés que pasemos al último principio (**Dependency Inversion Principle**) o querés ver algún ejemplo en un contexto más real (como un sistema de e-commerce, auth, o similar)?
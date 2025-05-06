---
title: Liskov Substitution Principle
status:
  - todo
level:
  - basic
created: 18-04-2025 00:17:48
updated: 19-04-2025 13:22:50
---

## 🧩 Liskov Substitution Principle (LSP)

**Definición**:  
Las subclases deben poder reemplazar a sus clases padre sin alterar el comportamiento del programa.

---

### 🔥 ¿Qué rompe LSP?

- Sobrescribir métodos con lógica distinta o más restrictiva.
- Cambiar reglas de negocio del padre.
- Lanzar errores inesperados.
- Cambiar efectos secundarios esperados.

---

### ✔️ Buenas prácticas

- Usar interfaces si hay comportamientos diferentes.
- Usar composición en lugar de herencia cuando no hay una verdadera relación "es-un".
- Diseñar clases base con contratos generales y estables.
- Escribir tests que verifiquen que las subclases se pueden usar sin romper expectativas.

---

### ✅ Regla clave

> **"Si un objeto de tipo hijo no puede ser usado como si fuera del tipo padre, entonces algo está mal con esa herencia."**


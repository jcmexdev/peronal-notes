---
title: IoC (inversion of control)
date: 16 de April de 2025
status:
  - todo
level:
  - basic
created: 16-04-2025 21:38:52
updated: 19-04-2025 13:22:36
---


## Summary
Brief overview of the topic. What is it? What is it used for? Where is it applied?
---

## Key Concepts
- Key point 1
- Key point 2
- Brief definition or highlighted formula

---

## ¿Qué es?

**Inversión de Control (IoC)** es un principio de diseño que consiste en **delegar el control del flujo de ejecución o la creación de dependencias** a un contenedor o framework externo.

En lugar de que tu código cree y administre sus propios objetos, otra entidad (como un framework) se encarga de eso.

> Es una forma de desacoplar tu aplicación de los detalles de bajo nivel (por ejemplo, cómo se crean los objetos).
---

## 🎯 ¿Para qué sirve?

- Facilita el desacoplamiento entre componentes.
- Mejora la mantenibilidad del código.
- Permite la inyección de dependencias, que simplifica pruebas unitarias y reutilización.
- Favorece la modularidad y el crecimiento escalable de la aplicación.
- Separa claramente el qué hace una clase del cómo obtiene lo que necesita.
La forma mas común para aplicar el concepto de IoC es por medio de [[Dependency Injection]]

---

## 💡 Ejemplo simple (sin IoC)

```typescript
const logger = new ConsoleLogger();
const service = new UserService(logger);
---

## Code (if applicable)

```language
// Example code
function ohm(V, R) {
  return V / R;
}
```

_Explanation of what it does and why._

---
### Trade offs

## Example

Describe a solved case or real-world application.

---

## Observations / Personal Notes

- Concepts that are hard to understand
    
- Analogies that helped
    
- Questions to resolve
    

---

## References
   
- https://hackernoon.com/beginners-guide-to-inversion-of-control
---
title: Technical Debt: Good vs Bad
status:
  - todo
---

# Technical Debt: Good vs Bad

🔖 **Tags**: #software_architecture #code_quality #technical_debt #software_design

---

## Questions?
- ¿Cómo se identifica si una deuda técnica es buena o mala?
- ¿Qué criterios se usan para decidir cuándo asumir deuda técnica intencional?
- ¿Cómo priorizar la reducción de deuda técnica?

---

## 🧠 Main idea

La **deuda técnica** representa las decisiones de desarrollo que priorizan la entrega rápida sobre una solución óptima, generando una "deuda" que debe pagarse más adelante mediante refactorización o mejoras. No toda deuda técnica es negativa: se distingue entre **deuda técnica buena** (intencional y controlada) y **deuda técnica mala** (no intencional y descuidada).

---

## 🧩 Context

La metáfora de la deuda técnica fue acuñada por Ward Cunningham. Al igual que una deuda financiera, permite avanzar rápido a corto plazo, pero debe ser pagada más tarde con intereses en forma de mayor complejidad, errores, o lentitud en el desarrollo.

### ✅ **Deuda Técnica Buena**
- Es **intencional**: se toma con un plan claro de pago o refactorización posterior.
- Ocurre en situaciones estratégicas: *“necesitamos salir al mercado ya con la versión funcional”*.
- Está **documentada y visibilizada**.
- Se asume con consciencia de sus impactos.
- Ejemplo: “Vamos a usar esta solución temporal para el MVP y luego la reemplazamos con algo escalable en el sprint 5.”

### ❌ **Deuda Técnica Mala**
- Es **accidental o negligente**.
- Proviene de malas prácticas, falta de revisión, o presión sin planeación.
- Suele ignorarse o crecer sin control.
- Dificulta el mantenimiento y evolución del sistema.
- Ejemplo: código duplicado, sin pruebas, sin documentación, acoplamientos innecesarios.

---

## 🔗 Enlaces relacionados

- [[Refactorización continua]]
- [[Code Smells]]
- [[Arquitectura evolutiva]]
- [[Gestión del ciclo de vida del software]]
- [[Decisiones arquitectónicas con trade-offs]]

---

## 📘 Referencias

- *Clean Code* – Robert C. Martin  
- *The Pragmatic Programmer* – Andy Hunt, Dave Thomas  
- Charla original de Ward Cunningham sobre Technical Debt  
- Blog de Martin Fowler: [Technical Debt Quadrant](https://martinfowler.com/bliki/TechnicalDebtQuadrant.html)

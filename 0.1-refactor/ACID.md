---
title: ACID
status:
  - todo
created: 21-04-2025 03:32:38
updated: 21-04-2025 03:35:04
---

# ACID (Atomicidad, Consistencia, Aislamiento, Durabilidad)

🔖 **Tags**: #bases_de_datos #transacciones #conceptos #sistemas_distribuidos

---

## Questions?
- ¿Cómo se implementan estas propiedades en bases de datos distribuidas?
- ¿En qué casos se relaja la consistencia o el aislamiento por motivos de rendimiento?
- ¿Cómo se compara ACID con BASE?

---

## 🧠 Main idea

**ACID** es un conjunto de propiedades que garantizan que las transacciones en una base de datos se procesen de manera confiable. Estas propiedades aseguran que los datos permanezcan consistentes incluso en caso de errores, fallos o accesos concurrentes.

---

## 🧩 Context

ACID es un acrónimo que representa cuatro propiedades fundamentales:

- **Atomicidad (Atomicity)**: Todas las operaciones dentro de una transacción se completan o ninguna lo hace. Ver también: [[Atomic Transactions]].
- **Consistencia (Consistency)**: La base de datos pasa de un estado válido a otro estado válido. Las reglas de integridad siempre se respetan.
- **Aislamiento (Isolation)**: Las transacciones concurrentes no interfieren entre sí. Cada una actúa como si fuera la única en ejecución.
- **Durabilidad (Durability)**: Una vez confirmada una transacción, sus efectos persisten incluso ante fallos del sistema.

Estas propiedades son esenciales para sistemas críticos como procesamiento de pagos, inventarios o cualquier operación sensible a errores.

En entornos distribuidos, mantener las propiedades ACID completas puede ser costoso o incluso inviable. Por eso, se recurre a patrones como [[Two-Phase Commit (2PC)]] o [[Saga Pattern]] para lograr un comportamiento transaccional que sea escalable y tolerante a fallos.

---

## 🔗 Enlaces relacionados


---

## 📘 Referencias

- *Designing Data-Intensive Applications* – Martin Kleppmann  
- *Database System Concepts* – Abraham Silberschatz  
- Apuntes de clase de Bases de Datos (semana 6)

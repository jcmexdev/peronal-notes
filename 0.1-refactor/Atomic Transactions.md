---
title: Transacciones Atómicas
status:
  - todo
created: 21-04-2025 03:27:01
updated: 21-04-2025 03:27:27
---

# Transacciones Atómicas

🔖 **Tags**: #sistemas_distribuidos #bases_de_datos #atomicidad #transacciones

---

## Questions?
- ¿Cuál es la diferencia entre una transacción atómica y una transacción distribuida?
- ¿Qué papel juega el aislamiento en la atomicidad?
- ¿Cómo se implementa atomicidad en sistemas que no tienen bases de datos tradicionales?

---

## 🧠 Main idea

Una **transacción atómica** es una operación o conjunto de operaciones que se ejecutan como una sola unidad indivisible: o todas se ejecutan correctamente, o ninguna se ejecuta. Es uno de los principios fundamentales del modelo **ACID**.

---

## 🧩 Context

La atomicidad es crucial en sistemas donde la integridad de los datos es importante, como en sistemas bancarios, procesamiento de pagos o cualquier sistema donde una operación incompleta pueda dejar los datos en un estado inconsistente.

Una transacción atómica garantiza que:
- Si ocurre un fallo (como caída de red, excepción en la lógica de negocio, etc.), todas las operaciones realizadas dentro de esa transacción se revierten (rollback).
- Si todo sale bien, los cambios se confirman (commit).

Esto se logra típicamente mediante un sistema de gestión de transacciones (como los manejadores de bases de datos) que utiliza logs de transacción para restaurar el sistema a un estado consistente si hay fallos.

En sistemas distribuidos, lograr atomicidad completa requiere coordinadores especiales como el **Two-Phase Commit (2PC)**, aunque esto puede ser costoso en términos de rendimiento. Como alternativa, se utilizan patrones como **Saga** para simular la atomicidad de manera más flexible y asíncrona.

---

## 🔗 Enlaces relacionados



---

## 📘 Referencias

- *Designing Data-Intensive Applications* – Martin Kleppmann  
- *Distributed Systems* – Maarten van Steen, Andrew S. Tanenbaum  
- Apuntes de clase de Bases de Datos (semana 7)

---
created: 18-04-2025 00:41:14
updated: 18-04-2025 00:41:17
---
## 💧 DRY — Don't Repeat Yourself

**Definición**:  
Cada pieza de conocimiento debe existir una única vez en el sistema.

---

### 🛑 Violaciones comunes

- Cálculos duplicados (ej: precios, impuestos)
- Validaciones repetidas
- Misma lógica en varios lugares (controladores, servicios)
- Queries SQL repetidas

---

### ✔️ Aplicación correcta

- Extraer métodos reutilizables
- Usar constantes, funciones o helpers
- Centralizar lógica en servicios o utilidades

---

### 🧠 Reglas clave

- "No repitas código. Reusalo."
- "Si algo cambia, debería cambiar en un solo lugar."
- "Duplica hasta que duela. Después, abstraé."

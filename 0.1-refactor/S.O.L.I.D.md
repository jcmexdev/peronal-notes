---
title: S.O.L.I.D
status:
  - todo
level:
  - basic
created: 17-04-2025 17:25:22
updated: 26-04-2025 17:20:41
---

##  Key Concepts
- [[Single Responsibility]]
- [[Open Closed Principle]]
- [[Liskov Substitution Principle]]
- [[Interface Segregation Principle]]
- [[Dependency Inversion Principle]]

¡Perfecto! Acá va la **metáfora de los alfajores** completa para entender los principios SOLID como si fueran una **fábrica de alfajores en Argentina** 🇦🇷✨

---

# 🧁 SOLID explicado con alfajores

Imaginemos que estás diseñando una **fábrica de alfajores**.  
Tu objetivo: producir muchos tipos de alfajores (dulce de leche, mousse, triple, sin TACC…) y que todo funcione bien a medida que el negocio crece. Para eso aplicás los **principios SOLID**.

---

## 🅢 — **Single Responsibility Principle (SRP)**

🧠 _Una clase debe tener una única responsabilidad._

🔧 En la fábrica:  
Tenés una máquina que **solo hornea tapas**, otra que **solo rellena**, y otra que **solo baña en chocolate**.

❌ Si una sola máquina hiciera todo, sería difícil de mantener y reparar.  
✅ Al separar responsabilidades, podés cambiar el chocolate o el relleno sin romper todo lo demás.

---

## 🅞 — **Open/Closed Principle (OCP)**

🧠 _El código debe estar abierto a la extensión, pero cerrado a la modificación._

🍫 En la fábrica:  
Ya tenés un proceso para hacer alfajores de dulce de leche.  
Ahora querés agregar uno de mousse sin cambiar las máquinas existentes.

✅ Entonces diseñás un sistema donde podés **agregar nuevos tipos de relleno** como "plugins", sin tocar lo que ya funciona.  
Tu línea de producción **se extiende** sin romper lo anterior.

---

## 🅛 — **Liskov Substitution Principle (LSP)**

🧠 _Las subclases deben poder reemplazar a las clases base sin alterar el funcionamiento del sistema._

🥄 En la fábrica:  
Tenés una línea de producción que espera cualquier tipo de "Relleno".  
Si reemplazás "Dulce de leche" por "Mousse", todo debería seguir funcionando.

❌ Pero si metés "Aire comprimido" como relleno (que no se puede envasar), **se rompe la cadena**.

✅ LSP dice: si tu sistema espera "relleno", **cualquier tipo de relleno debe funcionar igual de bien**, sin sorpresas.

---

## 🅘 — **Interface Segregation Principle (ISP)**

🧠 _No forzar a las clases a implementar métodos que no usan._

🥇 En la fábrica:  
Algunas máquinas solo **hornean**, otras solo **bañan con chocolate**.

❌ Si tu interfaz dice `preparar()`, `hornear()`, `bañar()`, `empaquetar()`, estás obligando a todas las máquinas a hacer todo.  
Una máquina de hornear no necesita empaquetar.

✅ Entonces creás **interfaces pequeñas y específicas**, como `Horneable`, `Bañable`, `Empaquetable`, y cada máquina implementa solo lo que usa.

---

## 🅓 — **Dependency Inversion Principle (DIP)**

🧠 _Los módulos de alto nivel no deben depender de módulos de bajo nivel, sino de abstracciones._

📦 En la fábrica:  
Tu máquina de empaquetado no debería depender directamente de “Caja de cartón N°45”.

✅ En vez de eso, depende de una interfaz como `Empaquetador`, y luego vos decidís si usás caja, bolsa, o envoltorio especial según el producto.

🔁 Eso te permite **cambiar fácilmente la presentación del alfajor** sin tener que reescribir toda la máquina.

---

## 🧠 Resumen general

Tu **fábrica de alfajores** funciona perfecto porque:

- 🔧 Cada máquina hace una sola cosa (SRP)
    
- 🧩 Podés agregar nuevos alfajores sin tocar los existentes (OCP)
    
- ✅ Todos los rellenos se comportan igual (LSP)
    
- 🔄 Cada máquina implementa solo lo que necesita (ISP)
    
- ♻️ Las máquinas dependen de contratos genéricos, no de detalles específicos (DIP)
    

---

¿Querés que te lo arme en formato `.md` directo para copiar/pegar a Obsidian?
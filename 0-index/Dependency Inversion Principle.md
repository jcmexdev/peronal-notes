---
title: Untitled
status:
  - todo
level:
  - basic
created: 18-04-2025 00:29:02
updated: 19-04-2025 13:21:31
---

¡Vamos con la última pieza del rompecabezas!  
La **D** es uno de los pilares más importantes para lograr **bajo acoplamiento y alta flexibilidad** en sistemas bien diseñados.

---

# 🧩 Dependency Inversion Principle (DIP)

---

## 📖 Definición

> **"Los módulos de alto nivel no deben depender de módulos de bajo nivel. Ambos deben depender de abstracciones."**  
> **"Las abstracciones no deben depender de los detalles. Los detalles deben depender de las abstracciones."**  
> — Robert C. Martin

---

## 🧠 ¿Qué significa en la práctica?

Significa que:

- No deberías acoplar directamente tu lógica de negocio a detalles concretos como clases, bases de datos, controladores HTTP, etc.
    
- En lugar de eso, **ambos deben depender de interfaces (abstracciones)** que definan el comportamiento necesario.
    

---

## 📌 ¿Por qué es importante?

Si un módulo de alto nivel (por ejemplo, un **servicio**) depende directamente de detalles de implementación (como una **clase concreta de base de datos**), tu sistema se vuelve **frágil y difícil de mantener o testear**.

Con DIP, podés:

- Reemplazar implementaciones fácilmente (ej: cambiar de MySQL a PostgreSQL).
    
- Hacer tests sin dependencias reales (mockear).
    
- Reusar la lógica en otros contextos.
    

---

## ❌ Ejemplo que **viola DIP** (PHP)

```php
class MySQLUserRepository {
    public function getUserById($id) {
        // Lógica con consultas SQL directas...
    }
}

class UserService {
    private $repo;

    public function __construct() {
        $this->repo = new MySQLUserRepository(); // ❌
    }

    public function getUser($id) {
        return $this->repo->getUserById($id);
    }
}
```

🔴 `UserService` depende **directamente** de una implementación concreta (`MySQLUserRepository`).  
No podés cambiarla, no podés testearla sin base de datos.

---

## ✔️ Aplicando DIP correctamente

Separás la **abstracción (interface)** de la **implementación**, y hacés que ambas dependan de la interfaz:

```php
interface UserRepository {
    public function getUserById($id);
}

class MySQLUserRepository implements UserRepository {
    public function getUserById($id) {
        // Lógica SQL
    }
}

class UserService {
    private UserRepository $repo;

    public function __construct(UserRepository $repo) {
        $this->repo = $repo;
    }

    public function getUser($id) {
        return $this->repo->getUserById($id);
    }
}
```

✅ Ahora `UserService` **depende de la interfaz**, no del detalle.  
Podés pasarle cualquier implementación de `UserRepository` (MySQL, Redis, Mock, etc.)

---

## 🧱 En Obsidian podrías guardarlo así:

````markdown
## 🧩 Dependency Inversion Principle (DIP)

**Definición**:  
- Los módulos de alto nivel no deben depender de módulos de bajo nivel.  
- Ambos deben depender de abstracciones.

---

### 🔥 Problema que resuelve

- Alto acoplamiento entre lógica de negocio y detalles concretos (bases de datos, APIs, etc.).
- Dificultad para testear, cambiar tecnologías o reutilizar módulos.

---

### 🛑 Violación típica

```php
class Servicio {
    public function __construct() {
        $this->repositorio = new RepositorioMySQL();
    }
}
````

El servicio depende directamente de una clase concreta. Si cambia esa clase, se rompe.

---

### ✔️ Aplicación correcta

- Definís una interfaz (`RepositorioDeUsuario`)
    
- Las implementaciones concretas (`RepositorioMySQL`, `RepositorioEnMemoria`) la implementan.
    
- El servicio recibe la interfaz como dependencia.
    

---

### ✅ Beneficios

- Código desacoplado
    
- Cambios localizados
    
- Testeo fácil (mocking)
    
- Alta flexibilidad y extensión
    

---

### 🧠 Regla clave

> "Programá contra interfaces, no contra implementaciones."
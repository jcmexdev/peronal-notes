---
title: Threads
status:
  - todo
created: 18-04-2025 09:36:17
updated: 20-04-2025 10:50:27
---

Un **hilo** es la **mínima unidad de ejecución** que puede ser programada por el sistema operativo.  
Un **proceso puede tener uno o varios hilos**, todos compartiendo el mismo entorno de ejecución (memoria, archivos abiertos, etc.), pero con **flujo de control independiente** (cada hilo tiene su propia lógica, su propio camino de ejecución).

🔹 Un **hilo** es una **unidad de ejecución dentro de un proceso**.  
🔹 Es como una **subtarea** que hace parte del trabajo general del programa.  
🔹 Todos los hilos de un proceso **comparten la misma memoria**, pero cada uno puede hacer cosas distintas al mismo tiempo.

When you start a process it contains one main thread bu default, when we have more then a thread in a single process we said that the process is multithread.

When we create a new thread the os need to create only enough resources to manage the stack space, registers and program counter, instead like a process allocate a full memory space
- **Espacio para la pila (stack)**: donde el hilo guardará variables locales, llamadas a funciones, etc.
    
- **Registros (registers)**: copias privadas del hilo para mantener su estado.
    
- **Contador de programa (program counter)**: que indica qué instrucción del hilo se va a ejecutar a continuación.

> “What goes on the stack space?
The stack space stores the local variables that live within a function. These are typically short-lived variables—when the function finishes, they are not used anymore. This space does not include variables that are shared between functions (using pointers), which are allocated on the main memory space, called the heap.”

![[threads-sharing-resources.png]]

### Trade offs 
- No se tiene la misma isolacion que los procesos ofrecen  
- Lo anterior conlleva al problema del race condition (o la sobre escritura de un hilo por otro)
- Lo importante es tener sincronizacion y comunicacion entre hilos 

resumir lo siguiente 
“Since threads share memory space, any change made in main memory by one thread (such as changing a global variable’s value) is visible to every other thread in the same process. This is the main advantage of using threads—multiple threads can use this shared memory to work on the same problem together. This enables us to write concurrent code that is very efficient and responsive.”

“Note Threads do not share stack space. Although threads share the same memory space, it’s important to realize that each thread has its own private stack space (as was shown in figure 2.6).”


### Enlaces relacionados
- [[user-level threads]]
- [[goroutines]]
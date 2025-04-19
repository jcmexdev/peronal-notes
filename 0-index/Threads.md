Un **hilo** es la **mínima unidad de ejecución** que puede ser programada por el sistema operativo.  
Un **proceso puede tener uno o varios hilos**, todos compartiendo el mismo entorno de ejecución (memoria, archivos abiertos, etc.), pero con **flujo de control independiente** (cada hilo tiene su propia lógica, su propio camino de ejecución).

🔹 Un **hilo** es una **unidad de ejecución dentro de un proceso**.  
🔹 Es como una **subtarea** que hace parte del trabajo general del programa.  
🔹 Todos los hilos de un proceso **comparten la misma memoria**, pero cada uno puede hacer cosas distintas al mismo tiempo.
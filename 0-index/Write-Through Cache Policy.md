---
title: Write-Through Cache Policy
status:
  - done
  - enhancement
created: 05-05-2025 08:52:05
updated: 05-05-2025 15:41:45
---

# Write-Through Cache Policy
## Keywords
- #cache 
- #memory 
- #complement

## Notes
Esta política especifica que cuando el procesador escribe un dato en cache este cambio se propaga de inmediato a la memoria principal. Es decir a escritura ocurre tanto en cache como en la memoria principal.

### Características 
1. Consistencia de datos: La memoria principal siempre tiene una copia actualizada de los datos, lo que reduce el riesgo de inconsistencias.
2. Operaciones de escritura lentas: Cada escritura requiere acceso a cache como a memoria principal lo que ocasiona un aumento en la latencia.
3. Mayor trafico en el bus, debido a la propagación las memorias caches y la principal se mantienen activamente escuchando al bus.

![[write-through-cache-policy.png]]
> [!info]
> imagen que representa una politica write-through (escritura inmediata)
## Questions?
- [ ] Esta política es una característica que se activa?, R: esta es una característica que sistemas avanzados puede ser configurada, generalmente ya existe una configuración y dependiendo de los niveles de caches algunas pueden implementar una u otra configuración.

## Summary

> [!important]
> Política la cual cuando el cpu realiza un cambio en cache este cambio también se propaga a memoria principal y mediante el bus a las otras caches, esto aumenta la conistencia pero también aumenta la latencia.
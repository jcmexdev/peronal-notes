---
title: Thread communication with memory sharing
status:
  - todo
  - refactor
created: 04-05-2025 02:52:21
updated: 05-05-2025 23:03:47
---

# Thread communication with memory sharing
## Keywords
- #threads 
- #communication 
- #memory 
- #cache 
- #bus

## Notes
Cuando los hilos se comunican a travez de memoria compartida en las arquitecturas "standard" se tienen varios procesadores los cuales [[Reading Data From Memory | leen información de la memoria ram]], adicional se maneja una capa de cache con el objetivo que el bus de datos no se convierta en un cuello de botella, ya que si varios procesos intentan leer, escribir información por medio del bus, esto aumenta la latencia y permite al procesador acceder a datos que usa con frecuencia.

![[basic-memory-sharing-architecture.png]]

La capa de cache resuelve el tema del bus de datos pero ahora el desafío es el tema de la sincronización de memoria ya que si un CPU actualiza una variable en memoria principal compartida el reto es tener las otras capas de cache actualizadas, para esto se utiliza una política de cache llamada [[Write-Through Cache Policy]]

![[write-through-cache-policy.png]]

Los mecanismos para manejar lecturas y escrituras en memoria en sistemas multiprocesadores son conocidos como [[Cache Coherency Protocols]]
## Questions?
- [ ] What type of thread communication should use?
	- [ ] it depends of the problem we are trying to solve
- [ ] Question 2?

## Summary

> [!important]
> 
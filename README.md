# godot-gameplay-samples

Muestras de programación de gameplay en Godot, basadas en Proyecto Luna y acompañadas de explicaciones técnicas. Repositorio en construcción.

## 01. Permiso para iniciar un ataque



Este fragmento de Proyecto Luna comprueba si el jugador puede comenzar un ataque según su estado actual. Devuelve `true` o `false`; no ejecuta el ataque.

```gdscript
func puede_iniciar_ataque() -> bool:
	if is_dead:
		return false

	if is_dodging:
		return false

	if is_attacking:
		return false

	return can_attack
```

La función consulta cuatro variables del jugador: `is_dead`, `is_dodging`, `is_attacking` y `can_attack`. No modifica esos estados ni ejecuta el ataque. Es un fragmento del script del jugador, no un programa independiente.
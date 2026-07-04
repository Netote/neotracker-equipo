# ⚡ Etapa 7 — Estrategia de Tokens

**Tiempo: continuo durante todo el challenge**
**Aplica en todos los modos**

---

## ¿Por qué importa?

Cada mensaje que le mandas a Bob consume tokens. Cuantos más tokens uses, más lento y costoso es el proceso. Un equipo que usa tokens eficientemente termina más rápido y con mejores resultados.

Esta etapa **no tiene un momento fijo** — la estrategia de tokens se aplica desde el minuto 1.

---

## Estrategias clave

### 1. Usa el modo correcto para cada tarea

| Necesitas... | Modo ideal | ¿Por qué? |
|---|---|---|
| Planificar, analizar, decidir | `Plan` o `Ask` | No ejecuta herramientas, menos tokens |
| Escribir o editar código | `Agent` | Necesita acceso a archivos |
| Entender algo técnico | `Ask` | Solo responde, no actúa |

### 2. Un prompt gordo > muchos prompts chicos

❌ Ineficiente:
```
Crea la función que identifica el asteroide más peligroso
```
*(Bob pregunta qué campo usar, luego el lenguaje, luego la estructura de datos...)*

✅ Eficiente:
```
En Python, crea la función find_most_dangerous(neo_list: list[dict]) -> dict
que reciba una lista de NEOs y retorne el que tenga el valor numérico 
más bajo en close_approach_data[0].miss_distance.kilometers.
```

### 3. Da contexto al inicio, no en el camino

Incluye en el **primer prompt** todo lo relevante: lenguaje, arquitectura decidida, estructura del JSON de la NASA, lo que ya existe, lo que falta.

### 4. Sé quirúrgico en las correcciones

❌ Costoso:
```
El código no funciona, rehazlo
```

✅ Barato:
```
La función find_most_dangerous() en src/analyzer.py siempre retorna el 
primer elemento. El bug está en la comparación: miss_distance.kilometers 
viene como string, no como float. Conviértelo antes de comparar.
```

### 5. Usa Skills si repites el mismo patrón

Si notan que le piden a Bob lo mismo varias veces (ej: "genera tests unitarios con datos mock para esta función"), es candidato para una **Skill**. Documéntenlo en `evidence/04-bob-skills/evidencia.md`.

---

## ✅ Checklist de salida

- [ ] `evidence/05-token-strategy/evidencia.md` completado con reflexión del equipo

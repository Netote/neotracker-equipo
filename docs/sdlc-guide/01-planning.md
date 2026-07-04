# 📐 Etapa 1 — Planificación

**Tiempo objetivo: ~8 minutos**
**Modo Bob recomendado: `Plan`**

---

## Objetivo

Transformar el requerimiento semilla en historias de usuario claras y definir el alcance de lo que van a construir.

---

## Instrucciones

### Paso 1 — Cambia Bob al modo `Plan`

En la barra lateral de Bob selecciona el modo **Plan**. Este modo está optimizado para pensar, analizar y estructurar sin escribir código aún.

### Paso 2 — Dale el requerimiento a Bob

Copia el requerimiento semilla del `README.md` y pégalo a Bob con este prompt:

```
Eres un analista de software. A partir del siguiente requerimiento, genera:
1. Una lista de historias de usuario en formato "Como [rol], quiero [acción] para [beneficio]"
2. Los criterios de aceptación de cada historia
3. Las entidades de datos principales que necesitaremos

Requerimiento:
[pega aquí el requerimiento semilla]
```

### Paso 3 — Refina con Bob

Si algo no queda claro, hazle preguntas de seguimiento. Ejemplo:

```
¿Qué campos del JSON de la NASA NeoWs API necesito para identificar 
el asteroide con mayor riesgo de acercamiento?
```

### Paso 4 — Guarda la evidencia

Documenta en `evidence/01-sdlc-stages/evidencia.md` los prompts usados, las historias de usuario y las decisiones del equipo.

---

## ✅ Checklist de salida

- [ ] Al menos 4 historias de usuario documentadas
- [ ] Criterios de aceptación por historia
- [ ] Entidades identificadas (ej: `NearEarthObject`, `WatchList`)
- [ ] Evidencia guardada

---

## 💡 Tip de tokens

En modo `Plan`, Bob no ejecuta herramientas — solo razona. Es el modo más eficiente en tokens. Aprovéchalo para toda la discusión conceptual antes de tocar código.

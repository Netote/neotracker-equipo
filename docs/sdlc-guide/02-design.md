# 🏗️ Etapa 2 — Diseño

**Tiempo objetivo: ~8 minutos**
**Modo Bob recomendado: `Ask`**

---

## Objetivo

Definir la arquitectura del sistema, los módulos principales y el contrato de la NASA NeoWs API antes de escribir una sola línea de código.

---

## Instrucciones

### Paso 1 — Cambia Bob al modo `Ask`

El modo **Ask** es ideal para consultas técnicas, exploración de opciones y decisiones de arquitectura sin modificar archivos.

### Paso 2 — Consulta la arquitectura

```
Basándome en estas historias de usuario: [pega tus historias del paso anterior]

Voy a construir esto en [tu lenguaje elegido]. Propón:
1. Una arquitectura de módulos/clases para el sistema
2. Los endpoints o comandos que necesitaré exponer
3. Cómo estructurar las llamadas a la NASA NeoWs API:
   GET https://api.nasa.gov/neo/rest/v1/feed?start_date=YYYY-MM-DD&end_date=YYYY-MM-DD&api_key=DEMO_KEY
4. Un diagrama de flujo simple en texto (ASCII o mermaid)
```

### Paso 3 — Consulta la estructura del JSON de la NASA

```
¿Cómo se estructura la respuesta JSON de la NASA NeoWs API?
¿Qué campos necesito para:
- Nombre del asteroide
- Tamaño estimado (diámetro)
- Velocidad relativa
- Distancia mínima de acercamiento a la Tierra (miss_distance)
- ¿Es potencialmente peligroso? (is_potentially_hazardous_asteroid)
Dame un ejemplo resumido de la respuesta.
```

### Paso 4 — Decide con tu equipo

Discutan las propuestas de Bob. **Bob sugiere, el equipo decide.** Documenten la decisión final.

---

## ✅ Checklist de salida

- [ ] Arquitectura de módulos/clases decidida
- [ ] Endpoints o comandos definidos
- [ ] Campos clave del JSON de NASA identificados
- [ ] Lenguaje y tipo de interfaz confirmados (CLI / REST / Web)
- [ ] Evidencia guardada en `evidence/01-sdlc-stages/evidencia.md`

---

## 💡 Tip de tokens

En modo `Ask`, Bob no abre archivos ni ejecuta comandos. Si ya saben el lenguaje y la estructura, inclúyanla en el prompt inicial para que Bob no tenga que inferirla — ahorran 1-2 llamadas de exploración.

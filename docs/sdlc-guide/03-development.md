# 💻 Etapa 3 — Desarrollo

**Tiempo objetivo: ~20 minutos**
**Modo Bob recomendado: `Agent`**

---

## Objetivo

Generar el código funcional del sistema usando Bob en modo `Agent`. Bob puede crear archivos, ejecutar comandos y navegar el proyecto directamente.

---

## Instrucciones

### Paso 1 — Cambia Bob al modo `Agent`

El modo **Agent** le da a Bob acceso a herramientas: puede crear archivos, leer el proyecto, ejecutar comandos de terminal y más.

### Paso 2 — Prompt de arranque

Dale a Bob el contexto completo de una sola vez para minimizar tokens:

```
Actúa como desarrollador senior en [lenguaje elegido].
Crea la estructura del proyecto con los siguientes módulos:
[pega aquí la arquitectura que definieron en el diseño]

Requisitos técnicos:
- Consume la NASA NeoWs API:
  GET https://api.nasa.gov/neo/rest/v1/feed?start_date=YYYY-MM-DD&end_date=YYYY-MM-DD&api_key=DEMO_KEY
- Implementa:
  1. Consultar asteroides por rango de fechas (máx 7 días)
  2. Listar y ordenar por tamaño estimado o velocidad relativa
  3. Identificar el asteroide con menor miss_distance del rango (el más peligroso)
  4. Agregar / eliminar asteroides de una lista de seguimiento en memoria
- Interfaz: [CLI / REST API / web — la que eligieron]
- Sin base de datos, sin autenticación propia

Crea los archivos necesarios con el código funcional.
```

### Paso 3 — Itera con prompts específicos

Si algo falta o necesita corrección, sé específico:

```
El método que identifica el asteroide más peligroso no está 
comparando correctamente el campo miss_distance.kilometers.
Corrígelo: debe encontrar el asteroide con el valor numérico más bajo en ese campo.
```

### Paso 4 — Verifica que el código corra

```
Ejecuta el proyecto con el rango de fechas 2025-01-01 a 2025-01-07 
usando api_key=DEMO_KEY y muéstrame el resultado.
```

---

## ✅ Checklist de salida

- [ ] Código fuente en carpeta `src/`
- [ ] Consulta de asteroides por fechas funciona con la API real
- [ ] Ordenamiento por tamaño o velocidad funciona
- [ ] Identificación del más peligroso (menor miss_distance) funciona
- [ ] Lista de seguimiento (agregar/eliminar) funciona
- [ ] La app corre sin errores

---

## 💡 Tips de tokens

- **Un prompt grande al inicio** es más eficiente que 10 prompts pequeños.
- **Incluye el contexto** de diseño en el primer prompt para que Bob no tenga que preguntar.
- Si Bob se equivoca, **señala exactamente la función o campo** en lugar de pedir reescribir todo.
- Usa `# Solo modifica este método:` para ediciones quirúrgicas.

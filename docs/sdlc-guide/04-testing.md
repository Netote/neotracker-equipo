# 🧪 Etapa 4 — Pruebas

**Tiempo objetivo: ~8 minutos**
**Modo Bob recomendado: `Agent`**

---

## Objetivo

Generar y ejecutar pruebas unitarias que validen la lógica del sistema sin depender de la API de la NASA en cada ejecución.

---

## Instrucciones

### Paso 1 — Pide los tests a Bob

```
Genera pruebas unitarias para los módulos de lógica del sistema NeoTracker.
Usa datos mock (no llames a la API real en los tests).
Cubre estos casos:
1. Ordenar una lista de asteroides por velocidad relativa (ascendente)
2. Ordenar una lista de asteroides por tamaño estimado (descendente)
3. Identificar correctamente el asteroide con menor miss_distance de una lista
4. Agregar un asteroide a la lista de seguimiento
5. Intentar agregar un asteroide duplicado a la lista de seguimiento (debe ignorarse o lanzar error)
6. Eliminar un asteroide que existe en la lista de seguimiento

Usa el framework de testing estándar de [tu lenguaje].
Guarda los tests en la carpeta tests/.
```

### Paso 2 — Ejecuta los tests

```
Ejecuta las pruebas y muéstrame el resultado.
```

### Paso 3 — Corrige si hay fallos

```
El test de identificación del más peligroso falla. 
Analiza el error y corrige el código fuente o el test según corresponda.
```

---

## ✅ Checklist de salida

- [ ] Al menos 6 tests escritos en `tests/`
- [ ] Todos los tests usan datos mock (sin llamadas reales a la NASA API)
- [ ] Todos los tests pasan
- [ ] Output de la ejecución documentado en `evidence/01-sdlc-stages/evidencia.md`

---

## 💡 Tip de tokens

Pide todos los tests en **un solo prompt** especificando los casos. Es mucho más eficiente que pedir test por test. Incluir datos mock de ejemplo en el prompt mejora la calidad de los tests generados.

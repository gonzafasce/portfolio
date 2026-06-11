# Plan de Mejoras — Portfolio PD
*Generado a partir de análisis recruiter · Junio 2026*

---

## Contexto rápido

Portfolio de Gonzalo Fasce, Product Designer. Sitio estático HTML/CSS en producción (o cerca). Tres casos: MOB (design system), Singular (IA + diseño), Mis Resultados (incentivos bancarios). Casos protegidos con contraseña por confidencialidad.

El estilo y la narrativa están bien. Los problemas son de acceso, evidencia de impacto y completitud de los casos secundarios.

---

## Mejoras prioritarias

### 1. Resolver la fricción de las contraseñas

**Problema:** Un recruiter con 4 portfolios abiertos no va a mandar un mail para pedir acceso. La contraseña mata la conversión.

**Solución propuesta:**
- Dejar las secciones "El problema", "El proceso" y "Decisiones clave" de cada caso **siempre visibles**.
- Bloquear con contraseña solo las imágenes/capturas sensibles (mockups, UI real del cliente).
- Agregar la contraseña visible en el mismo gate: *"Contraseña: portfolio2025"* — no hay seguridad real de todas formas, solo fricción innecesaria.
- Alternativa: password única, simple, mencionada en el About o en el CV.

**Archivos a modificar:** `casos/mob.html`, `casos/singular.html`, `casos/mis-resultados.html`

---

### 2. Agregar evidencia de impacto en cada caso

**Problema:** MOB explícitamente dice "no tengo métricas duras". Eso es munición en contra.

**Qué buscar y cómo formularlo (aunque sean cualitativos):**

Para **MOB:**
- ¿Cuántos equipos/módulos adoptaron el sistema?
- ¿Cuántos componentes tiene hoy vs. cuando arrancó?
- ¿Redujo tiempo de handoff o de QA? (aunque sea "notablemente" si no hay número)
- Frase modelo: *"De 8 equipos con criterios propios a un sistema único adoptado por toda la compañía."*

Para **Singular:**
- ¿Qué cambió en el flujo de trabajo real? ¿Cuánto tiempo ahorra por sesión de diseño?
- ¿Cuántas iteraciones permite hacer vs. antes?

Para **Mis Resultados:**
- ¿Cuántos usuarios/ejecutivos bancarios usa la feature?
- ¿Aumentó el engagement con los objetivos de venta?

**Tarea:** Gonza tiene que pensar/buscar estos datos. Luego los insertamos en el HTML de cada caso como una sección de "Resultados" o como métricas en el intro del caso.

---

### 3. Agregar foto en el About

**Problema:** El About tiene voz muy personal pero termina sin cara. Disonancia.

**Qué hacer:**
- Foto natural, buena luz, no corporativa. Coherente con el tono del texto.
- Ubicación: inicio del About, a la izquierda del texto intro, o como bloque visual propio antes del texto.
- Formato: cuadrada o ligeramente portrait, ~400x400px o más.

**Archivo a modificar:** `about.html`

---

### 4. Fortalecer el caso Singular

**Problema:** Un caso sobre IA en 2026 que no muestra proceso real es un buzzword. Necesita demostrar cómo cambió el trabajo concreto.

**Qué tiene que mostrar:**
- El antes: cómo era el flujo sin IA.
- El experimento: qué herramientas, qué prompt strategies, qué intentos fallidos.
- El resultado: qué quedó incorporado al flujo real.
- Captura o ejemplo concreto de output generado con IA vs. sin IA.

**Estado actual del caso:** revisar `casos/singular.html` para evaluar qué tan completo está esto.

---

### 5. Revisar el caso Mis Resultados

**Estado:** El más corto (600 líneas vs 744 de MOB). Puede estar incompleto.

**Qué revisar:**
- ¿Tiene sección de proceso o solo resultado?
- ¿Hay imágenes reales o placeholders?
- ¿Se entiende el problema de negocio que resolvía?

---

## Mejoras secundarias (no urgentes)

- **Mobile:** revisar que los tres casos se lean bien en móvil.
- **CV:** confirmar que el PDF descargable está actualizado y coherente con el tono del sitio.
- **Meta / OG tags:** para que cuando se comparta el link en LinkedIn, se vea bien con título + descripción + imagen preview.

---

## Cómo arrancar la próxima conversación

Decile a Claude algo como:

> *"Retomamos el portfolio. Tengo el plan de mejoras en `plan-mejoras.md`. Quiero arrancar con [elegir: fricción de contraseñas / evidencia de impacto / foto en About / caso Singular]. Los archivos están en la carpeta Portfolio PD."*

Claude va a poder leer el estado actual del HTML y el plan, y arrancar directo.

---

## Estado actual de los archivos

| Archivo | Estado |
|---------|--------|
| `index.html` | ✅ Completo |
| `about.html` | ⚠️ Sin foto |
| `casos/mob.html` | ⚠️ Sin métricas, gate de contraseña con fricción alta |
| `casos/singular.html` | ⚠️ Profundidad a revisar |
| `casos/mis-resultados.html` | ⚠️ El más corto, revisar completitud |
| `cv.html` | ❓ No revisado en esta sesión |

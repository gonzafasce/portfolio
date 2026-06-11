# Design System — Portfolio PD
**Gonza Fasce · Product Designer**
*Documento de referencia visual para diseño y desarrollo*

Referencia estética principal: [usehallmark.com/_tests/06-anya-portfolio](https://www.usehallmark.com/_tests/06-anya-portfolio/)
El principio rector: **el contenido es el diseño**. Sin decoración, sin ilustraciones en la UI, sin gradientes. La tipografía y el espacio hacen todo el trabajo.

---

## 01 · Tipografía

### Fuente única: Inter Tight

Una sola familia en todo el sitio. Sin serifa, geométrica, con un tracking naturalmente apretado que le da carácter sin esfuerzo. Se importa desde Google Fonts.

```html
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@300;400;500;600;700;900&display=swap" rel="stylesheet">
```

### Escala tipográfica

| Uso | Peso | Tamaño | Line-height | Tracking |
|-----|------|--------|-------------|---------|
| Display / H1 hero | 900 (Black) | 56–72px | 1.05 | -0.03em |
| H2 sección | 700 (Bold) | 36–44px | 1.1 | -0.02em |
| H3 subsección | 600 (Semibold) | 22–26px | 1.2 | -0.01em |
| Body principal | 400 (Regular) | 16–17px | 1.65 | 0 |
| Body secundario / notas | 400 (Regular) | 14px | 1.6 | 0 |
| Label / meta / UI tiny | 500 (Medium) | 11–12px | 1.4 | 0.05em |
| Número de sección (`00`) | 600 (Semibold) | 12px | — | 0.02em |

### Reglas tipográficas

- Los headings grandes van en **weight 900** — es donde Inter Tight brilla. Sin miedo al tamaño.
- El body nunca supera los 65–70 caracteres por línea (`max-width: 640px` en la columna de texto).
- Los labels de sección siempre en mayúsculas y con tracking positivo.
- **Cero fuentes secundarias.** Inter Tight resuelve todo.

---

## 02 · Colores

Paleta mínima de 4 valores. No hay más.

```css
:root {
  --color-bg:       #FFFFFF;   /* Fondo — blanco puro */
  --color-ink:      #0D0D0D;   /* Texto principal — casi negro */
  --color-muted:    #999999;   /* Texto secundario, meta, labels */
  --color-accent:   #2F6EEB;   /* Acento único — azul medio */
  --color-rule:     #E8E8E8;   /* Líneas divisorias */
}
```

### Reglas de uso de color

- `--color-accent` se usa **solo** para: números de sección, links en hover, indicador de sección activa en nav. Nada más.
- El fondo es siempre blanco. Sin grises de fondo, sin tarjetas con sombra.
- Las líneas divisorias (`--color-rule`) son la única textura permitida.
- Los estados hover en texto usan el acento — nunca subrayado por defecto, sí en hover.

### Modo oscuro

No se implementa en v1. El portfolio se ve en el contexto de una entrevista o revisión casual — blanco es el default correcto.

---

## 03 · Layout

### Estructura de página

```
┌─────────────────────────────────────────────────────┐
│  NAV (fixed top, full width)                        │
│  Logo/nombre · Links de navegación · CV download    │
├─────────────────────────────────────────────────────┤
│                                                     │
│  CONTENIDO PRINCIPAL                                │
│  max-width: 720px · margin: 0 auto                  │
│  padding: 0 24px                                    │
│                                                     │
└─────────────────────────────────────────────────────┘
```

**Diferencia respecto a la referencia:** Anya usa sidebar fijo lateral. El portfolio de Gonza usa **nav superior** (más adaptable a multi-página y mobile). El espíritu es el mismo: nav limpio, contenido centrado, mucho aire.

### Grid y spacing

```css
:root {
  --space-xs:   8px;
  --space-sm:   16px;
  --space-md:   32px;
  --space-lg:   64px;
  --space-xl:   96px;
  --space-xxl:  128px;

  --content-width: 720px;
  --nav-height:    60px;
}
```

- Las secciones dentro de un caso se separan con `--space-xl` (96px).
- Entre el número de sección y el título: `--space-sm` (16px).
- El contenido empieza siempre a `--space-xl` del nav.

### Navegación superior

```
GONZA FASCE                    MOB  Singular  Mis Resultados  About  ↓ CV
```

- Nombre a la izquierda, links a la derecha.
- Sin fondo, sin sombra. Solo una línea `1px` de `--color-rule` al hacer scroll (aparece con JS).
- Links en `--color-muted` por defecto, en `--color-ink` en hover.
- El link activo tiene un punto o subrayado fino en `--color-accent`.

---

## 04 · Componentes

### Número de sección

El elemento más característico de la referencia. Se usa tanto en la nav como en los encabezados de sección dentro del contenido.

```
00 · INTRO
01 · EL PROBLEMA
```

```css
.section-label {
  font-family: 'Inter Tight', sans-serif;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--color-accent);    /* número */
}
.section-label .sep {
  color: var(--color-muted);     /* el punto · */
}
.section-label .name {
  color: var(--color-muted);     /* la palabra */
}
```

### Cards de caso (Home)

Sin imágenes en la card — solo texto. La imagen entra dentro del caso.

```
┌──────────────────────────────────────┐
│  01 · MOB                            │
│                                      │
│  Sistema de Diseño N5 Now            │ ← H3 bold
│                                      │
│  Un sistema de diseño construido     │ ← body, 2 líneas max
│  desde cero para una plataforma      │
│  financiera enterprise.              │
│                                      │
│  Ver caso →                          │ ← link en accent
└──────────────────────────────────────┘
```

- Borde: `1px solid var(--color-rule)` — sin sombra.
- Padding: `--space-md` (32px).
- Hover: el borde cambia a `var(--color-ink)`. Transición `0.2s ease`.
- Sin imagen de preview — mantiene el minimalismo.

### Imagen dentro del caso

Las imágenes son el único elemento con peso visual. Se muestran al ancho completo del contenido (720px) o en grid 2 columnas cuando hay pares.

```css
.case-image {
  width: 100%;
  border-radius: 4px;
  border: 1px solid var(--color-rule);
  margin: var(--space-md) 0;
}

.case-image-caption {
  font-size: 12px;
  color: var(--color-muted);
  margin-top: var(--space-xs);
  font-style: italic;
}
```

### Password gate

Página entera centrada, sin nav visible (o nav ghosted).

```
┌─────────────────────────┐
│                         │
│  Este caso está         │
│  protegido.             │ ← H2 bold
│                         │
│  Pedime la contraseña   │
│  en gonza@email.com     │ ← body, link en accent
│                         │
│  [ ______________ ]     │ ← input minimal
│  [ Ingresar      ]      │ ← button
│                         │
└─────────────────────────┘
```

```css
.password-input {
  border: none;
  border-bottom: 1px solid var(--color-ink);
  border-radius: 0;
  padding: 8px 0;
  font-family: 'Inter Tight', sans-serif;
  font-size: 16px;
  outline: none;
  width: 280px;
}

.password-btn {
  background: var(--color-ink);
  color: var(--color-bg);
  border: none;
  padding: 12px 24px;
  font-family: 'Inter Tight', sans-serif;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.04em;
  cursor: pointer;
  margin-top: 16px;
}
```

---

## 05 · Animaciones

Principio: **animación funcional, no decorativa**. Si la animación no ayuda a entender algo, no va.

### Permitidas

| Elemento | Animación | Duración | Easing |
|----------|-----------|----------|--------|
| Links / botones hover | color change | 150ms | ease |
| Cards hover | border color | 200ms | ease |
| Nav scroll | border-bottom aparece | 200ms | ease |
| Page load | fade in del contenido | 400ms | ease-out |
| Imágenes | fade in al entrar al viewport | 500ms | ease-out |

### La única animación "de personalidad"

En la Home, el nombre `Gonza Fasce` en el hero puede tener un cursor parpadeante que deja de parpadear al llegar. Sutil, editorial, referencia directa a la escritura.

```css
@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}
.cursor {
  display: inline-block;
  width: 2px;
  height: 0.85em;
  background: var(--color-ink);
  margin-left: 2px;
  vertical-align: middle;
  animation: blink 0.8s step-end 5; /* para 4 segundos, luego desaparece */
}
```

### Prohibidas

- Parallax
- Scroll-triggered slides desde los costados
- Hover cards con elevación / sombra
- Loaders o spinners
- Cualquier animación que dure más de 600ms

---

## 06 · Hero de Home

```
[Nav]

──────────────────────────────────────

Gonza Fasce_

Product Designer.
Buenos Aires · disponible para oportunidades.

──────────────────────────────────────

01 · MOB          02 · Singular          03 · Mis Resultados

[cards]
```

- El nombre va en weight 900, ~64–72px. Sin subtítulo animado, sin foto.
- La línea de rol (`Product Designer.`) va en weight 400, mismo tamaño o un poco más chico.
- Las líneas divisorias son `<hr>` con `--color-rule`.
- El espacio entre el hero y las cards: `--space-xxl` (128px).

---

## 07 · Estructura de caso de estudio

Cada caso sigue el mismo template de secciones con su número:

```
[Nav]

01 · MOB: Methodology to Organise and Build
─────────────────────────────────────────────

[IMAGEN HERO — full width]

00 · EL PROBLEMA
Texto...

01 · EL PROCESO
Texto...
[IMAGEN]

02 · LA SOLUCIÓN
Texto...
[IMÁGENES — grid 2 col si hay pares]

03 · EL RESULTADO
Texto...

──────────────────────────────────────
← Volver        Siguiente caso →
```

- El título del caso va en display H1 (weight 900).
- Cada sección dentro del caso usa el sistema de numeración `00 · LABEL`.
- Navegación al final: link a caso anterior / siguiente. Sin nav central por ahora.

---

## 08 · CSS Variables — Resumen global

```css
:root {
  /* Colores */
  --color-bg:       #FFFFFF;
  --color-ink:      #0D0D0D;
  --color-muted:    #999999;
  --color-accent:   #2F6EEB;
  --color-rule:     #E8E8E8;

  /* Tipografía */
  --font-main: 'Inter Tight', sans-serif;

  /* Espaciado */
  --space-xs:   8px;
  --space-sm:   16px;
  --space-md:   32px;
  --space-lg:   64px;
  --space-xl:   96px;
  --space-xxl:  128px;

  /* Layout */
  --content-width: 720px;
  --nav-height:    60px;
}
```

---

*Design.md · Fase 2 — Diseño Web · Portfolio PD*

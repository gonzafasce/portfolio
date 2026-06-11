# Portfolio PD — Documento de Contenido Consolidado
**Gonza Fasce · Product Designer**
*Documento de referencia para la fase de diseño y desarrollo*

---

## Decisiones estructurales

| Decisión | Definición |
|----------|------------|
| Tipo de entrega | Web directa (sin PDF MVP) |
| Estructura | Páginas separadas por caso |
| Privacidad | Home + About públicos / Casos con contraseña |
| Stack | Figma para diseño · HTML/CSS para desarrollo |
| Hosting | Netlify o GitHub Pages |
| Dominio | Pendiente definir |
| CV | Descargable desde navegación principal y página About |
| Tono | Humano, directo, sin corporativo |

### Páginas del sitio
1. **Home** — Hero, intro breve, preview de los 3 casos (cards)
2. **Caso 1** — MOB: Sistema de Diseño N5 Now *(con contraseña)*
3. **Caso 2** — Singular: IA como co-piloto de diseño *(con contraseña)*
4. **Caso 3** — Mis Resultados: Sistema de incentivos bancarios *(con contraseña)*
5. **About** — Texto aprobado + CV descargable

---

## About Me

Soy Product Designer con raíces en el diseño gráfico y multimedial, pero mi trabajo real ocurre en la intersección entre diseño, estrategia y tecnología. Me especialicé en productos digitales complejos — plataformas financieras, sistemas de diseño, experiencias enterprise — donde aprendí que diseñar bien no es solo hacer interfaces prolijas: es construir estructuras que los equipos puedan sostener y evolucionar en el tiempo.

Una parte importante de mi carrera la pasé trabajando directamente con liderazgo ejecutivo: conceptualizando productos desde cero, prototipando ideas para validarlas con clientes reales, y traduciendo oportunidades de negocio en propuestas claras y accionables. Ese contexto me enseñó a moverme con velocidad, a comunicar con precisión y a entender el diseño como una herramienta que reduce incertidumbre — no solo que hace las cosas más lindas.

Hoy me interesa especialmente cómo está cambiando el rol del diseño frente a la IA y las nuevas formas de construir productos. No como amenaza, sino como una oportunidad de redefinir qué significa aportar valor como designer. Creo que los mejores productos nacen cuando el diseño se sienta en la misma mesa que el negocio y la tecnología — y eso es exactamente donde me gusta estar.

---

## Caso 1 — MOB: Methodology to Organise and Build

### Narrativa

#### El problema

Cuando entré a N5 Now, el diseño era básicamente un caos descentralizado. Cada equipo hacía lo suyo. Un mismo componente podía verse y comportarse diferente dependiendo del módulo que abrías. No había criterio compartido, no había sistema, no había nadie que lo estuviera reclamando.

Yo había entrado para hacer diseño web, gráfico y audiovisual. Pero cuando me propusieron pasarme al área de UX — que en ese momento no existía — me pareció exactamente el tipo de problema que me interesaba atacar.

#### El proceso

No arranqué con una gran propuesta ni una presentación para convencer a nadie. Arranqué a ordenar lo que había. Con un desarrollador frontend empezamos a construir el sistema en paralelo, casi en secreto. Le pusimos **MOB** — *Methodology to Organise and Build* — pero entre nosotros lo llamábamos "la mafia", porque eso era: algo que crecía desde las sombras sin que nadie lo hubiera pedido oficialmente.

La base fue Material Design, adaptado sobre MUI. Primero lo desarrollamos en Adobe XD, después lo migramos a Figma en el momento justo. Esa migración fue clave para que el sistema pudiera crecer y ser adoptado por el equipo de diseño.

Lo más difícil fue la evangelización. Los líderes no creían que esto era necesario — increíble pero real. Estuve meses convenciendo equipos, mostrando valor con cada módulo nuevo, mientras la estructura de la compañía cambiaba constantemente. No fue lineal para nada.

Pero de a poco fue tomando forma. Primero los componentes, después los patrones y los comportamientos, después la documentación dentro de Figma. Hasta que este año cerré el ciclo con una presentación de filosofía: **Los 8 Mandamientos del Diseño de Producto en N5**. Ya no era solo un sistema de componentes — era una forma de pensar el diseño que podía ser compartida con producto, tecnología y negocio.

#### La solución

MOB es un sistema de diseño completo para una plataforma financiera enterprise. Componentes, patrones, principios de interacción, documentación. Pero lo que más me importa no es el inventario — es la lógica detrás.

La premisa central: los clientes pueden personalizar la identidad visual, pero sin tocar el esqueleto que sostiene el producto. *La marca del cliente se ve. La esencia de N5 se siente.*

Los 8 mandamientos definen desde cómo usar el sistema hasta cómo tomar decisiones de diseño. No son solo reglas — son una cultura de trabajo que se extiende más allá del equipo de diseño.

#### El resultado

MOB pasó de ser una iniciativa que nadie había pedido a convertirse en el estándar oficial de diseño de N5 Now. No tengo métricas duras para mostrarte — la plataforma enterprise no funciona así. Pero sí pasaron cosas concretas: los módulos empezaron a tener coherencia, diseño y desarrollo se alinearon mejor, y apareció algo que antes no existía: un lenguaje común entre equipos.

Y creo que lo más importante fue lo que cambió en cómo la organización vio al diseño. De ser algo que "hacía las pantallas", pasó a ser algo que construía estructuras. Eso no es menor.

---

### Selección de imágenes

| Archivo | Sección | Rol en el caso |
|---------|---------|----------------|
| `filosofia-1.jpg` | Apertura | Hero image del caso. La portada del cura abre con personalidad antes de leer una palabra. |
| `antes-campaigns.png` | El problema | El "antes" más dramático. Muestra el estado previo al sistema. |
| `filosofia-2.jpg` | El proceso | "Nuestro Sistema de Diseño: MOB". Explica qué es el sistema con Figma visible. |
| `figma-variables.png` | El proceso | Variables N5 vs Itaú side by side. Profundidad técnica, flexibilidad visible. |
| `filosofia-3.jpg` | La filosofía | Slide del Padrino — Mandamiento 1. Personalidad del proyecto. |
| `despues-campaigns.png` | El resultado | El "después" del módulo más dramático. |
| `despues-carteras.png` | El resultado | Segundo módulo después. Muestra consistencia cross-módulo. |
| `fmc-mobile.png` | El resultado | Mobile. El sistema escala más allá del desktop. |
| `branding-itau.png` | Escala | Misma pantalla, identidad Itaú Chile. |
| `branding-bv.png` | Escala | Misma pantalla, identidad BV Brasil. El argumento visual de la flexibilidad. |
| `paleta-itau.png` | Escala | Tokens de color del cliente. Muestra el sistema en acción. |

**Total: 11 imágenes**

---

## Caso 2 — Singular: de idea del CEO a dos decks accionables en una semana

### Narrativa

#### El problema

El CEO de N5 baja una visión: **Singular**, una plataforma B2B de customer engagement con IA para bancos. Hay arquitectura técnica, hay hipótesis comercial, hay intuición fuerte sobre el lugar en el mercado. Lo que no hay es un producto diseñado, una narrativa visual, ni una manera concreta de mostrarle al equipo y a clientes cómo se ve la cosa.

El encargo fue claro: en una semana, producir algo que sirviera tanto para alinear internamente como para vender. Sin más contexto que eso.

#### El proceso

Lo primero que hice no fue abrir Figma. Fue entender el producto — y la primera decisión de diseño que tomé cambió todo lo que vino después: **Singular no es un producto, son dos**.

Un **panel operativo** para el CRM Manager del banco — alta densidad, dark mode, acciones en tiempo real. Y un **panel directivo** para el C-level — read-only, narrativa de arriba hacia abajo, síntesis estratégica. Tratarlos como una sola cosa habría comprometido a los dos. Separarlos fue el primer entregable de la semana, y fue conceptual: no había dibujado nada todavía.

A partir de ahí el trabajo corrió en dos carriles en paralelo.

El primero fue el **deck de UX** — la arquitectura de experiencia del sistema completo. Cómo funciona Singular como producto, sus tres capas (el cerebro que decide, la voz que ejecuta, el cliente que vive la consecuencia), los arquetipos de usuario, la lógica de canales. El tipo de documento que necesitás para que un equipo entienda qué está construyendo antes de tocar una pantalla.

El segundo fue la **exploración visual del admin** — y acá es donde el proceso se pone interesante. En vez de proponer una dirección y defenderla, decidí mapear el espacio completo: cinco herramientas de IA generativa distintas, mismo brief para todas, seis variantes visuales en paralelo. No para mostrar que podía producir mucho, sino para que el CEO pudiera elegir con criterio real en vez de aprobar a ciegas.

El insight que apareció en el proceso: cada herramienta de IA tiene una "voz por defecto" que tira hacia un estilo. Lovable tira a fintech limpio, v0 tira a Linear, Stitch tira a denso. Pelearle a esa voz desperdicia tiempo. Aprovecharla deliberadamente — usar cada herramienta para lo que mejor hace — es lo que permitió explorar seis direcciones en un día.

#### La solución

Dos decks accionables al final de la semana. El de UX para alinear al equipo sobre qué se está construyendo. El visual para que el CEO tomara una decisión real sobre estética y dirección — con trazabilidad completa de por qué se consideró cada variante y por qué se descartó.

La tesis metodológica que guió todo: la IA como co-piloto, no como ejecutora. Cada decisión de diseño la tomé yo. Cada producción de assets pasó por al menos una herramienta de IA. El rol del designer no desaparece — se convierte en director, curador y crítico de output.

#### El resultado

El CEO entró a la reunión final con una decisión real para tomar. Eso es lo que más me importa de este caso: no el volumen de lo que se produjo, sino el tipo de conversación que habilitó. En vez de "te traigo lo que decidí", la dinámica fue "te traigo el espacio para que decidas vos".

Y lo que quedó demostrado — al menos para mí — es que la velocidad bien usada no es un atajo. Es lo que te permite explorar el problema en lugar de resolver solo una versión de él.

---

### Selección de imágenes

| Archivo | Sección | Rol en el caso |
|---------|---------|----------------|
| `ilus-admin_dash.png` | Apertura | Ilustración del directivo frente al dashboard. Contextualiza antes de hablar del producto. |
| `deck-singular-apertura.png` | El problema | "Un chatbot habla con el cliente" tachado. Explica la propuesta en un segundo. |
| `ilus-infografia-singular-solo.png` | El sistema | Hero image del proceso. Las tres capas en Estilo Lápiz. Va grande. |
| `ilus-capturadechat.png` | La voz del producto | Conversación WhatsApp con Valentina. Materializa la experiencia del cliente. |
| `deck-singular--acto2.png` | El sistema | "El banco define el universo. North Star activa la versión correcta." |
| `1-MOB-light_ClaudeDesign.png` | La metodología | Variante A — MOB Light · Claude Design |
| `2-MOB-dark_ClaudeDesign.png` | La metodología | Variante B — MOB Dark · Claude Design |
| `3-LiquidGlass_ClaudeCode.png` | La metodología | Variante C — Liquid Glass · Claude Code |
| `4-BloombergStyle_Lovable.png` | La metodología | Variante D — Bloomberg Style · Lovable |
| `5-BUGATTI_stitch.png` | La metodología | Variante E — Bugatti Style · Stitch *(hero de la grilla)* |
| `6-LapizDark-v0.png` | La metodología | Variante F — Lápiz Dark · v0 |

**Total: 11 imágenes**

---

## Caso 3 — Mis Resultados: diseñar un sistema de incentivos que pueda vivir sin soporte manual

### Narrativa

#### El problema

Los bancos tienen equipos comerciales grandes, con metas, rankings e incentivos que cambian todos los meses. El problema es que gestionar todo eso es un caos — planillas de Excel, configuraciones manuales, información dispersa. Nadie tiene una visión clara de su propio desempeño en tiempo real.

La primera versión de esta plataforma existía, pero estaba diseñada para resolver los problemas puntuales de un banco específico. Sin módulo administrador, la configuración de objetivos y metas debía hacerse a mano cada mes — un costo enorme que asumía internamente el equipo de soporte. No era un producto, era un parche.

#### El proceso

Cuando me metí a fondo con el PO a analizar el scope real del proyecto, lo primero que quedó claro es que el problema era mucho más grande de lo que parecía. No se trataba de mejorar pantallas — se trataba de construir una plataforma que pudiera implementarse en cualquier banco, con reglas de negocio distintas, estructuras organizacionales distintas y modelos de incentivos distintos.

Eso cambió todo el enfoque.

El análisis nos llevó a definir tres perfiles de usuario con necesidades completamente diferentes: el **Vendedor**, que quiere saber cómo va respecto a sus objetivos; el **Supervisor**, que necesita ver el desempeño de su equipo; y el **Administrador**, que configura las reglas del sistema — metas, modelos de incentivos, distribución por ejecutivo, manejo de errores de pago.

El módulo administrador resultó ser el corazón del problema. Sin él, el sistema no puede escalar: alguien siempre tiene que configurar algo a mano. Pero diseñarlo correctamente era enormemente complejo — y acá está la diferencia con cualquier sistema de incentivos tradicional.

Un sistema de loyalty para una tienda de ropa o una concesionaria es relativamente directo: vendiste X, cumpliste la meta. En banca, las reglas son otra cosa. Si el objetivo de un ejecutivo es vender 15 tarjetas en el mes y vendió 15, pero 3 clientes cancelaron, su resultado real es 12 — no cumplió. Y eso es el caso más simple. Si además 3 de esas tarjetas las vendió un ejecutivo de call center a clientes que figuran en su cartera, la cuenta puede ser media tarjeta, una entera o ninguna, dependiendo de la regla del banco.

Cada banco tiene sus propias versiones de esa lógica. Cubrir todos los casos posibles sin que la interfaz del administrador se volviera inmanejable era el desafío real del producto.

Se vendió el proyecto para implementarlo en un banco grande de Perú. El scope era ambicioso, el tiempo ajustado, y las partes no encontraron la flexibilidad necesaria para avanzar. El proyecto quedó trunco.

#### La decisión

Cuando arrancó la v2, la pregunta fue cómo avanzar sin repetir el mismo error. La respuesta fue una decisión estratégica simple: empezar por donde hay más valor inmediato y menos riesgo de complejidad infinita.

Se priorizó **Mis Resultados** — el visualizador de performance para vendedores y supervisores. El módulo que más impacto tiene en el día a día del usuario comercial. Y para el administrador, en esta primera instancia, se optó por templates de Excel que mapean la configuración directamente al sistema — un puente pragmático que permite operar sin bloquear todo el desarrollo en el problema más difícil.

No es la solución final. Es la solución correcta para este momento.

#### El resultado

Una plataforma que permite a los equipos comerciales de un banco ver su performance en tiempo real — objetivos, resultados, rankings, estado de incentivos — sin depender de reportes manuales ni de alguien que actualice una planilla.

Lo más valioso de este caso no es el producto en sí, sino el proceso de entender dónde estaba realmente el problema. La v0 resolvía síntomas. La v1 encontró la dimensión real del desafío. La v2 tomó la decisión más difícil: acotar el scope con criterio, sin perder de vista hacia dónde tiene que ir el sistema.

---

### Selección de imágenes

| Archivo | Sección | Rol en el caso |
|---------|---------|----------------|
| `v0-home-resultados.png` | El problema | El "antes". Muestra la primera versión y su complejidad sin sistema. |
| `Ideación-feature_map-vendedor.jpg` | El proceso | Feature map del Vendedor — estructura clara y acotada. |
| `Ideación-feature_map-admin.jpg` | El proceso | Feature map del Admin — el contraste visual que muestra la complejidad real. |
| `Ideación-wireframes.jpg` | El proceso | Wireframes de v1 en XD. Evidencia del proceso de análisis. |
| `v2-home.png` | El producto | La pantalla estrella del caso. Vendedor viendo sus objetivos en tiempo real. |
| `v2-ranking.png` | El producto | Vista del ranking — una dimensión diferente del producto. |
| `v2-supervisor-mi_equipo.png` | El producto | Vista del Supervisor — muestra que el sistema cubre los 3 perfiles. |
| `concepto-admin2.png` | La complejidad | Sidebar con Objetivos, Tramos, Candados, Aceleradores, Tarifarios, Modelos de Incentivos. |
| `v2-configurador-home.png` | La decisión | El admin MVP via Excel. Solución pragmática antes de resolver el problema más difícil. |

**Total: 9 imágenes**

---

## Resumen de assets por caso

| Caso | Imágenes | Carpeta |
|------|----------|---------|
| MOB | 11 | `assets/caso-1-mob/` |
| Singular | 11 | `assets/caso-2-singular/` |
| Mis Resultados | 9 | `assets/caso-3-misresultados/` |
| **Total** | **31** | |

---

*Documento generado en Fase 1 — Estrategia y Contenido. Próximo paso: Fase 2 — Diseño Web.*

# Plan: servicios desde Buenos Aires (una ronda por hora)

**Enfoque:** servicios (no comercio), desde Buenos Aires, para la ciudad o para el mundo,
aprovechando que es la principal ciudad del país.

## Perfil del usuario (contado por él, 23 de octubre de 2026)
- Le gusta **armar y construir cosas con ayuda de la IA**: productos físicos, soldadura y
  carpintería. Está empezando: no tiene experiencia previa en esos oficios.
- Ahora está construyendo **un tráiler de metal para perro**.
- Usa la IA para **prototipar en Autodesk Fusion** (CAD).
- **Idea propia:** aprovechar el conocimiento técnico de la IA para armar **una app** basada en eso.
- Programa: hizo una tienda online en React con Firebase (este repo).
- Hobby: guitarra y canto (tiene experiencia, pero no quiere exponerse; queda fuera del foco).

### Lo que más le costó al construir el tráiler (dolores reales = funciones de la app)
Herramientas que usa: amoladora, taladro y las físicas de base.
1. **Entender bien las medidas**: qué significan, cómo tomarlas y cómo pasarlas al diseño.
2. **Qué comprar**: qué material sirve, en qué medida comercial, y cómo **simplificar** el diseño
   para comprar menos y cortar menos.
3. **Dónde guardar los materiales para que no se oxiden**: el cuidado de los materiales y las herramientas.
4. **Seguridad**: qué protección hace falta para cada herramienta y cada tarea.
5. **Una guía paso a paso** de verdad, no instrucciones sueltas.

### Ampliación: no solo construir, también instalar y reparar en la casa
Ejemplos del usuario:
- **Colocar un bidet**: hay muchísimos videos, pero no un paso a paso tipo manual que diga
  **cuándo va teflón y cuándo sellarroscas**, o si hay o-ring.
- **Armar la mochila del inodoro**: qué corrugado lleva y qué medidas tiene.

**La idea clave (la vuelta de tuerca):** saber **de antemano qué cosas pueden variar** en tu caso
(tipo de rosca, medida del caño, modelo del artefacto, material de la pared) **y cuáles son
universales**, para tenerlas en cuenta antes de comprar y antes de empezar. Así se minimizan los
errores. Es la diferencia entre un video ("mirá cómo lo hago yo") y un manual que se adapta a tu caso.

→ Las rondas tienen que incluir también **reparaciones e instalaciones del hogar** (plomería,
electricidad básica, armado y colgado de cosas), no solo fabricación.

→ Las rondas 2, 3 y 5 tienen que evaluar si algo en el mercado ya resuelve **estos cinco puntos
juntos y en español**. Si no, esa es la vuelta de tuerca.

**Pregunta central de las rondas:** ¿qué servicio o app puede armar alguien que construye cosas
con IA, desde Buenos Aires, para la ciudad o para el mundo?

**Tarea programada:** `trig_01L3ApodYh6rG8rSMSjaYSgf` — **borrada el 23/10 a las 16:15, al terminar las 8 rondas.**

### La idea, en palabras del usuario
Una **"fuente madre"** para hacer las cosas de la casa: plomería, electricidad (voltajes,
seguridad), construcción y armado, **bien específica de Argentina**: los términos, las medidas, los
materiales y las marcas de acá. Hoy cada albañil dice algo distinto y hay millones de medidas.
Quien no es del rubro no tiene dónde consultar con confianza.

**Preguntas que las rondas tienen que responder:**
1. ¿Hay algo parecido? ¿Es gratis o pago?
2. Si se arma, **¿cómo se gana plata?** (el usuario no lo sabe todavía)
3. ¿Qué tiene de específico Argentina y cómo se consigue esa información confiable?

| Ronda | Hora aprox. (Argentina) | Tema | Estado |
|---|---|---|---|
| 1 | 09:15 | Panorama general de servicios en Buenos Aires (anterior al perfil) | ✅ [ronda-01-panorama.md](ronda-01-panorama.md) |
| 2 | 10:13 | **¿Existe algo parecido?** En el mundo (asistentes de IA para arreglos del hogar, apps de Home Depot y Lowe's, iFixit, apps de bricolaje), en español (España y México) y en Argentina (Easy, Sodimac, ferreterías, YouTube, foros, Mercado Libre). Para cada uno: **gratis o pago**, qué resuelve y qué no, comparado con los 5 dolores del usuario y la idea de "qué varía y qué es universal" | ✅ [ronda-02-existe-algo-parecido.md](ronda-02-existe-algo-parecido.md) |
| 3 | 11:13 | **¿Cómo se gana plata?** Modelos posibles con ejemplos reales y cifras: suscripción freemium, afiliados (Mercado Libre, ferreterías), marcas que patrocinan (FV, Awaduct, Sika, etc.), lista de compras armada para retirar en la ferretería, derivar a un profesional matriculado cuando el trabajo es riesgoso (cobrar por contacto), venta a cadenas (Easy, Sodimac). Qué funcionó y qué no | ✅ [ronda-03-como-ganar-plata.md](ronda-03-como-ganar-plata.md) |
| 4 | 12:13 | **Lo específico de Argentina**: normas (AEA para electricidad, IRAM, gas con matriculado), 220 V y 50 Hz, medidas y roscas habituales, nombres locales de materiales (termofusión, sellarroscas, corrugado, etc.), marcas. **Qué está prohibido o es peligroso hacer sin matriculado** (gas, tableros) y cómo debe manejarlo la app. Fuentes confiables para alimentar la app | ✅ [ronda-04-lo-especifico-de-argentina.md](ronda-04-lo-especifico-de-argentina.md) |
| 5 | 13:13 | **Cómo construir la app con IA**: arquitectura simple (IA + base de conocimiento propia y verificada), cómo evitar que la IA invente medidas o dé consejos peligrosos, de dónde sacar contenido (manuales de fabricantes, normas, entrevistas a matriculados), costos y qué puede armar una persona sola | ✅ [ronda-05-como-construir-la-app.md](ronda-05-como-construir-la-app.md) |
| 6 | 14:13 | **Cómo conseguir los primeros usuarios**: documentar en público los propios proyectos (el tráiler, el bidet), comunidades y grupos de bricolaje en Argentina, YouTube e Instagram en español | ✅ [ronda-06-primeros-usuarios.md](ronda-06-primeros-usuarios.md) |
| 7 | 15:13 | **Síntesis**: ¿vale la pena? Riesgos (responsabilidad legal si alguien se lastima), puntaje con los mismos criterios, y comparación con las ideas anteriores | ✅ [ronda-07-sintesis.md](ronda-07-sintesis.md) |
| 8 | 16:13 | **Plan de prueba** con menos de US$ 200: un primer prototipo (por ejemplo, una guía "colocar un bidet en Argentina" con preguntas sobre tu caso) y cómo medir si a la gente le sirve | ✅ [ronda-08-plan-de-prueba.md](ronda-08-plan-de-prueba.md) |

## Reglas
- Búsquedas reales; cada competidor se verifica en tiendas de apps, Product Hunt, Reddit,
  Instagram y LinkedIn (lección de la ronda 2b: la prensa no ve a los jugadores chicos).
- Lo que no se pueda verificar se marca como **supuesto**.
- Cada ronda termina con commit, push y un resumen corto.

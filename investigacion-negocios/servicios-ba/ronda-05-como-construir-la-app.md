# Ronda 5 — Cómo construir la app con IA sin que invente medidas ni dé consejos peligrosos

Fecha: 23 de octubre de 2026, 13:20 (Argentina).

## Respuesta corta
- **No conviene que sea un chat libre con IA** (eso ya lo hace ChatGPT gratis y se equivoca). Conviene
  una **guía estructurada y verificada por humanos**, en la que la IA **solo adapta** la guía a tu caso
  y responde dudas **citando** esa guía.
- **La "fuente madre" es una base de guías propias**, una por trabajo (colocar bidet, cambiar mochila…),
  cada una con: lo que varía, lo universal, el semáforo, la lista de materiales y los pasos. Esa base es
  el verdadero activo del negocio; la IA es el motor.
- **Lo puede arrancar una persona sola**: el usuario ya programó una tienda en React con Firebase, que
  alcanza para la primera versión.
- **El costo de la IA es bajo**: de menos de **US$ 0,001** a unos **US$ 0,04** por consulta, según el
  modelo (cálculo abajo).

## 1. La arquitectura (en simple)

```
Usuario: "Quiero colocar un bidet"
   │
   ▼
[1] La app busca la guía "Colocar bidet" en la base propia (verificada)
   │
   ▼
[2] Hace las preguntas de "lo que varía":
     ¿Tu canilla es de 1/2" o de 3/4"?  ¿Trae o-ring?  ¿El piso es de cerámica?  (con fotos de ayuda)
   │
   ▼
[3] La IA arma TU guía: materiales exactos, pasos, advertencias de seguridad,
     usando SOLO el contenido de la guía verificada (y lo cita)
   │
   ▼
[4] Semáforo: si en algún punto aparece algo rojo (gas, tablero) → para y deriva a un matriculado
   │
   ▼
[5] Lista de compras → link a Mercado Libre o envío por WhatsApp a una ferretería
```

**Por qué así y no un chat abierto:** el riesgo de que la IA invente una medida o un paso peligroso baja
mucho cuando **solo puede responder con lo que está en la guía verificada** y cuando las preguntas
importantes (las variables) están **programadas de antemano**, no improvisadas.

## 2. Técnicas para que la IA no invente

| Técnica | Qué es | Para qué sirve acá |
|---|---|---|
| **Base de conocimiento propia** (en la jerga técnica, RAG) | La IA recibe la guía verificada antes de responder | Responde con datos argentinos verificados, no con lo que "recuerda" de internet |
| **Citas obligatorias** | La API de Claude permite activar citas: cada afirmación viene con el fragmento exacto de la guía de donde sale | Se puede mostrar "según el manual de FV…" y **detectar respuestas sin respaldo** |
| **Salidas estructuradas** | La IA devuelve un formato fijo (lista de materiales, pasos, nivel de semáforo) en vez de texto libre | La app puede validar: si falta el semáforo o una medida, no se muestra |
| **Reglas de "no sé"** | Instrucción explícita: si la guía no cubre el caso, decir "no está cubierto, consultá a un profesional" | Evita que complete los huecos inventando |
| **Bloqueo de zonas rojas** | Gas y tablero eléctrico: la app no genera instrucciones, aunque el usuario insista | Seguridad y responsabilidad legal |
| **Revisión humana de cada guía** | Un matriculado revisa la guía base antes de publicarla | Es la diferencia con todas las apps de la ronda 2 |
| **Registro de preguntas sin respuesta** | Lo que la base no cubre queda anotado | Indica qué guía escribir después |

## 3. Qué modelo de IA usar y cuánto cuesta

Precios actuales de la API de Claude (por millón de tokens; un token es aproximadamente ¾ de palabra):

| Modelo | Entrada | Salida | Para qué |
|---|---|---|---|
| **Claude Opus 5.5** (el más capaz de uso general) | US$ 4 | US$ 20 | Armar y revisar guías nuevas (trabajo interno, pocas veces) |
| **Claude Sonnet 5.5** | US$ 2 | US$ 10 | Opción intermedia para responder a usuarios |
| **Claude Haiku 5.5** (el más barato) | US$ 0,10 | US$ 0,50 | Responder a usuarios en volumen, si la calidad alcanza |

**Cuenta de una consulta típica** (supuestos: la guía pesa unos 8.000 tokens, la pregunta 500 y la
respuesta 1.500; la guía queda en caché, que cuesta cerca del 10% del precio normal):

| Modelo | Costo aproximado por consulta | 10.000 consultas por mes |
|---|---|---|
| Opus 5.5 | ~US$ 0,035 | ~US$ 350 |
| Sonnet 5.5 | ~US$ 0,017 | ~US$ 170 |
| Haiku 5.5 | ~US$ 0,001 | ~US$ 10 |

*(Son estimaciones; el razonamiento interno del modelo suma tokens de salida. Hay que medirlo con
consultas reales.)*

**Recomendación:** empezar con **Opus 5.5** para todo mientras hay pocos usuarios (la calidad importa
más que el costo al principio, y a esa escala son pocos dólares), y **probar** si Sonnet 5.5 o Haiku 5.5
dan la misma calidad en las respuestas a usuarios antes de cambiar. La decisión de bajar de modelo es
del usuario, con datos.

## 4. Cómo armar la base de guías (el verdadero trabajo)

Cada guía es un documento con siempre la misma estructura:

1. **Trabajo**: "Colocar un bidet con grifería monocomando".
2. **Semáforo**: verde, amarillo o rojo, y por qué.
3. **Lo que varía** (preguntas para el usuario, con fotos de ayuda): medida de rosca, tipo de caño,
   si trae o-ring, tipo de piso…
4. **Lo universal**: cortar la llave de paso, limpiar el caño antes de conectar…
5. **Materiales y herramientas**, con **medidas y nombres argentinos**, y qué cambia según cada variable.
6. **Pasos**, con advertencias de seguridad en el paso que corresponde.
7. **Errores comunes** (lo que te dicen los ferreteros y los plomeros).
8. **Fuentes**: manual del fabricante, ficha técnica y quién la revisó.

**Cómo producirlas rápido:** Opus 5.5 escribe un primer borrador a partir del manual del fabricante y
de la experiencia del usuario; un matriculado lo revisa y corrige. **La IA acelera, el humano verifica.**

**Por dónde empezar:** las 10 preguntas más comunes que junten los ferreteros (ronda 3), todas en zona
verde de plomería (ronda 4).

## 5. Qué puede armar una persona sola (y con qué)

| Pieza | Herramienta | ¿El usuario la sabe usar? |
|---|---|---|
| App web que funciona en el celular | React (lo que usó en su tienda) | ✅ Sí |
| Base de datos de guías y usuarios | Firebase (lo que usó en su tienda) | ✅ Sí |
| IA | API de Claude | Nuevo, pero se aprende rápido con ayuda de IA |
| Lista de compras | Links de afiliado de Mercado Libre | Fácil |
| Envío por WhatsApp | Link "wa.me" con el texto armado | Fácil |

**Primera versión realista:** una web, sin app en las tiendas, con 5 guías verificadas de plomería.
Se puede tener en pocas semanas de trabajo con ayuda de IA para programar.
*(Es una estimación: depende de las horas que pueda dedicarle.)*

## 6. Riesgos técnicos
1. **Que la IA igual se equivoque.** Mitigación: guía verificada, citas, salidas estructuradas y la
   aclaración visible de que no reemplaza a un profesional.
2. **Que la base quede corta** (el usuario pregunta algo que no está). Mitigación: responder "no está
   cubierto" y usar esas preguntas como lista de próximas guías.
3. **Dependencia de un solo proveedor de IA.** Mitigación: la base de guías es propia y se puede usar
   con cualquier modelo.

## Fuentes
- Documentación de la API de Claude (precios de modelos actuales, citas sobre documentos, salidas
  estructuradas y caché de prompts), consultada desde la referencia oficial del SDK el 23 de octubre de 2026.
- Rondas anteriores: [ronda 2](ronda-02-existe-algo-parecido.md) (por qué las apps actuales fallan),
  [ronda 3](ronda-03-como-ganar-plata.md) (ferreteros y afiliados), [ronda 4](ronda-04-lo-especifico-de-argentina.md)
  (semáforo y fuentes confiables).

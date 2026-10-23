# Ronda 4 — Lo específico de Argentina (y por qué es el corazón de la app)

Fecha: 23 de octubre de 2026, 12:20 (Argentina).

## Respuesta corta
- **Mi propia búsqueda confirmó el problema que planteó el usuario.** Al preguntar por roscas y
  selladores, los resultados mezclaron España, Chile y Alemania, y la equivalencia entre caño de
  termofusión y rosca (20 mm = 1/2") salió como "conocimiento general no verificado". **Si a un
  buscador y a una IA les cuesta, a una persona también. Ahí está el valor de la "fuente madre".**
- **Hay límites legales claros**: gas, siempre con gasista matriculado; electricidad, las
  instalaciones nuevas y el tablero requieren un profesional habilitado que firme. La app tiene que
  funcionar como un **semáforo**: verde (lo hacés vos), amarillo (con cuidado y estos pasos) y rojo
  (llamá a un matriculado).
- **La seguridad no es un detalle**: se citan unas **1.000 muertes por año** por fallas eléctricas
  y que **el 75% de los hogares tiene una instalación eléctrica deficiente** (cifras de asociaciones,
  no oficiales).

## 1. Normas y quién puede hacer qué

### Electricidad
- **Norma técnica de referencia:** la **AEA 90364** (Asociación Electrotécnica Argentina) define
  cuándo una instalación eléctrica en un inmueble se considera segura. Varias provincias adhieren
  (por ejemplo, Córdoba con su Ley de Seguridad Eléctrica desde 2017).
- **Para pedir un suministro nuevo** (Edenor y Edesur, bajo el ENRE), se exige una **Declaración de
  Conformidad de Instalación (DCI)** según la AEA 90364, firmada por un profesional (Resolución
  ENRE 225/11).
- **En CABA**, la habilitación de electricistas la otorga el **COPIME**. La Resolución 95/2026 mantiene
  a los "idóneos instaladores", pero **no pueden firmar cualquier documentación técnica**.
- *(No pude confirmar qué dice exactamente la Ley 6143 de CABA ni el requisito de disyuntor por norma.
  Hay que consultarlo con un electricista matriculado o con el COPIME.)*

### Gas
- **Siempre con gasista matriculado.** El ENARGAS ordenó en 2022 (Resolución 219/2022) un
  **registro nacional de instaladores matriculados** y les exige seguro de accidentes y de
  responsabilidad civil. Desde enero de 2026, el usuario tiene que registrarse en el portal de su
  distribuidora con una declaración jurada para conectarse.
- *(Las multas por trabajar sin matrícula que encontré, de $500.000 a $2.000.000, vienen de un sitio
  poco confiable. Hay que verificarlas en la norma NAG 200 del ENARGAS.)*

### Agua y sanitarios
- **No encontré una exigencia de matrícula** para cambios domésticos simples (bidet, canilla,
  mochila). Es el terreno ideal para la app: **mucha demanda, poco riesgo legal**.

## 2. El semáforo que tendría que tener la app

| Color | Qué incluye (ejemplos) | Qué hace la app |
|---|---|---|
| 🟢 Verde | Cambiar una canilla, colocar un bidet, armar o cambiar el mecanismo de la mochila, destapar un sifón, colgar un estante, armar muebles | Guía completa paso a paso, con las preguntas sobre tu caso |
| 🟡 Amarillo | Cambiar un tomacorriente o una lámpara **cortando la térmica**, instalar un termotanque eléctrico, trabajar en altura | Guía con **chequeos de seguridad obligatorios** antes de cada paso y aviso de cuándo parar |
| 🔴 Rojo | **Cualquier cosa de gas**, el tablero eléctrico, una instalación eléctrica nueva o la puesta a tierra | **No enseña a hacerlo.** Explica por qué es peligroso y deriva a un matriculado. *Ahí entra el modelo de derivación de la ronda 3.* |

*(La clasificación exacta tiene que validarla un electricista y un gasista matriculados antes de publicarla.)*

## 3. Lo que varía y lo que es universal (ejemplos argentinos)

Esta es la idea central del usuario. Algunos ejemplos que la app tendría que preguntar o explicar
**antes de empezar**. Son de conocimiento general y **cada dato tiene que verificarse con las fichas
técnicas de los fabricantes antes de publicarse**:

| Tema | Lo que varía (hay que preguntarlo) | Lo que suele ser universal |
|---|---|---|
| **Roscas de agua** | Si la conexión es de 1/2" o de 3/4"; si el caño es de termofusión, epoxi, hierro galvanizado o PVC | En Argentina se usa rosca tipo BSP (no la NPT de EE.UU.). Termofusión de 20 mm ≈ rosca de 1/2", de 25 mm ≈ 3/4" y de 32 mm ≈ 1" *(a verificar)* |
| **Sellado de roscas** | **Si la pieza trae o-ring o junta de goma**: en ese caso no lleva teflón en esa unión. Si la rosca es metálica o plástica. Si es agua o gas | Teflón para agua en uniones que se desarman; sellarroscas o teflón de alta densidad para uniones fijas. **El gas siempre lo resuelve un matriculado** |
| **Mochila del inodoro** | Modelo de inodoro y de mochila (apoyada o colgada), salida a piso o a pared, medida del corrugado o de la conexión | Cortar la llave de paso y vaciar la mochila antes de empezar |
| **Electricidad** | Si hay disyuntor diferencial, si hay puesta a tierra, sección de los cables existentes | **220 V y 50 Hz**; enchufe tipo I (tres patas planas, norma IRAM 2073); **siempre cortar la térmica** |
| **Pared** | Ladrillo hueco, ladrillo macizo, hormigón o durlock | El tarugo y el tornillo dependen de la pared y del peso |

## 4. Vocabulario argentino (por qué una app de afuera no sirve)
Términos que una app de EE.UU. o de España no usa, o usa con otro nombre (a ampliar y verificar):
- **Plomería:** termofusión, caño epoxi, flexible, llave de paso, sopapa, sifón, corrugado, mochila,
  sellarroscas, cáñamo, codo, cupla, buje de reducción, tapón.
- **Electricidad:** térmica, disyuntor (diferencial), jabalina (puesta a tierra), toma, ficha,
  caño corrugado (para cables), caja de luz, "fase y neutro".
- **Construcción:** durlock, tarugo, revoque, carpeta, contrapiso, cal, plasticor.
- **Marcas que la gente nombra** (y que la app tiene que reconocer): FV, Awaduct, Hidro3, Saladillo,
  Tigre, Acqua System, Sika, Fischer y otras. *(Lista a verificar; no implica acuerdos con esas marcas.)*

En España se dice "fontanería" y "grifo", en México "plomería" y "llave", en EE.UU. todo es en
pulgadas, 110 V y rosca NPT. **Una respuesta pensada para otro país puede llevar a comprar mal o a un
accidente.**

## 5. De dónde sacar información confiable (para alimentar la app)
1. **Fichas técnicas y manuales de fabricantes** (Nicoll, por ejemplo, publica medidas y la
   certificación de sus piezas de termofusión). Es la fuente más confiable para medidas.
2. **Normas**: AEA 90364 (electricidad) y NAG 200 del ENARGAS (gas), aunque solo para marcar los límites.
3. **Revisión de un matriculado**: un electricista y un plomero que revisen cada guía antes de
   publicarla. *Puede ser un acuerdo: revisan a cambio de recibir las derivaciones.*
4. **Ferreteros**: las preguntas que les hacen todos los días (ronda 3).
5. **La experiencia propia del usuario**: cada proyecto suyo (el tráiler, el bidet) se documenta y
   se convierte en guía.

## 6. Riesgo legal para la app (a consultar con un abogado)
- Si alguien sigue una guía y se lastima o rompe algo, ¿quién responde? Hace falta:
  términos y condiciones claros, el semáforo, no dar instrucciones en zonas rojas, y guías
  revisadas por matriculados.
- Ley de Defensa del Consumidor: si la app cobra, responde como prestadora de un servicio.

## Fuentes
- [Editores – La Ley de Seguridad Eléctrica (AEA)](https://editores-srl.com.ar/sites/default/files/ie327_aea_ley_seguridad_electrica.pdf)
- [Editores – Seguridad eléctrica (Fazzito)](https://www.editores-srl.com.ar/sites/default/files/ie296_fazzito_seguridad_electrica.pdf)
- [Derecho en Zapatillas – Matrícula de electricista (2026)](https://www.derechoenzapatillas.com/2026/matricula-de-electricista/)
- [AEA 90364 parte 7 sección 722](https://surtidores.com.ar/wp-content/uploads/2026/08/AEA-90364-7-722-1.pdf)
- [Cronista – Gasistas matriculados: registro unificado](https://www.cronista.com/economia-politica/gasistas-matriculados-crean-un-registro-unificado-con-los-requisitos-obligatorios-para-contratar/)
- [LM Neuquén – Los gasistas matriculados deberán contratar seguro](https://mase.lmneuquen.com/gas/los-gasistas-matriculados-deberan-contratar-seguro-n918027)
- [Diario Jornada – Nuevas pautas para la conexión de gas (2026)](https://diariojornada.com.ar/409855/economia/establecen_nuevas_pautas_para_la_conexion_a_la_red_de_gas)
- [Sodimac Uruguay – Tubo termofusión 25 mm x 1/2" (Nicoll)](https://www.sodimac.com.uy/sodimac-uy/product/1919555/tubo-termofusion-rosca-hembra-25-mm-x-1-2/1919555/)
- [Easy Argentina – Espiga rosca hembra 1/2"](https://easy.com.ar/espiga-ppl-rosca-hembra-1-2-ips/p)
- [Todoexpertos – Teflón o hilo sellador](https://www.todoexpertos.com/preguntas/8pch3epx9n9ite4q/que-utilizar-para-sellar-tuberias-teflon-o-hilo-sellador)
- [El Ancasti – El 75% de los hogares tiene una conexión deficiente](https://www.elancasti.com.ar/informacion-general/el-75-los-hogares-argentina-tiene-una-conexion-deficiente-n527426)
- [Editores – AIECh: seguridad eléctrica](https://www.editores-srl.com.ar/sites/default/files/ie341_aiech_seguridad_electrica.pdf)
- [CADIEEL – Riesgo alarmante en las conexiones eléctricas](https://editores-srl.com.ar/print/8197)

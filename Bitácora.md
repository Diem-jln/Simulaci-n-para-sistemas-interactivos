# Bitácora Unidad 1: Aleatoriedad
**Estudiante:** Diego Sebastian Molina Julian
**ID:** 000621964
**Curso:** Simulacion Para Sistemas Interactivos

---

##  Actividad 01: La aleatoriedad 
> *Reflexiones sobre los videos de Casey Reas, Refik Anadol, Tyler Hobbs.*

* **Reflexión principal:**
Al revisar el trabajo y la filosofía de artistas como Tyler Hobbs, Refik Anadol y  Casey Reas, me queda claro que en el arte generativo el concepto de aleatoriedad está muy lejos de ser considerado como caos o desorden. Más bien, se comprende mas como una **herramienta compositiva y principio generativo**.

De los eleemntos proporcionados, destacaria tres ideas fundamentales:

1. **La aleatoriedad controlada aporta naturalidad:** En sus ensayos, Hobbs nos deja claro que la aleatoriedad "uniforme" suele ser visualmente aburrida, ya que distribuye todo por igual y visualmente genera una textura muy parecida a la "estática" de una tele vieja. Lo verdaderamente fascinante ocurre cuando se aplica la *distribución de probabilidad no uniforme*. Ya que sesgar la aleatoriedad (haciendo que ciertos colores o tamaños sean más probables que otros), se puede imitar la variación orgánica que encontramos en areas naturales.

2. **El uso de código como medio expresivo:** Como nos muestra Reas, dibujar con código cambia los limites del artista. Ya no hablamos de pintar un cuadro estático con pintura, sino de diseñar y estableceer un **sistema de reglas**. La aleatoriedad se implanta en estas reglas, todo con la finalidad de que el sistema produzca resultados emergentes e impredecibles.

3. **Los datosy el azar algorítmico:** Anadol logra llevar estos sistemas a otra escala interactuando con multiples conjuntos de datos e incorporando inteligencia artificial. En sus obras, el uso de ruido algorítmico y variaciones fluidas permite que la información dura y estructurada adquiera formas líquidas y que se mantienen en constante mutación. 

Puedo concluir esta actividad diciendo que: el artista ya no crea la obra final, sino que el artista es quien crea el ecosistema que la produce. Y la aleatoriedad se convierte en el motor que da vida a cada ejecución de ese sistema, asegurando que aunque existan límites definidos, el resultado sea infinito.

---

## Actividad 02: Caminatas Aleatorias
> *Análisis del código Example 0.1: A Traditional Random Walk.*


Al estudiar el código base del *Random Walk* tradicional, he podido identificar los siguientes conceptos clave sobre su funcionamiento y estructura:

1. **Estructura Orientada a Objetos (Clase Walker):** El código encapsula la lógica en una entidad o "agente". Este agente tiene un *estado* (su posición en el canvas con las variables `x` y `y`) y un *comportamiento* (las funciones para mostrarse `display()` y moverse `step()`). Esto hace que el código sea modular y escalable si quisiéramos agregar múltiples caminantes.
2. **Aleatoriedad Uniforme y Decisiones Discretas:** En la función `step()`, el caminante toma una decisión en cada fotograma sobre hacia dónde moverse (arriba, abajo, izquierda o derecha). Esto se logra generando un número aleatorio entero. Como la función de números aleatorios básica devuelve valores con una **distribución uniforme**, todas las direcciones tienen exactamente la misma probabilidad de ser elegidas (25% cada una, o un porcentaje igual si se incluyen las diagonales).
3. **El Comportamiento Emergente (Movimiento errático):** Visualmente, el resultado es una línea que traza un camino errático y tembloroso que recuerda al polvo flotando en el aire o al movimiento browniano. Una observación importante es que, como no hay ninguna tendencia o sesgo (todas las opciones son igual de probables), el caminante tiende a quedarse merodeando cerca de su punto de origen o de su posición actual durante mucho tiempo, sin lograr "viajar" grandes distancias de manera eficiente.

**Conclusión:** Este ejemplo demuestra cómo reglas de decisión muy simples y estrictamente probabilísticas, ejecutadas repetidamente en un bucle, generan un patrón visual impredecible que simula fenómenos básicos de la naturaleza.
---

## Actividad 03: Distribuciones de Probabilidad

### 1. Diferencia conceptual
* **Distribución Uniforme:** Ocurre cuando todos los resultados posibles tienen exactamente la misma probabilidad de suceder. Es el equivalente a lanzar un dado de 6 caras; cada número tiene un 16% de probabilidad de salir. En programación, la función estándar `random()` suele generar una distribución uniforme, lo que en una caminata aleatoria significa que moverse arriba, abajo, izquierda o derecha tiene un 25% de posibilidades cada uno, resultando en un movimiento sin una dirección aparente.
* **Distribución No Uniforme:** Ocurre cuando ciertos resultados tienen una probabilidad mayor de suceder que otros. Es como lanzar un dado trucado para que el número 6 salga más veces. En el arte generativo y la simulación, usar distribuciones no uniformes nos permite introducir tendencias y comportamientos en un sistema que sigue siendo aleatorio.

### 2. Implementación: Tendencia a la derecha
* **Enlace al p5.js:** https://editor.p5js.org/natureofcode/sketches/5C69XyrlsR
* **Comentarios:** en lugar de poner todas las opciones por igual, aumente el rango matemático de la derecha. El caminante sigue moviéndose de forma aleatoria, pero ahora las matemáticas están a favor de avanzar hacia la derecha en la pantalla..

---

## Actividad 04: Distribución Normal
* **Enlace al p5.js:** https://editor.p5js.org/Diem-jln/sketches/1nw4LNZKh
* **Descripción de la visualización:**
Se me ocurrio que en lugar de hacer una "salpicadura" unidimensional de puntos negros que se acumulan horizontalmente, una forma de representarlo de manera mas llamativa era hacerlo circular.

---

## Actividad 05: Distribución Personalizada (Lévy Flight)
* **Enlace al p5.js:** https://editor.p5js.org/Diem-jln/sketches/whrucBYyq
* **Resultados esperados:** Específicamente, esperaba observar manchas densas de tinta donde el caminante pasa mucho tiempo dando pasos cortos y explorando exhaustivamente un área pequeña. Luego, esperaba ver líneas rectas largas y esporádicas que conectaran con esas manchas 
* **Justificación:** lo acomode de modo que hay un 99% de probabilidad de dar pasos cortos y 1% de dar un salto grande porque es la manera mas sencilla y efectiva de imitar a la naturaleza..

---

## Actividad 06: Ruido Perlin
* **Enlace al p5.js:** https://editor.p5js.org/Diem-jln/sketches/TUSVJ_2Jl
* **Resultados esperados:** Mi intension era que al correr el codigo pudiera ver lo mas parecido a una criatura "viva" aprovechando que los bordes estarian en cosntante movimiento
* **Justificación de la visualización:** Quería demostrar visualmente la característica más importante del ruido Perlin: la continuidad.

---

##  Actividad 07: Reto de diseño - Navegar la incertidumbre
> *Diseño de una experiencia generativa en tiempo real (Formato 9:16) para un festival de ciencia.*

### 1. Enlace al Prototipo Final
https://editor.p5js.org/Diem-jln/sketches/Q7c9WJFzT

### 2. Intención Conceptual
> *¿Cómo tradujiste cada concepto a reglas visuales y de comportamiento?*
* **Posibilidad:** se le dio la capacidad a cada semi circulo de rotar libremente hacia cualquier angulo.
* **Tendencia:** Utilizando Ruido Perlin. Estas pequeñas fuerzas matemáticas, continuas y repetitivas, obligan a los semi circulos a alinearse gradualmente creando patrones visuales que dirigen el flujo general.
* **Normalidad:** : Implementando una oscilación Gaussiana. Ya que unque la corriente intente llevarlos, cada dial tiene un leve temblor, y estadísticamente, la gran mayoría se desvía muy poco de la corriente principal.
* **Excepción:** Programando saltos aleatorios mediante el algoritmo de Vuelo de Lévy. De manera infrecuente pero garantizada, un "glitch" color ámbar interrumpe el patrón.
* **Influencia (Interacción):** Convirtiendo el raton en una fuente de "calor". Al acercarse, el espectador no controla los diales manualmente, pero su proximidad aumenta la rotación, revela colores ocultos y, a nivel general, desestabiliza el sistema acelerando el tiempo y duplicando la probabilidad de que ocurran "excepciones".

### 3. Proceso de Desarrollo
* **Conceptos técnicos integrados:** 1. Ruido Perlin: Utilizado para dirigir la Tendencia. 2. Distribución Gaussiana: Aplicada para la Normalidad 3. Vuelos de Lévy: Utilizado para la Excepción.
* **Experimentos y versiones intermedias:** 
  *V1. https://editor.p5js.org/Diem-jln/sketches/_MtgsysGc
  * V2: https://editor.p5js.org/Diem-jln/sketches/2fl45bEKU.
* **Decisiones tomadas y alternativas descartadas:**
  * Descarte la posibilidad de mover objetos por la pantalla de manera libre para ahorrar procesamiento.
* **Dificultades y soluciones:**
  * El editor web detenía el código creyendo por error que teníamos un bucle infinito en la estadística. Solución: Escribir el comando // noprotect en la primera línea del archivo.

### 4. Uso de IA Generativa
* **Prompt/Uso:** Lo primero que le pedí a la IA fue ayuda para aterrizar el concepto que tenía en mente y visualizarlo en una estructura básica de código. A partir de ahí, utilicé la IA como un asistente de programación para escalar iteraciones, resolver cuellos de botella matemáticos y ajustar el sistema a la estética y comportamiento exactos que buscaba.
* **Cambios realizados:** 1.La IA inicialmente sugirió sistemas de partículas convencionales moviéndose por la pantalla. Lo descarté y reestructuré el código por completo hacia una matriz fija (la cuadrícula de semicírculos) para lograr el efecto de ilusión óptica
* 2. El código base de la IA para "Vuelos de Lévy" estaba pensado para mover una partícula en el espacio. Yo modifiqué esa lógica para que, en su lugar, seleccionara posiciones aleatorias en la cuadrícula y generara los "cortocircuitos" de color.

### 5. Tabla de Autoevaluación
> *Completa marcando con una "X" la casilla correspondiente y escribiendo la evidencia.*

| Criterio | Cumplo | No cumplo | Evidencia |
| :--- | :---: | :---: | :--- |
| **Encargo completo:** interpreto los cinco momentos dentro de un mismo sistema visual. | [ ] | [ ] |
| **Simulación con intención:** utilizo al menos tres conceptos de la unidad para comunicar las ideas del encargo. | [ ] | [ ] |
| **Interacción significativa:** la interacción modifica el comportamiento o las probabilidades del sistema, que también funciona sin intervención. | [ ] | [ ] |
| **Prototipo funcional:** la experiencia puede ejecutarse y recorrerse completa sin errores que impidan comprenderla. | [ ] | [ ] |
| **Proceso documentado:** la bitácora evidencia avances, decisiones, dificultades, soluciones, uso de IA y enlace al prototipo. | [ ] | [ ] |









# Bitácora Unidad 2: Movimiento
**Estudiante:** Diego Sebastian Molina Julian
**ID:** 000621964
**Curso:** Simulación Para Sistemas Interactivos

---

## Actividad 01: Max Cooper
> *Análisis del trabajo de Max Cooper y el proyecto "The Shape Of Memory".*

* **Reflexión principal:**
Al revisar el trabajo de Max Cooper, comprendo que la tecnología y el código no son el tema principal de la obra, sino el medio para pensar y materializar conceptos abstractos. Lo más destacado de su enfoque es cómo diseña simultáneamente una idea, una estructura y una experiencia. 

En el caso de *The Shape Of Memory*, el uso de *Gaussian splats* para transformar imágenes de recuerdos de la audiencia en modelos 3D no es una simple decisión estética. Los artefactos, pérdidas y deformaciones del modelo tridimensional operan como una metáfora perfecta de cómo la memoria humana se fragmenta, se mezcla y se reescribe cada vez que recordamos algo. 

**Conclusión:** En la simulación interactiva, la técnica debe subordinarse a la intención. El objetivo no es solo lograr que algo se vea "bien", sino construir un sistema cuyas reglas hagan perceptible una experiencia o idea.

---

## Actividad 02: Motion 101
> *Revisión del algoritmo de movimiento de The Nature of Code.*

* **Concepto clave:** 
El estudio del movimiento en esta unidad trasciende el simple hecho de desplazar un objeto en la pantalla. Aplicando los principios de *Motion 101* (posición, velocidad y aceleración), el objetivo es establecer reglas físicas fundamentales que nos permitan diseñar **relaciones que produzcan comportamiento**. La aceleración actúa como el puente donde las fuerzas externas (intenciones de diseño) influyen en la velocidad y, por ende, en el destino final de la entidad.

---

## Actividad 03: Particle Life
> *Análisis de sistemas de partículas con relaciones asimétricas (Jeffrey Ventrella / Tom Mohr).*

* **Reflexión sobre el comportamiento emergente:**
Al explorar *Clusters* de Ventrella y *Particle Life* de Tom Mohr, resulta fascinante observar cómo reglas individuales extremadamente simples desencadenan resultados globales de alta complejidad. La clave de este comportamiento reside en las **relaciones asimétricas**. 

En la física clásica newtoniana, toda acción tiene una reacción igual y opuesta (si A atrae a B, B atrae a A). Sin embargo, en *Particle Life*, podemos programar que la partícula A sea atraída por la B, pero que la B huya de la A. Esta asimetría es la que produce la ilusión de persecuciones, agrupamientos y formas que parecen estar vivas ("Particle Life"). Las trayectorias no están animadas ni predefinidas, emergen de la constante negociación de distancias y fuerzas de atracción/repulsión en la matriz.

---

## Actividad 04: Diseño Generativo
> *Operaciones de la mentalidad generativa.*

* **Idea central:** El diseño generativo consiste en diseñar un sistema capaz de producir diseños, en vez de diseñar directamente una única pieza final. Ya no pregunto "cómo animo esto", sino "¿Qué quiero comunicar, y qué sistema de relaciones puede materializarlo?".

Para lograrlo, es necesario articular las operaciones del sistema generativo: definir una intención clara, establecer las entidades (partículas), configurar sus relaciones (matriz de atracción/repulsión), definir las reglas de cambio por *frame*, e identificar qué permanece constante (invariantes) y qué cambia en cada ejecución (variabilidad).

---

## Actividad 05: Reto de diseño - Una contradicción en movimiento
> *Diseño de un sistema generativo inspirado en Particle Life que explora una tensión significativa.*

### 1. Enlace al Prototipo Final
https://diem-jln.github.io/particle-life/

### 2. Intención Conceptual
* **Tensión:** Quiero explorar la tensión entre `[CONCEPTO 1, ej. la necesidad de agruparse]` y `[CONCEPTO 2, ej. el miedo al contacto]`.
* **Manifestación esperada:** `[Explica brevemente cómo se ve esto en pantalla. Ej: "Espero que una población persiga constantemente a la otra para formar clústeres, pero al acercarse demasiado, la segunda población se disperse violentamente, creando un ciclo interminable de persecución y ruptura".]`

### 3. Diseño del Sistema (Reglas y Justificación)

* **Tipos y Cantidades:**
  * `[Tipo 1 / Color]:` `[Cantidad]` partículas. 
  * `[Tipo 2 / Color]:` `[Cantidad]` partículas.
  * `[Tipo 3 / Color]:` `[Cantidad]` partículas.
* **Matriz y Relaciones:** 
  * *Seleccioné* `[una relación específica, ej. que las rojas repelan fuertemente a las azules]` *porque quiero hacer perceptible* `[tu intención conceptual]`. *Espero que produzca* `[el comportamiento emergente, ej. que las azules formen anillos de contención alrededor de las rojas]`.
* **Parámetros Físicos:**
  * **Distancias de interacción:** `[Ej. Rango de influencia configurado a 50 pixeles]`.
  * **Fricción y velocidad máxima:** `[Ej. Fricción alta para evitar que las partículas salgan volando sin control y simulen estar en un medio viscoso]`.

### 4. Registro de Pruebas y Manifestaciones
* **Hallazgos durante el desarrollo:** `[Describe un problema técnico que tuviste y cómo lo solucionaste. Ej. "Al principio todas las partículas colapsaban en un solo punto, lo solucioné ajustando la fuerza de repulsión a corta distancia".]`
* **Lo diseñado vs. Lo emergente:** Lo que diseñé fue `[tu matriz de reglas]`, lo que emergió de forma imprevista fue `[una forma específica que hacen las partículas, ej. "forman estructuras celulares con un núcleo que palpita"]`.

### 5. Tabla de Autoevaluación
> *aporte = valoración × peso ÷ 100*

| Criterio | Peso | Valoración | Aporte | Evidencia / Sustento |
| :--- | :---: | :---: | :---: | :--- |
| **La intención es clara y perceptible en el comportamiento.** | 20% | `[0-100]`% | `[Resultado]` | `[Justifica brevemente basado en tu código]` |
| **Los tipos, cantidades, matriz y parámetros están justificados desde la intención.** | 25% | `[0-100]`% | `[Resultado]` | Se documentó cada decisión en la sección 3. |
| **Comprendo y puedo modificar el funcionamiento técnico del sistema.** | 20% | `[0-100]`% | `[Resultado]` | `[Ej. Implementé y modifiqué el cálculo de distancias y fuerzas]` |
| **El sistema produce variaciones con una identidad reconocible.** | 15% | `[0-100]`% | `[Resultado]` | Sin importar la semilla inicial, la tensión conceptual siempre ocurre. |
| **Experimenté, comparé, seleccioné y descarté con criterios claros.** | 10% | `[0-100]`% | `[Resultado]` | Evidenciado en el registro de pruebas. |
| **Puedo distinguir y sustentar lo diseñado y lo emergente.** | 10% | `[0-100]`% | `[Resultado]` | Evidenciado en la sección 4 de esta bitácora. |
| **TOTAL (Nota propuesta)** | **100%** | | **`[TU NOTA / 5.0]`** | |





# Bitácora Unidad 3: Fuerzas
**Estudiante:** Diego Sebastian Molina Julian
**ID:** 000621964
**Curso:** Simulación Para Sistemas Interactivos

---

## 🔗 Entregable Principal
* **Instrumento funcional (Modo LAB y PERFORMANCE):** [Prototipo Unidad 3](https://diem-jln.github.io/Unidad3/)

---

## Actividad 01: Referentes para la unidad
> *Reflexiones sobre Robert Hodgin, Lumicles y Scribble (Golan Levin).*

* **Reflexión principal:**
Al analizar los referentes de esta unidad, comprendí que diseñar un **sistema** no es lo mismo que diseñar un **instrumento**. El sistema (como se ve en el trabajo de Robert Hodgin o Lumicles) establece el universo físico, las reglas de las partículas y las fuerzas matemáticas latentes. Sin embargo, el instrumento surge cuando se exponen controles expresivos que permiten a un ser humano **interpretar** esas fuerzas en vivo (como en Scribble). 

La obra no es una animación pre-renderizada ni un visualizador que reacciona de forma automática a los picos de audio (FFT). Lo que **emerge** visualmente es el resultado directo de una cadena de decisiones humanas: escucho la música, tomo una decisión interpretativa, acciono un control, esto modifica una fuerza en la simulación, y finalmente las partículas reaccionan a esa nueva física.

---

## Actividad 02: Laboratorio de Fuerzas (Mapa y Verificación)

### 1. Mapa del Sistema
Para poder utilizar la IA generativa de forma rigurosa y no perder el control de mi código (usando Three.js, TSL y WebGPU), mapeé las responsabilidades del repositorio base:

* **Estado:** Se encuentra en los *buffers* de la GPU (`positionBuffer`, `velocityBuffer`). Representa dónde está cada partícula y hacia dónde se dirige.
* **Fuerzas:** Se calculan en el bloque `force` del compute. Son las reglas matemáticas (vectores) que se suman en cada fotograma.
* **Integración:** Utilizando el método de Euler semiimplícito, la fuerza total modifica primero la aceleración, luego la velocidad, y esa velocidad actualizada es la que finalmente cambia la posición.
* **Render:** Se utiliza `InstancedMesh` para dibujar miles de partículas reutilizando la misma geometría y material, leyendo los datos directamente de la GPU sin colapsar el procesador.
* **Controles (Uniforms):** Son el puente entre la interfaz (JavaScript/HTML) y los cálculos matemáticos en la GPU (TSL).

### 2. Registro de Pruebas (5 Escenarios Base)
Antes de construir mi instrumento, aislé y verifiqué las fuerzas fundamentales en el modo LAB siguiendo el ciclo: *predicción → ejecución → observación → comparación*.

* **1. Inercia:** Al no aplicar fuerzas, predije que la velocidad conservaría su dirección. *Observación:* Las partículas mantuvieron su vector inicial sin alteraciones.
* **2. Fuerza constante (+X):** Predije que al aplicar un vector positivo en X, el conjunto se desplazaría a la derecha. *Observación:* El sistema se comportó como si hubiera un viento constante arrastrándolas.
* **3. Atracción:** Predije que una fuerza radial positiva empujaría la aceleración hacia el centro. *Observación:* Colapsaron hacia el atractor.
* **4. Repulsión:** Al invertir el signo a negativo, predije que huirían del centro. *Observación:* Se expandieron alejándose del punto de origen.
* **5. Vórtice:** Predije que al agregar un vector tangencial, empezarían a rotar. *Observación:* Se generó un flujo circular, emergiendo un comportamiento de remolino sin dibujar una ruta fija.

---

## Actividad 03: Encargo de Diseño (Instrumento Visual)
> *Interpretación en vivo de "LesAlpx" de Floating Points.*

### 1. Ficha de Fuerzas
Para este instrumento, diseñé el siguiente sistema de fuerzas. No reaccionan al audio automáticamente; yo las conduzco.

* **Fuerza Central 1: `[Nombre de tu fuerza, ej. Campo Gravitacional Intermitente]`**
  * **Ecuación / Dirección:** `[Explica brevemente la regla, ej. Fuerza radial que atrae hacia un punto dinámico controlado por el mouse, con atenuación por distancia]`.
  * **Predicción y Diseño:** Diseñé esta fuerza porque `[Justifica tu intención, ej. quería simular la tensión de los sintetizadores acumulándose antes del beat]`.
  * **Prueba aislada:** Al aislarla en el LAB, verifiqué que `[Qué observaste al probarla sola]`.

* **Fuerza Central 2: `[Nombre de tu fuerza 2, ej. Fricción Densa]`**
  * **Ecuación / Dirección:** `[Explica brevemente la regla, ej. Fuerza que se opone a la velocidad multiplicada por un factor variable]`.
  * **Predicción y Diseño:** La incluí porque `[Ej. necesitaba frenar el sistema abruptamente en los silencios de la canción]`.

### 2. Controles Expresivos (El Instrumento)
Seleccioné pocos parámetros, pero con alto potencial expresivo:
1. `[Control 1, ej. Slider de Intensidad del Vórtice]`: Me permite `[Qué haces con él durante la canción]`.
2. `[Control 2, ej. Posición X/Y del atractor (Mouse)]`: Me permite `[Qué haces con él]`.
3. `[Control 3, ej. Toggle de Repulsión Máxima]`: Lo uso como un "golpe" visual para los momentos de ruptura en la pista.

### 3. Score Visual e Interpretación ("LesAlpx")
Mi relación con la pieza se resume en: *escucha → intención → score → interpretación → fuerzas → comportamiento*.

* **0:00 - 1:15 (Tensión inicial):** `[¿Qué haces aquí? Ej. Mantengo la fuerza de atracción muy leve, generando una acumulación lenta y caótica en el centro.]`
* **1:15 - 3:30 (Desarrollo y Ruptura):** `[Ej. Activo la repulsión y el vórtice gradualmente. Hago movimientos amplios con el puntero para crear corrientes fuertes acompañando los sintetizadores.]`
* **3:30 - Final (Dispersión):** `[Ej. Aumento la fricción al máximo y apago las atracciones, dejando que las partículas floten y se detengan poco a poco hasta desaparecer.]`

---

## Bitácora de Inteligencia Artificial (IA)
> *Ciclo de especificación, verificación y modificación.*

* **Prompt / Intención Inicial:** Le pedí a la IA `[Ej. cómo escribir en sintaxis TSL una fuerza que repeliera a las partículas solo si estaban a menos de 10 unidades de distancia]`.
* **Archivos modificados:** La IA propuso modificar el bloque de fuerzas en `createSimulation.js`.
* **Verificación y Corrección:** `[Ej. El código de la IA funcionaba, pero creaba una fuerza infinita que hacía desaparecer las partículas. Lo corregí agregando un parámetro límite (clamp) para suavizar la aceleración a distancias muy cortas.]`
* **Decisión final:** Conservé `[Ej. la lógica del cálculo de distancia]`, pero descarté `[Ej. la ecuación de velocidad que propuso la IA porque no usaba la integración de Euler que requiere nuestro proyecto]`.

---

## Actividad 04: Autoevaluación Ponderada

| Criterio | Peso | Valoración | Aporte | Evidencia / Sustento |
| :--- | :---: | :---: | :---: | :--- |
| **Trazabilidad y comprensión del sistema** | 25% | `[0-100]`% | `[Resultado]` | Detallado en Actividad 02. Identifiqué los buffers y ubiqué dónde la IA modificó el `createSimulation.js`. |
| **Verificación del algoritmo de fuerzas** | 25% | `[0-100]`% | `[Resultado]` | Aislé las fuerzas base y la fuerza central de mi diseño, ejecuté predicciones y modifiqué parámetros conscientemente (ver Act. 02 y 03). |
| **Diseño de fuerzas e intención** | 20% | `[0-100]`% | `[Resultado]` | El comportamiento emerge de la suma de `[Fuerza 1]` y `[Fuerza 2]`, no hay trayectorias animadas fijas. |
| **Instrumento, score e interpretación** | 15% | `[0-100]`% | `[Resultado]` | Detallado en el Score Visual. No uso audioreactividad automática; opero los controles manualmente según mi escucha. |
| **Experimentación y criterio frente a la IA** | 10% | `[0-100]`% | `[Resultado]` | Evidenciado en la Bitácora de IA, donde rechacé código que rompía el modelo de Euler. |
| **Entrega técnica y documentación** | 5% | `[0-100]`% | `[Resultado]` | El enlace abre correctamente y presenta modos LAB y PERFORMANCE. |
| **TOTAL (Nota propuesta)** | **100%** | | **`[TU NOTA / 5.0]`** | |





# Bitácora Unidad 3: Fuerzas
**Estudiante:** Diego Sebastian Molina Julian
**ID:** 000621964
**Curso:** Simulación Para Sistemas Interactivos

---

## 🔗 Entregable Principal
* **Instrumento funcional (Modo LAB y PERFORMANCE):** [Prototipo Unidad 3](https://diem-jln.github.io/Unidad3/)

---

## Actividad 01: Referentes para la unidad
> *Reflexiones sobre Robert Hodgin, Lumicles y Scribble (Golan Levin).*

* **Reflexión principal:**
Al analizar los referentes de esta unidad, comprendí que diseñar un **sistema** no es lo mismo que diseñar un **instrumento**. El sistema (como se ve en el trabajo de Robert Hodgin o Lumicles) establece el universo físico, las reglas de las partículas y las fuerzas matemáticas latentes. Sin embargo, el instrumento surge cuando se exponen controles expresivos que permiten a un ser humano **interpretar** esas fuerzas en vivo (como en Scribble). 

La obra no es una animación pre-renderizada ni un visualizador que reacciona de forma automática a los picos de audio (FFT). Lo que **emerge** visualmente es el resultado directo de una cadena de decisiones humanas: escucho la música, tomo una decisión interpretativa, acciono un control, esto modifica una fuerza en la simulación, y finalmente las partículas reaccionan a esa nueva física.

---

## Actividad 02: Laboratorio de Fuerzas (Mapa y Verificación)

### 1. Mapa del Sistema
Para poder utilizar la IA generativa de forma rigurosa y no perder el control de mi código (usando Three.js, TSL y WebGPU), mapeé las responsabilidades del repositorio base:

* **Estado:** Se encuentra en los *buffers* de la GPU (`positionBuffer`, `velocityBuffer`). Representa dónde está cada partícula y hacia dónde se dirige.
* **Fuerzas:** Se calculan en el bloque `force` del compute. Son las reglas matemáticas (vectores) que se suman en cada fotograma.
* **Integración:** Utilizando el método de Euler semiimplícito, la fuerza total modifica primero la aceleración, luego la velocidad, y esa velocidad actualizada es la que finalmente cambia la posición.
* **Render:** Se utiliza `InstancedMesh` para dibujar miles de partículas reutilizando la misma geometría y material, leyendo los datos directamente de la GPU sin colapsar el procesador.
* **Controles (Uniforms):** Son el puente entre la interfaz (JavaScript/HTML) y los cálculos matemáticos en la GPU (TSL).

### 2. Registro de Pruebas (5 Escenarios Base)
Antes de construir mi instrumento, aislé y verifiqué las fuerzas fundamentales en el modo LAB siguiendo el ciclo: *predicción → ejecución → observación → comparación*.

* **1. Inercia:** Al no aplicar fuerzas, predije que la velocidad conservaría su dirección. *Observación:* Las partículas mantuvieron su vector inicial sin alteraciones.
* **2. Fuerza constante (+X):** Predije que al aplicar un vector positivo en X, el conjunto se desplazaría a la derecha. *Observación:* El sistema se comportó como si hubiera un viento constante arrastrándolas.
* **3. Atracción:** Predije que una fuerza radial positiva empujaría la aceleración hacia el centro. *Observación:* Colapsaron hacia el atractor.
* **4. Repulsión:** Al invertir el signo a negativo, predije que huirían del centro. *Observación:* Se expandieron alejándose del punto de origen.
* **5. Vórtice:** Predije que al agregar un vector tangencial, empezarían a rotar. *Observación:* Se generó un flujo circular, emergiendo un comportamiento de remolino sin dibujar una ruta fija.

---

## Actividad 03: Encargo de Diseño (Instrumento Visual)
> *Interpretación en vivo de "LesAlpx" de Floating Points.*

### 1. Ficha de Fuerzas
Para este instrumento, diseñé el siguiente sistema de fuerzas. No reaccionan al audio automáticamente; yo las conduzco.

* **Fuerza Central 1: `[Nombre de tu fuerza, ej. Campo Gravitacional Intermitente]`**
  * **Ecuación / Dirección:** `[Explica brevemente la regla, ej. Fuerza radial que atrae hacia un punto dinámico controlado por el mouse, con atenuación por distancia]`.
  * **Predicción y Diseño:** Diseñé esta fuerza porque `[Justifica tu intención, ej. quería simular la tensión de los sintetizadores acumulándose antes del beat]`.
  * **Prueba aislada:** Al aislarla en el LAB, verifiqué que `[Qué observaste al probarla sola]`.

* **Fuerza Central 2: `[Nombre de tu fuerza 2, ej. Fricción Densa]`**
  * **Ecuación / Dirección:** `[Explica brevemente la regla, ej. Fuerza que se opone a la velocidad multiplicada por un factor variable]`.
  * **Predicción y Diseño:** La incluí porque `[Ej. necesitaba frenar el sistema abruptamente en los silencios de la canción]`.

### 2. Controles Expresivos (El Instrumento)
Seleccioné pocos parámetros, pero con alto potencial expresivo:
1. `[Control 1, ej. Slider de Intensidad del Vórtice]`: Me permite `[Qué haces con él durante la canción]`.
2. `[Control 2, ej. Posición X/Y del atractor (Mouse)]`: Me permite `[Qué haces con él]`.
3. `[Control 3, ej. Toggle de Repulsión Máxima]`: Lo uso como un "golpe" visual para los momentos de ruptura en la pista.

### 3. Score Visual e Interpretación ("LesAlpx")
Mi relación con la pieza se resume en: *escucha → intención → score → interpretación → fuerzas → comportamiento*.

* **0:00 - 1:15 (Tensión inicial):** `[¿Qué haces aquí? Ej. Mantengo la fuerza de atracción muy leve, generando una acumulación lenta y caótica en el centro.]`
* **1:15 - 3:30 (Desarrollo y Ruptura):** `[Ej. Activo la repulsión y el vórtice gradualmente. Hago movimientos amplios con el puntero para crear corrientes fuertes acompañando los sintetizadores.]`
* **3:30 - Final (Dispersión):** `[Ej. Aumento la fricción al máximo y apago las atracciones, dejando que las partículas floten y se detengan poco a poco hasta desaparecer.]`

---

## Bitácora de Inteligencia Artificial (IA)
> *Ciclo de especificación, verificación y modificación.*

* **Prompt / Intención Inicial:** Le pedí a la IA `[Ej. cómo escribir en sintaxis TSL una fuerza que repeliera a las partículas solo si estaban a menos de 10 unidades de distancia]`.
* **Archivos modificados:** La IA propuso modificar el bloque de fuerzas en `createSimulation.js`.
* **Verificación y Corrección:** `[Ej. El código de la IA funcionaba, pero creaba una fuerza infinita que hacía desaparecer las partículas. Lo corregí agregando un parámetro límite (clamp) para suavizar la aceleración a distancias muy cortas.]`
* **Decisión final:** Conservé `[Ej. la lógica del cálculo de distancia]`, pero descarté `[Ej. la ecuación de velocidad que propuso la IA porque no usaba la integración de Euler que requiere nuestro proyecto]`.

---

## Actividad 04: Autoevaluación Ponderada

| Criterio | Peso | Valoración | Aporte | Evidencia / Sustento |
| :--- | :---: | :---: | :---: | :--- |
| **Trazabilidad y comprensión del sistema** | 25% | `[0-100]`% | `[Resultado]` | Detallado en Actividad 02. Identifiqué los buffers y ubiqué dónde la IA modificó el `createSimulation.js`. |
| **Verificación del algoritmo de fuerzas** | 25% | `[0-100]`% | `[Resultado]` | Aislé las fuerzas base y la fuerza central de mi diseño, ejecuté predicciones y modifiqué parámetros conscientemente (ver Act. 02 y 03). |
| **Diseño de fuerzas e intención** | 20% | `[0-100]`% | `[Resultado]` | El comportamiento emerge de la suma de `[Fuerza 1]` y `[Fuerza 2]`, no hay trayectorias animadas fijas. |
| **Instrumento, score e interpretación** | 15% | `[0-100]`% | `[Resultado]` | Detallado en el Score Visual. No uso audioreactividad automática; opero los controles manualmente según mi escucha. |
| **Experimentación y criterio frente a la IA** | 10% | `[0-100]`% | `[Resultado]` | Evidenciado en la Bitácora de IA, donde rechacé código que rompía el modelo de Euler. |
| **Entrega técnica y documentación** | 5% | `[0-100]`% | `[Resultado]` | El enlace abre correctamente y presenta modos LAB y PERFORMANCE. |
| **TOTAL (Nota propuesta)** | **100%** | | **`[TU NOTA / 5.0]`** | |








# Bitácora Unidad 4: Oscilación
**Estudiante:** Diego Sebastian Molina Julian
**ID:** 000621964
**Curso:** Simulación Para Sistemas Interactivos

---

## 🔗 Entregable Principal
* **Sistema audiovisual performativo (Kuramoto):** [Prototipo Unidad 4](https://diem-jln.github.io/modelo-de-kuramoto/)

---

## Actividad 01: Referentes para la unidad
> *Reflexiones sobre Memo Akten, Veritasium, Fireflies (Nicky Case) e Incredibox.*

* **Reflexión principal:**
Al estudiar los referentes de esta unidad, comprendí que la oscilación y la sincronización no consisten simplemente en hacer que las cosas se muevan de un lado a otro. Como demuestra el modelo de Kuramoto (explicado por Veritasium y de forma interactiva en *Fireflies*), la sincronización es un **fenómeno emergente**. 

Si analizamos *Incredibox*, vemos un sistema con identidades audiovisuales muy claras, pero funciona bajo un reloj global estricto (un secuenciador predeterminado). El reto de esta unidad es romper esa estructura centralizada. Mi objetivo es crear un sistema performativo donde el ritmo y la organización no estén dictados por un metrónomo general, sino que emerjan de la constante "negociación" matemática entre agentes individuales interactuando entre sí. 

---

## Actividad 02: Encargo de Diseño (Sistema con Kuramoto)
> *Diseño de un instrumento audiovisual basado en osciladores acoplados.*

### 1. La Pregunta Central de Diseño
**¿Qué hace Kuramoto en esta experiencia que no podría resolverse con un temporizador?**
A diferencia de un reloj global, el modelo de Kuramoto en mi sistema permite que exista la **incertidumbre y la transición**. Si usara un temporizador, el sistema solo sería "encendido/apagado" o "a tiempo/destiempo". Con Kuramoto, el sonido y la imagen transitan orgánicamente por el caos, luego por agrupamientos temporales (organización parcial) hasta llegar, si las condiciones lo permiten, a una estabilidad rítmica colectiva.

### 2. El Modelo de Kuramoto en mi Proyecto
En mi aplicación, las variables matemáticas del modelo original se traducen de la siguiente manera:
* **Fase (θ):** Representa `[Ej. el ciclo de la animación de cada agente y el momento exacto en el que emiten su sonido / percusión]`.
* **Frecuencia Natural (ω):** Representa `[Ej. la velocidad base a la que cada agente tiende a reproducir su loop si no estuviera influenciado por nadie más]`.
* **Fuerza de Acoplamiento (K):** Representa `[Ej. la capacidad de los agentes para "escucharse" entre sí. Si K es 0, todos van a su propio ritmo. Si K es alto, fuerzan sus fases para coincidir]`.
* **Modificación/Extensión:** `[Si modificaste la fórmula original, descríbelo aquí. Ej. "Modifiqué la topología para que los agentes solo se acoplen con los que están en un radio cercano, en lugar de un acoplamiento global, para generar sub-ritmos"]. Si no la modificaste, puedes borrar este viñeta.`

### 3. Personalidades Audiovisuales
El sistema cuenta con `[Número, ej. 8]` agentes gobernados por la dinámica, divididos en 4 personalidades (que no solo cambian de color, sino de comportamiento):
1. **`[Nombre de Personalidad 1, ej. Los Bajos Pesados]`**: Visualmente se manifiestan como `[forma/movimiento]` y su comportamiento se basa en `[ej. tener una frecuencia natural lenta y una alta resistencia a cambiar de fase]`.
2. **`[Nombre de Personalidad 2]`**: `[Descripción visual, sonora y de comportamiento]`.
3. **`[Nombre de Personalidad 3]`**: `[Descripción visual, sonora y de comportamiento]`.
4. **`[Nombre de Personalidad 4]`**: `[Descripción visual, sonora y de comportamiento]`.

### 4. Experiencia Performativa e Interacción
Mi sistema es un instrumento que puede tocarse en vivo, permitiendo transitar entre **desorden**, **organización parcial** y **organización estable**:

* **Interacción Global:** `[Ej. Un slider principal que modifica la fuerza de acoplamiento (K) y otro que altera la varianza de las frecuencias naturales, permitiéndome llevar al sistema del caos a la armonía]`.
* **Interacción Individual (Perturbación):** `[Ej. Al hacer clic sobre un agente específico, este "tropieza" (se altera su fase bruscamente), lo que me permite romper la estabilidad en vivo y observar cómo el resto del enjambre tarda unos segundos en volver a sincronizarlo]`.
* **Comunicación del estado colectivo:** El usuario sabe en qué estado está el sistema visual y sonoramente porque `[Ej. el fondo de la pantalla pulsa al unísono cuando alcanzan la estabilidad, y el sonido pasa de ser un ruido blanco rítmico a un acorde limpio]`.

---

## Actividad 03: Autoevaluación

| Criterio | Puntos | Valoración | Evidencia / Sustento |
| :--- | :---: | :---: | :--- |
| **Requisitos mínimos:** Leí y verifiqué que mi proyecto cumple con los requisitos (8 agentes, 4 personalidades, 2 interacciones globales/individuales, 3 estados). | 25 | `[0-25]` | `[Ej. Mi aplicación cuenta con 8 agentes en pantalla que responden a clics individuales y a controles globales de acoplamiento.]` |
| **Comprensión de variables:** Puedo explicar claramente qué representa cada variable del modelo de Kuramoto en mi proyecto. | 25 | `[0-25]` | Detallado en la sección "El Modelo de Kuramoto en mi Proyecto" de esta bitácora. |
| **Dinámica del modelo:** Puedo explicar claramente cómo las variables del modelo producen el comportamiento observado en mi proyecto. | 25 | `[0-25]` | `[Ej. El acoplamiento (K) fuerza visualmente a los agentes a igualar sus ciclos, generando los ritmos en la pista de audio sin usar un metrónomo.]` |
| **Objetivos de la unidad:** Puedo demostrar que mi proyecto cumple con los objetivos (instrumento performativo audiovisual, no solo una simulación matemática). | 25 | `[0-25]` | `[Ej. El proyecto funciona como un instrumento en vivo; lo probé creando una estructura musical que va del caos inicial a un ritmo estable usando perturbaciones.]` |
| **TOTAL (Nota propuesta)** | **100** | **`[TU NOTA / 100]`** | |








# Bitácora Unidad 6: Agentes Autónomos
**Estudiante:** Diego Sebastian Molina Julian
**ID:** 000621964
**Curso:** Simulación Para Sistemas Interactivos

---

## 🔗 Entregable Principal
* **Instrumento visual (Performance en vivo):** [Prototipo Unidad 6 - Agentes Orula](https://diem-jln.github.io/agentes-orula/)

---

## Actividad 01 y 02: Steering Behaviors, Flow Fields y Physarum
> *Reflexiones teóricas sobre algoritmos de autonomía.*

* **Reflexión principal:**
En las unidades pasadas diseñamos sistemas globales, pero en esta unidad el enfoque cambia al individuo. Los **agentes autónomos** operan bajo un principio fascinante: tienen una **capacidad limitada para percibir su entorno**. No existe un "cerebro central" o un líder dictando trayectorias. 

Al estudiar los *steering behaviors* (como el *flocking* con sus reglas de separación, alineación y cohesión), los *flow fields* y el algoritmo de *Physarum* (moho mucilaginoso), comprendí que la complejidad visual del sistema emerge de reglas locales muy simples. El agente percibe un radio corto a su alrededor, procesa esa información y calcula una "velocidad deseada" o acción. Como creador e intérprete, mi rol no es animar a los agentes, sino modificar las condiciones de su entorno y sus reglas de percepción en tiempo real para "conducir" el comportamiento emergente del colectivo.

---

## Actividad 03: Encargo de Diseño (Instrumento Visual)
> *Interpretación de una pieza musical utilizando agentes autónomos.*

### 1. Elección Musical e Intención
* **Pieza musical:** `[Nombre de la canción y artista, ej. "Xtal" de Aphex Twin]`.
* **Intención visual:** A través de este sistema, busco expresar `[Describe tu intención, ej. la sensación de flujo constante que se interrumpe abruptamente por momentos de tensión caótica en la percusión]`.

### 2. Diseño de los Agentes y el Entorno
Para construir este instrumento, utilicé `[Menciona los algoritmos que elegiste: ej. una combinación de Flocking y Flow Fields / o un sistema interactivo de Physarum]`.

* **¿Qué percibe el agente?:** `[Ej. Cada agente solo puede "ver" a sus vecinos numéricos dentro de un radio de 30 pixeles y el vector direccional del Flow Field en su posición actual]`.
* **Cálculo de acciones (Reglas):** `[Ej. Si un vecino se acerca mucho, aplica la fuerza de separación. Si no hay vecinos cerca, sigue ciegamente la dirección del campo de flujo]`.
* **Comportamiento emergente:** La combinación de estas reglas produce `[Ej. cardúmenes que fluyen como ríos, pero que al chocar entre sí generan remolinos impredecibles]`.

### 3. Controles Expresivos (El Instrumento)
El sistema no responde automáticamente al audio; yo actúo como el puente entre la música y los agentes a través de los siguientes controles:
1. `[Control 1, ej. Slider de Rango de Cohesión]`: Lo utilizo para `[Ej. agrupar a los agentes en esferas densas durante los crescendos]`.
2. `[Control 2, ej. Clic/Arrastrar el Mouse]`: Alimenta al sistema alterando `[Ej. los ángulos del Flow Field temporalmente, creando "viento" manual]`.
3. `[Control 3, ej. Botón de Dispersión Máxima]`: Modifica la percepción de los agentes para `[Ej. que huyan desesperadamente de sus vecinos, marcando los "drops" de la canción]`.

### 4. Score Visual e Interpretación
El performance en vivo sigue este mapa mental de escucha e intervención:

* **Inicio (0:00 - 1:20):** `[¿Qué estado sostienes aquí? Ej. Mantengo el Flow Field estático y una cohesión baja. Los agentes flotan a la deriva, acompañando el ambiente tranquilo de los sintetizadores.]`
* **Desarrollo (1:20 - 3:00):** `[Ej. Empieza el beat. Comienzo a intervenir con el mouse para generar turbulencia. Aumento gradualmente el rango de percepción para que formen bandadas (flocking).]`
* **Clímax y Cierre (3:00 - Final):** `[Ej. Rompo la cohesión al máximo. Uso el botón de dispersión en cada golpe de bajo. Al final, reduzco la velocidad máxima de los agentes hasta que se congelan.]`

---

## Actividad 04: Autoevaluación Ponderada

| Criterio | Puntos | Valoración | Evidencia / Sustento |
| :--- | :---: | :---: | :--- |
| **Cumplimiento del encargo:** El instrumento utiliza tecnología web, funciona en tiempo real y permite interpretar la pieza elegida. | 25 | `[0-25]` | El proyecto está alojado en GitHub Pages, corre fluido en pantalla completa y fue diseñado para ser tocado en vivo. |
| **Comprensión y verificación:** Puedo explicar cómo está construido, qué perciben los agentes y verificar los cambios de parámetros. | 25 | `[0-25]` | `[Ej. Documenté en esta bitácora las reglas exactas de percepción y cómo el cálculo de la velocidad deseada altera el movimiento.]` |
| **Diseño e intención:** Puedo justificar la selección/combinación de comportamientos y relacionarlos con la música. | 25 | `[0-25]` | `[Ej. Elegí usar Physarum porque la forma en que los rastros se desvanecen representa visualmente los ecos de la voz en mi canción.]` |
| **Interpretación humana:** El score y los controles permiten conducir el sistema en vivo y responder al comportamiento. | 25 | `[0-25]` | No hay análisis de audio ni secuencias fijas. Todo cambio de estado documentado en el Score Visual depende de mis clics y ajustes en vivo. |
| **TOTAL (Nota propuesta)** | **100** | **`[TU NOTA / 100]`** | |







# Bitácora Unidad 7: Tipografía Jugable (Word as a Playable System)
**Estudiante:** Diego Sebastian Molina Julian
**ID:** 000621964
**Curso:** Simulación Para Sistemas Interactivos

---

## 🔗 Entregable Principal
* **Sistema tipográfico jugable:** [Prototipo Unidad 7 - TOTOS lab](https://diem-jln.github.io/TOTOS_lab/)

---

## Actividad 01: Referentes y posibilidades de los sistemas jugables
> *Reflexiones sobre Ji Lee (Word as Image), Playables y motores de física.*

* **Reflexión principal:**
Al estudiar el proyecto *Word as Image* de Ji Lee y las piezas de *Playables*, comprendí que la tipografía puede trascender su función de lectura lineal para convertirse en un sistema de construcción de sentido a través del juego. No se trata de añadir adornos externos a las letras, sino de que su escala, posición y comportamiento físico comuniquen la idea. 

En unidades anteriores utilizamos fuerzas y oscilaciones puras, pero al introducir bibliotecas de física (o simulaciones espaciales complejas en WebGL/p5.js), las letras adquieren masa, volumen y restricciones. Esto es vital para un sistema jugable, ya que la física provee una expectativa natural de cómo los objetos deberían reaccionar a nuestras interacciones, permitiendo que la persona descubra el significado no leyendo un texto estático, sino "tocando" y manipulando el sistema.

---

## Actividad 02: Encargo de Diseño
> *Reto de diseño: una identidad que se descubre jugando.*

### 1. La Organización y su Contexto
* **Empresa / Organización:** TOTOS lab.
* **¿Qué hace y a qué público se dirige?:** `[Describe brevemente la actividad real o ficticia de la marca y su audiencia. Ej. Un laboratorio de experimentación visual y desarrollo interactivo dirigido a creativos y marcas tecnológicas]`.
* **Contexto de uso:** `[Ej. Diseñado para ser la experiencia introductoria en la portada web (landing page) de su portafolio digital]`.

### 2. Intención Semántica (El Atributo)
* **Atributo de identidad a comunicar:** `[Ej. La capacidad de encontrar soluciones integrales a partir de piezas fragmentadas / El pensamiento multidimensional]`.
* **Justificación:** Elegí este atributo porque `[Ej. representa la filosofía del laboratorio: a simple vista los problemas parecen caóticos, pero con la perspectiva correcta, todo encaja perfectamente]`.

### 3. El Sistema Jugable (Reglas y Consecuencias)
Desarrollé una experiencia interactiva y un rompecabezas tipográfico 3D utilizando p5.js y WebGL, donde los elementos gráficos provienen estrictamente de las letras que componen "TOTOS lab".

* **¿Qué puede hacer la persona?:** `[Ej. El usuario puede hacer clic y arrastrar con el mouse para orbitar la cámara alrededor de una nube caótica de fragmentos tridimensionales]`.
* **Reglas del sistema:** `[Ej. La física del entorno restringe las piezas a un volumen espacial específico. El movimiento del mouse controla los ángulos absolutos de la cámara en el espacio 3D]`.
* **Consecuencias y descubrimiento:** Al jugar e interactuar con el sistema, la persona descubre que `[Ej. lo que parecía un conjunto de geometrías abstractas flotando sin sentido, se alinea perfectamente en un ángulo exacto (ilusión anamórfica) para formar el logotipo de TOTOS lab, revelando el atributo de la marca]`.

---

## Actividad 03: Autoevaluación Ponderada

| Criterio | Puntos | Valoración | Evidencia / Sustento |
| :--- | :---: | :---: | :--- |
| **Cumplimiento del encargo:** El sistema utiliza las letras de una organización, permite jugar con ellas y funciona en tiempo real en la Web. | 25 | `[0-25]` | El proyecto está alojado en la Web (`diem-jln.github.io/TOTOS_lab/`) y el sistema gráfico está construido enteramente a partir del nombre de la marca. |
| **Comprensión y verificación:** Puedo explicar y justificar el modelo, sus estados, reglas, y predecir el efecto de modificar un parámetro. | 25 | `[0-25]` | `[Ej. Documenté cómo el uso de WebGL y p5.js maneja la profundidad (Z-axis). Si modifico el ángulo de la cámara o las coordenadas de los vértices, la ilusión anamórfica se rompe.]` |
| **Interacción e identidad:** Puedo justificar qué permiten descubrir las acciones y sus consecuencias sobre el atributo elegido. | 25 | `[0-25]` | `[Ej. La acción de buscar el ángulo correcto obliga al usuario a involucrarse activamente en la "resolución del problema", experimentando de primera mano la identidad de TOTOS lab.]` |
| **Resolución tipográfica y experiencia:** La composición, ritmo y respuestas perceptibles sostienen la intención y permiten explorar el sistema. | 25 | `[0-25]` | `[Ej. La estética de los materiales 3D y la suavidad de la rotación invitan a seguir jugando sin necesidad de instrucciones explícitas de victoria o puntuación.]` |
| **TOTAL (Nota propuesta)** | **100** | **`[TU NOTA / 100]`** | |





# Bitácora Unidad 8: Integración
**Estudiante:** Diego Sebastian Molina Julian
**ID:** 000621964
**Curso:** Simulación Para Sistemas Interactivos

---

## 🔗 Entregable Principal
* **Obra de simulación computacional:** [Prototipo Unidad 8 - Gestural Music Sim](https://diem-jln.github.io/gestural-music-sim/)

---

## Actividad 01: Why Bother? ¿Para qué tomarte el trabajo?
> *Reflexiones sobre la charla de Robert Hodgin y el aprendizaje en la era de la IA.*

* **Reflexión principal:**
Al escuchar la charla de Robert Hodgin y leer la reflexión del profesor, me enfrento a la pregunta central de esta época: si una IA puede escribir el código y generar el resultado visual en segundos, *¿qué sentido tiene mi esfuerzo?* 

Durante este curso, he utilizado la IA como un asistente poderoso para resolver cuellos de botella técnicos. Sin embargo, me he dado cuenta de que obtener un resultado sin comprender cómo se construyó es una ilusión de aprendizaje. Cumplir una tarea delegando las decisiones creativas a la máquina te deja vacío; en cambio, explorar por curiosidad y pelear con el código para que refleje exactamente tu intención es donde reside el valor. El esfuerzo vale la pena porque el proceso de traducir una idea abstracta a un sistema lógico es lo que moldea mi propio criterio como creador. 

---

## Actividad 02 y 03: Encargo de diseño y Presentación
> *Exploración práctica y sustentación de la obra "Gestural Music Sim".*

### 1. ¿Cómo interpretaste la pregunta "Why Bother?"?
* **Mi interpretación:** Decidí explorar el aspecto de la `[Ej. conexión física y el esfuerzo corporal en la creación de música, algo que la IA no puede experimentar]`. 
* **Evolución:** Mientras trabajaba, mi interpretación cambió de `[Ej. querer hacer un visualizador complejo a entender que lo importante era cómo mis propios gestos modificaban el sistema en tiempo real]`.

### 2. ¿Cómo lo exploraste? (Técnicas y decisiones)
* **Técnicas elegidas:** Para construir esta simulación utilicé `[Ej. MediaPipe para el reconocimiento gestual / análisis de audio / un sistema de partículas asimétrico]`.
* **Decisiones y pruebas:** Elegí estas herramientas porque `[Ej. quería que el cuerpo fuera el controlador principal, obligando al usuario a "tomarse el trabajo" de moverse para generar el resultado]`. Durante el desarrollo, las pruebas me llevaron a ajustar `[Ej. la sensibilidad de los vectores de movimiento para que no fuera ni muy fácil ni incontrolable]`.

### 3. ¿Qué encontraste?
* **Lo esperado:** Ocurrió como esperaba que `[Ej. las partículas respondieran de manera fluida a los movimientos bruscos]`.
* **Las sorpresas:** Me sorprendió cómo `[Ej. el sistema generó formas armónicas imprevistas cuando cruzaba ambas manos lentamente]`.
* **Lo que sigue abierto:** Todavía me pregunto si `[Ej. podría integrar físicas más complejas o si eso saturaría la intención original del proyecto]`.

### 4. ¿Qué aprendiste realmente?
Más allá de completar el encargo, ahora puedo comprender, explicar y modificar `[Ej. cómo los datos de un input externo (como una cámara o el mouse) se normalizan y se convierten en aceleración y velocidad dentro de un entorno WebGL/p5.js]`. Sé qué partes hizo la IA y qué partes estructuré yo, y tengo la capacidad de alterar el comportamiento base sin romper la simulación.

### 5. ¿Qué sentido tuvo tomarte el trabajo?
* **El motor para continuar:** Lo que me hizo continuar frente a los errores de código fue `[Ej. la necesidad de ver mi concepto materializado exactamente como lo imaginé, no como la IA sugería por defecto]`.
* **El esfuerzo valioso:** Considero valioso el esfuerzo de `[Ej. calibrar la interacción]`, porque ahí es donde la obra dejó de ser un simple bloque de código y se convirtió en una experiencia humana. 
* **Frente a Hodgin:** Hoy me sitúo frente a la pregunta de Hodgin concluyendo que el trabajo vale la pena porque la obra final no es el único objetivo; el objetivo real es la transformación que ocurre en mi mente mientras descubro cómo construirla.

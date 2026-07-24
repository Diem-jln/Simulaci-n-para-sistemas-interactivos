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

---

## Actividad 08: Evaluación
> *Espacio reservado para las notas de la presentación pública de la experiencia interactiva (Reto de Diseño).*
* **Feedback recibido:** [Espacio para anotar la retroalimentación del profesor y compañeros tras tu exposición].



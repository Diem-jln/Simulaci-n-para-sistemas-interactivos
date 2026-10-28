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
Al estudiar los referentes de esta unidad, comprendí que la oscilación y la sincronización no consisten simplemente en hacer que las cosas se muevan de un lado a otro. Como demuestra el modelo de Kuramoto (explicado por Veritasium y de forma interactiva en *Fireflies*), la sincronización es un fenómeno emergente.

Si analizamos *Incredibox*, vemos un sistema con identidades audiovisuales muy claras, pero que funciona bajo un reloj global estricto (un secuenciador predeterminado). El reto de esta unidad es romper esa estructura centralizada. Mi objetivo es crear un sistema performativo donde el ritmo y la organización no estén dictados por un metrónomo general, sino que emerjan de la constante "negociación" matemática entre agentes individuales interactuando entre sí en un entorno 3D abisal.

---

## Actividad 02: Encargo de Diseño (Sistema con Kuramoto)
> *Diseño de un instrumento audiovisual basado en osciladores acoplados.*

### 1. La Pregunta Central de Diseño
**¿Qué hace Kuramoto en esta experiencia que no podría resolverse con un temporizador?** 
A diferencia de un reloj global, el modelo de Kuramoto en mi sistema permite que exista la incertidumbre, la fricción y la transición fluida. Si usara un temporizador o un secuenciador estático, los elementos solo podrían encenderse o apagarse a compás fijo. Con Kuramoto, el sonido abisal y la pulsación bioluminiscente transitan orgánicamente desde la cacofonía y el desorden, pasando por fases de agrupamiento rítmico parcial, hasta consolidar una coherencia colectiva donde las criaturas y los osciladores sintetizados respiran y emiten destellos en fase.

### 2. El Modelo de Kuramoto en mi Proyecto
En mi aplicación, las variables matemáticas del modelo original se traducen de la siguiente manera:

* **Fase ($\theta$):** Representa la posición angular dentro del ciclo de pulsación de cada entidad en la escena de Three.js. Esta variable determina la escala del resplandor de su material bioluminiscente y el instante exacto en el que se dispara su modulación de síntesis de audio.
* **Frecuencia Natural ($\omega$):** Representa la velocidad angular intrínseca con la que oscila cada criatura marina en aislamiento. Está configurada a partir de frecuencias base asíncronas para simular ciclos metabólicos y tonos individuales en el fondo abisal.
* **Fuerza de Acoplamiento ($K$):** Representa la intensidad con la que los osciladores perciben y corrigen su fase con respecto al orden colectivo. Controlada dinámicamente por la interacción del usuario; un $K = 0$ mantiene a los agentes en deriva disonante, mientras que un $K$ elevado arrastra al enjambre hacia la sincronía pura.
* **Modificación/Extensión:** Se implementó el cálculo del parámetro de orden global complejo $R(t) = \frac{1}{N}\sum_{j=1}^{N} e^{i\theta_j}$, utilizando la magnitud de coherencia $R$ (donde $0 \le R \le 1$) para alimentar en tiempo real el HUD de métricas y regular dinámicamente la ganancia del sintetizador de ambiente armónico.

### 3. Personalidades Audiovisuales
El sistema cuenta con **8 agentes tridimensionales** gobernados por la dinámica de Kuramoto, distribuidos en **4 personalidades** bien diferenciadas visual, sonora y físicamente:

1. **Nodrizas Abisales (Bajos de Frecuencia Lenta):** Visualmente se manifiestan como mallas esferoidales densas con deformación volumétrica suave y pulsación profunda en tonos azul cobalto. Su comportamiento sonoro genera tonos sinusoidales subgraves con una frecuencia natural baja e inercia alta frente a cambios abruptos de fase.
2. **Medusas Bioluminiscentes (Medios Texturados):** Se manifiestan como filamentos y estructuras flotantes translúcidas en cian. Emiten armónicos resonantes de frecuencia media y presentan una reactividad intermedia que actúa como puente de sincronización en el cardumen.
3. **Centellas de Tensión (Altas / Moduladoras):** Geometrías poliédricas puntiagudas con emisiones en teal y blanco de alta intensidad. Operan con frecuencias naturales rápidas y disparan micro-clicks percusivos agudos al cruzar el ciclo angular $\theta = 0$.
4. **Tensor / Núcleo Armónico:** Una entidad central articulada que actúa como ancla visual. Su rotación y material reaccionan directamente a la magnitud del orden $R$, generando una base armónica continua (*drone*) que se estabiliza cuando el sistema converge.

### 4. Experiencia Performativa e Interacción
Mi sistema es un instrumento que puede tocarse en vivo, permitiendo transitar entre desorden, organización parcial y organización estable:

* **Interacción Global:** El desplazamiento horizontal del puntero del mouse (Mouse X) mapea en tiempo real la fuerza de acoplamiento colectivo ($K$). Desplazar el cursor a la izquierda reduce $K$ a 0 provocando el colapso hacia el desorden, mientras que moverlo al extremo derecho eleva $K$, forzando la transición hacia la estabilidad rítmica y visual. Adicionalmente, la tecla `P` conmuta la visibilidad del HUD y la tecla `V` activa el modo visor.
* **Interacción Individual (Perturbación):** Mediante un sistema de Raycasting tridimensional, hacer clic sobre cualquier criatura específica altera su fase de forma instantánea mediante un salto de $\pi$ radianes ($\theta_i \leftarrow \theta_i + \pi$). Esto quiebra localmente la sincronía lograda, permitiendo observar cómo el resto del sistema interactúa para absorber la anomalía y reordenar la fase colectiva.
* **Comunicación del estado colectivo:** El usuario visualiza el estado en el panel superior mediante un indicador dinámico (DESORDEN, ORGANIZACIÓN PARCIAL o SINCRONÍA / ESTABILIDAD) y los valores en vivo de Coherencia ($R$) y Acoplamiento ($K$). Sonoramente, el sistema pasa de una textura discordante y caótica a un acorde puro y pulsante cuando el orden $R$ supera el umbral crítico.

---

## Actividad 03: Autoevaluación Ponderada

| Criterio | Puntos Max. | Valoración | Evidencia / Sustento |
| :--- | :---: | :---: | :--- |
| **Requisitos mínimos**<br><small>Leí y verifiqué que mi proyecto cumple con los requisitos mínimos de la unidad.</small> | 25 | 25 | La simulación en Three.js/TypeScript cuenta con 8 agentes abisales en 4 arquetipos sonoros/visuales, control continuo de $K$ por mouse, perturbación por clic vía Raycasting, y transiciones verificables entre los 3 estados (desorden, orden parcial, sincronía). |
| **Comprensión de variables**<br><small>Puedo explicar claramente qué representa cada variable del modelo de Kuramoto en mi proyecto.</small> | 25 | 25 | Detallado en la sección "El Modelo de Kuramoto en mi Proyecto", con mapeos claros y matemáticos de fase ($\theta$), frecuencia natural ($\omega$), acoplamiento ($K$) y coherencia compleja ($R$). |
| **Dinámica del modelo**<br><small>Puedo explicar claramente cómo las variables del modelo producen el comportamiento observado.</small> | 25 | 25 | El acoplamiento $K$ y la diferencia de fases modulan la velocidad de rotación angular de cada criatura; a mayor $K$, las diferencias de fase se cancelan matemáticamente, obligando a los osciladores a igualar sus destellos y la emisión armónica sin temporizadores externos. |
| **Objetivos de la unidad**<br><small>Puedo demostrar que mi proyecto cumple con los objetivos establecidos en la unidad.</small> | 25 | 25 | La plataforma responde como un instrumento audiovisual performativo en vivo: el sistema transita deliberadamente entre caos sonoro y armonía rítmica mediante perturbaciones físicas puntuales y control del acoplamiento. |
| **TOTAL (Nota propuesta)** | **100** | **100** | Cumplimiento total de la arquitectura matemática de Kuramoto integrada a síntesis Web Audio y renderizado en WebGL/Three.js. |

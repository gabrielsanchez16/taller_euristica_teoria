# Heurística y Teoría de Juegos

### Inteligencia Artificial

**Estudiante:** Gabriel Sánchez
**Profesor:** Wilman Quiñones
**Asignatura:** Inteligencia Artificial
**Universidad:** Universidad del Pacífico

---

# Introducción

Dentro del campo de la **Inteligencia Artificial (IA)** existen diferentes enfoques para resolver problemas complejos, optimizar decisiones y modelar comportamientos inteligentes. Dos conceptos fundamentales en este contexto son **la heurística** y **la teoría de juegos**.

La heurística se enfoca en estrategias prácticas que permiten encontrar soluciones eficientes cuando los métodos exactos son demasiado costosos computacionalmente. Por otro lado, la teoría de juegos analiza cómo múltiples agentes toman decisiones estratégicas cuando sus resultados dependen de las acciones de otros.

Este documento presenta una investigación sobre ambos conceptos, explicando **qué son, para qué sirven, cómo funcionan**, y mostrando ejemplos aplicados en el ámbito de la inteligencia artificial y la toma de decisiones.

---

# 1. Heurística

## ¿Qué es la heurística?

Una **heurística** es una estrategia o método práctico utilizado para resolver problemas de manera más rápida cuando los métodos exactos son demasiado lentos o complejos.

En inteligencia artificial, las heurísticas se utilizan para **reducir el espacio de búsqueda y encontrar soluciones razonablemente buenas en menos tiempo**.

En lugar de evaluar todas las posibles soluciones, una heurística **guía el proceso de búsqueda hacia las opciones más prometedoras**.

Según Russell y Norvig (2021), una heurística es:

> "Una función que estima qué tan cerca está un estado de la meta en un problema de búsqueda."

Esto significa que las heurísticas permiten **priorizar caminos o decisiones que probablemente conduzcan a una solución óptima o cercana a ella**.

---

## ¿Para qué sirve la heurística?

Las heurísticas son fundamentales en múltiples áreas de la inteligencia artificial y la informática, especialmente cuando los problemas tienen **grandes espacios de búsqueda**.

Se utilizan principalmente para:

* Optimizar algoritmos de búsqueda.
* Reducir tiempo de cálculo.
* Tomar decisiones rápidas en entornos complejos.
* Resolver problemas donde no es viable calcular todas las combinaciones posibles.

Algunos campos donde se utilizan heurísticas incluyen:

* Inteligencia artificial
* Optimización
* Robótica
* Videojuegos
* Sistemas de navegación
* Machine Learning

---

## ¿Cómo funciona una heurística?

Las heurísticas funcionan mediante **funciones de evaluación** que asignan un valor o puntuación a cada posible estado del problema.

Este valor representa **qué tan prometedor es ese estado para llegar a la solución**.

En algoritmos de búsqueda, como **A***, se utilizan dos componentes principales:

* **Costo acumulado:** cuánto costó llegar al estado actual.
* **Estimación heurística:** qué tan lejos está el estado de la meta.

La fórmula típica utilizada es:

```
f(n) = g(n) + h(n)
```

Donde:

* **g(n)** = costo real desde el inicio hasta el nodo n
* **h(n)** = estimación heurística desde n hasta la meta
* **f(n)** = costo total estimado

El algoritmo entonces selecciona el nodo con el menor valor de **f(n)** para continuar la búsqueda.

---

## Ejemplo 1: Navegación GPS

Un ejemplo cotidiano de heurística es el funcionamiento de **los sistemas de navegación GPS**.

Cuando una aplicación calcula la mejor ruta entre dos puntos, no evalúa todas las rutas posibles. En cambio, utiliza heurísticas como:

* distancia en línea recta al destino
* tiempo estimado de viaje
* estado del tráfico

Estas estimaciones ayudan al sistema a **descartar rutas menos prometedoras y concentrarse en las más eficientes**.

---

## Ejemplo 2: Ajedrez en inteligencia artificial

Los programas de ajedrez utilizan heurísticas para evaluar posiciones del tablero.

Dado que el número de posibles movimientos es extremadamente grande, los sistemas utilizan funciones heurísticas que consideran factores como:

* valor de las piezas
* control del centro del tablero
* seguridad del rey
* movilidad de las piezas

Cada posición recibe una puntuación, lo que permite al algoritmo elegir las jugadas más prometedoras sin analizar todas las combinaciones posibles.

---

# 2. Teoría de Juegos

## ¿Qué es la teoría de juegos?

La **teoría de juegos** es una rama de las matemáticas y la economía que estudia **las decisiones estratégicas entre múltiples agentes** cuando el resultado para cada participante depende también de las decisiones de los demás.

Fue desarrollada formalmente por **John von Neumann y Oskar Morgenstern** en 1944.

La teoría de juegos analiza situaciones en las que:

* existen varios jugadores
* cada jugador tiene diferentes estrategias
* el resultado depende de la combinación de decisiones

En inteligencia artificial, esta teoría se utiliza para **modelar comportamientos competitivos o cooperativos entre agentes**.

---

## ¿Para qué sirve la teoría de juegos?

La teoría de juegos tiene aplicaciones en múltiples áreas:

* Inteligencia artificial
* Economía
* Política
* Negociación
* Estrategias militares
* Sistemas multi-agente
* Mercados financieros

En IA es particularmente útil para:

* modelar competencia entre agentes
* diseñar sistemas de negociación automática
* analizar estrategias en videojuegos
* desarrollar algoritmos de toma de decisiones

---

## ¿Cómo funciona la teoría de juegos?

Un juego estratégico generalmente se define por los siguientes elementos:

### 1. Jugadores

Los agentes que participan en la toma de decisiones.

### 2. Estrategias

Las posibles acciones que cada jugador puede elegir.

### 3. Pagos (payoffs)

Las recompensas o resultados que obtiene cada jugador dependiendo de las decisiones tomadas.

### 4. Equilibrio

Un concepto fundamental es el **Equilibrio de Nash**, donde ningún jugador puede mejorar su resultado cambiando su estrategia si los demás mantienen la suya.

---

## Ejemplo 1: El dilema del prisionero

El **Dilema del Prisionero** es uno de los ejemplos más conocidos en teoría de juegos.

Dos sospechosos son interrogados por separado y tienen dos opciones:

* cooperar con el otro (guardar silencio)
* traicionar al otro

Las decisiones generan diferentes resultados:

| Jugador A  | Jugador B  | Resultado                      |
| ---------- | ---------- | ------------------------------ |
| Cooperar   | Cooperar   | Ambos reciben penas leves      |
| Traicionar | Cooperar   | El traidor queda libre         |
| Cooperar   | Traicionar | El cooperador recibe pena alta |
| Traicionar | Traicionar | Ambos reciben pena moderada    |

Este ejemplo demuestra cómo **la decisión racional individual puede llevar a un resultado peor para ambos jugadores**.

---

## Ejemplo 2: Estrategias en videojuegos

Muchos videojuegos competitivos utilizan principios de teoría de juegos.

Por ejemplo, en juegos multijugador los jugadores deben decidir:

* atacar
* defender
* cooperar
* formar alianzas

Cada decisión depende de lo que **los otros jugadores probablemente harán**, lo que genera dinámicas estratégicas similares a las estudiadas en teoría de juegos.

---

## Ejemplo 3: Subastas

Las subastas son otro ejemplo clásico.

Cada participante decide cuánto ofertar por un objeto, considerando:

* cuánto lo valoran
* cuánto creen que ofertarán los demás

La teoría de juegos permite analizar diferentes tipos de subastas como:

* subasta inglesa
* subasta holandesa
* subasta de sobre cerrado

Estos modelos ayudan a entender cómo los participantes **ajustan sus estrategias según la información disponible y el comportamiento esperado de los demás**.

---

# Conclusión

A partir de la investigación realizada, puedo entender que tanto la heurística como la teoría de juegos son herramientas muy importantes dentro del campo de la inteligencia artificial y la toma de decisiones.

En mi entendimiento, la heurística permite abordar problemas complejos de una manera más eficiente, especialmente cuando analizar todas las posibilidades sería demasiado costoso o incluso imposible en términos de tiempo o recursos computacionales. Gracias a las heurísticas, los sistemas pueden enfocarse en las opciones más prometedoras y encontrar soluciones que, aunque no siempre sean perfectas, resultan bastante buenas y prácticas en muchos contextos reales.

Por otro lado, la teoría de juegos me permite comprender cómo diferentes agentes o personas pueden tomar decisiones estratégicas cuando sus resultados dependen también de lo que hagan los demás. Esto me ayuda a ver cómo muchos problemas del mundo real, desde la economía hasta los videojuegos o la inteligencia artificial, pueden analizarse considerando las interacciones entre múltiples participantes.

En conclusión, desde mi perspectiva, ambos conceptos aportan herramientas muy valiosas para el desarrollo de sistemas inteligentes, ya que permiten optimizar la búsqueda de soluciones y entender mejor los procesos de toma de decisiones en entornos donde existen múltiples variables y actores involucrados.
---

# Referencias

Russell, S., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach*. Pearson.

Von Neumann, J., & Morgenstern, O. (1944). *Theory of Games and Economic Behavior*. Princeton University Press.

Osborne, M. (2004). *An Introduction to Game Theory*. Oxford University Press.

Poole, D., & Mackworth, A. (2017). *Artificial Intelligence: Foundations of Computational Agents*. Cambridge University Press.

---

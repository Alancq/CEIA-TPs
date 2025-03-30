# Trabajo Práctico N.º 1 - Inteligencia Artificial

**Integrantes**: 
- Alan Cornejo 
- Martin Paura

---

## 1. PEAS del problema de la Torre de Hanoi


- **Performance**: resolver el problema en la menor cantidad de movimientos, minimizando además tiempo y memoria.
- **Environment**: tres varillas, discos de distinto tamaño con reglas que impiden mover más de un disco a la vez o la regla de no colocar uno mayor sobre uno menor.
- **Actuators**: mover un disco de una varilla a otra.
- **Sensors**: estado actual de los discos en las varillas.


---

## 2. Propiedades del entorno de trabajo

- **Completamente observable**: conocemos todo el estado en cada momento.
- **Determinista**: cada acción lleva a un solo estado siguiente.
- **Secuencial**: las acciones se realizan una tras otra.
- **Estático**: el entorno no cambia a menos que el agente actúe.
- **Discreto**: hay un número finito de estados.
- **Conocido**: todas las reglas del problema son conocidas.

---

## 3. Definiciones en el contexto del problema

- **Estado**: configuración de los discos en las tres varillas.
- **Espacio de estados**: todas las configuraciones posibles.
- **Árbol de búsqueda**: representación jerárquica de todos los posibles estados alcanzables desde el inicial.
- **Nodo de búsqueda**: un estado con información adicional como su profundidad y costo acumulado.
- **Objetivo**: todos los discos ordenados en la tercera varilla.
- **Acción**: mover un disco de una varilla a otra según las reglas.
- **Frontera**: conjunto de nodos a explorar (implementado como una cola de prioridad).

---

## 4. Método de búsqueda implementado: A*

Se implementó el algoritmo A* con una heurística propia premiando la colocación correcta de discos 

---

## 5. Complejidad teórica del algoritmo A*

- **Tiempo**: En el peor caso, es exponencial: ` O(b^d)`.
- **Memoria**: Igual que el tiempo, ya que A* almacena todos los nodos generados.

---

## 6. Tiempo y memoria en la implementación (5 discos)

Se realizaron 10 ejecuciones:

- **Tiempo promedio**: 0.0096 s  
- **Desviación estándar del tiempo**: 0.0017 s  
- **Memoria promedio**: 0.09 MB  
- **Desviación estándar de memoria**: 0.0 MB
- **Eficiencia respecto a nodos explorados**: 81.58%

---

## 7. Comparación con la solución óptima

- **Solución óptima**: `( 2^5 - 1 = 31 `) movimientos.  
- **Solución encontrada por el algoritmo**: 32 movimientos.  
- **Eficiencia del algoritmo**: 81.5789 % 

---



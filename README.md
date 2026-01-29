# Simulación de Algoritmos de Planificación de Procesos

Este proyecto sirve como base para simular distintos **algoritmos de planificación de procesos** usados en sistemas operativos.

---

## Conjunto de procesos

| Proceso | Llegada | Ejecución |
|--------|---------|-----------|
| P1 | 0 | 5 |
| P2 | 1 | 3 |
| P3 | 2 | 10 |
| P4 | 3 | 1 |
| P5 | 4 | 2 |

---

## Algoritmos de planificación

### FIFO (First In, First Out)

- No expropiativo  
- El primero en llegar es el primero en ejecutarse

**Orden:**  
`P1 → P2 → P3 → P4 → P5`

**Gantt:**

| P1 | P2 | P3 | P4 | P5 |
0 5 8 18 19 21


---

### SJF (Shortest Job First – sin expropiación)

- Selecciona el proceso con menor tiempo de ejecución
- No permite interrupciones

**Orden:**  
`P1 → P4 → P5 → P2 → P3`

**Gantt:**

| P1 | P4 | P5 | P2 | P3 |
0 5 6 8 11 21


---

### SRTF (Shortest Remaining Time First)

- Versión expropiativa de SJF
- Interrumpe si llega un proceso con menor tiempo restante

**Orden real:**  
`P1 → P2 → P4 → P5 → P1 → P3`

**Gantt:**

| P1 | P2 | P4 | P5 | P1 | P3 |
0 1 4 5 7 11 21


---

### Round Robin (Quantum = 2)

- Planificación justa
- Cada proceso se ejecuta por un tiempo fijo

**Quantum:** `2`

**Gantt:**

| P1 | P2 | P3 | P1 | P4 | P5 | P2 | P3 | P1 | P3 | P3 | P3 |
0 2 4 6 8 9 11 12 14 15 17 19 21


---

## Conclusiones

- **FIFO** es simple pero ineficiente en tiempos de espera.
- **SJF** optimiza el tiempo promedio.
- **SRTF** mejora SJF con expropiación.
- **Round Robin** es ideal para sistemas interactivos.

---

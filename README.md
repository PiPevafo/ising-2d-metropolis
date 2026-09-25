# Ising 2D con Metropolis

Simulación Monte Carlo del modelo de Ising en dos dimensiones (red cuadrada, condiciones periódicas de frontera) usando el algoritmo de Metropolis. Tarea 3: Modelo de Ising, Mecánica Estadística - Uniandes.

Todo está en `Tarea3.ipynb`.

## Qué hace

- Implementa Metropolis para el hamiltoniano $H=-J\sum_{\langle i,j\rangle}s_is_j$.
- Guarda energía y magnetización por espín en cada paso Monte Carlo.
- Grafica cómo evoluciona la energía hasta estabilizarse (termalización).
- Calcula promedios de energía y magnetización descartando los primeros pasos.
- Repite para varias temperaturas por debajo y por encima de $T_c$, y grafica $\langle|m|\rangle$ vs $T$.
- Valida contra los límites conocidos ($T\to0$ y $T\to\infty$) y contra $T_c$ exacta de Onsager.

## Requisitos

- Python 3
- numpy
- matplotlib

```
pip install numpy matplotlib
```

## Cómo correrlo

Abrir `Tarea3.ipynb` con Jupyter (o VSCode) y correr las celdas en orden.

```
jupyter notebook Tarea3.ipynb
```

El barrido en temperatura (25 puntos, L=16, 7500 pasos Monte Carlo) tarda unos minutos en correr, todo lo demás es rápido.

## Convención

Un paso Monte Carlo = $N=L^2$ intentos de voltear un espín, para que en promedio cada espín tenga oportunidad de cambiar. Se usa $k_B=1$, así que las temperaturas están en unidades de $J/k_B$.

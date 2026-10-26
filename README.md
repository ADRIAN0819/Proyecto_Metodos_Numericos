# Proyecto de Métodos Numéricos

**Análisis comparativo de la eficiencia de métodos iterativos para el factor de fricción de Colebrook-White en redes de tuberías**

CC2104 Métodos Numéricos - UTEC, ciclo 2026-2. Sección 2, Grupo 2.

## Integrantes

- Diestro Palao Mateo (líder)
- Urbina Mendoza Adrian Aron Fabricio Alberto
- Mitma Martínez Jeanpierre Anthony
- Espinoza Camargo Lázaro Andrei
- Quevedo Vega Ivonne Gianela

## Contenido

```
codigos/
  MN_Codigos_Grupo2.mlx       Implementación y análisis completo
figuras/
  robustez_iteraciones.pdf    Iteraciones en el dominio de Re y rugosidad (objetivo 3)
  costo_repetitivo.pdf        Tiempo total frente al número de tuberías (objetivo 4)
```

## Descripción del código

Se resuelve la ecuación de Colebrook-White en la forma F(x) = 0, con x = 1/sqrt(lambda), mediante tres métodos: bisección, Newton-Raphson y Newton-Secante.

| Bloque | Contenido |
|---|---|
| Código 1 | Parámetros base, punto inicial, tolerancia y ecuación |
| Código 2 | Método de la bisección |
| Código 3 | Método de Newton-Raphson |
| Código 4 | Método híbrido Newton-Secante |
| Código 5 | Comparación en los cinco conjuntos base (objetivo 2) |
| Código 6 | Robustez en una malla de 780 puntos de Re y rugosidad (objetivo 3) |
| Código 7 | Costo de resolver N tuberías, de 10^2 a 10^5 (objetivo 4) |
| Funciones Principales | `biseccion`, `newton`, `newton_analitica`, `new_sec` |

Parámetros comunes: x0 = 7.273626085, tolerancia 1e-8 e intervalo de bisección [3.6, 13.0]. El intervalo [3.68, 12.47] de Praks y Brkić (2018) no contiene la raíz en 8 de los 780 puntos de la malla, por lo que se amplió a partir de las raíces en los extremos del dominio (x = 3.606 y x = 12.975).

## Ejecución

1. Abrir `codigos/MN_Codigos_Grupo2.mlx` en MATLAB (requiere Symbolic Math Toolbox para la función `newton`).
2. Ejecutar con Run. La ejecución completa tarda alrededor de 2 minutos.

El archivo incluye los resultados de la última ejecución. Las raíces y las iteraciones son reproducibles; los tiempos de ejecución varían según el equipo.

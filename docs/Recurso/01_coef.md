---
layout: default
title: Interpretación de coeficientes 
parent: Recursos y Guías
nav_order: 1
mathjax: true
---
# Interpretación de Coeficientes de una Regresión Semilogarítmica

## Regresión: Log-nivel

Para facilitar la interpretación, consideremos la siguiente regresión (hipotético)

$$
\ln(salario_i)= \alpha_0 + \beta_1Sexo_i + \beta_2Edad_i + \epsilon_i
$$

**Donde**:

- **ln** logaritmo natural
- **ln(salario)** es una variable continua.
- **Sexo** es una variable nominal dicotómica o dummy. Hombre: sexo=1, y Mujer: sexo=0
- **Edad** es una varaible continua.

**¿Cómo se interpretan los coeficientes de este tipo de regresión?**

---

* **Primer caso, cuando los coeficientes son pequeños o cercanos a cero.**

  *Supongamos la siguiente regresión:*

  $$
  \ln(salario_i)= 10 + 0.025Sexo_i + 0.012Edad_i + \epsilon_i
  $$

| Interpretación directa                                                                                                                                                                             | Interpretación exacta                                                                                                                                                              |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Efecto**:$$\beta_1 \times 100$$. Ser hombre (sexo = 1) está asociado con un salario aproximadamente 2.5% mayor en comparación con ser mujer, manteniendo las demás variables constantes. | **Efecto** $$(e^{0.025}-1)\times 100 \approx 2.5\%$$. Entonces, el efecto es igual a la interpretación directa. Por lo tanto esto es equivalente hacer $$\beta_1 \times 100$$  |
| **Efecto**: $$\beta_2 \times 100$$. Por cada año adicional de edad, el salario aumenta en aproximadamente 1.2%, manteniendo las demás variables constantes.   | **Efecto** $$(e^{0.012}-1)\times 100 \approx 1.2\%$$. Entonces, el efecto es igual a la interpretación directa.  Por lo tanto esto es equivalente hacer $$\beta_2 \times 100$$ |

---

* **Segundo caso, cuando los coeficientes son grandes.**

  *Supongamos la siguiente regresión:*

  $$
  \ln(salario_i)= 10 + 0.25Sexo_i + 0.52Edad_i + \epsilon_i
  $$

| Interpretación directa                                                                                                                                                                            | Interpretación exacta                                                                                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Efecto**:$$\beta_1 \times 100$$. Ser hombre (sexo = 1) está asociado con un salario aproximadamente 25% mayor en comparación con ser mujer, manteniendo las demás variables constantes. | **Efecto** $$(e^{0.25}-1)\times 100 \approx 28\%$$. Entonces, el efecto no es igual a la interpretación directa.  |
| **Efecto**: $$\beta_2 \times 100$$. Por cada año adicional de edad, el salario aumenta en aproximadamente 52%, manteniendo las demás variables constantes.  | **Efecto** $$(e^{0.52}-1)\times 100 \approx 68\%$$. Entonces, el efecto no es igual a la interpretación directa. Esto implica que el salario incrementa en un 68% por cada año adicional de edad. |

---

#### Conclusión:

**Interpretación directa:** Es una aproximación rápida y fácil de comunicar, especialmente útil para coeficientes pequeños.

**Interpretación exacta:** Es más precisa y debe usarse para coeficientes más grandes o cuando se requiere mayor exactitud del efecto.

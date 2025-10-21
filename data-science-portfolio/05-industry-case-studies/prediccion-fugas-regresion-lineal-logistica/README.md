# Predicción de Fugas mediante Modelos de Regresión

Proyecto de análisis y modelado de datos industriales enfocado en la **predicción de fugas** a partir de variables ambientales y operativas.  
Se implementaron **modelos de regresión lineal y logística** utilizando Python y bibliotecas del ecosistema científico.

---

## Objetivo del Proyecto

Analizar el comportamiento de la variable **Tprom − Tamb** (temperatura promedio menos ambiente)  
y predecir la **ocurrencia de fugas (Fuga = 1)** a partir de variables medidas en planta.

---

## Dataset

El dataset contiene 2927 registros con las siguientes variables:

| Variable | Descripción | Unidad |
|-----------|-------------|--------|
| Temperatura Inferior [°F] | Temperatura en la parte inferior del sistema | °F |
| Humedad Relativa | Porcentaje de humedad ambiental | % |
| Presión Dif Filtro [mmH2O] | Diferencia de presión en el filtro | mmH₂O |
| Potencia [MW] | Potencia de salida del sistema | MW |
| 4-E | Variable técnica de energía o eficiencia | - |
| Presión Dif Enclosure [mmH2O] | Variable utilizada para definir Fuga | mmH₂O |

---

## Flujo del Proyecto

### 1. Análisis Exploratorio de Datos (EDA)
- Identificación de correlaciones entre variables.
- Gráficos de dispersión, boxplots y análisis temporal.
- Detección de posibles outliers y normalización adecuada.

### 2. Modelos de Regresión Lineal
- Variable objetivo: **Tprom − Tamb**  
- Se probaron 5 modelos variando las variables predictoras.  
- Evaluación mediante métricas: **MSE**, **MAE**, **R²**  
- El mejor modelo logró:
  - `MSE ≈ 13.16`
  - `MAE ≈ 2.48`
  - `R² ≈ 0.49`

*Conclusión:* el modelo lineal captura parcialmente la variabilidad de la temperatura diferencial, pero podría mejorarse con modelos no lineales.

###3. Modelos de Regresión Logística
- Variable objetivo: **Fuga = 1 si Presión Dif Enclosure > mediana**
- Variables predictoras seleccionadas:
  - Temperatura Inferior [°F]
  - Humedad Relativa
  - Presión Dif Filtro [mmH2O]
  - Potencia [MW]
  - 4-E
- Normalización de datos con `StandardScaler`.
- División: 70% entrenamiento, 30% prueba.

Evaluación de métricas:
| Métrica | Valor |
|----------|--------|
| Precision | 0.78 |
| Recall | 0.73 |
| F1-score | 0.75 |

*Conclusión:* el modelo logra buena capacidad para identificar correctamente los casos con fuga, aunque se observó un leve desbalanceo en la clase objetivo.

---

## Librerías Utilizadas

- **pandas** – Manipulación de datos  
- **numpy** – Cálculos numéricos  
- **matplotlib / seaborn / plotly** – Visualización de datos  
- **scikit-learn** – Modelado predictivo y métricas  

---

## Modelos Evaluados

| Tipo | Descripción | Variables principales | Mejor métrica |
|------|--------------|----------------------|----------------|
| Regresión Lineal | Predicción de Tprom-Tamb | Temp, Humedad, Potencia, 4-E | R² = 0.49 |
| Regresión Logística | Predicción de Fuga (binaria) | Temp, Humedad, Potencia, 4-E | F1 = 0.75 |

---

## Conclusiones Generales

- Los modelos lineales ofrecen una buena base explicativa, pero podrían mejorarse con técnicas no lineales (árboles o redes neuronales).  
- La variable **Presión Dif Filtro** tuvo gran peso negativo en la predicción de la temperatura diferencial.  
- La normalización **StandardScaler** fue la más adecuada por mantener la media y desviación estándar estables frente a outliers moderados.  
- El modelo de **regresión logística** logró una predicción razonable de la variable *Fuga*, mostrando la relevancia de las variables térmicas y de potencia en el comportamiento del sistema.

---

## Autora

**Victoria Coronel**  
Estudiante de Ciencia de Datos e Inteligencia Artificial (UPATECO)  
Apasionada por el análisis de datos, la programación y la ciencia aplicada.

📫 [LinkedIn](https://www.linkedin.com/in/victtoria77/)  
📁 [GitHub](https://github.com/Vixxtory)

---

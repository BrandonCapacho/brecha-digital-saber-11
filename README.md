# 📶 Brecha digital y resultados Saber 11 en Colombia

**Proyecto final · DATAXPERIENCE · Universidad EAN**

> ¿Qué tanto se relaciona el acceso a internet y computador en el hogar con el puntaje global del examen Saber 11, y podemos usar esa información para predecir el desempeño de un estudiante?

## 👥 Integrantes

| Nombre | Programa |
|---|---|
| BRANDON CAPACHO | Ingeniería de Sistemas |
| JUAN NICOLAS GALINDO | Ingeniería de Sistemas |


## 🎥 Video de presentación



## 📌 Contexto

Como futuros ingenieros de sistemas, la conectividad y el acceso a tecnología son parte de nuestro campo. Analizamos si la **brecha digital** (no tener internet o computador en casa) se convierte en una **brecha de aprendizaje** en el Saber 11, usando datos abiertos del ICFES.

- **Fuente:** ICFES – *Resultados únicos Saber 11*, https://www.datos.gov.co/resource/kgxf-xxbe (API pública).
- **Muestra:** periodo 2022-2, muestra sistemática por consecutivo (termina en 317, 569 u 842): 3.170 filas crudas → **1.584 estudiantes** únicos.
- **Herramientas:** Python en Google Colab · pandas · seaborn/matplotlib · SciPy · statsmodels · scikit-learn.

## 🔍 Principales hallazgos

| | Resultado |
|---|---|
| Brecha de acceso | 28 % de los estudiantes no tiene internet y 46 % no tiene computador en casa |
| Brecha de puntaje | Con internet + PC: **266** puntos en promedio vs. **223** sin ninguno (+42) |
| Prueba de hipótesis | Diferencia por internet significativa (p < 0,001), d de Cohen = 0,68 |
| Dentro de cada estrato | Tener internet suma entre +17 y +31 puntos |
| Modelo múltiple | R² = 0,24 en prueba, MAE = 36,7 pts; internet **+10** y computador **+8** pts controlando el contexto |
| Territorio | Caribe y Amazonía: ~50 % sin internet y los puntajes más bajos |

## 🗂️ Estructura del repositorio

```
├── README.md                     ← este archivo
├── datos/
│   ├── saber11_2022_muestra_raw.csv   ← datos crudos descargados de la API
│   └── saber11_2022_limpio.csv        ← datos depurados (salida de la Etapa 1)
├── notebook/
│   ├── proyecto_saber11_brecha_digital.ipynb   ← cuaderno de Colab con las 3 etapas
│   └── figuras/                                ← gráficos generados por el cuaderno
├── presentacion/
│   ├── presentacion_brecha_digital_saber11.pptx
│   └── presentacion_brecha_digital_saber11.pdf
└── video/
    └── guion_video.md            ← guion y enlace del video
```

## ▶️ Cómo ejecutar

1. Abrir `notebook/proyecto_saber11_brecha_digital.ipynb` en [Google Colab](https://colab.research.google.com/) (Archivo → Abrir cuaderno → GitHub → pegar la URL de este repositorio).
2. Ejecutar todo (*Entorno de ejecución → Ejecutar todas*). Si el cuaderno no encuentra el CSV local, descarga automáticamente la misma muestra desde la API de datos.gov.co.

## 🧭 Etapas del proyecto

1. **Fundamentos y herramientas:** exploración, detección de problemas (duplicados, tipos, valores imposibles, nulos codificados) y limpieza documentada.
2. **Estadística descriptiva:** tendencia central, dispersión, outliers (IQR), comparación de grupos, correlaciones, prueba t de Welch y ANOVA.
3. **Modelado y storytelling:** visualizaciones narrativas, regresión lineal simple y múltiple (train/test, validación cruzada, intervalos de confianza), conclusiones y aplicación profesional.

## 💼 Aplicación profesional

Proponemos un **sistema de alerta temprana y priorización de conectividad educativa**: un pipeline ETL que consume los datos abiertos, un modelo que estima el puntaje esperado por municipio y un dashboard que indica dónde invertir en wifi, equipos y aulas digitales, midiendo luego el impacto.

## ⚠️ Limitaciones

Datos observacionales (asociación, no causalidad), un solo periodo, variables autoreportadas y poder explicativo moderado (R² ≈ 0,25).

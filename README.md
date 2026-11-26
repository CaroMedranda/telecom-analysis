# 📊 Análisis de una empresa de telecomunicaciones - ConnectaTel

## 1. Descripción del proyecto

Este proyecto consiste en un análisis exploratorio de datos (EDA) de **ConnectaTel**, una empresa de telecomunicaciones con operaciones en México y Colombia.

El objetivo principal es comprender cómo se comportan los clientes en relación con el uso de los servicios de llamadas y mensajes, identificar patrones de consumo, detectar valores atípicos y reconocer segmentos de usuarios con necesidades diferenciadas.

A partir de estos hallazgos, se proponen recomendaciones comerciales orientadas a optimizar la oferta de planes, fortalecer la fidelización y generar oportunidades de crecimiento para el negocio.

## 2. Objetivos

- Explorar e integrar información proveniente de diferentes fuentes.
- Identificar problemas de calidad y realizar la limpieza de los datos.
- Analizar las características demográficas de los clientes y sus patrones de consumo.
- Identificar distribuciones y valores atípicos mediante técnicas estadísticas y visualizaciones.
- Segmentar a los usuarios según su edad y nivel de uso.
- Traducir los resultados en conclusiones y recomendaciones accionables para el negocio.

## 3. Datasets utilizados

Para el desarrollo del proyecto se utilizaron tres conjuntos de datos:

| Archivo | Descripción |
|---|---|
| `users_latam.csv` | Información de los clientes: edad, ciudad, fecha de registro, plan contratado y cancelaciones. |
| `usage.csv` | Registros de actividad de los usuarios: llamadas, mensajes, duración y longitud. |
| `planes.csv` | Catálogo de planes disponibles, precios, beneficios y costos por consumo adicional. |

Los tres datasets se complementan para analizar la relación entre las características de los clientes, el plan contratado y el comportamiento de consumo.

**Periodo de análisis:** información registrada hasta 2024, de acuerdo con el alcance del proyecto.

## 4. Herramientas y tecnologías

- **Python:** lenguaje utilizado para el análisis.
- **Pandas:** exploración, limpieza y transformación de datos.
- **NumPy:** operaciones y cálculos numéricos.
- **Matplotlib:** visualización de datos.
- **Seaborn:** construcción de gráficos estadísticos.
- **Jupyter Notebook / Google Colab:** desarrollo y documentación del análisis.
- **GitHub:** almacenamiento y presentación del proyecto.

## 5. Etapas del análisis

El proyecto se desarrolló siguiendo un flujo de trabajo de análisis de datos:

### 1. Carga y exploración de datos
- Importación de los tres datasets.
- Revisión de las primeras filas, dimensiones, columnas y tipos de datos.
- Identificación de inconsistencias iniciales.

### 2. Identificación de problemas de calidad
- Detección de valores nulos y datos faltantes.
- Identificación de valores sentinel e información inválida.
- Revisión de fechas fuera del periodo de análisis.
- Evaluación de la consistencia de los registros.

### 3. Limpieza y transformación
- Corrección de valores inválidos.
- Tratamiento de valores faltantes según su naturaleza.
- Conversión y estandarización de tipos de datos.
- Preparación de las variables para el análisis.

### 4. Análisis estadístico exploratorio
- Cálculo de estadísticas descriptivas.
- Exploración de variables numéricas y categóricas.
- Análisis de edad y comportamiento de consumo.

### 5. Visualización y detección de valores atípicos
- Construcción de histogramas para analizar las distribuciones de edad, mensajes, llamadas y minutos.
- Elaboración de boxplots para identificar posibles valores atípicos.
- Aplicación del método del rango intercuartílico (IQR).
- Evaluación y justificación de la conservación de los valores atípicos identificados.

### 6. Segmentación de clientes
- Clasificación de usuarios por grupos de edad: jóvenes, adultos y adultos mayores.
- Segmentación por nivel de uso: bajo, medio y alto.
- Comparación del comportamiento de consumo según el tipo de plan.

### 7. Análisis ejecutivo y recomendaciones
- Identificación de segmentos de interés comercial.
- Interpretación de patrones de uso y comportamientos extremos.
- Propuestas de fidelización y migración entre planes.
- Recomendaciones para evaluar nuevas alternativas comerciales según las necesidades de los clientes.

## 6. Principales hallazgos

El análisis permitió identificar los siguientes patrones:

- La distribución de mensajes, llamadas y minutos presenta asimetría positiva, con una mayor concentración de usuarios en niveles moderados de consumo.
- Se identificaron valores atípicos en las variables de mensajes, llamadas y minutos, que podrían representar usuarios con mayor intensidad de uso.
- El segmento de uso medio concentra la mayor cantidad de usuarios según la segmentación realizada.
- Se identificaron oportunidades para desarrollar estrategias diferenciadas de fidelización, activación y migración hacia planes con mayores beneficios.
- Se recomienda profundizar en la comparación del consumo por tipo de plan para identificar oportunidades comerciales con mayor precisión.

## 7. Estructura del repositorio

La organización de los archivos del proyecto es la siguiente:

```text
analisis-de-telecomunicaciones/
│
├── data/
│   ├── planes.csv
│   ├── usage.csv
│   └── users_latam.csv
│
├── README.md
│
└── analisis_connectatel.ipynb
```

## 8. Cómo ejecutar el proyecto

El notebook puede ejecutarse utilizando Google Colab o Jupyter Notebook.

### En este caso la opción 2

### Opción 2. Ejecutar localmente con Jupyter Notebook

1. Clonar o descargar el repositorio.
2. Instalar las librerías necesarias:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Abrir Jupyter Notebook desde la carpeta del proyecto:

```bash
jupyter notebook
```

4. Abrir `analisis_connectatel.ipynb`.
5. Ejecutar las celdas en orden.

## 9. Guía de reproducción

Para reproducir los resultados del análisis:

1. Descargar o clonar el repositorio completo.
2. Verificar que los archivos CSV estén ubicados dentro de la carpeta `data`.
3. Confirmar que las rutas de lectura de los archivos en el notebook correspondan a su ubicación:

```python
plans = pd.read_csv('data/planes.csv')
users = pd.read_csv('data/users_latam.csv')
usage = pd.read_csv('data/usage.csv')
```

4. Instalar las dependencias necesarias.
5. Ejecutar todas las celdas del notebook en orden.
6. Revisar las tablas, visualizaciones, segmentaciones y conclusiones generadas.


## 10. Conclusión

Este proyecto permitió aplicar un proceso integral de análisis de datos, desde la exploración y limpieza de información hasta la identificación de patrones de consumo y la segmentación de clientes.

Los resultados muestran cómo el análisis de datos puede contribuir a comprender mejor el comportamiento de los usuarios y proporcionar información útil para la toma de decisiones comerciales.

**Proyecto desarrollado como parte de mi formación en Análisis de Datos en TripleTen.**

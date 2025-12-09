# Actividad 2: Evaluación Exhaustiva de Parámetros en UNet para Segmentación de Vasos Sanguíneos

Este repositorio contiene el código y los resultados de la Actividad 2 de la asignatura de Procesamiento de Imagen Mediante Inteligencia Artificial, del Grado en Ingeniería Biomédica de la Universidad Francisco de Vitoria.

**Autores:**
- Damián Vidal
- Gonzalo Sarabia

## Descripción del Proyecto

El objetivo de este proyecto fue realizar una evaluación exhaustiva de 14 hiperparámetros de un modelo de red neuronal UNet para la segmentación de vasos sanguíneos en imágenes de fondo de ojo. El proyecto implicó un profundo análisis de cómo cada parámetro afecta el rendimiento del modelo, así como la superación de numerosos desafíos técnicos, como desconexiones en Google Colab y la gestión de dependencias.

Durante el desarrollo, se utilizaron herramientas de inteligencia artificial como **Claude** y **Perplexity** para asistir en el análisis del código, la depuración y la interpretación de los resultados.

## Estructura del Repositorio

El repositorio está organizado de la siguiente manera:

```
Actividad2-UNet-Segmentacion/
├── notebooks/                  # Notebooks principales con los experimentos (v2 y v3)
├── codigos_parametros/         # Notebooks individuales para los parámetros 11-14
├── resultados/
│   ├── parametro_10/           # Resultados del Parámetro 10 (Loss Function)
│   ├── parametro_11/           # Resultados del Parámetro 11 (Augmentation)
│   └── parametro_12/           # Resultados del Parámetro 12 (Num Layers)
├── README.md                   # Este archivo
└── .gitignore                  # Archivo para ignorar archivos innecesarios
```

- **`notebooks/`**: Contiene los dos notebooks principales (`Actividad2_Damián_y_Gonzalo_v2.ipynb` y `v3.ipynb`) donde se realizaron la mayoría de los experimentos (parámetros 1-9, 13-14).
- **`codigos_parametros/`**: Contiene los notebooks individuales que se crearon para ejecutar los parámetros 10, 11 y 12 de forma aislada y evitar problemas de memoria en Google Colab.
- **`resultados/`**: Almacena los resultados generados por los notebooks, incluyendo métricas en formato JSON y logs de entrenamiento en formato TXT.

## Cómo Utilizar

1.  **Clonar el repositorio:**
    ```bash
    git clone https://github.com/monchilin81/Actividad2-UNet-Segmentacion.git
    ```
2.  **Abrir en Google Colab:**
    - Sube los notebooks de la carpeta `notebooks/` o `codigos_parametros/` a tu Google Drive.
    - Ábrelos con Google Colab.
3.  **Ejecutar los experimentos:**
    - Asegúrate de tener un entorno con GPU.
    - Ejecuta las celdas en orden para replicar los experimentos.

## Resumen de Resultados

El análisis de los 14 parámetros reveló varios hallazgos clave:

- **Configuración Óptima:** Se encontró que una configuración con 10 épocas, un tamaño de imagen de 256x256, 32 filtros iniciales y el optimizador Adam ofrecía el mejor rendimiento.
- **Resultados Inesperados:** Sorprendentemente, la aumentación de datos no mejoró el rendimiento, y un modelo más simple (menos filtros, menos capas) fue más efectivo, sugiriendo que la calidad de los datos originales era más importante que la cantidad artificialmente generada.
- **Componentes Críticos:** La normalización (Batch Normalization) y la función de pérdida (BCE) demostraron ser componentes esenciales para la estabilidad del entrenamiento.

Para un análisis más detallado, consulta el informe completo del proyecto.

## Herramientas Utilizadas

- **Lenguaje:** Python
- **Librerías Principales:** TensorFlow, Keras, Matplotlib, NumPy, OpenCV
- **Entorno de Desarrollo:** Google Colab
- **Asistentes de IA:** Claude, Perplexity

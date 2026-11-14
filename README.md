
# TP2 - Visión por Computadora I

**CEIA - Facultad de Ingeniería, Universidad de Buenos Aires**

**Alumnos:** Corominas - Fierens - Yanez Flores

## Objetivo

Implementar un detector automático de enfoque sobre un video mediante el análisis de su contenido frecuencial.

Se utiliza la métrica FM propuesta por De y Masilamani (2013) en el artículo *Image Sharpness Measure for Blurred Images in Frequency Domain*.

Se realizan dos experimentos:

1. Cálculo de FM sobre el fotograma completo.
2. Cálculo de FM sobre una región de interés (ROI) central, equivalente al 8 % del área del fotograma.

Se analiza la evolución temporal de la métrica y se identifican automáticamente los intervalos de mayor enfoque mediante un umbral relativo al máximo de FM.

Como punto adicional, se aplica *unsharp masking* para evaluar su efecto sobre la métrica y los intervalos detectados.

## Contenido del repositorio

- `TP2.ipynb`: desarrollo del trabajo práctico, código, gráficos, resultados y conclusiones.
- `focus_video.mov`: video utilizado en los experimentos.
- `ImageSharpnessMeasureforBlurredImagesinFrequency.pdf`: artículo de referencia.
- `README.md`: instrucciones de ejecución.

## Entorno de desarrollo

El trabajo se desarrolló utilizando Python 3.12 y un entorno conda denominado `vision_cv`.

El entorno local se creó clonando `ia_env`, utilizado previamente durante la cursada, e instalando OpenCV.

```bash
conda create -n vision_cv --clone ia_env
conda activate vision_cv
pip install opencv-python
```

## Instalación en otra computadora

Para ejecutar el notebook desde cero, se recomienda tener instalado Anaconda o Miniconda.

Crear y activar un entorno independiente:

```bash
conda create -n vision_cv python=3.12
conda activate vision_cv
```

Instalar las bibliotecas necesarias:

```bash
python -m pip install opencv-python numpy pandas matplotlib jupyter
```

Las bibliotecas utilizadas son:

- **OpenCV:** lectura del video y procesamiento de imágenes.
- **NumPy:** cálculos numéricos y transformada de Fourier.
- **Pandas:** organización y presentación de resultados.
- **Matplotlib:** gráficos y visualización de imágenes.
- **Jupyter:** ejecución del notebook.

## Ejecución

1. Descargar o clonar el repositorio.
2. Abrir una terminal en la carpeta que contiene `TP2.ipynb` y `focus_video.mov`.
3. Activar el entorno e iniciar Jupyter:

```bash
conda activate vision_cv
jupyter notebook TP2.ipynb
```

4. En Jupyter, seleccionar **Restart Kernel and Run All Cells** para ejecutar el trabajo completo desde el comienzo.

El notebook utiliza rutas relativas. Por lo tanto, el directorio de trabajo debe contener el archivo `focus_video.mov`.

## Resultados

El notebook presenta:

- Implementación de los seis pasos de la métrica FM.
- Evolución temporal de FM para el fotograma completo y la ROI central.
- Detección automática del intervalo de enfoque mediante un umbral del 80 % del máximo de FM.
- Análisis de sensibilidad para umbrales del 80 %, 85 % y 90 %.
- Aplicación de unsharp masking y comparación de los intervalos detectados.
- Tablas, gráficos, discusión y conclusiones.

Los resultados se presentan directamente en el notebook y no requieren archivos de salida adicionales.

## Referencia

De, K., & Masilamani, V. (2013). *Image Sharpness Measure for Blurred Images in Frequency Domain*. Procedia Engineering, 64, 149–158.


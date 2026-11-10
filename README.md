# TP2 - Visión por Computadora I

Esta carpeta contiene la resolución del TP2 de la materia Visión por Computadora I (CEIA / FIUBA). El trabajo consiste en implementar un detector de máximo enfoque sobre un video aplicando análisis espectral, similar al que usan las cámaras digitales modernas. Para medir el enfoque se implementa la métrica propuesta en el paper "Image Sharpness Measure for Blurred Images in Frequency Domain", que cuenta las componentes de alta frecuencia del espectro centrado de cada frame.

## Contenido

- `TP2.ipynb`: resolución del trabajo práctico.
- `focus_video.mov`: video de entrada a procesar.
- `ImageSharpnessMeasureforBlurredImagesinFrequency.pdf`: paper de referencia con la métrica a implementar.
- `README.md`: este archivo.

## Entorno

Para correr el notebook se usa un entorno conda llamado `vision_cv`. Fue creado a partir del entorno `ia_env` (armado previamente durante la cursada) agregando la librería de OpenCV, que es la única que faltaba para este trabajo.

Características del entorno:

- Python 3.12.13
- opencv-python 5.0.0
- numpy 2.5.0
- scipy 1.18.0
- matplotlib 3.11.0
- jupyter (IPython 9.15.0, notebook)

## Creación del entorno en esta computadora

El entorno local se creó con estos comandos:

```
conda create -n vision_cv --clone ia_env
conda activate vision_cv
pip install opencv-python
```

## Creación del entorno en otra computadora

Para reproducir el entorno desde cero en otra máquina alcanza con:

```
conda create -n vision_cv python=3.12
conda activate vision_cv
pip install opencv-python numpy scipy matplotlib jupyter
```

## Cómo ejecutar el notebook

Con el entorno activado, abrir Jupyter y lanzar el notebook:

```
conda activate vision_cv
jupyter notebook TP2.ipynb
```

La carpeta de trabajo debe ser esta misma carpeta, porque el notebook lee el video con rutas relativas.

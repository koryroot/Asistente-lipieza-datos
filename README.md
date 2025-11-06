# Asistente Interactivo de Limpieza de Datos (Interactive EDA Cleaner) 🧹📊

[Estado: En Desarrollo 🚧]

Un script de Python para Jupyter/Colab que automatiza el diagnóstico del Análisis Exploratorio de Datos (EDA) y proporciona una interfaz interactiva para la toma de decisiones de limpieza de datos.

## El Problema: El EDA Manual es Lento

El Análisis Exploratorio de Datos (EDA) es fundamental, pero a menudo nos encontramos ejecutando los mismos comandos (`.isnull().sum()`, `.describe()`, `boxplot...`) repetidamente. Identificar un problema es solo el primer paso; decidir *cómo* solucionarlo (imputar, eliminar, transformar) es la parte crítica, y suele ser un proceso manual de prueba y error.

## La Solución: Un Asistente de Decisión

Este proyecto combina el poder del **diagnóstico automático** con la **toma de decisiones interactiva**.

En lugar de solo generar un informe estático, esta herramienta:
1.  **Diagnostica:** Utiliza `ydata-profiling` para escanear un DataFrame e identificar problemas clave (faltantes, duplicados, outliers, tipos de datos).
2.  **Pregunta:** Emplea `ipywidgets` para presentar estos problemas al usuario con opciones de limpieza razonadas (ej. imputar con media, mediana, moda; eliminar filas/columnas).
3.  **Actúa:** Aplica las transformaciones seleccionadas al DataFrame, permitiendo un ciclo de limpieza iterativo y controlado.

## Tecnologías Utilizadas

* **Python 3.x**
* **Pandas:** Para la manipulación de datos.
* **ydata-profiling:** Para la generación de informes de diagnóstico.
* **ipywidgets:** Para la creación de la interfaz interactiva en Jupyter.
* **Scikit-learn:** (Próximamente) Para imputaciones más avanzadas (KNNImputer).

## ¿Cómo Empezar?

1.  Clona este repositorio:
    ```bash
    git clone https://github.com/koryroot/Asistente-lipieza-datos.git
    ```
2.  Instala las dependencias:
    ```bash
    pip install pandas ydata-profiling ipywidgets
    ```
3.  Abre el notebook `interactive_eda.ipynb` en Jupyter Lab o Google Colab.
4.  Carga tu dataset y ¡empieza a limpiar!

## Roadmap (Próximos Pasos)

* [ ] Implementar manejo interactivo de duplicados.
* [ ] Agregar detección y manejo de outliers (IQR, Z-score).
* [ ] Integrar imputación avanzada (KNNImputer) como opción.
* [ ] Añadir visualizaciones "antes y después" de la limpieza.

## Contribuciones

¡Este es un proyecto de aprendizaje y está abierto a contribuciones! Si tienes ideas para mejorar la herramienta, por favor abre un "Issue" o envía un "Pull Request".


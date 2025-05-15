#1. Introducción

El presente trabajo, consiste en un análisis de datos, y modelado de una inteligencia artificial, a partir de un conjunto de datos denominado "adult", proveniente del [censo de los Estados Unidos en el año 1994](https://archive.ics.uci.edu/dataset/2/adult).

El objetivo principal de este proyecto, es analizar los datos brindados por el censo analizando patrones, y buscando posibles desigualdades en los Estados Unidos en el año 1994. También se construirá un modelo capaz de predecir con cierto grado de certeza, si una persona gana más o menos de 50.000 dólares anuales. El dataset a utilizar para entrenar el modelo contiene 30014 filas de datos tras depurar, y tiene las siguientes columnas:

*   **Edad**
*   **Sector laboral**
*   **Peso muestral (Cuantas personas están representadas por los datos presentes en determinada fila)**
*   **Educación formal en años**
*   **Estado civil**
*   **Área laboral**
*   **Relación con el jefe/a de hogar**
*   **Grupo étnico**
*   **Sexo**
*   **Ganancias sobre el capital invertido durante el último año**
*   **Pérdidas sobre el capital invertido durante el último año**
*   **Carga laboral semanal**
*   **País de origen**
*   **Ingreso anual**



#2. Objetivos.

1. Explorar desigualdades salariales por género y raza:
    * Analizar la distribución del nivel de ingresos (mayor o menor a 50K) entre hombres y mujeres, identificando posibles brechas salariales y sus causas.

2. Evaluar el impacto del nivel educativo en los ingresos:
    * Investigar la relación entre los años de educación formal y la proporción de personas con ingresos altos, desglosando esta información por género y carga horaria.

3. Relacionar el estado civil con la carga laboral:
    * Estudiar cómo influye el estado civil en las horas trabajadas semanalmente, diferenciando entre hombres y mujeres.

4. Detectar correlaciones entre variables claves:
    * Utilizar análisis de correlación para descubrir relaciones significativas entre variables como edad, nivel educativo, horas trabajadas, y capital ganado o perdido.

5. Construir un modelo predictivo de ingresos:
    * Desarrollar un modelo de inteligencia artificial capaz de predecir si una persona gana más o menos de 50.000 dólares anuales, basado en variables sociodemográficas y laborales.





#3. Herramientas y técnicas utilizadas

Para desarrollar el modelo, se hará uso del lenguaje de programación Python, y librerías del mismo.
A continuación se detallan las principales librerías y prácticas a utilizar:


*   **Pandas**: Manipulación, carga, y limpieza de datos.
*   **NumPy**: Permite realizar operaciones numéricas y manejar estructuras matriciales.
*   **Scikit-learn**: Será la herramienta principal para construir el modelo de predicción,
    *   *Preprocesamiento*: se utilizará OneHotEncoder para codificar variables categóricas.
    *   *Entrenamiento del modelo*
    *   *Evaluación del modelo*: Usando métricas como accuracy, precision, recall y f1-score.
*   **Matplotlib**: Librería interactiva para la creación de gráficos.
*   **Seaborn**: librería para la visualización de datos graficados, basada en Matplotlib.
*   **Display**: Librería para la visualización de datos en tablas.

Además de estas herramientas mencionadas, se realizarán las siguientes transformaciones sobre el dataset inicial, para facilitar y mejorar el entrenamiento del modelo:


*   Eliminación de las filas con valores faltantes (Representados por "?")
*   Eliminación de la columna 'education' por ser redundante con education-num, y esta última ser más adecuada.
*   Codificación de variables categóricas (One-Hot Encoding)



#4. Consideraciones éticas
En este modelo, he decidido **incluir tanto el sexo como la raza** en los datos a utilizar para entrenar el modelo. El razonamiento para llegar a esta decisión, se basa en la premisa de incluir la mayor cantidad de atributos disponibles en el dataset para ayudar a obtener una predicción más precisa en el modelo, dado que dichas características podrían, si bien no estar directamente relacionadas (No ser inherentes al sexo), sí podrían estar correlacionadas con patrones reales de ingreso, que podrían denotar una desigualdad estructural, o elecciones que tienden a tomar personas de un mismo sexo.
No obstante, en el análisis de los datos, se generarán gráficas con el fin de comparar y reflexionar sobre los posibles sesgos que esto podría introducir en el modelo, y la posible existencia de inequidades de género o de discriminación en los ingresos en los Estados Unidos en el año 1994, y en la actualidad.

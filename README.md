# Modelo ML (Random Forest) de predicción de puntajes ICFES de estudiantes segun sus variables socio-economicas 

*Por favor tener en cuenta que este proyecto dejará de funcionar a partir del mes de julio debido al vencimiento de la licencia de la base de datos en Google Big Querry*

### Navegación rapida:
* **[:exclamation: Información importante](#exclamation-información-importante)**
* **[:page_facing_up: Información del proyecto](#page_facing_up-información-del-proyecto)**
* **[:pushpin: Descripción del proyecto](#pushpin-descripción-del-proyecto)**
* **[:question: Restricciones/aclaraciones](#question-restriccionesaclaraciones)**
***


## :exclamation: Información importante:
Para el correcto funcionamiento es necesario conocer la siguiente información: <br>
* Será necesario que se instalen las dependencias establecidas dentro de cada archivo requirements.txt en cada carpeta establecida para el correcto funcionamiento, por favor recordar que la linea de codigo para realizar esta instalación es la siguiente:<br>
    `pip install -r requirements.txt`
<br>
* Este proyecto solo podrá funcionar con una base de datos activa de las pruebas ICFES proporcionada publicamente por el gobierno de colombia, si desea actualizar, personaliza o utilizar su propia base de datos le sugerimos realizar los siguientes pasos:<br>
**1.** Descargar o guardar la base de datos deseada en algun servicio online o onpremise
**2.** Generar una cuenta de servicios, una clave o una conexion directa a la base de datos. Tener en cuenta que en el proyecto presente se utilizó una cuenta de servicios de Google BigQuerry con una key autogenerada.
**3.** Cambiar la key o la ruta de el acceso a su base de datos segun la que se desee
**4.** Realizar pruebas en caso el funcionamiento no sea el deseado

***


## :page_facing_up: Información del proyecto
Este proyecto está basado en los resultados de las pruebas ICFES otorgados públicamente por el gobierno, que comprenden los resultados desde el año 2013 hasta el año 2021. Se ha realizado un análisis exhaustivo de la información, así como una limpieza de los datos. Posteriormente, estos datos se han pasado a un modelo pre-entrenado de regresión logística, específicamente Random Forest, mediante el cual, gracias a su estudio, se han deducido las variables de mayor impacto. Utilizando estas mismas variables, el modelo generará una respuesta que consiste en el rango más probable en el que el estudiante quede según su calificación de las ICFES.

***

## :pushpin: Descripción del proyecto:
Este proyecto tiene como objetivo proporcionar un rango de resultados probables que un estudiante podría obtener en sus futuras pruebas ICFES, según sus variables socioeconómicas. Se ha alcanzado una precisión del 87%, lo que representa un logro satisfactorio.

Para llevar a cabo este proyecto, se han utilizado los datos públicos proporcionados por el gobierno de Colombia sobre los resultados de las pruebas ICFES, así como todas las variables socioeconómicas relacionadas con cada participante de dichas pruebas. Estos datos abarcan un período desde el año 2013 hasta el año 2021. Fue necesario realizar una limpieza exhaustiva de los datos para garantizar su correcto funcionamiento, lo que resultó en un total de más de 3 millones de resultados obtenidos.

Para la lectura, procesamiento y predicción de estos datos, se ha empleado un modelo preconstruido proporcionado por Scikit-learn en el lenguaje de programación Python. Este lenguaje fue fundamental para el análisis de los datos, proporcionando una matriz de confusión que fue crucial para seleccionar las variables con mayor incidencia en los resultados. Posteriormente, utilizando estos modelos, se entrenó el modelo con los datos en una proporción del 70% para entrenamiento y el 30% para pruebas, lo que resultó en un modelo con una precisión de predicción superior al 80%.

El propósito de este modelo entrenado fue determinar en qué rangos de resultados se ubicaría el participante:

- Puntaje alto: Comprendido entre 500 y 250.
- Puntaje bajo: Comprendido entre 249 y 0.

Posteriormente, esta información se presenta en una interfaz de usuario desarrollada utilizando Flask con Python. Esta interfaz toma los datos que se desean predecir y los transmite a través de una puerta de enlace a Graphene, lo que garantiza una mayor seguridad en el tratamiento de los datos. Graphene accede al modelo con los datos proporcionados y realiza la predicción, que luego se devuelve a la interfaz de usuario mediante otra puerta de enlace.

***

## :question: Restricciones/aclaraciones:
* Este proyecto ha empleado la base de datos libre proporcionada por el gobierno nacional de Colombia de los resultados de las pruebas ICFES tomados de [Datos gov](https://www.datos.gov.co/).

* Este proyecto* **NO** *ofrece una predicción exacta del puntaje futuro; por el contrario, predice un posible rango en el cual podría encontrarse el puntaje futuro.

* En este proyecto, no se ha creado un modelo de regresión logística; en su lugar, se han utilizado los proporcionados por Scikit-learn en el lenguaje de programación Python.

* Se ha utilizado la prueba gratuita de Google BigQuery para almacenar los datos, por lo que transcurrido un tiempo, esta no seguirá en funcionamiento.

<details>
    <summary>Información extra...</summary>

:shipit: **Integrantes**
* Christian Manga Arrazola
* Nefer Medina Ricaurte
* Natalia Mendoza Acosta

:computer: **Asignatura** <br>
*Minería de datos 202330*

:school_satchel: **Programa académico** <br>
*Ingeniería de sistemas y computación*

:mortar_board: **Institución** <br>
*Universidad del Norte*
</details>


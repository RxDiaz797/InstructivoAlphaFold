# InstructivoAlphaFold
Este es un instructivo explicativo sobre la instalacion y ejecucion de AlphaFold
Instructivo AlphaFold Colad
Inteligencia Artificial-  Resolver problemas
Estudiantes de ING. Mecatrónica
Correo
 Alcides Jose Diaz Castellano
alcdiazca@unal.edu.co

Este repositorio es una copia traducida al español de : https://github.com/deepmind/alphafold.git




Este es un instructivo para la implementación, instalación y uso de AlphaFold.
AlphaFold es un sistema de predicción de plegamiento de proteínas basado en aprendizaje profundo desarrollado. Estos son los pasos para ejecutar y usar AlphaFold

Instalación de repositorio desde CERO:

**Si deseas ahorrarte la parte de la instalación, utiliza este notebook: https://colab.research.google.com/drive/1MD7T7L5zqy2aalLyox0VgMvShvCWFIHL?usp=sharing **
Descargar el repositorio

Entrar a google colad https://colab.research.google.com/?hl=es >> archivo (ubicado en la parte superior izquierda de la página web >> Subir Notebook
Del repositorio descargado de GitHub, subir el documento AlphaFold.ipynb ubicado en la carpeta “Notebooks”

	A Continuación se importará como notebook en Google Colab


Una vez cargado el repositorio en Google Colad, se procede con la instalación de librerías y código dentro del mismo


Una vez instalado ir al menú “Setup”  y correr “Install third-party software”, esto  descargar e importar software de terceros en este cuaderno de Colab.


**Ejecutamos la celda numero 2. “Download AlphaFold”**

**Hacer una predicción**

Por favor, pegue la secuencia de su proteína en el cuadro de texto de abajo, luego ejecute las celdas restantes a través de Tiempo de ejecución > Ejecutar después. También puede ejecutar las celdas individualmente pulsando el botón Reproducir de la izquierda.
Especificamos la cadena de nuestra proteína a examinar , recuerda que puede implementar varias secuencias de proteínas.


La siguiente casilla  Ubicada en la parte inferior de la celda, permite ejecutar el modelo multimérica para una única secuencia. Para proteínas que son monoméricas en su forma nativa, o para cadenas individuales muy grandes, se puede obtener mejor precisión y eficiencia de memoria utilizando el modelo multimero.

Debido a la mayor eficiencia de la memoria, el modelo multimero tiene un límite máximo de 4000 residuos, mientras que el modelo monomero tiene un límite de 2500 residuos.

**Ejecutamos la celda numero 4. “Search against genetic databases”**
Una vez que se haya ejecutado esta celda, verá estadísticas sobre la alineación de secuencia múltiple (MSA) que utilizará AlphaFold. En particular, verá qué tan bien cada residuo está cubierto por secuencias similares en el MSA
Tenga en cuenta que la búsqueda en las bases de datos y la predicción en sí pueden llevar algún tiempo, de minutos a horas, dependiendo de la longitud de la proteína y del tipo de GPU que le haya asignado Colab (ver FAQ más abajo).



**Ejecutamos la celda número 5. “Run AlphaFold and download prediction”,** esta celda nos proporciona la visualización de nuestra proteína con información gráfica, antes deberá especificarle al programa “multimer_model_max_num_recycles”, por defecto viene en 3.
El modelo multimérico continuará reciclando hasta que las predicciones dejen de cambiar, hasta el límite establecido aquí. Para una mayor precisión, al costo potencial de tiempos de inferencia más largos, establezca esto en 20.







**FAQ & Troubleshooting**
¿Cómo puedo obtener una predicción de la estructura de mi proteína?


Haga clic en el botón Conectar de la parte superior derecha para empezar.
Pegue la secuencia de aminoácidos de su proteína (sin encabezados) en "Introducir la secuencia de aminoácidos a plegar".
Ejecute todas las celdas en el Colab, ya sea ejecutándose individualmente (con el botón de reproducción en el lado izquierdo) o a través de Runtime > Run all. Asegúrese de ejecutar las 5 celdas en orden.
La estructura de la proteína predicha se descargará una vez que se hayan ejecutado todas las celdas. Nota: Esto puede tardar de minutos a horas - ver más abajo.


**¿Cuánto tiempo tardará?**

La descarga del código fuente de AlphaFold puede tardar unos minutos.
La descarga e instalación del software de terceros puede llevar unos minutos.
La búsqueda en bases de datos genéticas puede llevar de minutos a horas.
Ejecutar AlphaFold y generar la predicción puede llevar de minutos a horas, dependiendo de la longitud de su proteína y del tipo de GPU que Colab le haya asignado.
Parece que mi Colab ya no hace nada, ¿qué debo hacer?
Algunos pasos pueden tardar de minutos a horas en completarse.
Si no ocurre nada o si recibe un mensaje de error, intente reiniciar el tiempo de ejecución de Colab a través de Tiempo de ejecución > Reiniciar tiempo de ejecución.
Si esto no ayuda, intente reiniciar su Colab runtime a través de Runtime > Factory reset runtime.


**¿Qué es un Colab?**

Google Colab es un entorno de Jupyter Notebook gratuito que se ejecuta en la nube y es proporcionado por Google. Es una herramienta útil para investigadores, estudiantes y desarrolladores que desean experimentar con tecnologías de inteligencia artificial, aprender a programar y crear aplicaciones de aprendizaje automático.

Con Google Colab, puedes escribir y ejecutar código en lenguajes como Python, ejecutar tareas de procesamiento de datos y visualización de datos, entre otras cosas. Además, Google Colab proporciona acceso a GPUs y TPUs gratuitos, lo que lo hace ideal para tareas de aprendizaje profundo que requieren mucho poder de procesamiento.

En resumen, Google Colab es una herramienta de código abierto que permite a los usuarios crear y ejecutar proyectos de aprendizaje automático en la nube, lo que facilita el acceso a tecnologías avanzadas y la colaboración con otros usuarios en tiempo real.





 




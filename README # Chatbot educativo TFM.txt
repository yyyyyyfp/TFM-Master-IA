# Chatbot educativo TFM

Este notebook permite probar la recuperación de información en los documentos docentes de la asignatura «La IA en el mundo empresarial». El sistema localiza fragmentos relacionados con una pregunta y muestra frases extraídas con el nombre del documento y la página de origen. No genera respuestas mediante un modelo de lenguaje.

## Archivos necesarios

- El notebook `Chatbot_educativo_TFM Yaiza.ipynb`.
- Los documentos PDF de la asignatura, guardados en la carpeta **Documentacion asignatura** de Dropbox.

## Abrir el notebook

1. Descarga el notebook desde Dropbox.
2. Abre [Google Colab](https://colab.research.google.com/).
3. Selecciona **Archivo > Subir notebook** y carga el archivo descargado.

## Ejecutar una consulta

1. Ejecuta las celdas iniciales en orden. La primera instala las bibliotecas necesarias.
2. Cuando aparezca la celda para cargar archivos, descarga los PDF desde **Documentacion asignatura** a tu equipo y selecciónalos para cargarlos en Colab.
3. Continúa ejecutando las celdas en orden para extraer el texto, crear los fragmentos y preparar la búsqueda semántica.
4. Cuando llegues a la celda que solicita una clave de OpenAI, no la ejecutes. La consulta de prueba no utiliza esa API. En su lugar, añade una celda de código justo debajo, copia estas líneas y ejecútalas:

   ```python
   TOP_K = 4
   UMBRAL_SIMILITUD = 0.20
   ```

5. Continúa ejecutando las celdas que definen las funciones de consulta.
6. Ejecuta la celda de consulta interactiva, donde aparece el mensaje «Escribe tu pregunta sobre el material docente», e introduce esta pregunta de ejemplo: ¿Qué usos de inteligencia artificial se describen para Tesla?

## Resultado esperado

El notebook mostrará frases de los fragmentos recuperados, junto con el documento y la página de origen. La prueba sirve para observar la recuperación de información de los materiales docentes; la salida no es una respuesta redactada por un modelo generativo.
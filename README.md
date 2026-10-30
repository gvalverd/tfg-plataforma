# Plataforma de TFG y TFM

Cuestionario inicial para alumnos de TFG y TFM, con recomendación de línea de trabajo y propuesta en Word para el tutor. Sirve para varias universidades, convocatorias y tutores.

**Web:** https://tfg.brain-ford-demos.live

## Qué hace

- **Alumnos.** Cada convocatoria tiene su enlace (`/?c=nombre-de-la-convocatoria`). El alumno rellena el cuestionario, que se adapta a sus respuestas, y recibe un enlace personal para volver a editarlo. Solo ve lo suyo.
- **Tutores.** En `/tutor.html` cada profesor se registra y, cuando el administrador lo aprueba, crea convocatorias a partir de una plantilla (TFG, TFM o vacía) o copiando otra.
- **Cotutela.** Una convocatoria se puede compartir con otros profesores. Todos ven a los alumnos y reciben el aviso de cada respuesta.
- **Recomendador.** Compara el nivel que pide cada línea con las respuestas del alumno (programación, estadística, aprendizaje automático y negocio), su interés, sus preferencias y el sector que le motiva.
- **Documentos.** Propuesta de TFG/TFM en Word con problema, objetivos y fases de la línea elegida, ficha completa en Markdown y exportación a CSV.
- **Editables por convocatoria.** Preguntas (con condiciones para mostrarlas), textos de la página del alumno y líneas de trabajo.

## Cómo está hecho

Páginas estáticas en GitHub Pages y base de datos en Supabase. Las reglas de seguridad viven en la base de datos: un alumno solo puede leer su propia respuesta y cada tutor solo ve las convocatorias en las que participa. Los avisos se envían por correo con Resend.

| Archivo | Para qué |
| --- | --- |
| `index.html` | Cuestionario del alumno |
| `tutor.html` y `tutor-*.js` | Panel del tutor |
| `shared.js` | Preguntas condicionales y recomendador |
| `plantillas.js` | Plantillas de cuestionario y líneas |
| `config.js` | Dirección del proyecto de Supabase y clave pública |

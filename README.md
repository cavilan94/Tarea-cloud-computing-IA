En el presente documento se dara una descripción del proyecto desarrollado para la materia NUTI (nuevas tecnologías de la información), en la conferencia: HPC y sus aplicaciones en simulación basada en Agentes.

El proyecto tiene como objetivo: Crear y publicar un sitio web estático que funcione como CV/perfil profesional utilizando Azure App Service para la publicación del sitio, un repositorio en github para el control de versiones y Kiro, una herramienta para eld esarrollo de codigo potenciada con IA.
La arquitectura del proyecto se puede ver a continuación:

<img width="1017" height="651" alt="image" src="https://github.com/user-attachments/assets/b0f03c56-0156-44b7-9f6f-e057d2ea9652" />

A continuación se indicaran los pasos ejecutados apra el desarrollo del proyecto:
1. Se descargó e instaló Kiro desde su sitio web, y se le realizó una solicitud para crear un sitio web estático de una sola página en HTML y CSS puro, indicandole que se requería para ser suado como una hoja de vida de un perfil profesional con los siguientes campos: Nombre completo, Foto profesional, resumen profesional, formación académica, habilidades técnicas, proyectos e información de contacto.
2. Kiro generó 2 archivos, uno en HTML con toda la estructura del codigo/campos solicitados y un archivo CSS, con los estilos de la pagina estática.
3. se validó localmente cone l uso de un navegador que el archivo generado en html si mostrara contenido, el resultado fue una pagina webe statica que servia como hoja de vida, sin embargo el contenido tocaba editarlo ya que como no se indicó que ingresar en cada uno de los campos solicitados, creo la hoja de vida para el perfil de un desarrollador fullstack, ya que kiro es una herramienta para desarrollo de codigo, asume que el proyecto esta pensado para un desarrollador.
4. Se creo un repositorio publico en github para subir los archivos creados por kiro, modificados y con la información correcta, se subieron 3 archivos al repositorio, el HTML, el CSS y una foto para usar dentro de la hoja de vida generada.
5. Se ingreso al portal de AZURE desde el perfil de estudiante y se creó un app service para poder desplegar la pagina estatica, se creo teniendo en cuenta cercania de regiones, tipo de arquitectura implementada (codigo) y el plan de tarífa F1 (gratuito).
6. Ya una vez se tiene el app service creado se procedió a configurar en el centro de despliegue de Azure la integración con github para poder hacer el despliegue automatico del codigo presente en el repositorio.

En el presente documento se dará una descripción del proyecto desarrollado para la materia NUTI (nuevas tecnologías de la información), en la conferencia: HPC y sus aplicaciones en simulación basada en Agentes.

El proyecto tiene como objetivo: Crear y publicar un sitio web estático que funcione como CV/perfil profesional utilizando Azure App Service para la publicación del sitio, un repositorio en github para el control de versiones y Kiro, una herramienta para el desarrollo de código potenciada con IA. La arquitectura del proyecto se puede ver a continuación:

<img width="1017" height="651" alt="image" src="https://github.com/user-attachments/assets/b0f03c56-0156-44b7-9f6f-e057d2ea9652" />

A continuación se indicaran los pasos ejecutados para el desarrollo del proyecto:
1. Se descargó e instaló Kiro desde su sitio web (https://kiro.dev/), y se le realizó una solicitud para crear un sitio web estático de una sola página en HTML y CSS puro, indicándole que se requería para ser usado como una hoja de vida de un perfil profesional con los siguientes campos: Nombre completo, Foto profesional, resumen profesional, formación académica, habilidades técnicas, proyectos e información de contacto.
2. Kiro generó 2 archivos, uno en HTML con toda la estructura del código/campos solicitados y un archivo CSS, con los estilos de la pagina estática.
3. se validó localmente con el uso de un navegador que el archivo generado en html si mostrara contenido, el resultado fue una pagina web estática que sirve como hoja de vida, sin embargo el contenido tocaba editarlo ya que como no se indicó que ingresar en cada uno de los campos solicitados, creo la hoja de vida para el perfil de un desarrollador fullstack, ya que kiro es una herramienta para desarrollo de código, asume que el proyecto esta pensado para un desarrollador; se hicieron ajustes tanto de contenido como de diseño hasta obtener el resultado deseado.
4. Se creo un repositorio publico en github para subir los archivos creados por kiro, modificados y con la información correcta, se subieron 3 archivos al repositorio, el HTML, el CSS y una foto para usar dentro de la hoja de vida generada, todos los archivos se subieron en la rama main del repositorio.
5. Se ingreso al portal de AZURE desde el perfil de estudiante y se creó un app service para poder desplegar la pagina estática, se creo teniendo en cuenta cercanía de regiones, tipo de arquitectura implementada (código) y el plan de tarifa F1 (gratuito).
6. Ya una vez se tiene el app service creado se procedió a configurar en el centro de despliegue de Azure la integración con github para poder hacer el despliegue automático del código presente en el repositorio, indicando el nombre del repositorio y la rama donde se encuentran los archivos.
7. Una vez se guardo la configuración del centro de despliegue, inicio de forma automática el despliegue de la pagina web estática y en minutos se completó de forma exitosa y desde el app service al dar clic en la URL generada para el servicio, se pudo evidenciar que la pagina web estática estaba funcionando de manera correcta.
8. Por último se hicieron pruebas haciendo pequeñas modificaciones en el contenido del archivo html, para forzar un cambio de versión y por ende un redespliegue, se evidenció que los cambios eran aplicados de forma automática y que le tomaba unos minutos aplicarlos.


Archivos del repositorio en la rama main, para el despliegue de la pagina
<img width="1162" height="552" alt="image" src="https://github.com/user-attachments/assets/05cdc83b-f457-4da0-b586-6982ac5b748b" />

Appservice desplegado y activo
<img width="1827" height="402" alt="image" src="https://github.com/user-attachments/assets/39df73ca-37f7-41b9-bd1f-cfd57f104506" />

Centro de implementación, despliegues realizados
<img width="1237" height="537" alt="image" src="https://github.com/user-attachments/assets/830dc4b6-f1d3-4f8a-862d-942ac246e18c" />

Pagina web estática desplegada en Azure App service.
<img width="1482" height="546" alt="image" src="https://github.com/user-attachments/assets/b0c96793-b33a-4035-9081-09f75c3eb999" />


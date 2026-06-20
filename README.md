# -DOSW_LABORATORIO_3_JonathanJonathanCarlos
- ¿Qué es un pull request en GitHub?

Un pull request es una solicitud para que los cambios realizados en un repositorio sean revisados e integrados en el proyecto original. Es una herramienta esencial para colaborar en proyectos de código abierto o en equipo, permitiendo a los desarrolladores contribuir con mejoras, correcciones o nuevas funcionalidades.

- ¿Cómo se crea un pull request en GitHub?

lo primero es clonar el repositorio de forma local con git clone
segundo creamos una nueva rama para trabajar en cambios con git checkout -b
realizamos cambios y confirmalos con git add . y git commit -m
y los enviamos con git push

Crear el Pull Request Ve a tu repositorio en GitHub y haz clic en el botón "Pull Request". Proporciona una descripción detallada de los cambios realizados y envía la solicitud.

Sincronizar con el Repositorio Original

Antes de enviar un pull request, sincroniza tu rama maestra con el repositorio original para evitar conflictos:

git remote add upstream [URL DEL REPOSITORIO ORIGINAL]
git fetch upstream
git checkout master
git merge upstream/master
git push origin master

Si tu pull request es aceptado, recibirás una notificación. En caso de rechazo, no te desanimes; los mantenedores del proyecto buscan lo mejor para el código. Sigue practicando y contribuyendo al mundo del código abierto

- ¿Cómo se aprueba un pull request en GitHub?

Los mantenedores revisarán tu Pull Request, podrán hacer comentarios o solicitar ajustes.

Si es aprobado, tus cambios serán fusionados al repositorio original.

Consejos Importantes

Asegúrate de seguir las directrices del proyecto (archivo CONTRIBUTING.md si existe).

Mantén tus Pull Requests pequeños y específicos para facilitar la revisión.

Resuelve conflictos antes de enviar el Pull Request.

Con estos pasos, estarás listo para colaborar eficazmente en proyectos de código abierto o privados en GitHub.

- Bibliografía en norma APA de las fuentes consultadas.

Bibliografía
Aprende Git. (s. f.). ¿Qué es un pull request? https://aprendegit.com/que-es-un-pull-request/
freeCodeCamp. (s. f.). Cómo hacer tu primer pull request en GitHub. https://www.freecodecamp.org/espanol/news/como-hacer-tu-primer-pull-request-en-github/
GitHub Docs. (s. f.). Crear una solicitud de extracción (pull request). https://docs.github.com/es/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request?gt

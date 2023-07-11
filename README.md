Requisitos previos
Antes de comenzar, asegúrate de tener instalado lo siguiente:

Node.js: Visita https://nodejs.org y descarga la versión adecuada para tu sistema operativo.

Git: Visita https://git-scm.com/downloads y descarga la versión adecuada para tu sistema operativo.

Vue: Si aún no tienes Vue instalado, puedes instalarlo ejecutando el siguiente comando:

npm install -g @vue/cli

Pasos
Clona el repositorio: Abre una terminal y ejecuta el siguiente comando para clonar el repositorio de Vue:

git clone <URL_DEL_REPOSITORIO>

Reemplaza <URL_DEL_REPOSITORIO> con la URL del repositorio que deseas clonar.

Accede al directorio del proyecto: Navega al directorio del proyecto clonado ejecutando el siguiente comando:

cd <NOMBRE_DEL_DIRECTORIO>

Reemplaza <NOMBRE_DEL_DIRECTORIO> con el nombre del directorio del proyecto clonado.

Instala las dependencias: Ejecuta el siguiente comando para instalar las dependencias del proyecto:

npm install
Esto descargará todas las dependencias necesarias definidas en el archivo package.json del proyecto.

Crea el archivo .env: En la raíz del proyecto, crea un archivo llamado .env y añade la siguiente línea:

VUE_APP_API_URL=https://localhost:7003/api/

Esta configuración permitirá que el proyecto acceda a la URL de la API.

Levanta el proyecto: Una vez que hayas completado los pasos anteriores, puedes levantar el proyecto ejecutando el siguiente comando:

npm run dev
Esto iniciará un servidor de desarrollo y el proyecto estará disponible en tu navegador en la dirección http://localhost:8080 (o en otro puerto si se especifica).
# lubee-front

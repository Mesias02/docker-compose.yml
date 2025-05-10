# docker-compose.yml
### 1. Titulo
Wordpress con postgresql-pgadmin  en docker-compose

### 2. Tiempo de duración
El tiempo fue de 180 minutos.

### 3. Fundamentos
Volúmenes Docker
Los volúmenes en Docker permiten almacenar datos de forma persistente más allá del ciclo de vida del contenedor. En el documento, se hace mención a la asociación de volúmenes en los servicios definidos en docker-compose.yml, lo cual garantiza que los datos de las bases de datos y aplicaciones (como WordPress y MySQL) no se pierdan al detener o eliminar contenedores.

PostgreSQL
Aunque el documento se enfoca principalmente en WordPress y MySQL, el principio de persistencia con volúmenes se aplica también a PostgreSQL, asegurando la retención de datos tras reinicios del servicio. Esta práctica es directamente extrapolable a entornos con PostgreSQL, donde se usarían volúmenes para almacenar datos del contenedor.

Docker compose
Es una herramienta que permite definir y ejecutar aplicaciones Docker con múltiples contenedores. Con Compose, usas un archivo YAML para configurar los servicios de tu aplicación. Luego, con un solo comando, puedes crear e iniciar todos los servicios especificados en tu configuración" (Docker Docs, 2025)

### 4. Conocimientos previos
Para desarrollar esta práctica, se requiere que el estudiante tenga conocimientos básicos sobre:

Docker y su línea de comandos.

Creación y edición de archivos docker-compose.yml.

Conceptos generales sobre contenedores, redes y volúmenes.

Manejo básico de servidores de bases de datos como MySQL o PostgreSQL.

Administración de servicios web como WordPress y phpMyAdmin.

### 5. Objetivos a alcanzar
Verificar la instalación de Docker Compose.

Asegurarse de que Docker esté funcionando correctamente.

Crear un entorno funcional con WordPress, MySQL y phpMyAdmin usando Docker Compose.

Configurar redes y volúmenes en Docker para asegurar la persistencia de datos.

### 6. Equipo necesario
Computadora personal.

Docker y Docker Compose instalados y funcionando.

Editor de texto (Visual Studio Code, Notepad++, etc.).

Navegador web para acceder a WordPress y phpMyAdmin.

### 7. Material de apoyo
Documentación oficial de Docker.

Documentación oficial de Docker Compose.

Recursos en línea sobre instalación y uso de WordPress con Docker.

Videos tutoriales sobre Docker, WordPress y bases de datos.

Guía de la asignatura.

### 8. Procedimiento
Parte 1: Preparación del entorno
Verificar que Docker Compose esté instalado en el sistema.

Validar que Docker se esté ejecutando correctamente.

Parte 2: Estructura del proyecto
Crear un directorio para el proyecto.

Dentro del directorio, crear un archivo docker-compose.yml.

Parte 3: Configuración de servicios
En el archivo docker-compose.yml, configurar tres servicios:

WordPress: para la gestión de contenido.

MySQL: como motor de base de datos.

phpMyAdmin: como interfaz de administración de la base de datos.

Asociar una red común entre los servicios.

Crear y asociar un volumen para asegurar la persistencia de datos de la base de datos MySQL.

Parte 4: Despliegue
Levantar los servicios utilizando el comando:

Copiar
Editar
docker-compose up -d
Parte 5: Verificación
Verificar que los contenedores estén activos.

Acceder a:

WordPress desde el navegador para confirmar su funcionamiento.

phpMyAdmin para gestionar la base de datos y validar la conexión con MySQL.

### 9. Resultados esperados
Se logró verificar que Docker y Docker Compose estaban correctamente instalados y funcionando.

Se creó un entorno completo de desarrollo utilizando Docker Compose con WordPress, MySQL y phpMyAdmin.

La configuración con redes y volúmenes permitió que los servicios se comuniquen entre sí y se mantuvieran los datos persistentes incluso tras reiniciar los contenedores.

Este entorno se puede adaptar fácilmente para trabajar también con PostgreSQL, sustituyendo el servicio de MySQL en el docker-compose.yml.

### 10. Bibliografía
Docker Documentation. (n.d.). Volumes. Recuperado el 17 de abril de 2025 de: https://docs-docker-com.translate.goog/engine/storage/volumes/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc

Docker Blog. (n.d.). How to Use the Postgres Docker Official Image. Recuperado el 17 de abril de 2025 de: https://www.docker.com/blog/how-to-use-the-postgres-docker-official-image/

Docker Docs. (2025). Overview of Docker Compose. Docker. Recuperado el 10 de mayo de 2025, de https://docs.docker.com/compose/

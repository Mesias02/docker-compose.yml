# docker-compose.yml

---
### 1. Titulo
Wordpress con postgresql-pgadmin  en docker-compose formato yml

![image](https://github.com/user-attachments/assets/4d5dc3e1-8561-41e4-8169-d62e17598d23)

---
### 2. Tiempo de duración
El tiempo fue de 180 minutos.

---
### 3. Fundamentos
Volúmenes Docker
Los volúmenes en Docker permiten almacenar datos de forma persistente más allá del ciclo de vida del contenedor. En el documento, se hace mención a la asociación de volúmenes en los servicios definidos en docker-compose.yml, lo cual garantiza que los datos de las bases de datos y aplicaciones (como WordPress y MySQL) no se pierdan al detener o eliminar contenedores.

![image](https://github.com/user-attachments/assets/af3eaa24-1c30-467d-8c63-839780a46e1f)


PostgreSQL
Aunque el documento se enfoca principalmente en WordPress y MySQL, el principio de persistencia con volúmenes se aplica también a PostgreSQL, asegurando la retención de datos tras reinicios del servicio. Esta práctica es directamente extrapolable a entornos con PostgreSQL, donde se usarían volúmenes para almacenar datos del contenedor.

![image](https://github.com/user-attachments/assets/c78b927d-b3fb-4320-85e9-fc9448826b39)


Docker compose
Es una herramienta que permite definir y ejecutar aplicaciones Docker con múltiples contenedores. Con Compose, usas un archivo YAML para configurar los servicios de tu aplicación. Luego, con un solo comando, puedes crear e iniciar todos los servicios especificados en tu configuración" (Docker Docs, 2025)

![image](https://github.com/user-attachments/assets/de73263c-b359-4e3f-b53a-36b2014b547b)

---
### 4. Conocimientos previos
Para desarrollar esta práctica, se debe tener conocimientos básicos sobre:

Docker y su línea de comandos.

Creación y edición de archivos docker-compose.yml.

Conceptos generales sobre contenedores, redes y volúmenes.

Manejo básico de servidores de bases de datos como MySQL o PostgreSQL.

Administración de servicios web como WordPress y phpMyAdmin.

---
### 5. Objetivos a alcanzar
Construir un archivo docker compose usando el formato YML.

Estructurar 3 servicios: wordpress, mysql, phpmyadmin

Definir una red.

Definir un volumen

---
### 6. Equipo necesario
Computadora personal.

Docker y Docker Compose instalados y funcionando.

Editor de texto (Visual Studio Code, Notepad++, etc.).

Navegador web para acceder a WordPress y phpMyAdmin.

---
### 7. Material de apoyo
Documentación oficial de Docker.

Documentación oficial de Docker Compose.

Recursos en línea sobre instalación y uso de WordPress con Docker.

Videos tutoriales sobre Docker, WordPress y bases de datos.

Guía de la asignatura.

---
### 8. Procedimiento
Parte 1: Preparación del entorno
Verificar que Docker Compose esté instalado en el sistema.

![image](https://github.com/user-attachments/assets/64fd7462-5e08-4846-86cc-bc18fd1df072)

Validar que Docker se esté ejecutando correctamente.

![image](https://github.com/user-attachments/assets/4fdf878a-478e-49d5-b10a-12d9c7256ab1)

Parte 2: Estructura del proyecto
Crear un directorio para el proyecto.

![image](https://github.com/user-attachments/assets/b81d913f-8d0a-43d6-9e11-f9cdd2a0b932)

Dentro del directorio, crear un archivo docker-compose.yml.

![image](https://github.com/user-attachments/assets/ddb25e5d-3671-44b4-94fe-e1a3effa73e1)


Parte 3: Configuración de servicios
En el archivo docker-compose.yml, configurar tres servicios:

![image](https://github.com/user-attachments/assets/0772e7f7-7b90-4edc-b08d-683305fca788)

WordPress: para la gestión de contenido.

![image](https://github.com/user-attachments/assets/fd2eaf28-1821-40ab-a867-21537b3d63b7)

MySQL: como motor de base de datos.

![image](https://github.com/user-attachments/assets/337f2833-430d-48d2-bd80-216b8073ff82)

phpMyAdmin: como interfaz de administración de la base de datos.

![image](https://github.com/user-attachments/assets/8d383b10-0167-4948-955a-950e24014626)

Asociar una red común entre los servicios.

![image](https://github.com/user-attachments/assets/e25c03d0-e6c7-4ce0-ac6a-a8c156e656fd)

Crear y asociar un volumen para asegurar la persistencia de datos de la base de datos MySQL.

![image](https://github.com/user-attachments/assets/403270ae-a312-4400-a2d6-6b7fb0077b03)

Parte 4: Despliegue
Levantar los servicios utilizando el comando:
Copiar
Editar

![image](https://github.com/user-attachments/assets/d1e31840-8a61-45f8-8dc0-f2f748bf8c2a)

docker-compose up -d

![image](https://github.com/user-attachments/assets/8840c286-4fb3-4360-962e-f66f85def018)

Parte 5: Verificación
Verificar que los contenedores estén activos.

Acceder a:

WordPress desde el navegador para confirmar su funcionamiento.

![image](https://github.com/user-attachments/assets/bba5214e-7508-4ea3-b1c7-098cf5ee9d0e)

![image](https://github.com/user-attachments/assets/40ea62e9-16b0-43a1-9572-2edf81e0847e)


phpMyAdmin para gestionar la base de datos y validar la conexión con MySQL.

![image](https://github.com/user-attachments/assets/877ba516-ea66-4471-981f-36409a9f3338)

---
### 9. Resultados esperados
Se logró verificar que Docker y Docker Compose estaban correctamente instalados y funcionando.

Se creó un entorno completo de desarrollo utilizando Docker Compose con WordPress, MySQL y phpMyAdmin.

La configuración con redes y volúmenes permitió que los servicios se comuniquen entre sí y se mantuvieran los datos persistentes incluso tras reiniciar los contenedores.

Este entorno se puede adaptar fácilmente para trabajar también con PostgreSQL, sustituyendo el servicio de MySQL en el docker-compose.yml.

---
### 10. Bibliografía
Docker Documentation. (n.d.). Volumes. Recuperado el 17 de abril de 2025 de: https://docs-docker-com.translate.goog/engine/storage/volumes/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc

Docker Blog. (n.d.). How to Use the Postgres Docker Official Image. Recuperado el 17 de abril de 2025 de: https://www.docker.com/blog/how-to-use-the-postgres-docker-official-image/

Docker Docs. (2025). Overview of Docker Compose. Docker. Recuperado el 10 de mayo de 2025, de https://docs.docker.com/compose/

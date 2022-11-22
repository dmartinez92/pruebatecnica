
# Prueba 2
## Despliegue de una aplicación Django y React.js 
Elaborar el deployment dockerizado de una aplicación en django (backend) con frontend
en React.js contenida en el repositorio. Es necesario desplegar todos los servicios
en un solo docker-compose.
Se deben entregar los Dockerfiles pertinentes para elaborar el despliegue y justificar la forma en la que elabora el deployment (supervisor, scripts, dockercompose, kubernetes, etc)
Subir todo lo elaborado a un repositorio (github, gitlab, bitbucket, etc). En el
repositorio se debe incluir el código de la aplicación y un archivo README.md
con instrucciones detalladas para compilar y desplegar la aplicación, tanto en
una PC local como en la nube (AWS o GCP)
# SOLUCION

Se comienza haciendo el dockerfile de la imagen de backend. Se intento utilizar python 3.9 pero daba error por los requirement se coloco la version python 3.7. Al intentar crear la imagen los logs muestran errors de instalaciones faltantes que fueron solucionadas con la instalacion en RUN. Ademas se agrega el archivo .env que es necesitaria para django 
Se expone el puerto 8000 que es el que django utiliza por defecto


Para el frontend no hubo mucho inconveniente al crear la imagen. Se utiliza node:alpine por lo ligero se copia los archivos,se hace un RUN de npm install y se expone el puerto 3000 que es el defecto de node 


## Docker compose 
Para el docker compose se utiliza la version estable 3.7 se crean los dos servicios tanto frontend como backend, se buildean la imagen con el dockerfile en su directorio y se exponen los mismos puertos de los dockerfiles. En el backend se tuvo que especificar el archivo env y necesitario.

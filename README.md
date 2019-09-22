#Introducción
Este repositorio continene los ficheros originales del artículo del blog Contenedor Inseguro sobre la herramienta trivy de Aquasec. Esta herramienta permite auditar la seguridad de imágenes de Docker. 

En el artículo se utiliza una aplicación sencilla en python y varios ejemplos de imágenes con diferentes configuraciones e imágenes base para ver las vulnerabilidades que detecta Trivy en cada una de ellas.  

#Instalación
Para bajar el copiar el repositorio: 


Para ejecutar en local la aplicación se requieren las siguientes librerías: 
* Flask
* waitress

Para la instalación de estos paquetes: 

```
pip3 install Flask waitress
```

Para crear las imágenes deberéis tener instalado Docker y para la la auditoría de seguridad de las imágenes hay que instalar trivy. 

#Creando las imágenes de Docker
A continuación se muestran los comandos para crear las diferentes imágenes con las que se va a probar trivy.

Imagen base python:3.5-alpine

```
docker build -f Dockerfile_alpine_python35 -t pythonapp-alpine-python35 .
```

Imagen base python:3.5.7-alpine3.10

```
docker build -f Dockerfile_alpine310_python357 -t pythonapp-alpine310-python357 .
```

Imagen base python:3.5-stretch

```
docker build -f Dockerfile_stretch_python35 -t pythonapp-stretch-python35 .
```




author: Álvaro Caro Fernández
summary: Realizar la adquisición forense de una memoria USB empleando las siguientes herramientas: FTK Imager, GuyImager y dd
id: Actividad05
categories: codelab,markdown
environments: Web
status: Publicado

# Actividad 05

## Introducción

La adquisición forense de una memoria USB es un proceso crítico en la informática forense, diseñado para recopilar y preservar evidencias digitales de manera integra y auténtica. Este proceso implica crear una copia exacta del contenido de la memoria USB, incluyendo datos eliminados y espacios de memoria libres, sin modificar el dispositivo original. La integridad de la evidencia es fundamental, por lo que es esencial evitar cualquier modificación accidental durante el proceso.

Para realizar esta tarea, se utilizan herramientas especializadas como FTK Imager, GuyImager y 'dd'. FTK Imager, desarrollado por AccessData, es una herramienta poderosa que permite seleccionar el dispositivo a imagenar y elegir el formato de la imagen, como E01. GuyImager, por otro lado, es una herramienta de código abierto que ofrece opciones para la compresión y fragmentación de la imagen. dd, una herramienta de línea de comandos en sistemas Unix-like, es muy versátil y se utiliza comúnmente para crear imágenes raw de dispositivos.

<br>

## FTK Imager

FTK Imager es una herramienta forense digital desarrollada por AccessData, utilizada para adquirir, examinar y analizar datos de dispositivos de almacenamiento digital. Permite crear imágenes forenses de dispositivos como discos duros, unidades USB y tarjetas de memoria, realizando una copia bit a bit del contenido para preservar la integridad de los datos originales. También facilita la verificación de la integridad de la imagen, la búsqueda de palabras clave y la extracción de archivos específicos. Es una herramienta esencial en la informática forense para obtener evidencia digital válida en investigaciones y procesos legales

![FTK-1](/img/1-ftk.png)
Resultados de la adquisición mediante el uso de FTK Imager 

<br>

![FTK-2](/img/2-ftk.png)
![FTK-3](/img/3-ftk.png)
Resumen de la información de la adquisición

<br>

## GuyImager

Guymager es una herramienta forense que crea imágenes de dispositivos de almacenamiento digital, como discos duros y unidades USB. Ofrece una interfaz gráfica intuitiva y soporta varios formatos de imagen, incluyendo EWF y AFF. Permite la generación de hashes para verificar la integridad de los datos y mantiene registros detallados del proceso de imagenación. Es ideal para investigaciones forenses debido a su eficiencia y flexibilidad.

![GuyImager-1](/img/inicio-adquisicion-guy.png)
Imagen del inicio del proceso de adquisición con la herramienta GuyImager

![GuyImager-1](/img/final-adquisicion-guy.png)
Resultado final de la adquisición con la herramienta GuyImager

Esta herramienta genera un fichero .info donde se encuentran los hash generados.

<br>

## DD
El comando 'dd' (Data Duplicator o Dataset Definition) es una herramienta de línea de comandos en sistemas Unix-like, utilizada para crear copias bit a bit de dispositivos de almacenamiento. Es ampliamente usada en la informática forense para adquirir imágenes de discos duros, unidades USB y otros dispositivos, preservando la integridad de los datos. Ofrece flexibilidad y control detallado sobre el proceso de copia, incluyendo la capacidad de calcular hashes para verificar la integridad de la imagen. Es una herramienta esencial para investigaciones forenses debido a su precisión y eficiencia.

![DD-1](/img/Comando.png)
Captura de los 3 comandos utilizados para obtener la imagen del USB, y luego los diferentes hash, que se muestran por línea de comandos
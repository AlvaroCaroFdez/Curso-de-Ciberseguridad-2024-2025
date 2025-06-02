# Dispositivo IoT Alexa

<br>

### Verificación de Hash 


![Imagen de verificación de hash](Verficación%20Alexa.png)

<br>

## Introducción

En el marco de una investigación forense digital, se ha llevado a cabo el análisis de un dispositivo del tipo IoT, específicamente un **Amazon Echo** con el asistente virtual **Alexa**. Este análisis está relacionado con un presunto incidente ocurrido el **17 de julio de 2017**, una fecha que ha sido verificada mediante archivos con metadatos `.json` y capturas del historial de interacciones del dispositivo.

<br>

## Contenido analizado

Se recibió un total de **14 archivos de audio en formato .wav**, acompañados de varios archivos `.json` y capturas de pantalla del historial de Alexa. Todo el contenido ha sido revisado y organizado cronológicamente para facilitar su interpretación. Los audios reflejan interacciones verbales dirigidas a Alexa por distintas voces, tanto masculinas como femeninas.

---

### Resumen de archivos de audio

Los archivos de audio analizados cubren un intervalo aproximado entre las **2:45 PM y las 3:20 PM** del día del suceso. A continuación, se detallan por categoría:

#### Audios repetidos y control de dispositivos

**1.wav y 2.wav – 3:20 PM**

Voz masculina: *"Alexa, call ambulance!"*
Ambos archivos contienen el mismo audio, lo que puede indicar insistencia o una situación urgente.

**3.wav y 4.wav – 3:20 PM**

Voz masculina: *"Alexa, turn off TV"*
Audios idénticos, posiblemente evidencia de reiteración en la orden o fallos de ejecución del dispositivo.

**5.wav y 6.wav – 3:12-3:13 PM**

Voz femenina: *"Alexa... stop"*
Se detecta una pausa significativa entre el nombre del asistente y el comando, lo cual podría interpretarse como nerviosismo, tensión o interrupción.

---

#### Fragmentos con carga rmocional

**7.wav – 3:12 PM (registro de historial, JSON vacío)**

Voz femenina: *"Alexa... stop"*
Voz masculina (posterior): *"I can't believe you're doing this to me. We said we would. What are you thinking?"*
Se trata de una interacción en la que el dispositivo graba más allá del simple comando, registrando parte de una discusión.

**8.wav – 3:12 PM**

Mismo esquema que el audio anterior.
Voz masculina: *"How can you do this? What are you thinking?"*
Ambos audios reflejan un posible conflicto personal con tono emocional elevado.

#### Otros fragmentos

**9.wav y 10.wav – 3:06 PM**
Voz femenina: *"Alexa, turn on Pandora"*
Pandora es un servicio de música en streaming, lo que indica un intento de reproducción de música. Audios duplicados.

**11.wav y 12.wav – 3:01 PM**
Voz masculina: *"Alexa, turn on TV"*
Se repite el mismo audio, lo que podría implicar una reiteración por parte del usuario o un fallo en el reconocimiento del dispositivo.

**13.wav – 2:45 PM**
Se identifican varias voces, lo que sugiere un ambiente social o introductorio en el uso del dispositivo, posiblemente con visitas presentes.

**14.wav – 2:57 PM**
Fragmento con voz masculina, pero el contenido es ininteligible. La calidad del audio no permite una transcripción precisa, posiblemente por lejanía del micrófono o interferencia.

<br>

## Archivos JSON y capturas de historial

Se analizaron también cuatro archivos `.json`, algunos sin datos útiles. Las capturas del historial de Alexa incluyen registros anteriores al incidente, destacando uno en particular: **16 de abril de 2017 a las 8:24 PM**, aunque su relevancia con los hechos actuales es nula.

Además, se detectaron al menos tres consultas relacionadas con el clima. En todos los casos, Alexa responde con el pronóstico de la ciudad de **Seattle**, aunque en diferentes unidades: una respuesta en **grados Celsius** y las otras dos en **Fahrenheit**, lo que puede deberse a cambios manuales en la configuración de preferencias de idioma o región.

<br>


### Línea temporal de los hechos – 17 de julio de 2017

A continuación, se presenta una reconstrucción gráfica de los eventos ocurridos entre las **14:45 y las 15:50 UTC**, basada en los audios extraídos del dispositivo Alexa, archivos JSON y otros elementos de evidencia:

![Línea del tiempo](Línea%20del%20tiempo.png)

Esta línea de tiempo detalla los momentos clave registrados por el dispositivo, incluyendo interacciones de voz, discusiones, solicitudes a Alexa y la posterior intervención de los servicios de emergencia. Ofrece una visión clara de la evolución de los hechos y del contexto en el que ocurrieron.

<br>

## Conclusiones

Del análisis de los archivos proporcionados se ha podido establecer una secuencia de interacciones registradas por el dispositivo Alexa el **17 de julio de 2017**. Estas muestran actividad continua en el entorno, incluyendo comandos relacionados con música, televisión y una solicitud de contacto con servicios de emergencia. No se han detectado elementos destacables en registros anteriores.
# ANEXO METODOLOGÍA


## Índice 

[**1. Adquisición y Preservación**](#1-adquisición-y-preservación)

[**2. Entorno de Análisis**](#2-entorno-de-análisis)

  - [Herramientas de análisis forense](#herramientas-de-análisis-forense)

[**3. Fases del Análisis**](#3-fases-del-análisis)

  - [Identificación de la Propiedad del Dispositivo](#identificación-de-la-propiedad-del-dispositivo)
  - [Análisis de Procesos en Ejecución](#análisis-de-procesos-en-ejecución)
  - [Análisis de la Master File Table (MFT)](#análisis-de-la-master-file-table-mft)
  - [Análisis de Handles](#análisis-de-handles)
  - [Búsqueda de Cadenas de Texto (Strings)](#búsqueda-de-cadenas-de-texto-strings)
  - [Análisis de la conversación en Discord](#análisis-de-la-conversación-en-discord)

[**4. Documentación**](#4-documentación)

[**5. Limitaciones**](#5-limitaciones)

[**6. Conclusión**](#6-conclusión) 


## Anexo metodología

Esta sección describe la metodología detallada empleada en el análisis forense del volcado de memoria del ordenador perteneciente a Francisco José Jiménez ("Pacopepe"). El objetivo principal fue identificar evidencia digital que pudiera vincular al sospechoso con la amenaza de bomba falsa.

<br>

## 1. Adquisición y Preservación

El volcado de memoria fue proporcionado al equipo de análisis. Inmediatamente después de la recepción, se procedió a:

**Cálculo de hashes**: Se calcularon los hashes (MD5, SHA-1, y SHA-256) del volcado de memoria utilizando PowerShell. Esto se realizó para garantizar la integridad de la evidencia digital y para poder verificar que la imagen analizada no había sido modificada durante el proceso. Los hashes calculados se documentan en el Anexo 1\.

<br>

## 2. Entorno de Análisis

El análisis forense se llevó a cabo en un entorno controlado y seguro, utilizando las siguientes herramientas:

**Sistema operativo**: Kali Linux (versión más reciente disponible en el momento del análisis).

### Herramientas de análisis forense:

* **Volatility framework**: Versión 2.6. Esta herramienta es fundamental para el análisis de volcados de memoria, permitiendo la extracción de información valiosa sobre los procesos en ejecución, conexiones de red, archivos abiertos, y otra información relevante.  
* **PowerShell**: Se utilizó para el cálculo de hashes y la verificación de la integridad de la imagen de memoria.

<br>

## 3. Fases del Análisis

El análisis se dividió en las siguientes fases:

### Identificación de la Propiedad del Dispositivo:

**Objetivo**: Confirmar que el volcado de memoria correspondía al ordenador de Francisco José Jiménez ("Pacopepe").

**Método**: Se utilizó el plugin sysinfo de Volatility para obtener información sobre el sistema operativo, nombre del equipo, y otra información de identificación. Específicamente, se buscó el nombre del equipo en la configuración del sistema.

**Plugin volatility utilizado**: *sysinfo*

**Justificación**: El plugin sysinfo proporciona una visión general rápida y precisa de la configuración del sistema, lo que permite confirmar la propiedad del dispositivo de manera eficiente.

---

### Análisis de Procesos en Ejecución:

**Objetivo**: Identificar procesos sospechosos o inusuales que pudieran estar relacionados con la amenaza de bomba.

**Método**: Se utilizó el plugin pslist de volatility para listar todos los procesos en ejecución en el momento en que se realizó el volcado de memoria. Se prestó especial atención a procesos relacionados con navegadores web, editores de texto, programas de mensajería, y cualquier otra aplicación que pudiera haber sido utilizada para planificar o ejecutar la amenaza.

**Plugin volatility utilizado**: *pslist*

**Justificación**: El plugin pslist proporciona una lista completa de los procesos en ejecución, lo que permite identificar rápidamente actividades sospechosas. La presencia de AcroCEF.exe (un componente de Adobe Acrobat/Reader) fue considerada relevante, ya que sugiere que el usuario estaba visualizando documentos PDF.

---

### Análisis de la Master File Table (MFT):

**Objetivo**: Identificar archivos relevantes que pudieran estar relacionados con la amenaza.

**Método**: Se utilizó el plugin mftparser de Volatility para analizar la Master File Table (MFT) del sistema de archivos NTFS. Esto permitió identificar archivos creados, modificados, o accedidos recientemente, incluyendo documentos, imágenes, y otros archivos que pudieran contener información relevante. Se buscó específicamente el archivo "Trabajo historia Pacopepe.pdf".

**Plugin volatility utilizado**: *mftparser*

**Justificación**: El análisis de la MFT proporciona una visión detallada de la actividad del sistema de archivos, permitiendo identificar archivos relevantes que podrían no ser evidentes a través de otros métodos.

---

### Análisis de Handles:

**Objetivo**: Determinar qué archivos estaban abiertos y en uso en el momento de la adquisición de la memoria.

**Método**: Se utilizó el plugin handles de Volatility para identificar los handles abiertos por los procesos en ejecución. Esto permitió determinar qué archivos estaban siendo accedidos por cada proceso, proporcionando información adicional sobre la actividad del usuario. Se buscó específicamente el archivo "*Trabajo historia Pacopepe.odt*".

**Plugin volatility utilizado**: *handles*

**Justificación**: El análisis de handles permite determinar qué archivos estaban en uso en el momento de la adquisición de la memoria, lo que proporciona contexto adicional sobre la actividad del usuario.

---

### Búsqueda de Cadenas de Texto (Strings):

**Objetivo**: Identificar conversaciones, contraseñas, o cualquier otra información relevante que pudiera estar presente en la memoria.

**Método**: Se utilizó Volatility para convertir el archivo de volcado de memoria a formato raw. Se utilizó la herramienta *strings* para extraer cadenas de texto legibles del volcado de memoria. Se realizó una búsqueda de palabras clave relacionadas con la amenaza de bomba, como "bomba", "amenaza", y el nombre del centro educativo.

**Plugins volatility utilizados**: Plugin para convertir el volcado de memoria a RAW

**Justificación**: La búsqueda de cadenas de texto puede revelar información valiosa que no es evidente a través de otros métodos. En este caso, permitió descubrir la conversación en Discord donde el sospechoso admitía ser el autor de la amenaza.

---

### Análisis de la conversación en discord:

**Objetivo**: Verificar la autenticidad y el contexto de la conversación en Discord encontrada.

**Método**: Se analizó la conversación encontrada para determinar la identidad de los participantes, la fecha y hora de la conversación, y el contenido exacto de los mensajes. Se buscó corroboración de esta información a través de otras fuentes, si fuera posible.

**Justificación**: La conversación en Discord proporcionó evidencia directa de la implicación del sospechoso en la amenaza de bomba, lo que la convirtió en una pieza clave del análisis.

<br>

## 4. Documentación

Cada fase del análisis fue cuidadosamente documentada, incluyendo:

* Fecha y hora de cada acción.  
* Herramientas y comandos utilizados.  
* Resultados obtenidos.  
* Capturas de pantalla de los hallazgos relevantes.

<br>

## 5\. Limitaciones

El análisis forense se vio limitado por los siguientes factores:

* **Disponibilidad de la imagen de memoria**: El análisis depende de la calidad y la integridad del volcado de memoria proporcionado. Cualquier corrupción o modificación de la imagen podría haber afectado los resultados.  
* **Técnicas Anti-forenses**: Es posible que el sospechoso haya utilizado técnicas anti-forenses para ocultar o eliminar evidencia, lo que podría haber dificultado el análisis.  
* **Limitaciones de las herramientas**: Las herramientas de análisis forense tienen limitaciones inherentes. Es posible que no hayan podido detectar toda la evidencia relevante presente en el volcado de memoria

<br>

## 6\. Conclusión

La metodología empleada en este análisis forense se adhirió a las mejores prácticas de la industria, asegurando la integridad y la precisión de los resultados. A pesar de las limitaciones mencionadas, el análisis proporcionó evidencia sólida que vincula al sospechoso con la amenaza de bomba falsa.  
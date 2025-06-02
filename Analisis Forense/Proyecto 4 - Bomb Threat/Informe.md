# Proyecto 4 - Bomb Threat

![Portada](./img/portada_p4.png)

<br>

# Índice
  - [**1. Introducción**](#1-introducción)

  - [**2. Resumen Ejecutivo**](#2-resumen-ejecutivo)

    - [2.1. Antecedentes](#21-antecedentes)

    - [2.2. Alcance](#22-alcance)

    - [2.3. Objetivos](#23-objetivos)

  - [**3. Análisis**](#3-análisis)

    - [3.1. Comprobación de hashes](#31-comprobación-de-hashes)

    - [3.2. Cadena de Custodia](#32-cadena-de-custodia)

    - [3.3. Metodología](#33-metodología)

    - [3.4. Hallazgos: Investigación del Incidente](#34-hallazgos-investigación-del-incidente)

  - [**4. Conclusiones**](#4-conclusiones)

  - [**5. Recomendaciones**](#5-recomendaciones)

  - [**6. Anexos**](#6-anexos)

<br>

# 1. Introducción

Este informe presenta el análisis forense llevado a cabo sobre el volcado de memoria de un ordenador perteneciente a Francisco José Jiménez ("*Pacopepe*"), un estudiante del centro educativo, quien fue señalado como sospechoso en relación con una amenaza de bomba falsa. A través de este análisis, se buscó obtener evidencia que permitiera esclarecer los hechos y confirmar si el sospechoso tenía alguna implicación en el incidente. Para ello, se utilizó la herramienta **Volatility**, una herramienta especializada en el análisis de volcado de memoria, que permitió descubrir una serie de hallazgos técnicos que se documentan en este informe.

# 2. Resumen ejecutivo

El análisis forense realizado sobre la memoria del ordenador de Pacopepe ha confirmado su implicación en la amenaza de bomba falsa. Mediante la herramienta **Volatility**, se verificó que el dispositivo pertenecía al sospechoso al comprobarse que el nombre del equipo "**DESKTOP-01S7HH9**" coincidía con el del alumno. Además, se detectó la presencia de *AcroCEF.exe*, lo que sugiere que Adobe Acrobat o Reader estaba en uso al visualizar documentos PDF.

El análisis de la Master File Table (**MFT**) reveló que el archivo "*Trabajo historia Pacopepe.pdf*" había sido generado a partir de un archivo **.odt**, y que dicho archivo estaba siendo editado en el momento de la intervención policial. Asimismo, la herramienta **handles** permitió identificar que el archivo "*Trabajo historia Pacopepe.odt*" estaba abierto y en proceso de edición.

Por último, mediante el análisis de **strings** en el volcado de memoria, se descubrió una conversación en *Discord* en la que el usuario "*pakopepe88*" admitía ser el autor de la amenaza de bomba. Esta evidencia digital vinculó directamente al sospechoso con el incidente.

## 2.1. Antecedentes

El centro escolar recibió una llamada anónima informando sobre la posible presencia de una bomba. Francisco José Jiménez ("*Pacopepe*"), estudiante conocido por sus habilidades técnicas, fue señalado como posible sospechoso. Aunque él negó cualquier implicación, un compañero sugirió su culpabilidad. Ante la falta de pruebas físicas, se decidió realizar un análisis forense digital de su ordenador para obtener evidencia que aclare los hechos y determinar si Pacopepe está involucrado o si, por el contrario, ha sido señalado sin fundamento.

## 2.2. Alcance

El análisis se centra en el volcado de memoria del ordenador personal de *Pacopepe*, con el objetivo de identificar cualquier evidencia digital que lo relacione con la falsa amenaza de bomba. Esto incluye la búsqueda detallada de **archivos**, registros de **actividad**, comunicaciones y cualquier otro dato relevante que pueda arrojar luz sobre su posible implicación en el incidente.

## 2.3. Objetivos 

Los objetivos del análisis forense son los siguientes:
- Verificar la **propiedad** del volcado de memoria en el ordenador personal del sospechoso.  
- Identificar **evidencias** directas o indirectas que puedan vincular al sospechoso con la realización de la falsa amenaza de bomba.

# 3. Análisis

## 3.1. Comprobación de hashes

De acuerdo con la memoria distribuida al equipo de análisis, se ha procedido a verificar los hashes del material adquirido, lo cual puede consultarse en el [Anexo 1](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-1).

| Archivo | SHA256 |
| :---- | :---- |
| DESKTOP-01S7HH9-20220408-171552.dmp | EDCDBCAC27263A45D6DFE27F6C8BAFF55952B2357A70031DE20DE057730CD359 |
| DESKTOP-01S7HH9-20220408-171552.json | CBCD0AC591B4FC425550EB1292AD8F1DDDC4B0146A6D0DF7B23F6D13FA84B049 |
| DESKTOP-01S7HH9-20220408-171552.dmp.zip	 | 2246B2ABB178B3A508B5C8207D50E7E6F86D5C1F09487B50DAAA6387BEF639F0 |

## 3.2. Cadena de custodia

La cadena de custodia está disponible en el siguiente enlace: [Anexo Cadena de Custodia](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexo%20Cadena%20de%20Custodia.md).

## 

## 3.3. Metodología

La metodología aplicada por el equipo de análisis corresponde a la indicada en el enlace de referencia, desarrollada para uso interno: [Anexo Metodología](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexo%20Metodolog%C3%ADa.md).

## 3.4. Hallazgos: investigación del incidente

En el análisis realizado, se documentaron los siguientes hallazgos técnicos que permiten esclarecer la implicación del usuario en el incidente:

Para confirmar la propiedad del dispositivo, se utilizó la herramienta **sysinfo** de SysInternals, la cual proporcionó un informe detallado sobre la configuración del sistema. A través de esta herramienta, se verificó que el nombre del equipo "**DESKTOP-01S7HH9**" coincidía con el del alumno investigado. La evidencia de este hallazgo se muestra en el [Anexo 2](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-2).

Al investigar los procesos del sistema, se identificó la presencia de **AcroCEF.exe**, un componente de *Adobe Acrobat*. Aunque no se trata de un lector PDF directo, su presencia sugiere que Adobe Acrobat o Reader estaba instalado y en ejecución en el sistema. Este hallazgo es importante para determinar qué aplicación estaba involucrada en la visualización de *documentos PDF*. Los detalles técnicos, incluyendo la captura de pantalla de este hallazgo, están documentados en el [Anexo 3](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-3).

A través del análisis de la Master File Table (**MFT**), se descubrió que el archivo PDF "*Trabajo historia Pacopepe.pdf*" había sido generado a partir de un archivo **.odt**. Se encontró también evidencia de la descarga y el uso de una herramienta de conversión. Además, mediante el uso del plugin **handles**, se determinó que el archivo "*Trabajo historia Pacopepe.odt*" estaba siendo editado en el momento de la intervención. El proceso asociado con este archivo fue **soffice.bin** de la suite Office. Las capturas correspondientes a estos hallazgos se encuentran en el [Anexo 4](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-4).

En cuanto a la amenaza de bomba, se realizó un análisis de la imagen de memoria utilizando **Volatility** para convertir el archivo de volcado de memoria a formato **raw**. Posteriormente, se generó un archivo de **strings** para buscar evidencia textual relevante. Al buscar la palabra "*bomba*" en el archivo de strings, se encontró una conversación en la plataforma Discord entre los usuarios "*pakopepe88*" y "*marcosheredia666*", donde el primero admitía ser el autor de la amenaza de bomba falsa. Esta conversación fue esencial para vincular al sospechoso con el incidente. Las capturas de pantalla de esta conversación se encuentran en el [Anexo 5](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-5).

# 4. Conclusiones

La investigación forense realizada en el volcado de memoria del ordenador de *Pacopepe* ha proporcionado una serie de hallazgos técnicos que confirman la implicación del sospechoso en la amenaza de bomba falsa. El uso de la herramienta **Volatility** permitió acceder a información clave, como la verificación de la propiedad del dispositivo y la identificación de los procesos relevantes que indican la interacción del sospechoso con archivos vinculados a la amenaza.

Se halló que el documento "*Trabajo historia Pacopepe.pdf*" había sido abierto en el navegador y generado a partir de un archivo **.odt**, que había sido editado en el momento de la intervención. Además, la conversación encontrada en *Discord*, donde el sospechoso admitía ser el autor de la amenaza, constituyó la pieza clave de evidencia que confirmó su implicación directa. El análisis forense realizado fue exhaustivo y permitió reconstruir los eventos clave relacionados con la amenaza, proporcionando una sólida base de evidencia que apoya la acusación contra el sospechoso.

# 5. Recomendaciones

Para prevenir incidentes similares, es esencial que la institución educativa refuerce la educación en ciberseguridad tanto para el personal como para los estudiantes. Programas educativos sobre el uso seguro de la tecnología y la identificación de amenazas deben ser implementados. Además, es crucial que la institución cuente con políticas claras sobre el uso de dispositivos personales y el acceso a internet, garantizando un entorno seguro para todos.

También se recomienda establecer procedimientos de monitoreo para detectar posibles actividades sospechosas, y fomentar la conciencia sobre las consecuencias legales de realizar amenazas, ya sea en línea o en persona, para evitar futuros incidentes.

# 6. Anexos

A continuación, se presentan los anexos con la documentación adicional relacionada con el análisis forense llevado a cabo. Estos contienen evidencias, capturas de pantalla y registros detallados de los procedimientos realizados durante la investigación.

## Anexo 1

[Anexo 1](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-1): Verificación de hashes y autenticidad de los archivos analizados.

## Anexo 2

[Anexo 2](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-2): Evidencia de la propiedad del dispositivo investigado.

## Anexo 3

[Anexo 3](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-3): Análisis de procesos en memoria y detección de AcroCEF.exe.

## Anexo 4

[Anexo 4](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-4)): Análisis de la Master File Table y archivos relevantes.

## Anexo 5

[Anexo 5](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexos.md#anexo-5): Conversaciones encontradas en Discord vinculadas con la amenaza de bomba.

## Anexo Cadena de Custodia

[Anexo Cadena de Custodia](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexo%20Cadena%20de%20Custodia.md): Documento detallado sobre la preservación y manejo de la evidencia digital durante todo el proceso de investigación.

## Anexo Metodología

[Anexo Metodología](https://github.com/IES-Rafael-Alberti/24-25--Grupo1--Ciberseguridad/blob/main/1.-%20An%C3%A1lisis%20Forense%20Inform%C3%A1tico/Unidad%204/Anexos/Anexo%20Metodolog%C3%ADa.md): Explicación detallada de los procedimientos y herramientas utilizadas en el análisis forense, asegurando la rigurosidad y reproducibilidad del estudio.

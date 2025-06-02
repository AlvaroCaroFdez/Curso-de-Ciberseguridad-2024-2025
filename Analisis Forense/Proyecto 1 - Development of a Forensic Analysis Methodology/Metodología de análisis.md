# Development of a Forensic Analysis Methodology
![Portada](/Assets/portada.png)

<br>

# ÍNDICE
- [Introducción](#introducción)
- [Investigación de normas y estándares forenses](#investigación-de-normas-y-estándares-forenses)
- [Comparativa de normas y estándares](#comparativa-de-normas-y-estándares)
  - [Análisis comparativo](#análisis-comparativo)
    - [Objetivo](#objetivo)
    - [Alcance](#alcance)
    - [Contenido](#contenido)
    - [Aplicación](#aplicación)
- [Desarrollo de metodología propia](#desarrollo-de-metodología-propia)
  - [Adquisición de evidencia digital (ISO/IEC 27037)](#adquisición-de-evidencia-digital-isoiec-27037)
  - [Preservación y almacenamiento de la evidencia  (RFC 3227)](#preservación-y-almacenamiento-de-la-evidencia-rfc-3227)
  - [Análisis de las evidencias (UNE 71506:2013)](#análisis-de-las-evidencias-une-715062013)
  - [Documentación de hallazgos (UNE 71506:2013)](#documentación-de-hallazgos-une-715062013)
  - [Presentación de resultados (UNE 71506:2013)](#presentación-de-resultados-une-715062013)
- [Resumen](#resumen)
- [Fuentes](#fuentes)

<br>

# Introducción
Hemos asumido el compromiso de desarrollar una metodología de análisis forense propia que refuerce la calidad y precisión de nuestros servicios de análisis de incidentes.

Nuestro  es crear un proceso robusto y metódico que abarque desde la adquisición hasta la presentación de evidencias digitales, garantizando que cada paso cumpla con los más altos estándares de integridad y credibilidad.

Para ello, investigaremos y adaptamos normas y estándares forenses reconocidos, asegurando que nuestra metodología se alinee con las mejores prácticas internacionales y ofrezca a nuestros clientes resultados fiables y consistentes.

<br>

# Investigación de normas y estándares forenses.

En el ámbito de la seguridad de la información y el análisis forense digital, existen diversas normas y estándares que proporcionan directrices fundamentales para la recopilación, manejo y análisis de evidencias digitales. Entre estas, destacan tres normas de particular relevancia:

## ISO/IEC 27037

La ISO/IEC 27037 es una norma internacional que proporciona directrices para la identificación, recolección, adquisición y preservación de evidencias digitales potenciales. Esta norma está diseñada para optimizar el valor probatorio de las evidencias digitales en investigaciones forenses.

**Objetivo.**

El propósito principal de esta norma es establecer un marco estandarizado para el manejo de evidencias digitales, asegurando su validez y admisibilidad en procesos judiciales. Busca facilitar el intercambio de evidencias digitales entre diferentes jurisdicciones y proporcionar orientación sobre mejores prácticas en el tratamiento de estas evidencias.


**Estructura**.

- Identificación de evidencias digitales potenciales
    
- Recolección de dispositivos físicos que pueden contener evidencias
    
- Adquisición de datos digitales
    
- Preservación de la integridad de las evidencias
    

Además, se definen dos **roles** especializados:

- Digital Evidence First Responders (DEFR)
    
- Digital Evidence Specialists (DES)
    

**Aplicabilidad.**

La ISO/IEC 27037 es aplicable a una amplia gama de dispositivos y escenarios, incluyendo medios de almacenamiento digitales, dispositivos móviles y personales, sistemas de navegación, cámaras digitales y de video, ordenadores conectados a redes, así como redes basadas en protocolos TCP/IP. Su enfoque integral permite su utilización en diversas situaciones donde se requiera la gestión adecuada de evidencias digitales.


**Importancia**.

Esta norma es fundamental porque asegura que la evidencia digital se recopila de manera válida para su uso legal. Proporciona un estándar internacional que mejora la credibilidad y admisibilidad de las evidencias en procesos judiciales. Además, facilita la colaboración entre diferentes jurisdicciones en casos que involucran evidencias digitales y establece buenas prácticas para profesionales en el campo de la informática forense.

En **resumen**, la ISO/IEC 27037 es una herramienta esencial para garantizar la integridad y validez de las evidencias digitales en investigaciones forenses, proporcionando un marco estandarizado que puede ser utilizado internacionalmente en contextos legales y de seguridad informática.


## ISO/IEC 27042

La ISO/IEC 27042 es una norma que proporciona un marco para las directrices y posterior interpretación de las evidencias electrónicas. Establece cómo un perito debe abordar el análisis y la interpretación de evidencias digitales en investigaciones forenses.

**Objetivo**. El objetivo principal de esta norma es proporcionar orientación sobre cómo realizar el análisis e interpretación de evidencias digitales potenciales en incidentes de seguridad. Busca identificar y evaluar aquellas evidencias que pueden ayudar a comprender el incidente, asegurando que el proceso sea válido, reproducible y repetible.


**Estructura**. La norma se estructura en torno a varios elementos clave:
- Selección y justificación de métodos de análisis
    
- Relación entre la evidencia y el método utilizado
    
- Competencia y proficiencia del equipo investigador
    
- Documentación y registro del proceso de análisis
    
- Marco común para el manejo de incidentes de seguridad


**Aplicabilidad**. 

La **ISO/IEC 27042** tiene varias áreas de aplicabilidad. Es relevante en investigaciones forenses digitales, en el análisis de incidentes de seguridad informática, y en los procesos judiciales que involucren evidencias digitales. Además, es útil en el desarrollo de nuevos métodos de análisis forense digital, ya que establece pautas claras para estos campos.


**Importancia**.

En cuanto a su **importancia**, esta norma juega un papel crucial por varios motivos. En primer lugar, establece un estándar común para el análisis e interpretación de las evidencias digitales, lo cual es fundamental para garantizar consistencia en su tratamiento. También contribuye a mejorar la credibilidad y la admisibilidad de las evidencias en procesos legales, lo que es clave en situaciones judiciales donde las pruebas digitales son parte del caso.

Por otro lado, la norma proporciona una base sólida para la implementación de nuevos métodos de análisis forense digital, facilitando la innovación en este ámbito. Además, asegura que las opiniones de los investigadores se mantengan claramente separadas de los hechos, lo cual es crucial para evitar sesgos en la interpretación de las evidencias. Finalmente, la norma subraya la importancia de que los analistas forenses mantengan una competencia adecuada y una formación continua, lo que garantiza la calidad y confiabilidad de su trabajo.

En **resumen**, la ISO/IEC 27042 es fundamental para garantizar la calidad, fiabilidad y validez de los análisis forenses digitales, proporcionando un marco estandarizado que puede ser utilizado tanto en contextos legales como en investigaciones de seguridad informática.


## RFC 3227

La RFC 3227 es una guía de alto nivel que establece directrices para la recolección y archivo de datos relacionados con intrusiones y evidencias digitales en incidentes de seguridad. Esta norma está diseñada principalmente para administradores de sistemas e investigadores de incidentes.

**Objetivo.** Proporcionar orientación sobre cómo recopilar y archivar evidencias relevantes ante un incidente de seguridad, de manera que puedan ser admisibles en procesos judiciales.

**Estructura.** La norma aborda:

*   Principios fundamentales durante la recolección de evidencia, incluyendo consideraciones de privacidad y legales.
    
*   El proceso de recolección, enfatizando la transparencia y proporcionando pasos detallados.
    
*   El proceso de archivo, incluyendo la cadena de custodia y las mejores prácticas para el almacenamiento de evidencias.
    

**Aplicabilidad.**

La **RFC 3227** es útil para administradores de sistemas e investigadores de incidentes de seguridad, ya que establece pautas para la correcta recopilación de evidencias. También ayuda a las organizaciones a desarrollar procedimientos específicos para la preparación ante posibles procesos judiciales relacionados con incidentes de seguridad.
    

**Importancia.**

Esta norma es fundamental por varias razones. Primero, facilita la trazabilidad del atacante al proporcionar métodos adecuados para la recopilación de evidencias, lo que permite un seguimiento más eficaz en las investigaciones. También aumenta la probabilidad de que estas evidencias sean admitidas en procesos judiciales, lo cual es crucial para que las organizaciones puedan defenderse o procesar adecuadamente a los responsables. Además, ayuda a mantener la integridad de las evidencias durante todo el proceso de investigación, asegurando que no sean alteradas o comprometidas. Finalmente, esta norma proporciona una base sólida para que las organizaciones desarrollen sus propios procedimientos específicos y detallados, adaptados a sus necesidades particulares, fortaleciendo así su capacidad de respuesta ante incidentes de seguridad.
    

En **resumen**, la RFC 3227 es crucial para asegurar que la recopilación y manejo de evidencias digitales se realice de manera sistemática, transparente y legalmente admisible, lo cual es esencial en la investigación de incidentes de seguridad y en posibles procesos legales subsecuentes.

## UNE 71506:2013

La norma UNE 71506:2013 establece la metodología para el análisis forense de evidencias electrónicas. Esta norma complementa a la serie UNE 71505 y se enfoca específicamente en el proceso de análisis forense dentro del ciclo de gestión de evidencias electrónicas. Algunos aspectos clave de la norma son:

**Objetivo.** Define el proceso de análisis forense de evidencias electrónicas, proporcionando una metodología estandarizada para su preservación, adquisición, documentación, análisis y presentación.


**Estructura.** La norma se divide en varias fases principales:

1.  **Preservación.** Enfocada en mantener la validez y confiabilidad de las evidencias originales. Incluye procedimientos para el almacenamiento seguro y manejo adecuado de las evidencias.
    
2.  **Adquisición.** Detalla el proceso de clonado a bajo nivel de los datos originales, considerando diferentes escenarios (sistemas encendidos o apagados).
    
3.  **Documentación.** Establece la necesidad de documentar todo el procedimiento desde el inicio del análisis hasta la entrega del informe pericial. Incluye la documentación de procesos, herramientas utilizadas y la cadena de custodia.
    
4.  **Análisis.** Describe las tareas y procesos para analizar las evidencias, incluyendo:
    
    *   Recuperación de ficheros borrados
        
    *   Estudio de particiones y sistemas de archivos
        
    *   Análisis del sistema operativo
        
    *   Estudio de la seguridad implementada
        
    *   Análisis detallado de los datos obtenidos
        
5.  **Presentación.** Guía la elaboración del informe pericial, enfatizando la necesidad de usar un lenguaje comprensible para un público no técnico.
    

**Aplicabilidad.** La norma es aplicable a cualquier organización, independientemente de su tamaño o actividad, así como a profesionales competentes en el ámbito del análisis forense digital.


**Importancia.** Contribuye a la estandarización y sistematización de la metodología de análisis forense, especialmente en países de habla hispana. Aumenta la probabilidad de que las evidencias electrónicas sean admitidas en procedimientos legales al seguir un proceso riguroso y estandarizado.

Esta norma es fundamental para garantizar la calidad, fiabilidad y admisibilidad legal de las evidencias electrónicas en investigaciones forenses digitales.

<br>

# Comparativa de normas y estándares

Para realizar una selección de las normas que usaremos en nuestra metodología, es conveniente comparar las normas anteriormente para ver cuales nos pueden ser más útiles. En esta comparativa es importante tener en cuenta el objetivo, el alcance el contenido y la aplicación de cada norma.

## Análisis Comparativo

### Objetivo

*   **ISO/IEC 27037 y RFC 3227**.Ambas normas se enfocan en la recolección y preservación de evidencia digital, asegurando su integridad y admisibilidad en investigaciones legales. ISO/IEC 27037 ofrece un marco amplio, mientras que RFC 3227 brinda recomendaciones prácticas para incidentes de seguridad.
    
*   **UNE 71506.** Se especializa en procedimientos técnicos para el análisis forense de sistemas de información, aplicando herramientas avanzadas para extraer información relevante.
    
*   **ISO/IEC 27042.** Complementa a la ISO/IEC 27037 al centrarse en el análisis e interpretación de la evidencia digital, proporcionando pautas sobre cómo evaluar datos, reconstruir eventos y presentar información de manera clara y objetiva.
    
### Alcance

*   **ISO/IEC 27037.** Se centra en la recolección y manejo de evidencia digital en diversos entornos. Cubre exhaustivamente desde la identificación hasta la preservación de evidencia en múltiples plataformas, asegurando la integridad y admisibilidad de la evidencia en procesos legales.
    
*   **RFC 3227.** Enfocada en respuestas a incidentes críticos, prioriza la captura de datos volátiles y minimiza la alteración de evidencia. Proporciona guías prácticas para la recolección rápida y efectiva de evidencia digital en situaciones de emergencia.
    
*   **UNE 71506.** Especializada en el análisis forense de sistemas de información complejos en entornos empresariales. Va más allá de la preservación, ofreciendo técnicas específicas para analizar, interpretar y documentar pruebas admisibles en tribunales o investigaciones corporativas.
    

*   **ISO/IEC 27042.** Se enfoca en el análisis y evaluación de evidencia digital ya recolectada. Proporciona directrices para interpretar evidencia, aplicar métodos de análisis según el tipo de incidente y generar informes para investigaciones o litigios.


### Contenido

*   **ISO/IEC 27037.** Ofrece directrices sobre identificación, recolección y preservación de evidencia digital, asegurando su admisibilidad legal. Incluye métodos para mantener la cadena de custodia, recomendaciones sobre herramientas forenses y gestión de equipos multidisciplinarios.
    
*   **RFC 3227.** Proporciona un enfoque práctico con listas de verificación para la recolección en emergencias. Prioriza tipos de evidencia y detalla cómo preservar datos en sistemas comprometidos, enfatizando la documentación para garantizar la validez.
    
*   **UNE 71506.** Presenta procedimientos técnicos exhaustivos para el análisis forense, incluyendo recuperación de datos borrados y análisis de tráfico de red. Se centra en la integridad de la evidencia y la preparación de información para auditorías o tribunales.
    

*   **ISO/IEC 27042.** Se centra en el análisis e interpretación de evidencia digital, ofreciendo un marco para evaluar la validez de los datos y reconstruir incidentes. Incluye pautas para generar informes claros y objetivos para audiencias técnicas y legales.

### Aplicación

*   **ISO/IEC 27037.** Se aplica en la fase de respuesta a incidentes, asegurando la preservación e integridad de la evidencia digital. Es versátil y se adapta a diferentes plataformas, siendo esencial para mantener la validez de la evidencia en investigaciones legales.
    
*   **RFC 3227.** Ideal para situaciones críticas que requieren respuestas rápidas. Proporciona listas de verificación y prioriza la recolección de datos volátiles, garantizando que la evidencia se preserve sin alteraciones.
    
*   **UNE 71506.** Utilizada en análisis forenses detallados en entornos empresariales. Se enfoca en técnicas avanzadas para investigar incidentes complejos y preparar reportes técnicos para auditorías o procedimientos legales.
    
*   **ISO/IEC 27042.** Se centra en el análisis e interpretación de evidencia digital. Ayuda a convertir resultados forenses en información procesable y es clave para comunicar hallazgos de manera clara a audiencias técnicas y legales.
    

**Justificación de la elección**

La elección de **ISO/IEC 27037**, **RFC 3227** y **UNE 71506** está justificada por su cobertura integral del proceso forense digital.

*   **ISO/IEC 27037** asegura una **recolección y preservación de la evidencia digital** adecuada, manteniendo su integridad y garantizando su validez en auditorías o tribunales.
    
*   **RFC 3227** es esencial para situaciones críticas, proporcionando **guías prácticas para la preservación inmediata** de datos volátiles durante incidentes de seguridad.
    
*   **UNE 71506** ofrece un enfoque avanzado para el **análisis forense técnico de sistemas de información**, permitiendo extraer información detallada y procesable.
    

Juntos, estos estándares aseguran una gestión completa de la evidencia, desde su recolección hasta su análisis técnico, mejorando la eficacia de las investigaciones forenses.

Desarrollo de metodología propia
================================

Presentamos una metodología de análisis forense digital, desarrollada a partir de un análisis exhaustivo de las normativas internacionales ISO/IEC, NIST, UNE y DSFI.

Adquisición de evidencia digital. (ISO/IEC 27037)
-------------------------------------------------

Primeramente, es vital detectar qué datos pueden ser evidencias digitales. Según la norma que utilizamos, tenemos que tratar de reconocer qué datos son más o menos volátiles, identificarlos correctamente y posteriormente proceder a su recolección y clasificación.

El orden de recolección a seguir según la volatilidad en un caso post-mortem debe ser:

*   **Registros y caché**: Datos temporales que se borran al apagar el sistema.
    
*   **Tabla de enrutamiento, caché ARP, procesos, kernel, memoria**: Información sobre rutas, IP/MAC, procesos, rendimiento y uso de memoria.
    
*   **Información temporal**: Hora y fecha que cambian y se pierden al reiniciar.
    
*   **Disco**: Datos persistentes, incluso con el sistema apagado.
    
*   **Logs del sistema**: Registros de eventos y errores, editables.
    
*   **Topología de red**: Estructura y dispositivos de la red.
    
*   **Documentos**: Archivos que se conservan hasta ser eliminados.
    

A medida que vamos identificando, es importante anotar estos hallazgos de forma que queden reflejados en un documento.

El documento debe incluir la ruta de la evidencia encontrada, el hash no alterado, el marketime y una breve descripción. El documento que usaremos tendrá la siguiente estructura:

```
Documentación de evidencia forense

Información general

   - Número de caso:
    
   - Investigador:
    
   - Fecha y hora de recolección:
    

Detalles de la evidencia

1.- Ruta de la evidencia

   - Ubicación física:
    
   - Ruta del sistema:
    

2.- Hash no alterado

   - Algoritmo utilizado:
    
   - Valor hash:
    

3.- Mtime (Tiempo de modificación)

   - Fecha:
    
   - Hora:
    

4.- Descripción breve de la evidencia

   - Breve descripción:
```    

Antes de comenzar con la adquisición de evidencias es importante tener las autorizaciones pertinentes para poder manipularlas. Esto es muy importante ya que en ocasiones se pueden manejar datos confidenciales o incluso que la disponibilidad de los servicios quede afectada.

Un proceso importante, sería realizar fotografías de todo el proceso y etiquetar el cableado o dispositivos, para asegurar que el proceso sea repetible y reproducible, para ello deberemos de rellenar un acta de adquisición el cual es un documento crucial que registra detalladamente el proceso de obtención de evidencia digital. 

Basándonos en la norma ISO/IEC 27037 el acta de adquisición debe de ser como el siguiente ejemplo:
```
ACTA DE ADQUISICIÓN FORENSE

Número de caso: [ ] Fecha: [ ] Hora de inicio: [ ] Lugar: [ ] 

Investigador responsable: [ ]

1.- Identificación del dispositivo

   - Tipo de dispositivo: [Ej. Ordenador portátil, disco duro externo]
    
   - Marca y modelo: [Detalles del dispositivo]
    
   - Número de serie: [Número de serie]
    
   - Estado físico: [Descripción del estado]
    

2.- Método de adquisición

   - Herramienta(s) utilizada(s): [Nombre y versión del software/hardware]
    
   - Tipo de adquisición: [Ej. Imagen forense completa, adquisición lógica]
    
   - Bloqueo de escritura utilizado: [Detalles del dispositivo de bloqueo]
    

3.- Detalles de la evidencia adquirida

   - Nombre del archivo de imagen: [Insertar nombre del archivo]
    
   - Tamaño del archivo: [Tamaño en bytes]
    
   - Hash de la evidencia:
    
       - Algoritmo: [Ej. SHA-256]
        
       - Valor: [Insertar valor hash]
        

4.- Observaciones

[Cualquier detalle relevante o incidencia durante el proceso]

Hora de finalización: [Hora de finalización]

Firmas:

[Nombre del perito]

[Nombre del testigo]
```

<br>

# Preservación y almacenamiento de la evidencia  (RFC 3227).


Una incorrecta preservación, uso o manipulación de las evidencias puede invalidar una investigación ante un tribunal, lo cual es un aspecto crucial en la metodología forense.

La cadena de custodia es el proceso controlado que se aplica a las evidencias desde su hallazgo en la escena hasta su análisis en el laboratorio, evitando manipulaciones indebidas y manteniendo un registro claro de quién las ha manejado, cómo y cuándo. A la hora de crear un documento de custodia es esencial asegurarse de que se cumplan una serie de requisitos y se garantice la integridad, autenticidad y la cadena de custodia mediante unos elementos claves. Dichos elementos son:

*   ¿Dónde?, ¿cuándo? y ¿quién? descubrió y recolectó la evidencia.
    
*   ¿Dónde?, ¿cuándo? y ¿quién? manejó la evidencia.
    
*   ¿Quién ha custodiado la evidencia?, ¿cuánto tiempo? y ¿cómo la ha almacenado?
    
*   En el caso de que la evidencia cambie de custodia indicar cuándo y cómo se realizó el intercambio, incluyendo número de albarán, etc.
    

Es esencial documentar detalladamente cada evidencia desde su identificación para asegurar su control y trazabilidad. 

Mientras los dispositivos estén en el laboratorio, deben estar embalados y etiquetados con información clave, como un identificador único, el responsable, descripción, propietario y lugar de confiscación, así como fecha y hora. Dependiendo del tipo de equipo, como discos duros o placas electrónicas, se deben tomar precauciones adicionales, como protección contra electricidad estática mediante bolsas antiestáticas. Se debe almacenar la información en dispositivos cuya seguridad haya sido demostrada y que permitan detectar intentos de acceso no autorizados.

<br>

# Análisis de las evidencias (UNE 71506:2013).

La fase de análisis concluye cuando se identifica quién o qué causó el incidente, cómo ocurrió y cuál fue el impacto en el sistema. Es el núcleo de la investigación, y debe generar la mayor cantidad de información posible para elaborar informes bien documentados.

En la investigación de datos, es esencial no usar los datos originales sin autorización y cumplir con las leyes y normativas vigentes. Los resultados deben ser verificables y reproducibles, permitiendo que otros investigadores puedan replicar el análisis. Esto asegura la integridad y credibilidad del estudio.

A continuación, se detallan las acciones y procedimientos específicos que se llevarán a cabo:

**Recuperación de ficheros borrados**: Se emplearán técnicas especializadas de recuperación de datos para intentar restaurar ficheros que han sido eliminados del sistema. Este proceso es clave para acceder a información que pudo haber sido intencionadamente borrada o perdida accidentalmente y que podría ser crucial para la investigación.

**Estudio de las particiones y sistemas de archivos:** Se analizará la estructura lógica del disco duro, con especial énfasis en las particiones (es decir, cómo se ha dividido el espacio de almacenamiento). Además, se examinarán los sistemas de archivos utilizados (por ejemplo, NTFS, FAT32, ext4) para comprender cómo se almacena, organiza y gestiona la información. Este análisis puede revelar alteraciones, accesos o modificaciones inusuales en las particiones o el sistema de archivos.

**Estudio del sistema operativo:** El análisis del sistema operativo permitirá evaluar cómo interactúa con el hardware y el software del sistema investigado. Se buscarán rastros de actividad sospechosa, como instalaciones de programas maliciosos, vulnerabilidades explotadas, procesos anómalos o archivos de registro alterados. El objetivo es identificar cómo el sistema operativo pudo haber sido comprometido o cómo facilitó la ocurrencia del evento investigado.

**Estudio de la seguridad implementada en el sistema:** Se evaluarán las medidas de seguridad instaladas y su efectividad, incluyendo el análisis de firewalls, software antivirus, sistemas de detección de intrusiones (IDS), políticas de acceso y autenticación, y otros mecanismos de protección. Este examen ayuda a determinar si la seguridad fue vulnerada y de qué manera.

**Análisis detallado de los datos obtenidos:** Una vez que se ha recuperado y organizado la información, se procederá a un análisis detallado de los datos. Se buscarán patrones, correlaciones, rastros de acceso, transferencias de datos y cualquier actividad que pueda explicar el evento. En este proceso se pueden emplear herramientas de análisis forense para visualizar, interpretar y contextualizar la información.

Cabe recordar que no existe ningún proceso estándar que ayude a la investigación y habrá que estudiar cada caso por separado teniendo en cuentas las diversas particularidades que nos podamos encontrar.

<br>

# Documentación de hallazgos (UNE 71506:2013).


En esta fase de nuestro análisis forense, nos enfocaremos en la redacción de informes que detallan los antecedentes del incidente, el trabajo realizado a lo largo del proceso, el método empleado y las conclusiones obtenidas, así como el impacto que ha generado todo el suceso.

Para realizar esta documentación es importante redactar dos informes: un informe técnico y un informe ejecutivo. A continuación, mostraremos de que manera se hacen estos informes:

**Informe ejecutivo:** El informe ejecutivo utilizará un lenguaje claro y accesible ya que hay que tener en cuenta que va destinado a personas no expertas en el tema (jueces y gerentes por norma general), por lo tanto hay que evitar el uso de tecnicismos.

**Estructura del informe ejecutivo**

1.- **Resumen del incidente**

*   ¿Qué ocurrió?: Descripción general del incidente
    
*   Impacto:  Breve mención de los sistemas o datos comprometidos y las posibles consecuencias.
    
*   Fechas clave: Cuando fue detectado el incidente y el tiempo estimado de duración del ataque.

<br>

2.- **Acciones tomadas**
    

*   Medidas inmediatas: Resumen de las acciones que se tomaron para contener el incidente.
    
*   Investigación: Descripción simplificada de cómo se llevó a cabo la investigación forense.
    
<br>

3.- **Resultados principales**
    

*   Causa del incidente: Explicación sencilla de cómo ocurrió el incidente.
    
*   Consecuencias: Impacto a nivel de negocio, como interrupción de operaciones, pérdida de datos o reputación.
    
*   Identificación del atacante: Sin fue posible, identificar si el ataque provino de una fuente interna o externa.
    
<br>

4.- **Conclusión:** 
*  Resumen breve de la situación actual, indicando si el incidente ha sido completamente resuelto o si se necesita un monitoreo adicional.
    
<br><br>

**Informe técnico:** El informe técnico es para los equipos de TI, seguridad y forenses. Debe contener todos los detalles del análisis, las herramientas utilizadas, las pruebas, los hallazgos y las recomendaciones técnicas. Es fundamental para documentar todo el proceso en detalle.

**Estructura del informe técnico**

1.- **Descripción  del incidente:**
    

*   Cronología detallada: Incluir la fecha y hora en que se detectó el incidente, cuándo se reportó, cuándo se empezaron a tomar acciones y cuánto tiempo duró cada etapa.
    
*   Identificación del tipo de ataque: Descripción técnica del tipo de amenaza.
    
<br>

2.- **Recolección de evidencias:**
    

*   Procedimiento de recolección: Describir cómo y qué tipo de evidencias se recolectaron.
    
*   Herramientas utilizadas: Mencionar las herramientas forenses empleadas.
    
*   Cadena de custodia: Describir cómo se mantuvo la integridad de las evidencias.
    
<br>

3.- **Análisis forense:**
    

*   Examinación de logs: Presentar los análisis de los logs de sistemas, servidores o firewalls. Indicar si hubo actividad inusual.
    
*   Análisis de malware: Descripción del análisis estático y dinámico del malware encontrado.
    
*   Actividad de red: Descripción de cualquier tráfico sospechoso, exfiltración de datos o conexión a IPs maliciosas.
    
*   Examen de discos o dispositivos: Resultados del análisis de dispositivos afectados, extracción de archivos maliciosos o modificaciones a sistemas.
    
<br>

4.- **Resultados detallados:**
    

*   Vector de ataque: Explicación técnica de cómo el atacante consiguió acceso o explotó vulnerabilidades
    
*   Sistemas comprometidos: Detallar los sistemas o archivos comprometidos.
    
*   Atacante identificado: Si se pudo determinar, incluir detalles técnicos sobre el origen del ataque.
    
<br>

5.- **Acciones correctivas y preventivas:**
    

*   Contención del ataque: Explicar cómo se detuvo el ataque y qué medidas se tomaron.
    
*   Mitigación: Descripción de las soluciones aplicadas para restaurar sistemas y eliminar la amenaza.
    
*   Parcheo y actualización: Mencionar cualquier parche o actualización implementada.
    
<br>

6.- **Conclusión técnica:**
    

*   Resumen del estado final del sistema después de la investigación y la mitigación.
    
*   Indicación de cualquier seguimiento adicional necesario.
    

La elaboración de ambos informes es esencial para una comunicación clara y efectiva. El informe ejecutivo facilita la comprensión del incidente para aquellos no especializados, mientras que el informe técnico ofrece un análisis detallado para los profesionales del área. Juntos, aseguran una documentación completa que apoya la toma de decisiones informadas y contribuye a la transparencia del proceso forense.

<br>

# Presentación de resultados (UNE 71506:2013).
En la fase final del proceso, toda la información obtenida a partir del análisis de las evidencias se reúne en un informe pericial. Este documento, firmado por el perito informático, se entrega a la entidad u organismo que solicitó la evaluación. Dado que el informe generalmente está dirigido a personas con conocimientos limitados en informática, es esencial que esté redactado de manera clara, sin perder la precisión técnica. 

Una vez completado, el informe se remite al solicitante, acompañado del registro de las evidencias manejadas, lo que marca la conclusión del proceso de custodia y garantiza un seguimiento completo de las pruebas.

Además de los resultados del análisis, es recomendable incluir recomendaciones prácticas basadas en los hallazgos, orientadas a mejorar la ciberseguridad y prevenir incidentes futuros. También es fundamental garantizar la integridad tanto de las evidencias como del propio informe mediante el uso de firmas digitales, hashes o mecanismos similares que aseguren que no ha habido alteraciones.

<br>

# Resumen
Después de realizar una investigación exhaustiva sobre normas y estándares y desarrollar nuestra propia metodología de análisis forense, identificamos la importancia de seguir procedimientos específicos y adoptar medidas adecuadas para garantizar la integridad, autenticidad y validez de las evidencias digitales en el ámbito legal. Al comparar diversas normativas, logramos identificar las mejores prácticas que deben implementarse en nuestra metodología.

Como resultado de esta comparación, hemos propuesto una metodología propia, basada en diferentes normas estudiadas, seleccionando los aspectos que consideramos más relevantes y esenciales. Confiamos en que esta metodología permitirá tener una visión integral de evidencias digitales y las pruebas encontradas en casos futuros.

En resumen, creemos que este desarrollo es lo suficientemente sólido para satisfacer las necesidades actuales.

<br>

Aquí tenemos un esquema resumen de toda la metodología:

![Esquema Resumen](/Assets/Esquema%20resumen.jpg)
[Ejemplo de otro equemas resumen](/Assets/Esquema%20resumen%202.png)

<br>

# Fuentes

[UNE 71605:2013](https://peritoinformaticocolegiado.es/blog/estandares-nacionales-e-internacionales-que-puede-seguir-un-perito-informatico-para-realizar-el-analisis-forense-de-una-evidencia-y-para-la-elaboracion-de-un-peritaje-informatico/) <br>
[ISO/IEC 27037](https://ciberseguridad.com/normativa/espana/iso-iec-27037-evidencia-digital/) <br> 
[ISO/IEC 27037](https://peritosinformaticos.es/iso-27037-2012-perito-informatico/) <br> 
[RFC 3227](https://www.incibe.es/incibe-cert/blog/rfc3227)

# Cloud Forensics  

![Portada](./img/portada.png)

Trabajo realizado por:  
*Ángel Alberto Martínez Sánchez*  
*Yeray Almoguera González*  
*Rafael Tocino Batista*  
*Álvaro Caro Fernández*  
*Gonzalo Pulido Sánchez*  

<br>

# Índice
- [Introducción](#introducción)

- [Resumen ejecutivo](#resumen-ejecutivo)

- [Desarrollo de la investigación](#desarrollo-de-la-investigación)

    - [Fundamentos y objetivos del análisis forense en la nube](#fundamentos-y-objetivos-del-análisis-forense-en-la-nube)

    - [Herramientas y tecnologías](#herramientas-y-tecnologías)

    - [Características de la computación en la nube](#características-de-la-computación-en-la-nube)

- [Análisis crítico y propuestas de mejora](#análisis-crítico-y-propuestas-de-mejora)

    - [Estrategias y metodologías](#estrategias-y-metodologías)

    - [Desafíos y limitaciones](#desafíos-y-limitaciones)

    - [Propuesta de mejora](#propuesta-de-mejora)

- [Análisis de normativas y su impacto](#análisis-de-normativas-y-su-impacto)

- [Referencias](#referencias)


<br>

# Introducción
Este informe técnico analiza el análisis forense en entornos de computación en la nube, una disciplina crítica para la investigación de incidentes de seguridad en infraestructuras distribuidas. Se examinan las metodologías forenses adaptadas a la nube, los desafíos técnicos y normativos inherentes, y se articulan mejores prácticas para la identificación, recolección y preservación de evidencias digitales. El objetivo principal es proporcionar una visión integral para fortalecer las capacidades investigativas, garantizar la validez probatoria de las evidencias y asegurar el cumplimiento normativo en el contexto de la nube.

<br>

# Resumen ejecutivo

El análisis forense en entornos de computación en la nube es una disciplina emergente que enfrenta retos únicos debido a la naturaleza distribuida, dinámica y volátil de estos sistemas. Este informe examina las metodologías forenses adaptadas a la nube, los principales desafíos técnicos y normativos, y propone mejores prácticas para la recolección y preservación de evidencias digitales.

**Metodologías Forenses en la Nube**  
La investigación forense en la nube requiere adaptar técnicas tradicionales para abordar limitaciones como la falta de control físico sobre la infraestructura y la dependencia de los proveedores de servicios en la nube (CSP). Es fundamental establecer acuerdos claros con los CSP que definan responsabilidades y procedimientos para la recolección de evidencias. Además, el uso de herramientas automatizadas para capturar registros y crear imágenes de servidores virtuales es crucial para preservar evidencias en entornos altamente volátiles.

**Desafíos Técnicos y Normativos**  
Los principales desafíos incluyen el acceso limitado a los datos, la volatilidad inherente de los entornos cloud y las complejidades en la cadena de custodia. La dispersión geográfica de los datos plantea problemas legales significativos, ya que las diferencias entre legislaciones nacionales pueden dificultar las investigaciones.

**Mejores Prácticas**  
Para mitigar estos desafíos, se recomienda colaborar estrechamente con los CSP, implementar auditorías y registros exhaustivos, y formar al personal en procedimientos forenses específicos para entornos cloud. Estas medidas fortalecen las capacidades investigativas, garantizan la integridad de las evidencias digitales y aseguran el cumplimiento normativo.

<br>

# Desarrollo de la investigación

## Fundamentos y objetivos del análisis forense en la nube

El **análisis forense en entornos cloud** se centra en la recopilación, preservación y análisis de evidencias digitales dentro de infraestructuras distribuidas. Según Patau (2023), los principales objetivos incluyen la **detección de incidentes de seguridad**, la **preservación de la cadena de custodia** y el **cumplimiento normativo.** Este enfoque permite auditar entornos virtualizados sin afectar su operatividad, gracias a la automatización de procesos de recolección de evidencias.

Uno de los beneficios clave del análisis forense en la nube es la capacidad de realizar auditorías sobre **entornos virtualizados** sin afectar su operatividad. Esto se logra mediante la automatización de procesos de recopilación de evidencias, lo que facilita la identificación y almacenamiento de registros en tiempo real. Sin embargo, para garantizar la fiabilidad de las pruebas obtenidas, es fundamental la implementación de **mecanismos de monitoreo continuo** y el uso de **herramientas forenses especializadas** que permitan la extracción de datos sin comprometer su integridad. Además, la colaboración con los proveedores de servicios en la nube es esencial para obtener acceso legítimo a los registros de actividad y garantizar una respuesta efectiva ante incidentes de seguridad.

## Herramientas y tecnologías

Según el manual técnico de Sánchez Martín (2021), las herramientas clave utilizadas para la investigación forense incluyen software especializado como FTK Imager y EnCase. Estas herramientas permiten la recuperación y análisis de datos sin comprometer su integridad, lo que las convierte en soluciones fundamentales para investigaciones en entornos cloud. 

Además, Campus Ciberseguridad (2023) menciona otras soluciones esenciales para el análisis forense en la nube, como Magnet AXIOM y X1 Social Discovery, que facilitan la extracción de datos de servicios cloud populares como Google Drive y Dropbox. Estas herramientas emplean técnicas avanzadas de recuperación de datos y validación mediante hashes criptográficos, asegurando la autenticidad de la evidencia digital. 

La automatización de la recopilación de registros mediante APIs forenses permite capturar información sin intervención manual, minimizando la posibilidad de alteraciones o pérdidas de datos durante el proceso de análisis. Herramientas como Velociraptor y GRR Rapid Response han ganado relevancia en el ámbito forense al permitir la recolección de evidencias a gran escala en entornos distribuidos. Dichas soluciones ofrecen capacidades avanzadas de filtrado y análisis de datos en tiempo real, lo que agiliza la identificación de incidentes de seguridad y la respuesta ante amenazas.

El uso de inteligencia artificial en herramientas forenses está revolucionando la disciplina. Según el informe de ISMS Forum (2023), los algoritmos de aprendizaje automático facilitan la detección de patrones en grandes volúmenes de datos, permitiendo identificar anomalías que podrían pasar desapercibidas con técnicas tradicionales. La combinación de estas tecnologías mejora significativamente la eficacia y precisión del análisis forense en la nube, optimizando la respuesta ante incidentes y la preservación de evidencias digitales. Estas herramientas permiten la recuperación de datos de dispositivos y entornos virtualizados sin comprometer su integridad. 

## Características de la computación en la nube

La computación en la nube se caracteriza por ofrecer recursos bajo demanda, accesibilidad ubicua, multiusuario, elasticidad, uso medido, redundancia y alta disponibilidad. Estos atributos permiten a las organizaciones escalar sus operaciones y optimizar costos, pero también introducen desafíos únicos en términos de seguridad y análisis forense. Según Enteracloud (s.f.), la escalabilidad dinámica y el acceso universal seguro son fundamentales para el funcionamiento eficiente de la nube, pero estas mismas características presentan retos para la ciberseguridad y el análisis forense digital, como la necesidad de asegurar la integridad y disponibilidad de los datos.

**Elasticidad y volatilidad:** La capacidad de la nube para escalar dinámicamente recursos según la demanda introduce un desafío en la preservación de evidencias. El informe de ISMS Forum Spain (2018) resalta que la elasticidad permite la reubicación automática de datos en múltiples servidores o su eliminación cuando ya no son necesarios, lo que dificulta la retención y análisis de la evidencia digital. Asimismo, el manual de Sánchez Martín (2021) indica que la volatilidad inherente de los entornos cloud requiere la implementación de técnicas avanzadas de recolección de evidencia en tiempo real para evitar la pérdida de información crítica.

**Ubicuidad y compartición:** La ubicuidad de la nube significa que los datos pueden almacenarse y procesarse en múltiples ubicaciones geográficas de manera simultánea. Según Gómez Flores (2024), esta característica, aunque beneficiosa para la disponibilidad de la información, representa un desafío para la trazabilidad forense, ya que dificulta la delimitación de jurisdicción y la atribución de actividades sospechosas a usuarios específicos. Además, ISMS Forum Spain (2018) destaca que la compartición de recursos en entornos multiusuario incrementa el riesgo de exposición de datos, lo que hace imprescindible la implementación de auditorías y monitoreo constante.

**Abstracción:** La capa de abstracción en la nube impide a los investigadores el acceso directo a la infraestructura física, lo que limita las herramientas disponibles para la recopilación de evidencias. Según Red Seguridad (2020), dependiendo del modelo de servicio utilizado (IaaS, PaaS o SaaS), el acceso a registros y datos forenses puede ser restringido o incluso inaccesible sin la cooperación del proveedor del servicio. ISMS Forum Spain (2018) recomienda la formalización de acuerdos con los proveedores para garantizar la disponibilidad de datos en caso de incidentes, así como el uso de bitácoras inmutables accesibles por API para documentar cualquier cambio relevante en los sistemas cloud.

<br>

# Análisis crítico y propuestas de mejora

El análisis forense en la nube es un campo en constante evolución que enfrenta desafíos significativos debido a la naturaleza distribuida de los entornos cloud y las restricciones legales asociadas. Esta revisión de literatura recopila y sintetiza los hallazgos clave de diversas fuentes académicas y técnicas para proporcionar una visión integral del estado actual de la disciplina.

## Estrategias y metodologías

El informe de ISMS Forum Spain (2018) propone estrategias clave para la auditoría y el análisis forense en la nube, destacando la **supervisión continua de incidentes** como un pilar fundamental para la detección temprana de amenazas y la respuesta inmediata a incidentes de seguridad. Asimismo, enfatiza la importancia de la **gestión de riesgos en entornos cloud**, abordando la necesidad de identificar vulnerabilidades potenciales y mitigarlas mediante controles proactivos. Otro aspecto crucial señalado en este informe es la **integración de auditorías dentro del modelo de seguridad de la organización**, asegurando la trazabilidad de eventos mediante bitácoras inmutables y el acceso controlado a los registros de actividad.

Por otro lado, la revisión sistemática de la informática forense de Dialnet (2019) profundiza en metodologías específicas para la recopilación de datos en entornos cloud, destacando la aplicación de técnicas de preservación de evidencia digital que garantizan su autenticidad e integridad. Esta revisión subraya la necesidad de emplear herramientas especializadas capaces de **extraer datos sin alterar su estado original**, como imágenes forenses de discos virtuales o capturas en memoria de máquinas virtuales en ejecución. Además, se resalta la importancia de la validación de la evidencia mediante técnicas de hash y firmas digitales, lo que refuerza la fiabilidad de la información obtenida en investigaciones forenses.

## Desafíos y limitaciones

Uno de los principales desafíos identificados es la dificultad para acceder a datos almacenados en infraestructura de terceros, lo que complica la adquisición de evidencias y el mantenimiento de la cadena de custodia. De acuerdo con Red Seguridad (2020), también se presentan barreras jurídicas relacionadas con la soberanía de datos y regulaciones internacionales, lo que puede generar conflictos en la obtención de información relevante para una investigación. 

Además, el acceso a registros críticos puede estar limitado por políticas de privacidad de los proveedores de servicios cloud, lo que dificulta la obtención de pruebas sin su cooperación. Tecnek (2023) enfatiza la necesidad de colaboración entre proveedores de servicios en la nube y las entidades de investigación forense para facilitar el acceso controlado a la información sin comprometer la seguridad ni la privacidad de los usuarios. Asimismo, la adopción de estándares de interoperabilidad y marcos normativos internacionales podría contribuir a reducir estas barreras, estableciendo directrices claras para la recolección y análisis de evidencias en entornos distribuidos.

## Propuesta de mejora

Para abordar las limitaciones identificadas, se propone una guía forense estandarizada basada en las mejores prácticas de ISMS Forum (2023). Esta guía incluiría:

- **Automatización del proceso de adquisición de evidencias** mediante herramientas especializadas que reduzcan la intervención manual y minimicen la alteración de datos.  
- **Uso de inteligencia artificial y machine learning** para la detección de patrones en incidentes de seguridad y el análisis rápido de grandes volúmenes de datos en la nube.  
- **Colaboración con proveedores de servicios cloud** para desarrollar protocolos de acceso a evidencias que garanticen el cumplimiento normativo sin comprometer la seguridad y privacidad de los datos.  
- **Implementación de registros blockchain** para preservar la cadena de custodia de la evidencia digital, asegurando su inmutabilidad y verificabilidad en procesos judiciales.

Esta propuesta permitiría una mejora significativa en la eficiencia, confiabilidad y legalidad del análisis forense en entornos cloud, facilitando la investigación de incidentes sin comprometer la privacidad y seguridad de los datos involucrados.

<br>


# Análisis de normativas y su impacto

El análisis forense en entornos de computación en la nube debe alinearse con diversas normativas que buscan proteger la seguridad y privacidad de los datos. Entre las más relevantes se encuentran el **Reglamento General de Protección de Datos** (RGPD), la **Directiva NIS2**.

El **RGPD** establece directrices estrictas para la recopilación, procesamiento y almacenamiento de datos personales dentro de la Unión Europea. En el contexto del análisis forense en la nube, es esencial garantizar que la recolección y análisis de evidencias digitales cumplan con los principios de minimización de datos y limitación de propósito. Por ejemplo, al investigar un incidente de seguridad, solo deben recopilarse los datos estrictamente necesarios, y su uso debe restringirse exclusivamente a fines de la investigación en curso. Por lo tanto, se debe evitar la recopilación excesiva de datos y garantizar la transparencia en el procesamiento de la información personal.

La **Directiva NIS2**, que actualiza y amplía la Directiva NIS original, tiene como objetivo reforzar la seguridad de las redes y sistemas de información en la Unión Europea. Esta directiva impone obligaciones más estrictas a las organizaciones consideradas esenciales o importantes, incluyendo la implementación de medidas de seguridad adecuadas y la notificación de incidentes significativos. En el ámbito forense, esto implica que las organizaciones deben estar preparadas para realizar análisis exhaustivos tras un incidente, asegurando que las evidencias se manejen de manera que cumplan con los estándares establecidos por la directiva. Así, la formación del personal en procedimientos forenses específicos para entornos cloud y la implementación de auditorías y registros exhaustivos se convierten en elementos clave para el cumplimiento normativo.

El **cumplimiento** de estas normativas tiene un impacto directo en las prácticas forenses en entornos cloud. Por ejemplo, la NIS2 exige que las organizaciones implementen medidas de seguridad técnicas y organizativas apropiadas, lo que incluye la capacidad de realizar análisis forenses efectivos tras un incidente. Además, la directiva destaca la responsabilidad de la alta dirección en la supervisión de las políticas de ciberseguridad, lo que implica que los equipos forenses deben colaborar estrechamente con la gerencia para garantizar el cumplimiento normativo. La colaboración y comunicación efectiva son clave para asegurar que las prácticas forenses se alineen con los objetivos de seguridad y cumplimiento de la organización.

En el contexto del **análisis forense en la nube**, es importante reconocer que existen desafíos clave en el cumplimiento normativo, como los conflictos de jurisdicción, las limitaciones técnicas, los costos asociados y la obtención del consentimiento adecuado. Para abordar estos desafíos de manera efectiva, es fundamental establecer acuerdos contractuales claros con los proveedores cloud, implementar medidas de seguridad robustas y proporcionar capacitación continua al personal en relación con las leyes y regulaciones aplicables. Al adoptar un enfoque proactivo y bien informado, las organizaciones pueden fortalecer sus capacidades de análisis forense en la nube y garantizar el cumplimiento normativo en todo momento.

<br>

# Referencias

Patau, M. (2023). *Todo lo que necesitas saber sobre el análisis forense en la nube*. Ackcent. [https://ackcent.com/es/todo-lo-que-necesitas-saber-sobre-el-analisis-forense-en-la-nube/](https://ackcent.com/es/todo-lo-que-necesitas-saber-sobre-el-analisis-forense-en-la-nube/)

ISMS Forum Spain. (2018). *Cloud Audit & Forensics*.  
[https://www.ismsforum.es/ficheros/descargas/cloudauditforensics2018v41544463021.pdf](https://www.ismsforum.es/ficheros/descargas/cloudauditforensics2018v41544463021.pdf)

Espinoza Mina, M. (2019). *Informática Forense: Una Revisión Sistemática*. Dialnet.  
[https://dialnet.unirioja.es/descarga/articulo/7047153.pdf](https://dialnet.unirioja.es/descarga/articulo/7047153.pdf)

Sánchez Martín, M. (2021). *Análisis Forense en la Nube \- Manual Técnico*. IES San Clemente.  
[https://manuais.pages.iessanclemente.net/apuntes/ciberseguridad/forense/\_index.files/15%20-%20An%C3%A1lisis%20Forense%20en%20la%20nube.pdf](https://manuais.pages.iessanclemente.net/apuntes/ciberseguridad/forense/_index.files/15%20-%20An%C3%A1lisis%20Forense%20en%20la%20nube.pdf)

Campus Ciberseguridad. (2025). *Informática Forense: Herramientas y Técnicas Clave*.  
[https://www.campusciberseguridad.com/blog/item/189-informatica-forense-herramientas-tecnicas-deber-dominar](https://www.campusciberseguridad.com/blog/item/189-informatica-forense-herramientas-tecnicas-deber-dominar)

Red Seguridad. (2020). *Introducción al Análisis Forense en Entornos Cloud*.  
[https://www.redseguridad.com/especialidades-tic/cloud-y-virtualizacion/introduccion-al-analisis-forense-en-entornos-cloud\_20201028.html](https://www.redseguridad.com/especialidades-tic/cloud-y-virtualizacion/introduccion-al-analisis-forense-en-entornos-cloud_20201028.html)

Tecnek. (2023). *Análisis Forense en la Nube*.  
[https://www.tecnek.com/noticias-ciberseguridad/197-analisis-forense-en-la-nube.html](https://www.tecnek.com/noticias-ciberseguridad/197-analisis-forense-en-la-nube.html)

Enteracloud. (s.f.). *Principales Características de la Computación en la Nube que debes conocer*.  
[https://enteracloud.mx/principales-caracteristicas-de-la-computacion-en-la-nube-que-debes-conocer/](https://enteracloud.mx/principales-caracteristicas-de-la-computacion-en-la-nube-que-debes-conocer/)

ISMS Forum. (2023). *Propuesta de Guía Forense para Entornos Cloud*.  
[https://wikincident.ismsforum.es/?p=145](https://wikincident.ismsforum.es/?p=145)

Gómez Flores, V. M. (2024). *Informe sobre el análisis forense en entornos cloud*. INFOTEC.  
[https://infotec.repositorioinstitucional.mx/jspui/bitstream/1027/642/1/INFOTEC\_MDTIC\_VMGF\_20022024.pdf](https://infotec.repositorioinstitucional.mx/jspui/bitstream/1027/642/1/INFOTEC_MDTIC_VMGF_20022024.pdf)
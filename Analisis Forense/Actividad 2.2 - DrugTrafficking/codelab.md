author: Álvaro Caro Fernández
summary: Actividad Drug Trafficking parte 1
id: docs
categories: codelab,markdown
environments: Web
status: Published

# A2.2-DrugTrafficking

## Entorno de trabajo

Para la realización de esta actividad se van a utilizar las siguientes herramientas:

- **Máquina propia:**

    En este caso usaré mi propia máquina, un portátil HP Laptop 15-dw0xxx, donde hay una máquina virtual instalada con un sistema operativo Windows 10, dónde se usarán las herramientas descritas a continuación para poder completar la actividad.

<br>

- **Autopsy:**

    Es una herramienta de análisis forense digital diseñada para examinar dispositivos de almacenamiento, como discos duros y memorias USB, o imágenes de discos. Su propósito principal es ayudar a recuperar archivos eliminados, analizar datos almacenados, y detectar rastros de actividad del usuario que puedan servir como evidencia en investigaciones. Ofrece funciones avanzadas, como análisis de sistemas de archivos, revisión de historiales de navegación, análisis de correos electrónicos, y recuperación de imágenes y videos. Gracias a esta herramienta podremos extraer los diferentes archivos que posteriormente examinaremos con Windows Registry Recovery

<br>

- **Windows Registry Recovery:**

    Esta herramienta se centra en el análisis y recuperación del Registro de Windows, que es una base de datos crítica donde el sistema operativo almacena configuraciones relacionadas con hardware, software, usuarios y redes. Esta herramienta permite extraer información clave, como programas instalados, configuraciones de red, dispositivos previamente conectados y rastros de actividad de los usuarios. Es especialmente útil en situaciones donde el Registro está dañado o se necesita realizar un análisis forense, ya que puede revelar pistas sobre cambios recientes en el sistema, actividad sospechosa o configuraciones que puedan ser relevantes para una investigación. Mediante esta aplicación será desde donde sacaremos toda la información de los diferentes archivos.

<br>
<br>


## Información del sistema
| Información del sistema |  |
| :---- | :---- |
| **Tamaño de la partición (Byte)** | 2623832064 |
| **Prueba** | ![Foto1](/img/informacion_sistema/Foto1.png) |
| **Sistema y versión del SO** | Microsoft Windows XP |
| **Nombres de usuarios registrados** | John |
| **Organización registrada** | home |
| **“Product ID” asociado al sistema** | 76487-341-1072684-22504 |
| **“Service Pack” instalado** | Service Pack 3 |
| **Fecha y hora de instalación del sistema operativo** | 18 de abril de 2013 a las 15:17:02 (UTC) |
| **Fecha y hora del último “shutdown”** | 19/06/2013 2:11:46 |
| **Pruebas** | ![Foto2](/img/informacion_sistema/Foto2.png) ![Foto3](/img/informacion_sistema/Foto3.png) |

## Información de usuarios

Estos son los usuarios definidos en el sistema:

![usuarios](/img/informacion_usuarios/Usuarios.png)

Quitando los usuarios ya definidos por defecto en el sistema, se encuentran los siguientes usuarios creados:

| John |  |
| :---- | :---- |
| **Fecha último “logon”** | 28/03/2013 - 3:10:49 |
| **Fecha último cambio de contraseña** | 18/04/2013 - 15:18:44 |
| **Prueba** | ![john](/img/informacion_usuarios/John.png) |

<br>

| Ian |  |
| :---- | :---- |
| **Fecha último “logon”** | 25/04/2013 - 2:06:52 |
| **Fecha último cambio de contraseña** | 18/04/2013 - 15:18:44 |
| **Prueba** | ![ian](/img/informacion_usuarios/Ian.png) |

<br>

| Jessy |  |
| :---- | :---- |
| **Fecha último “logon”** | 23/04/2013 - 2:18:56 |
| **Fecha último cambio de contraseña** | 18/04/2013 - 15:18:44 |
| **Prueba** | ![jessy](/img/informacion_usuarios/Jessy.png) |

<br>

Sí, existe una contradicción entre las fechas halladas en este apartado y el anterior.

El último inicio de sesión de John aparece como **28/03/2013 a las 03:10:49**, mientras que la fecha de instalación del sistema es **18 de abril de 2013 a las 15:17:02 (UTC)**. Esto implica que el usuario aparentemente inició sesión en un sistema que, según el registro, aún no había sido instalado. Esto se puede deber a diferentes motivos:

- **Restauración desde una copia de seguridad:**
El sistema pudo haber sido reinstalado o restaurado desde una imagen anterior, lo que preservaría los registros de inicio de sesión con fechas anteriores a la instalación.

- **Manipulación intencionada:**
No se puede descartar que alguien haya alterado las fechas para encubrir actividades o generar confusión.

<br>
<br>


## Extracción de archivos
### **Archivos eliminados:**
---
### **Almacen mataro 2.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | Almacen mataro 2.jpg                                                 |
| **Imagen**       | ![mataro2](/img/pruebas/archivos_eliminados/almacen_mataro_2.jpg)                                      |
| **Modified Time**| 2013-03-27 06:39:14 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 9935 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/Almacen mataro 2.jpg                     |
| **MD5 Hash**     | ba0268ffe1d3a340a595cfd9a8cd6b87                                     |
| **SHA-256 Hash** | 9dd2e70416e70e5099303f04e5d48ad72d27155cf3e8dd5bc50dcfb93ebc056d     |
| **Extension**    | jpg                                                                  |

<br>

### **Almacen mataro 3.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | Almacen mataro 3.jpg                                                 |
| **Imagen**       | ![mataro3](/img/pruebas/archivos_eliminados/almacen_mataro_3.jpg)                                      |
| **Modified Time**| 2013-03-27 06:39:26 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 14399 bytes                                                          |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/Almacen mataro 3.jpg                     |
| **MD5 Hash**     | 07e03d5971f5b5a6433a13565cac407d                                     |
| **SHA-256 Hash** | 9e75a74404967693442b99278fcce969ddc4f7046903e3fc449b537960e93394     |
| **Extension**    | jpg                                                                  |

<br>

### **Almacen mataro.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | Almacen mataro.jpg                                                   |
| **Imagen**       | ![mataro](/img/pruebas/archivos_eliminados/almacen_mataro.jpg)                                      |
| **Modified Time**| 2013-03-27 06:39:04 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 6998 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/Almacen mataro.jpg                       |
| **MD5 Hash**     | c7c5a5521ed005ddad94cb9a9b254d6b                                     |
| **SHA-256 Hash** | 5cec8378687c3255665e4123cb30b6e05b2117a8ee9e65fe9a4b986e0cc0fe84     |
| **Extension**    | jpg                                                                  |

<br>

### **Almacen terrassa 3.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | Almacen terrassa 3.jpg                                               |
| **Imagen**       | ![terrasa3](/img/pruebas/archivos_eliminados/almacen_terrassa_3.jpg)                                      |
| **Modified Time**| 2013-03-27 06:39:42 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 6943 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/Almacen terrassa 3.jpg                   |
| **MD5 Hash**     | 1e6f15394d075ba43308da22ba92059c                                     |
| **SHA-256 Hash** | 805967a139624368bb0c0dd494a0b4c751a649e022b7a32f957d6f592784a29a     |
| **Extension**    | jpg                                                                  |

<br>

### **Almacen terrassa 4.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | Almacen terrassa 4.jpg                                               |
| **Imagen**       | ![terrasa4](/img/pruebas/archivos_eliminados/almacen_terrassa_4.jpg)                                      |
| **Modified Time**| 2013-03-27 06:40:28 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 7349 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/Almacen terrassa 4.jpg                   |
| **MD5 Hash**     | c641391cfe11009563aaf6d5ff7caf1b                                     |
| **SHA-256 Hash** | c8ab21e06cdcf9524c68f6ab6e2df645a19ebe86fc253a85c052c0d5696910cb     |
| **Extension**    | jpg                                                                  |

<br>

### **Almacen terrassa.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | Almacen terrassa.jpg                                                 |
| **Imagen**       | ![terrasa](/img/pruebas/archivos_eliminados/almacen_terrassa.jpg)                                      |
| **Modified Time**| 2013-03-27 06:20:50 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 9637 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/Almacen terrassa.jpg                     |
| **MD5 Hash**     | e9bc32019fe6c4bffb1ec9bef18b85aa                                     |
| **SHA-256 Hash** | bd9a18a33b5cec923b6a19d7ddcfb27c580377211761eb602c209d5fb8dfa9bd     |
| **Extension**    | jpg                                                                  |

<br>

### **coca.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | coca.jpg                                                             |
| **Imagen**       | ![coca](/img/pruebas/archivos_eliminados/coca.jpg)                                      |
| **Modified Time**| 2013-03-27 06:19:58 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 5777 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/coca.jpg                                 |
| **MD5 Hash**     | 1ffb5afbe2990760fd1b504386593f95                                     |
| **SHA-256 Hash** | 061c9e9cef4e2f62ddf8ab1e25e7f665037890119f958d385868d752832148c0     |
| **Extension**    | jpg                                                                  |

<br>

### **fabricando coca 2.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | fabricando coca 2.jpg                                                |
| **Imagen**       | ![fabricando-coca2](/img/pruebas/archivos_eliminados/fabricando_coca_2.jpg)                                      |
| **Modified Time**| 2013-03-27 06:42:34 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 14373 bytes                                                          |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/fabricando coca 2.jpg                    |
| **MD5 Hash**     | 5131b40b7b745677b6a6b06e3580508c                                     |
| **SHA-256 Hash** | 12ac6ae66c460ba004e1389991f429495246d743080c2c00c05c326b4da8368c     |
| **Extension**    | jpg                                                                  |

<br>

### **fabricando coca 3.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | fabricando coca 3.jpg                                                |
| **Imagen**       | ![fabricando-coca3](/img/pruebas/archivos_eliminados/fabricando_coca_3.jpg)                                      |
| **Modified Time**| 2013-03-27 06:43:20 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 9994 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/fabricando coca 3.jpg                    |
| **MD5 Hash**     | 99631163aabedd753f9a5d00b6fe74ac                                     |
| **SHA-256 Hash** | 800242322a228a4db8567b0de03f33f259ebd46e6601b51a2b8e4907f7c87853     |
| **Extension**    | jpg                                                                  |

<br>

### **fabricando coca 4.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | fabricando coca 4.jpg                                                |
| **Imagen**       | ![fabricando-coca4](/img/pruebas/archivos_eliminados/fabricando_coca_4.jpg)                                      |
| **Modified Time**| 2013-03-27 06:43:30 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 12608 bytes                                                          |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/fabricando coca 4.jpg                    |
| **MD5 Hash**     | ffbedbaa75fff0a2f405489082667c65                                     |
| **SHA-256 Hash** | 7c6dffced23041315aa7fb9e3ac90e2f3934e1430d819eebb135ee9d634c3b63     |
| **Extension**    | jpg                                                                  |

<br>

### **fabricando coca.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | fabricando coca.jpg                                                  |
| **Imagen**       | ![fabricando-coca](/img/pruebas/archivos_eliminados/fabricando_coca.jpg)                                      |
| **Modified Time**| 2013-03-27 06:42:28 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 6413 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/fabricando coca.jpg                      |
| **MD5 Hash**     | 66a8a952396995a7800ac63e8e2234bd                                     |
| **SHA-256 Hash** | 7352059b3e7a29143d0c38dcb8610cbc79251049d41cc8a58662a8101dd2cdf3     |
| **Extension**    | jpg                                                                  

<br>

### **fiesta Jorge.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | fiesta Jorge.jpg                                                     |
| **Imagen**       | ![fiesta-jorge](/img/pruebas/archivos_eliminados/fiesta_jorge.jpg)                                      |
| **Modified Time**| 2013-03-27 06:20:20 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 8905 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/fiesta Jorge.jpg                         |
| **MD5 Hash**     | c6661d1558b767f31c1f65242af95118                                     |
| **SHA-256 Hash** | bd87c563633f99998dc3956239afcf2b3ea8d19dd8f65e6f483c1bc8ca27166e     |
| **Extension**    | jpg                                                                  |

<br>

### **kasius 2.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | kasius 2.jpg                                                         |
| **Imagen**       | ![kasius-2](/img/pruebas/archivos_eliminados/kasius_2.jpg)                                      |
| **Modified Time**| 2013-03-27 06:42:04 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 5716 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/kasius 2.jpg                             |
| **MD5 Hash**     | 28f5966b1a4a72cb3b434f688bf8dd0b                                     |
| **SHA-256 Hash** | 1ed78fad0270ba13b15f1222d973cab3f2de072f5d72902af7bc48bd1ac35db1     |
| **Extension**    | jpg                                                                  |

<br>

### **kasius.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | kasius.jpg                                                           |
| **Imagen**       | ![kasius](/img/pruebas/archivos_eliminados/kasius.jpg)                                      |
| **Modified Time**| 2013-03-27 06:41:58 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 9175 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/kasius.jpg                               |
| **MD5 Hash**     | d56befec0c93acbad7fe9d48f5415a2b                                     |
| **SHA-256 Hash** | 28bb98cf7e09a6d96f8bcb4ee5d683740a4a334790f946354df061f175ba20c0     |
| **Extension**    | jpg                                                                  |

<br>

### **Maria en negocio Jorge.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | Maria en negocio Jorge.jpg                                           |
| **Imagen**       | ![maria](/img/pruebas/archivos_eliminados/maria.jpg)                                      |
| **Modified Time**| 2013-03-27 06:38:30 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 5083 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/Maria en negocio Jorge.jpg               |
| **MD5 Hash**     | 18f5a99105c58f8a71a3405562d2eafa                                     |
| **SHA-256 Hash** | b2412594f86335be25a83db0ee9ecaf576f9182a322fe69581ece2ccd4d6911f     |
| **Extension**    | jpg                                                                  |

<br>

### **mercancia 2.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | mercancia 2.jpg                                                      |
| **Imagen**       | ![mercancia-2](/img/pruebas/archivos_eliminados/mercancia_2.jpg)                                      |
| **Modified Time**| 2013-03-27 06:21:06 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 8620 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/mercancia 2.jpg                          |
| **MD5 Hash**     | 5b5a015f4041bbed1bca11fc7be74fcc                                     |
| **SHA-256 Hash** | 25543a3af9f7a0e72fed485116c24a4a45f9705aba49470b1cd891bf8ec8ea0e     |
| **Extension**    | jpg                                                                  |

<br>

### **Mercancia terrassa.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | Mercancia terrassa.jpg                                               |
| **Imagen**       | ![mercancia-terrassa](/img/pruebas/archivos_eliminados/mercancia_terrassa.jpg)                                      |
| **Modified Time**| 2013-03-27 06:38:52 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 8968 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/Mercancia terrassa.jpg                   |
| **MD5 Hash**     | 957894f16f61655cec7110625c7e344b                                     |
| **SHA-256 Hash** | bbc8f083cb8bd891463aa62d477620fe884f653e6725ad833f13b312b9f43490     |
| **Extension**    | jpg                                                                  |

<br>

### **mercancia.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | mercancia.jpg                                                        |
| **Imagen**       | ![mercancia](/img/pruebas/archivos_eliminados/mercancia.jpg)                                      |
| **Modified Time**| 2013-03-27 06:20:08 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 6917 bytes                                                           |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/mercancia.jpg                            |
| **MD5 Hash**     | c1481b245fe4f3b5362cd5e19ffaffba                                     |
| **SHA-256 Hash** | 32700fcb07ed7a1c760911c5aa43a24a06afbb42c119fa54197330dc57978546     |
| **Extension**    | jpg                                                                  |

<br>

### **pastillas.jpg**

| Campo            | Valor                                                                 |
|------------------|-----------------------------------------------------------------------|
| **Nombre**       | pastillas.jpg                                                        |
| **Imagen**       | ![pastillas](/img/pruebas/archivos_eliminados/pastillas.jpg)                                      |
| **Modified Time**| 2013-03-27 06:19:22 CET                                              |
| **Change Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Access Time**  | 2013-06-19 04:11:24 CEST                                             |
| **Created Time** | 2013-06-19 04:11:24 CEST                                             |
| **Tamaño**       | 12942 bytes                                                          |
| **Location**     | /img_AFI_W.E01/$OrphanFiles/pastillas.jpg                            |
| **MD5 Hash**     | 6fe69a3ad25893e824b7c40e252f96a8                                     |
| **SHA-256 Hash** | 9d51fd7fabfa93a72fcc7b947cc88d12536834756597b7dcf8b155eaf6f5d7c0     |
| **Extension**    | jpg                                                                  |

<br>
<br>

## Ficheros encriptados y comprimidos
Se han encontrado una serie de archivos comprimidos uno de ellos en formato ".zip" y el otro fichero en formato ".xls". Estos ficheros están encriptados presuponiendo que incluyen información delicada. Los archivos tienen los siguientes nombres:
- pedofilia.zip
- Contactes.xls

![ficheros-encriptados](/img/pruebas/ficheros_encriptados/ficheros-encriptados.png)

<br>

Hemos podido obtener a quién pertenecía cada archivo, en este caso, el fichero **"pedofilia.zip"** pertenece al usuario **"Ian"**:

![pedofilia](/img/pruebas/ficheros_encriptados/pedofilia.png)

y el fichero **"Contactes.xls"** que pertenece a **"John"**:

![contactos](/img/pruebas/ficheros_encriptados/contactos.png)


<br>
<br>

## Navegación en Internet
Para encontrar esta información basta con navegar por **Autopsy**, yendo a "Web Search", "Web History", "Web Bookmarks"

### [Enlace a historial](https://github.com/AlvaroCaroFdez/A2.2-DrugTrafficking/blob/main/img/pruebas/navegacion_web/Historial.csv)

### [Enlace a búsquedas](https://github.com/AlvaroCaroFdez/A2.2-DrugTrafficking/blob/main/img/pruebas/navegacion_web/Busquedas.csv)

### [Enlace a marcadores](https://github.com/AlvaroCaroFdez/A2.2-DrugTrafficking/blob/main/img/pruebas/navegacion_web/Marcadores.csv)

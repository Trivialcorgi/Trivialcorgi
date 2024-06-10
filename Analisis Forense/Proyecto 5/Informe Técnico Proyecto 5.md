# Informe Técnico Proyecto 5

# 1. Resumen Ejecutivo

Se detectó una vulnerabilidad en una aplicación web tras encontrar el archivo ping.php en la raíz de la aplicación (/root/var/www), utilizado por un intruso para inyectar código en el servidor. Se investigaron los registros de conexión en /root/var/log/apache2/access.log para identificar al atacante, donde se halló su IP, sistema operativo y navegador web. Además, se descubrió una copia del archivo passwd del sistema, llamado passwd.txt, en /root/var/www/, indicando una filtración de información al no estar en la ubicación esperada (/root/etc).

# 2. Introducción

## 2.1 Antecedentes

Un técnico, Vicente, recibió la notificación de un posible incidente de seguridad: la infiltración de datos sensibles desde un servidor a través de una aplicación web aparentemente segura. La aplicación web en cuestión, diseñada para realizar escaneos de red remotos, ocultaba una vulnerabilidad crítica. 

## 2.2 Objetivos

Los objetivos de este informe técnico son:

- Encontrar indicios de la extracción de datos sensibles de la empresa
- Resolver el incidente
- Descubrir información del atacante y su intención

## 2.3 Alcance

Análisis completo de la imagen del disco del equipo afectado así como de un volcado de su memoria RAM en busca de el rastro dejado por el intruso.

# 3. Información analizada

| Adquisición | captura_ram.lime |
| --- | --- |
| Tamaño (Bytes) | 1.073.282.112 |
| HASH MD5 | 64381bfe96d147c5c75735b14666dff3 |
| HASH SHA1 | 2abdc4fdacd26e216d10902fef828aaa0e10768b |
| HASH SHA256 | 0f5d751208b08450e298b8d27f22451dd2ae158dfc1cb80b974f360e9a88ff05 |

| Adquisición | image_disco.dd |
| --- | --- |
| Tamaño (Bytes) | 8.589.934.592 |
| HASH MD5 | 6d51519be6b8a7a83a24d20f32de8f1d |
| HASH SHA1 | 9ff3a2604d4c3bc35e2ca245e0952cd4ea80e902 |
| HASH SHA256 | 9f2b2dace6cfebec1b6f956fc231e199c00f39e05d50286b8f284043537d65d9 |

# 4. Análisis

### 4.1 Comparación de hashes

Para validar la integridad de los archivos y determinar si han sido modificados durante el ataque, se compararán los hashes de los archivos relevantes. Esta comparación permitirá identificar cualquier alteración no autorizada en los archivos del sistema.

Hashes otorgados:

| Archivos | SHA-256 |
| --- | --- |
| perfil_memoria.zip | 18b30b973223b8ab233aa1581bccd35bef6c678b29e671b3fe3a7ee5ea24b076 |
| captura_ram.lime.zip | 632d3d95260753029d7c9ade15e0dcab69b8fe7eb08d7001d9f923b22ddf003f |
| captura_ram.live | 0f5d751208b08450e298b8d27f22451dd2ae158dfc1cb80b974f360e9a88ff05 |
| imagen_disco.dd.zip | b0189203fa682fd086ed3c52a3723ac46ab896a2fb8e4daf49ed6228bc7d3b76 |
| imagen_disco.dd | 9f2b2dace6cfebec1b6f956fc231e199c00f39e05d50286b8f284043537d65d9 |

Hashes comprobados:

- perfil_memoria.zip

SHA256:

![Untitled](Informe%20Te%CC%81cnico%20Proyecto%205%20844c0d6cd7434be4bf62f55424e2aec6/Untitled.png)

- captura_ram.lime.zip

SHA256:

![Untitled](Informe%20Te%CC%81cnico%20Proyecto%205%20844c0d6cd7434be4bf62f55424e2aec6/Untitled%201.png)

- captura_ram.live

SHA256:

![Untitled](Informe%20Te%CC%81cnico%20Proyecto%205%20844c0d6cd7434be4bf62f55424e2aec6/Untitled%202.png)

- imagen_disco.dd.zip

SHA256:

![Untitled](Informe%20Te%CC%81cnico%20Proyecto%205%20844c0d6cd7434be4bf62f55424e2aec6/Untitled%203.png)

- image_disco.dd

SHA256:

![Untitled](Informe%20Te%CC%81cnico%20Proyecto%205%20844c0d6cd7434be4bf62f55424e2aec6/Untitled%204.png)

Con esto, podemos ver que con los 5 Hashes, coinciden todos con los dados anteriormente.

### 4.2 Investigación

La información de la memoria RAM ha sido analizada utilizando la herramienta Volatility, lo que ha revelado la presencia de un servidor Apache en la máquina objetivo. Con este descubrimiento, se llevó a cabo una búsqueda de evidencias en las carpetas subyacentes (/var/www), lo que condujo al hallazgo de dos archivos.

(Véase Anexo de hallazgos. Hallazgo 1)

Sabiendo esto, buscamos los logs de conexión para determinar la identidad de este sujeto a nuestro servidor apache.

Dicha información se encuentran en la ruta /root/var/log/apache2/ y en el fichero access.log en el cual podemos encontrar tanto la IP, el sistema operativo y el navegador web que estaba utilizando el atacante.

(Véase Anexo de hallazgos. Hallazgo 2)

Mediante una búsqueda exhaustiva entre las líneas de código en la captura de la memoria RAM y la revisión detallada de los registros previos, se logró identificar al archivo sospechoso como el origen de una inyección de comandos en el sistema. Este archivo, nombrado "ping.php", es responsable de la creación de un archivo denominado "passwd.txt", cuya fecha de creación coincide con el último POST registrado en los logs de Apache.

(Véase Anexo de hallazgos. Hallazgo 3)

# 5. Conclusión

Tras analizar la memoria RAM con Volatility, se detectó la presencia de un servidor Apache en la máquina objetivo. Esta revelación impulsó una búsqueda en las carpetas subyacentes, donde se descubrieron dos archivos: "ping.php" y "phpinfo.php". Posteriormente, se procedió a examinar los registros de conexión en "/root/var/log/apache2/access.log", donde se encontró información crucial sobre el atacante, incluyendo su IP, sistema operativo y navegador web.

A través de una minuciosa inspección de las líneas de código y una revisión detallada de los registros previos, se identificó a "ping.php" como el responsable de una inyección de comandos en el sistema. Este archivo fue capaz de generar un archivo llamado "passwd.txt", cuya creación coincidió con el último POST registrado en los logs de Apache. Este hallazgo proporciona una comprensión más clara de cómo se llevó a cabo el ataque y cuál fue su impacto en el sistema comprometido.

### 5.1 Soluciones ante la vulnerabilidad explotada

Para solucionar la vulnerabilidad en el script PHP "ping.php" que permite la ejecución de comandos a través del parámetro 'count', se pueden implementar las siguientes medidas:

1. **Validación de Entradas:**
    - Implementar una validación rigurosa de los datos de entrada, especialmente del parámetro 'count', para asegurarse de que solo se acepten valores esperados y seguros. Esto implica verificar que el valor proporcionado sea un número entero positivo y dentro de un rango específico si es aplicable.
2. **Escape de Comandos:**
    - Utilizar funciones de escape de comandos específicas del lenguaje de programación (como **`escapeshellarg()`** en PHP) para evitar la ejecución de comandos maliciosos introducidos a través del parámetro 'count'.
3. **Limitar los Comandos Permitidos:**
    - Restringir la ejecución de comandos únicamente a aquellos necesarios para la funcionalidad legítima del script. Se deben eliminar o deshabilitar los comandos innecesarios y restringir el acceso a las funciones del sistema que no son requeridas.
4. **Implementar Listas Blancas (Whitelists):**
    - Si es posible, utilizar listas blancas para definir explícitamente los comandos permitidos y rechazar cualquier otro comando no autorizado. Esto reduce la superficie de ataque al limitar las opciones disponibles para los atacantes.

# 6. Herramientas usadas

FTK Imager:

| Nombre | FTK Imager |
| --- | --- |
| Versión: | 3.1.2 |
| Página web | https://www.mitec.cz/wrr.html |

Autopsy:

| Nombre | Autopsy |
| --- | --- |
| Versión: | 4.21.0 |
| Página web | https://www.autopsy.com/ |

Volatility:

| Nombre | Volatility |
| --- | --- |
| Versión: | 2.7 |
| Página web | https://volatilityfoundation.org/ |

# 7. Anexo

### 7.1 Metodología Utilizada

A continuación, se explica la metodología que ha seguido el perito para adquirir y analizar
las evidencias:

- Adquisición de evidencia digital
1. La captura de la adquisición debe ser lo más precisa posible.
2. Detallar las fechas y horas a la que se realizó la extracción.
3. Intentar no sobrescribir las pruebas instalando software, si no es estrictamente
necesario.
4. Recoger las evidencias en orden de volatilidad:
5. Transparencia: A la hora de realizar la adquisición tendremos que explicar
detalladamente el proceso que hemos seguido para que pueda ser totalmente
reproducible.
- Preservación y almacenamiento de evidencia
A la hora de almacenamiento, se documentará:
- Dónde, cuándo y quién descubrió y recolectó la evidencia.
-  Dónde, cuándo y quién manejó la evidencia.
-  Quién ha custodiado la evidencia, cuánto tiempo y cómo la ha almacenado
-  Si se ha cambiado de custodia indicar a quien, que fecha y hora y comprobar que los
hashes coinciden
-  Dónde almacenarlo. Dependiendo del dispositivo tendremos que almacenarlo de una
u otra forma, por ejemplo, si es un dispositivo portátil tendremos que custodiarlo en
una bolsa de Faraday para que no pueda ser comprometido por las redes móviles.
- Análisis de evidencias

Se llevarán a cabo una serie de procesos y tareas que intentarán dar respuesta a preguntas
relacionadas con una intrusión, como su origen, la lista de sistemas afectados, los métodos
usados, etc. Todos estos procesos y tareas deberán realizarse de forma metódica,
auditable, repetible y defendible.

## 8. Anexo de hallazgos

Hallazgo 1

| Ruta | /root/var/www/ping.php |
| --- | --- |
| Contenido |  |
| MAC | Modify: 2022-05-20 11:09:37.000000000 -0400 |
| Tamaño | 542 |
| HASH MD5 | d3f424335dac2d8af26ad3f0a99a1a7d  |
| HASH SHA1 | 525132ce24328226594b0f97d0ef2d3f8b7a422e |

![Untitled](Informe%20Te%CC%81cnico%20Proyecto%205%20844c0d6cd7434be4bf62f55424e2aec6/Untitled%205.png)

Hallazgo 2

| Ruta | /root/var/log/apache2/access.log |
| --- | --- |
| Contenido |  |
| MAC | Modify: 2022-05-20 11:21:03.000000000 -0400 |
| Tamaño | 3494 |
| HASH MD5 | a71e80bd1ad541352d5907628f1bb3ce |
| HASH SHA1 | 640b5541fb9d263389b923ad786701ab149f84f9 |

![Untitled](Informe%20Te%CC%81cnico%20Proyecto%205%20844c0d6cd7434be4bf62f55424e2aec6/Untitled%206.png)

Hallazgo 3

| Ruta | /root/var/www/passwd.txt |
| --- | --- |
| Contenido |  |
| MAC | Modify: 2022-05-20 11:13:49.000000000 -0400 |
| Tamaño | 1626 |
| HASH MD5 | 7cd7b33f99cc526d01473b553e1042d5 |
| HASH SHA1 | 2d8c72a744c486342f5ec770ac27e8dd7b2f2ee0 |

![Untitled](Informe%20Te%CC%81cnico%20Proyecto%205%20844c0d6cd7434be4bf62f55424e2aec6/Untitled%207.png)

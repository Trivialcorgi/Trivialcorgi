# Stapler

# OBJETIVO

El propósito de este informe de pentest es vulnerar la seguridad de la máquina Stapler, a su vez, tiene como objetivo comunicar y documentar los resultados, así como brindar recomendaciones sobre cómo abordar y resolver las vulnerabilidades identificadas. 

# RESUMEN EJECUTIVO

Este informe presenta los resultados de un pentesting realizado a la maquina Stapler, con el objetivo de evaluar y mejorar la seguridad de sus servicios. El pentest se llevó a cabo siguiendo una metodología sólida y utilizando herramientas y técnicas estándar de la industria para identificar y explotar vulnerabilidades en los sistemas.

# METODOLOGIA

## RECONOCIMIENTO

En esta etapa, se recopila información sobre los objetivos, como direcciones IP, nombres de dominio, sistemas operativos y tecnologías utilizadas. El objetivo del reconocimiento es obtener una visión general de la infraestructura y los sistemas de la empresa.

## ESCANEO

Una vez recopilada la información inicial, se realiza un escaneo exhaustivo para identificar puertos abiertos, servicios en ejecución, aplicaciones y versiones. Esta información es esencial para determinar posibles vectores de ataque y planificar la fase de explotación.

## ENUMERACIÓN

Después del escaneo, se recopila información adicional sobre los servicios y aplicaciones identificados
Esto puede incluir la enumeración de usuarios, contraseñas, recursos compartidos, configuraciones y datos adicionales relevantes para el pentest.

## EXPLOTACIÓN

En esta fase, se intenta comprometer los sistemas utilizando las vulnerabilidades identificadas en las etapas anteriores. Se utilizan técnicas y herramientas específicas para explotar cada vulnerabilidad y obtener acceso a los sistemas y recursos.

## ANALISIS Y DOCUMENTACIÓN

Por último, se analizan y documentan los hallazgos, incluyendo las vulnerabilidades identificadas y explotadas, las técnicas utilizadas, el impacto de las vulnerabilidades y las recomendaciones para solucionar los problemas de seguridad. Esta información se presenta en un informe detallado que se envía a la empresa.

# RECONOCIMIENTO, ESCANEO Y ENUMERACIÓN

He comenzado con un escaneo de puertos con nmap para enumerar los servicios que encontramos en la máquina, una vez terminado, importamos el escaneo a metasploit.

### Servicios:

![Untitled](Stapler%20298a55292de04ccd835f6aab7dcc59e8/Untitled.png)

Realizaremos a su vez un escaneo de vulnerabilidades con nessus.

Para comenzar tenemos una vulnerabilidad critica en el samba, corresponde al CVE-1999-0519.

Este CVE consta de que podemos acceder al samba utilizando un usuario sin uso de credenciales.

# EXPLOTACIÓN DE VULNERABILIDADES, POST-EXPLOTACIÓN Y HALLAZGOS

## MÁQUINA STAPLER

## CVE-1999-0519

### Descripción:

Este CVE permite acceder al samba utilizando un usuario sin necesidad de credenciales, lo que puede ser explotado por atacantes malintencionados para comprometer la seguridad de la empresa y acceder a información confidencial.

### **Puntuación base CVSS 2.0: 7.5**

 En este caso, Nessus nos proporcionó el usuario "kathy", lo que permitió el acceso sin necesidad de contraseñas ni acciones adicionales. También se encontró el usuario "tmp", que tenía permiso de escritura y se pudo explotar utilizando Metasploit para obtener acceso como "root".

Para explotarlo simplemente vamos al terminal y ingresamos lo siguiente:

![Untitled](Stapler%20298a55292de04ccd835f6aab7dcc59e8/Untitled%201.png)

Como podemos apreciar me he logeado sin usar contraseñas ni acción de ningún tipo.

Tambien se encontraba el usuario tmp, que este tiene permiso de escritura:

![Untitled](Stapler%20298a55292de04ccd835f6aab7dcc59e8/Untitled%202.png)

Utilizando metasploit podemos explotar esto, usando una reverse_shell y acceder como root:

![Untitled](Stapler%20298a55292de04ccd835f6aab7dcc59e8/Untitled%203.png)

### Solución:

Para solucionar esta vulnerabilidad, se recomienda configurar adecuadamente los permisos de acceso a los servicios y aplicaciones, incluyendo la autenticación segura y el control de acceso. También se debe mantener actualizados los sistemas y aplicaciones con los parches de seguridad más recientes para evitar vulnerabilidades conocidas.

### Conclusión

La explotación de la vulnerabilidad CVE-1999-0519 en la máquina Stapler destaca la importancia de asegurar adecuadamente el acceso a servicios y aplicaciones. Es crucial mantener actualizados los parches de seguridad para prevenir que los atacantes malintencionados exploten las vulnerabilidades conocidas. Además, la implementación de medidas de autenticación y control de acceso seguras puede reducir aún más el riesgo de acceso no autorizado a información confidencial.

# Anexo

[SMB share full access by Everyone group CVE-1999-0519 Vulnerability Report](https://exchange.xforce.ibmcloud.com/vulnerabilities/1)
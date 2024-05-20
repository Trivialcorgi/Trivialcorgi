# Proyecto 02: Offensive Audit Services.
## Índice
1. [Investigación de Tipos de Ataque](#id1)
2. [Tipos de Auditoría de seguridad informática](#id2)  
3. [Investigación de Metodología del Prentesting](#id3)
4. [Evaluación de Herramientas de Monitorización](#id4)
5. [Referencias](#id5)

# Investigación tipos de ataques<a name="id1"></a>

Los ataques informáticos son un intento organizado o intencionado que busca explotar alguna vulnerabilidad o debilidad en las redes informáticas, tanto software como hardware, con el objetivo de tener algún beneficio.

Cada vez las tecnologías de información y comunicación avanzan, llegando a estar más conectadas a Internet, generando más datos con cada acción que se realiza. Aparte de traer muchas ventajas, tiene muchos inconvenientes, debido a que ha traído muchas vulnerabilidades que son aprovechadas por los ciberdelincuentes para robar, secuestrar o destruir cualquier tipo de información que recojan.

Los ataques informáticos se mantendrán e incluso aumentaran con el tiempo, basado en el comportamiento que han tenido a lo largo de los años. Cada día son más numerosos y más sofisticados.

Debido a ello, las medidas de seguridad informáticas se han convertido en una prioridad, especialmente para empresas que dependen casi del 100% de Internet en sus operaciones.

## Ataque de fuerza bruta

Un ataque de fuerza bruta es un método de prueba y error utilizado para decodificar datos confidenciales. Las aplicaciones más comunes para los ataques de fuerza bruta son descifrar contraseñas y descifrar claves de encriptación (sigue leyendo para obtener más información sobre las claves de encriptación). Otros destinos comunes para los ataques de fuerza bruta son las claves API y los inicios de sesión de SSH. Los ataques de contraseña de fuerza bruta a menudo se llevan a cabo mediante scripts o bots que tienen como destino la página de inicio de sesión de un sitio web.

Lo que distingue los ataques de fuerza bruta de otros métodos de decodificación es que los ataques de fuerza bruta no emplean una estrategia intelectual; simplemente intentan usar diferentes combinaciones de caracteres hasta encontrar la combinación correcta.

### **¿Qué ganan los hackers con los ataques de fuerza bruta?**

He aquí cómo se benefician los ciberdelincuentes de los ataques de fuerza bruta:

- Sacar provecho de los anuncios o recopilar datos de actividad
- Robo de datos personales y objetos de valor
- Difusión de malware para causar perturbaciones
- Secuestro de tu sistema para actividades maliciosas
- Arruinar la reputación de un sitio web

### Tipos de ataque de fuerza bruta

Cada ataque de fuerza bruta puede utilizar diferentes métodos para descubrir tus datos sensibles. Podrías estar expuesto a cualquiera de los siguientes métodos populares de fuerza bruta:

- **Ataques simples de fuerza bruta:** Los hackers intentan adivinar lógicamente tus credenciales, sin ayuda de herramientas de software u otros medios. Estos pueden revelar contraseñas y PIN extremadamente sencillos. Por ejemplo, una contraseña establecida como *“guest12345”*.
- **Ataques de diccionario:** En un ataque estándar, un hacker elige un objetivo y comprueba las posibles contraseñas con ese nombre de usuario. A este tipo de ataques se les denomina ataques de diccionario. Los ataques de diccionario son la herramienta más básica en los ataques de fuerza bruta.
- **Ataques híbridos de fuerza bruta:** Estos ataques se utilizan para averiguar contraseñas combinadas que mezclan palabras comunes con caracteres aleatorios. Un ejemplo de ataque de fuerza bruta de esta naturaleza incluiría contraseñas como *NewYork1993* o *Spike1234*.
- **Ataques de fuerza bruta inversos** Tal y como su nombre indica, un ataque de fuerza bruta inverso invierte la estrategia de ataque comenzando con una contraseña conocida. A continuación, los hackers buscan en millones de nombres de usuario hasta encontrar una coincidencia.
- **Relleno de credenciales** Si un hacker tiene una combinación de nombre de usuario y contraseña que funciona en un sitio web, la probará también en muchos otros.

## Inyección SQL

La inyección de SQL es un tipo de ciberataque encubierto en el cual un hacker inserta código propio en un sitio web con el fin de quebrantar las medidas de seguridad y acceder a datos protegidos. Una vez dentro, puede controlar la base de datos del sitio web y secuestrar la información de los usuarios.

### **Efectos de las SQLI en las personas**

Los ataques de inyección de SQL pueden tener consecuencias graves para las personas, a saber:

- **Pérdida de dinero**: un hacker puede usar una SQLI en la página de una entidad bancaria u otra institución financiera a fin de transferir dinero desde la cuenta de un usuario.
- **Robo de identidad**: cuando un hacker controla una base de datos, puede hacerse con la información que contiene y venderla en la red oscura. Otros ciberdelincuentes pueden comprar estos datos y utilizarlos para robar identidades.

### Efectos de las SQLI en las empresas

A continuación, detallamos algunos de los daños que pueden sufrir las empresas en un ataque de SQLI:

- **Sabotaje:** un hacker puede sembrar el caos fácilmente en una empresa borrando su base de datos o destrozando el sitio web.
- **Robo de datos**: muchos ataques de SQLI tienen por objeto robar datos confidenciales tales como secretos comerciales, información privilegiada, propiedad intelectual protegida y, a menudo, información de los usuarios o clientes.
- **Filtraciones de seguridad:** un hacker podría usar el contenido de una base de datos quebrantada para acceder a otras partes de la red interna de una empresa. Al final, toda la red puede estar en riesgo.
- **Pérdida de reputación:** tras sufrir los efectos de un ataque de SQLI, puede resultar difícil que una empresa recupere la confianza de sus clientes y del público en general.

### Tipos de Ataques SQLI

Cada ataque de SQLI es distinto dependiendo de el lugar donde se produce la inyección:

- **Inyección de SQL mediante la introducción de datos del usuario: Ocurre cuando un atacante inserta código SQL malicioso en campos de entrada de formularios web, como los de login o búsqueda, sin la debida validación.**
- **Inyección de SQL mediante la modificación de cookies:** Un atacante manipula los valores de las cookies, que son utilizados en consultas SQL sin ser validados, para insertar código SQL malicioso.
- **Inyección de SQL mediante variables de servidor:** Las variables de servidor, como las cabeceras HTTP, pueden ser manipuladas para incluir código SQL malicioso si se usan en consultas SQL sin ser saneadas.
- **Inyección de SQL mediante herramientas de hackeo automáticas:** Herramientas como SQLmap buscan y explotan automáticamente vulnerabilidades de inyección SQL, acelerando el proceso de ataque.
- **Ataques SQL de segundo orden: El código malicioso se almacena en la base de datos y se ejecuta más tarde, cuando es utilizado en otra consulta SQL sin ser validado adecuadamente**

## Ataques de phishing

Un ataque de phishing es una técnica de ciberataque que se utiliza para engañar a las personas con el fin de obtener información confidencial, como nombres de usuario, contraseñas, números de tarjetas de crédito u otra información sensible. Los atacantes se hacen pasar por entidades o personas confiables para lograr que las víctimas revelen esta información.

### **Características:**

Las características que predominan en este tipo de ataque son:

1. **Suplantación de Identidad:**
Los atacantes se hacen pasar por entidades de confianza, como bancos, empresas conocidas o contactos personales.
2. **Engaños Visuales:**
Utilizan gráficos, logos y diseños que imitan los de las entidades legítimas para hacer que los mensajes parezcan auténticos.
3. **Urgencia o Miedo:**
Los mensajes suelen incluir elementos de urgencia o amenazas (por ejemplo, "su cuenta será suspendida") para provocar una reacción rápida y poco meditada.
4. **Solicitudes de Información Sensible:**
Buscan obtener información confidencial, como credenciales de acceso, números de tarjetas de crédito o datos personales.

### **Objetivos:**

Los objetivos de los ciberdelincuentes que utilizan estos ataques son:

1. **Robo de Identidad:**
Obtener información personal para suplantar a la víctima y realizar fraudes.
2. **Acceso a Cuentas Financieras:**
Robar credenciales de cuentas bancarias o de servicios de pago para transferir dinero.
3. **Propagación de Malware:**
Inducir a las víctimas a descargar archivos o software malicioso que comprometen sus sistemas.
4. **Obtención de Información Confidencial:**
Recoger datos sensibles para venderlos en el mercado negro o utilizarlos en ataques posteriores.
5. **Secuestro de Cuentas:**
Acceder a cuentas de correo electrónico o redes sociales para usarlas en nuevos ataques de phishing o para obtener información valiosa.

### **Métodos:**

Estos son los métodos utilizados por los delincuentes:

1. **Correos Electrónicos Falsos:**
Envío masivo de correos que parecen provenir de fuentes legítimas, pidiendo a las víctimas que ingresen información personal en sitios falsificados.
2. **Mensajes de Texto (Smishing):**
Uso de mensajes SMS para engañar a las víctimas con enlaces maliciosos o solicitudes de información.
3. **Llamadas Telefónicas (Vishing):**
Los atacantes llaman por teléfono haciéndose pasar por representantes de empresas o instituciones, solicitando información sensible.
4. **Páginas Web Falsificadas:**
Creación de sitios web que imitan los originales, donde las víctimas ingresan información personal pensando que están en un sitio seguro.
5. **Ingeniería Social:**
Tácticas de persuasión y manipulación para ganarse la confianza de la víctima y obtener información confidencial.
6. **Phishing a través de Redes Sociales:**
Mensajes engañosos enviados a través de plataformas como Facebook, Twitter o LinkedIn, pidiendo a los usuarios que compartan información personal o hagan clic en enlaces maliciosos.
7. **Pharming:**
Redirigir el tráfico de un sitio web legítimo a un sitio falso sin que la víctima se dé cuenta, generalmente mediante la manipulación de la resolución DNS.

## Ataques de ramsonware

Los ataques de ransomware son una forma de ciberataque en la que los atacantes cifran los datos de la víctima y exigen un rescate para su liberación. La prevención y respuesta efectiva incluyen una combinación de buenas prácticas de seguridad, educación de los usuarios y preparación para incidentes.

### **Características:**

Las características de este tipo de ataque son:

1. **Encriptación de Datos:**
El ransomware cifra los archivos de la víctima, haciéndolos inaccesibles hasta que se pague un rescate.
2. **Demandas de Rescate:**
Los atacantes exigen un pago, generalmente en criptomonedas como Bitcoin, a cambio de la clave de desencriptación.
3. **Notificaciones de Rescate:**
La víctima recibe una notificación con instrucciones sobre cómo pagar el rescate y recuperar los archivos.
4. **Amenazas de Exposición:**
Algunos ransomware también amenazan con publicar datos sensibles si no se paga el rescate.

### **Objetivos:**

Los objetivos de este tipo de ataque son:

1. **Ganancias Económicas:**
Obtener dinero de las víctimas a través del pago del rescate.
2. **Interrupción de Operaciones:**
Causar interrupciones en las operaciones de una organización, lo que puede presionar a la víctima a pagar rápidamente.
3. **Robo de Datos:**
En algunos casos, los atacantes roban datos antes de cifrarlos, con la intención de vender la información o usarla para otros fines maliciosos.
4. **Propagación del Malware:**
Extender el ransomware a otros sistemas y redes para maximizar el impacto y los pagos de rescate.

### **Métodos de Distribución del Ransomware:**

Los vectores de ataque que utiliza el ransomware para propagarse serian:

1. **Correos Electrónicos de Phishing:**
Correos electrónicos con archivos adjuntos maliciosos o enlaces que descargan el ransomware al ser abiertos.
2. **Descargas Maliciosas:**
Sitios web comprometidos o anuncios maliciosos que descargan e instalan ransomware en el dispositivo de la víctima.
3. **Explotación de Vulnerabilidades:**
Uso de exploits para aprovechar vulnerabilidades en software desactualizado o sin parches.
4. **Ingeniería Social:**
Técnicas que engañan a los usuarios para que descarguen e instalen el ransomware.
5. **Redes de Botnets:**
Uso de redes de computadoras infectadas (botnets) para distribuir ransomware de manera masiva.

## **Tipos de auditorías de seguridad informática**<a name="id2"></a>

No todas las empresas necesitan realizar una auditoría completa de todos sus servicios y activos. En cambio, vamos a optar por auditorías específicas que son comunes y aplicables a la mayoría de las organizaciones:

### **1. Auditoría de cumplimiento normativo**

Esta auditoría verifica si una organización cumple con los requisitos legales y normativos en materia de seguridad de la información. Esto puede incluir el cumplimiento de leyes de protección de datos, regulaciones específicas de la industria y estándares internacionales.

El objetivo es asegurar que la empresa no infrinja ninguna normativa relevante, evitando problemas legales y detectando vulnerabilidades.

### **2. Auditoría de políticas y procedimientos**

Se centra en evaluar las políticas, normas y procedimientos de seguridad de la organización. El objetivo es determinar si son adecuados, están actualizados y se cumplen en la práctica.

Esta auditoría permite verificar si las políticas y procedimientos son efectivos y si necesitan ser actualizados para alinearse con las nuevas tecnologías.

### **3. Auditoría de controles de acceso**

Evalúa los sistemas y métodos utilizados para controlar el acceso a los sistemas y datos de la organización. Esto incluye la revisión de la gestión de contraseñas, niveles de privilegios de los usuarios, autenticación multifactor, entre otros.

El resultado de esta auditoría ayuda a identificar debilidades en los controles de acceso y a mejorar las medidas de autenticación y permisos para prevenir accesos no autorizados.

### **4. Auditoría de seguridad de redes**

Examina la infraestructura de red de la organización para identificar vulnerabilidades y riesgos de seguridad. Esto incluye pruebas de penetración, análisis de configuración de firewall, detección de intrusiones y evaluación de la protección de la red contra ataques.

Esta auditoría permite probar y mejorar las medidas de seguridad de la red, asegurando que las redes no sean vulneradas fácilmente y mitigando posibles ataques futuros.

### **5. Auditoría de seguridad de aplicaciones**

Evalúa la seguridad de las aplicaciones y sistemas utilizados por la organización. Esto implica revisar el código fuente, la configuración de seguridad de las aplicaciones, la autenticación y autorización de usuarios, y la protección contra vulnerabilidades comunes.

El propósito de esta auditoría es identificar vulnerabilidades en las aplicaciones, evaluar su impacto en la seguridad y la integridad de los datos, y encontrar formas de mitigarlas.

### **6. Auditoría de gestión de incidentes**

Evalúa los procedimientos y capacidades de respuesta de la organización ante incidentes de seguridad. Esto incluye la preparación y planificación de incidentes, la detección y notificación, la gestión de respuesta y recuperación, y el aprendizaje de lecciones de incidentes anteriores.

Esta auditoría prueba la capacidad de la empresa para reaccionar ante incidentes, su contención y resolución, y la eficacia del playbook de incidentes para evitar la propagación y gestionar futuros incidentes de manera eficiente.

# **Investigación de Metodologías de Pentesting**<a name="id3"></a>

En esta parte del proyecto, realizaremos un estudio de diferentes metodologías de pentesting que podemos utilizar durante una auditoría.

## **OSSTMM**

El OSSTMM (Open Source Security Testing Methodology Manual) es una metodología integral desarrollada por ISECOM para llevar a cabo pruebas, análisis y medición de la seguridad operativa.

Es una herramienta diseñada para realizar auditorías técnicas de seguridad de manera consistente y repetible.

### **Objetivos**

El objetivo principal del OSSTMM es construir defensas de seguridad efectivas. Sus objetivos específicos incluyen:

- Establecer un enfoque sistemático para auditorías de seguridad más consistentes y repetibles.
- Proporcionar un mecanismo para evaluar los resultados de las auditorías de manera objetiva.
- Permitir una presentación estructurada y comparativa de los resultados.

### **Fases de una Auditoría**

Las fases de una auditoría según OSSTMM son:

1. **Lanzar el proyecto:** Aprobar recursos y crear conciencia sobre los posibles impactos no deseados en los sistemas de información.
2. **Fase inductiva:** Comprender los requisitos, alcance y limitaciones de la auditoría para determinar las pruebas a realizar.
3. **Fase interactiva:** Planificar la auditoría después de definir el alcance y los tipos de pruebas para cada elemento.
4. **Fase de investigación:** Analizar aspectos organizativos y de gestión, junto con un análisis técnico inicial de fuentes abiertas.
5. **Fase de intervención:** Realizar pruebas técnicas en los elementos del alcance, pudiendo modificar, sobrecargar o bloquear elementos para evaluar la seguridad.
6. **Reporte:** Elaborar un informe que evalúe los resultados y valore los hallazgos identificados.
7. **Resolución de deficiencias:** Abordar las deficiencias identificadas, utilizando los resultados para priorizar las acciones correctivas.

## **OWASP Testing Guide**

La metodología de pruebas de penetración de OWASP (Open Web Application Security Project) se centra en evaluar la seguridad de las aplicaciones web y en identificar y abordar vulnerabilidades de seguridad.

### **Objetivos**

Los objetivos de OWASP son:

1. **Identificar vulnerabilidades de seguridad**
2. **Evaluar la seguridad de las aplicaciones web**
3. **Proporcionar recomendaciones de mitigación**
4. **Concienciar sobre la seguridad**
5. **Ayudar a las organizaciones a proteger sus activos digitales**
6. **Mejorar la calidad del software**
7. **Promover pruebas de penetración éticas**

### **Fases**

Las fases de una auditoría según la metodología OWASP son:

1. **Fase de Recopilación de Información:** Reunir datos sobre el objetivo, como información sobre la aplicación, tecnologías utilizadas y arquitectura.
2. **Fase de Análisis:** Analizar vulnerabilidades potenciales, puntos de entrada y flujos de datos, evaluando la lógica de la aplicación y posibles vectores de ataque.
3. **Fase de Descubrimiento de Vulnerabilidades:** Realizar pruebas activas para descubrir vulnerabilidades como inyecciones SQL y ataques de XSS.
4. **Fase de Explotación:** Intentar explotar vulnerabilidades significativas para evaluar el impacto real de un ataque.
5. **Fase de Informe:** Documentar todas las vulnerabilidades encontradas, su gravedad y recomendaciones para solucionarlas.
6. **Fase de Validación:** Validar que las vulnerabilidades corregidas se hayan solucionado adecuadamente.
7. **Fase de Documentación y Entrega Final:** Documentar todo el proceso y entregar esta documentación a la organización objetivo.

## **PTES**

El Penetration Testing Execution Standard (PTES) proporciona un marco común para realizar pruebas de penetración en empresas y proveedores de servicios de seguridad.

### **Objetivos**

Los objetivos del estándar PTES son:

- Proporcionar un marco de referencia para auditorías técnicas de seguridad de sistemas de información de manera consistente y replicable.
- Incrementar el valor de las pruebas de penetración.

### **Fases**

1. **Interacción Previa:** Definir el alcance y las acciones a realizar para llevar a cabo con éxito la prueba de penetración.
2. **Recopilación de Información:** Recopilar información sobre el objetivo a través de fuentes OSINT, inspección y caracterización, considerando medidas de protección a evitar.
3. **Modelado de Amenazas:** Analizar el contexto para identificar elementos que podrían utilizarse en ataques. Caracterizar activos y amenazas para perfilar tipos de ataques probables.
4. **Análisis de Vulnerabilidades:** Buscar fallos en los sistemas que puedan ser explotados, desde mala configuración hasta diseños inseguros, y verificar su posible explotación.
5. **Explotación:** Ejecutar mecanismos para obtener acceso a sistemas o recursos aprovechando las vulnerabilidades identificadas.
6. **Post-Explotación:** Asegurar la persistencia del acceso obtenido, realizar movimientos laterales para controlar otros activos y recopilar información valiosa.
7. **Informe:** Elaborar un informe detallado que resuma los resultados técnicos y metodológicos de la prueba, así como un informe ejecutivo que resuma resultados, riesgos y propuestas de mitigación.

# **Metodología Elegida: PTES (Penetration Testing Execution Standard)**

La metodología PTES (Penetration Testing Execution Standard) es un marco estructurado y detallado para realizar pruebas de penetración, ofreciendo un enfoque integral y sistemático que cubre todos los aspectos de la seguridad informática. Esta metodología proporciona una guía clara para llevar a cabo auditorías de seguridad de manera consistente, replicable y exhaustiva.

## **Objetivos de PTES**

1. **Proveer un marco estructurado para las pruebas de penetración:**
Asegurar que las auditorías de seguridad se realicen de manera sistemática y replicable.
2. **Incrementar el valor de las pruebas de penetración:**
Proporcionar resultados útiles y accionables que ayuden a las organizaciones a mejorar su postura de seguridad.
3. **Facilitar la identificación y explotación de vulnerabilidades:**
Permitir a los auditores identificar y explotar vulnerabilidades de manera efectiva para evaluar la seguridad de los sistemas.
4. **Mejorar la comunicación de resultados:**
Estandarizar la documentación y presentación de los hallazgos para que sean fácilmente comprensibles y utilizables por las organizaciones.

## **Fases de PTES**

La metodología PTES se compone de varias fases, cada una de las cuales aborda un aspecto específico del proceso de pruebas de penetración. A continuación se detallan estas fases:

### **1. Interacción Previa**

**Descripción:**

- Definir el alcance de la prueba de penetración.
- Establecer expectativas y objetivos con el cliente.
- Identificar los recursos necesarios y las restricciones operativas.

**Objetivos:**

- Asegurar una comprensión clara y mutua de lo que se va a probar y por qué.
- Determinar los límites del proyecto para evitar cualquier impacto no deseado en las operaciones del cliente.

### **2. Recopilación de Información**

**Descripción:**

- Reunir información sobre el objetivo utilizando fuentes de inteligencia de código abierto (OSINT).
- Realizar inspección y caracterización de los sistemas y redes objetivo.

**Objetivos:**

- Obtener una visión detallada del entorno objetivo.
- Identificar posibles puntos de entrada y vectores de ataque.

### **3. Modelado de Amenazas**

**Descripción:**

- Analizar el contexto interno y externo del objetivo.
- Identificar activos críticos y posibles amenazas.

**Objetivos:**

- Perfilar los tipos de ataques más probables y su impacto potencial.
- Priorizar las áreas de enfoque para la prueba de penetración.

### **4. Análisis de Vulnerabilidades**

**Descripción:**

- Identificar fallos y debilidades en los sistemas objetivo.
- Verificar la presencia de vulnerabilidades que puedan ser explotadas.

**Objetivos:**

- Descubrir vulnerabilidades de seguridad desde malas configuraciones hasta fallos en el diseño.
- Validar la efectividad de las medidas de seguridad implementadas.

### **5. Explotación**

**Descripción:**

- Intentar explotar las vulnerabilidades identificadas para obtener acceso no autorizado a los sistemas o datos.

**Objetivos:**

- Evaluar el impacto real de las vulnerabilidades.
- Demostrar cómo un atacante podría comprometer el sistema.

### **6. Post-Explotación**

**Descripción:**

- Asegurar la persistencia del acceso obtenido.
- Realizar movimientos laterales para comprometer otros activos dentro del entorno.
- Recopilar información valiosa y sensible.

**Objetivos:**

- Comprender el alcance completo del compromiso.
- Evaluar la capacidad del atacante para mantener el acceso y moverse dentro de la red.

### **7. Informe**

**Descripción:**

- Elaborar un informe detallado que documente todos los hallazgos técnicos y metodológicos de la prueba.
- Incluir un informe ejecutivo que resuma los resultados, riesgos y propuestas de mitigación.

**Objetivos:**

- Proporcionar una documentación clara y comprensible de los hallazgos.
- Ofrecer recomendaciones prácticas para mejorar la seguridad del cliente.

## **Relación con los Tipos de Auditoría**

La metodología PTES se puede adaptar para abordar diferentes tipos de auditorías de seguridad que ofreceremos:

1. **Auditoría de Cumplimiento Normativo:**
    - Utiliza la fase de Recopilación de Información y Análisis de Vulnerabilidades para asegurar que los sistemas cumplen con los estándares y regulaciones aplicables.
    - La fase de Informe proporciona documentación detallada sobre el cumplimiento y las áreas de mejora necesarias.
2. **Auditoría de Políticas y Procedimientos:**
    - La fase de Interacción Previa y Modelado de Amenazas permite evaluar las políticas y procedimientos existentes.
    - Las fases de Explotación y Post-Explotación prueban la efectividad de estas políticas en escenarios reales.
3. **Auditoría de Controles de Acceso:**
    - La fase de Recopilación de Información y Análisis de Vulnerabilidades se enfoca en la gestión de accesos y autenticación.
    - La fase de Explotación prueba la robustez de los controles de acceso y la capacidad de los sistemas para resistir ataques.
4. **Auditoría de Seguridad de Redes:**
    - Todas las fases de PTES son aplicables, con un énfasis especial en la Recopilación de Información, Análisis de Vulnerabilidades y Explotación para identificar y mitigar riesgos en la infraestructura de red.
5. **Auditoría de Seguridad de Aplicaciones:**
    - La fase de Recopilación de Información y Análisis de Vulnerabilidades se centra en la revisión del código fuente y configuración de seguridad de las aplicaciones.
    - La fase de Explotación evalúa la seguridad de las aplicaciones a través de pruebas prácticas.
6. **Auditoría de Gestión de Incidentes:**
    - La fase de Modelado de Amenazas y Post-Explotación permite evaluar la capacidad de respuesta ante incidentes de seguridad.
    - La fase de Informe y la fase de Resolución de Deficiencias se utilizan para documentar los hallazgos y mejorar los procedimientos de gestión de incidentes.
    
    # **Evaluación de Herramientas de Monitorización**<a name="id4"></a>
    
    Para ofrecer servicios de auditoría ofensiva efectivos, es crucial contar con herramientas avanzadas de monitorización de seguridad. Estas herramientas permitirán detectar y analizar vulnerabilidades, gestionar eventos de seguridad y monitorear el tráfico de red, esencial para implementar la metodología PTES de manera eficiente.
    
    He investigado una variedad de herramientas de monitorización de seguridad, incluyendo sistemas de gestión de eventos de seguridad (SIEM), herramientas de detección de vulnerabilidades y análisis de tráfico de red. Entre las herramientas más relevantes encontramos:
    
    ### **1. Nessus**
    
    Nessus es una herramienta de escaneo de vulnerabilidades que permite detectar configuraciones incorrectas y generar informes detallados de seguridad. Es compatible con una amplia gama de sistemas operativos y dispositivos. Requiere hardware estándar de servidor y una licencia de software con un costo de $2,990 anual (Nessus Professional).
    
    ### **2. Splunk**
    
    Splunk es un SIEM avanzado con capacidades de análisis de big data, detección en tiempo real de amenazas, informes personalizados y análisis forense. Se integra con diversas fuentes de datos y herramientas de seguridad. Requiere hardware robusto para almacenamiento y procesamiento, y una licencia de software cuyo costo es aproximadamente $2,000 anual por 100 GB/día, además de un hardware estimado en $5,000.
    
    ### **3. Wireshark**
    
    Wireshark es una herramienta de análisis de tráfico de red en tiempo real, que permite la decodificación de cientos de protocolos y el análisis forense de tráfico de red. Es un software de código abierto y gratuito, aunque requiere hardware estándar valorado en aproximadamente $1,000.
    
    ### **4. Burp Suite Professional**
    
    Burp Suite Professional es una herramienta para el escaneo automatizado de vulnerabilidades en aplicaciones web, con herramientas manuales para pruebas detalladas, manipulación de tráfico HTTP/S y generación de informes detallados. Requiere una licencia de software anual que cuesta $399 por usuario.
    
    ### **5. Metasploit**
    
    Metasploit es un marco de pruebas de penetración que permite la explotación de vulnerabilidades, automatización de tareas repetitivas y generación de informes detallados. Requiere una licencia de software (edición profesional) con un costo de $2,000 anual y hardware estándar valorado en $1,000.
    
    ### **Selección de Herramientas Relevantes y Justificación**
    
    Basándonos en los servicios de auditoría ofensiva definidos y la metodología PTES, las herramientas seleccionadas son:
    
    - **Nessus**: Permite realizar escaneos de vulnerabilidades y detectar configuraciones incorrectas, cruciales para las fases de Análisis de Vulnerabilidades y Explotación de PTES.
    - **Splunk**: Su capacidad de gestión de eventos de seguridad y análisis forense es fundamental para la fase de Post-Explotación y la generación de informes detallados.
    - **Wireshark**: Es vital para el análisis detallado del tráfico de red y la identificación de amenazas y anomalías durante la fase de Recopilación de Información y Modelado de Amenazas.
    - **Burp Suite Professional**: Esencial para las pruebas de seguridad de aplicaciones web, cubriendo las fases de Análisis de Vulnerabilidades y Explotación con un enfoque en aplicaciones web.
    - **Metasploit**: Proporciona un marco completo para la explotación de vulnerabilidades, permitiendo la ejecución efectiva de la fase de Explotación y Post-Explotación.
    
    ### **Estimación de Inversión Inicial**
    
    La inversión inicial necesaria para adquirir estas herramientas se detalla a continuación:
    
    - **Nessus**: $2,990
    - **Splunk**: $7,000 (licencia + hardware)
    - **Wireshark**: $1,000 (hardware)
    - **Burp Suite Professional**: $399
    - **Metasploit**: $3,000 (licencia + hardware)
    - **Personal Técnico**: $120,000 anual (considerando un equipo inicial de 2 analistas a $60,000 cada uno)
    - **Capacitación**: $5,000
    
    **Total Estimado**: $139,389
    
    Esta inversión inicial asegura que nuestra empresa de ciberseguridad cuenta con las herramientas y recursos necesarios para realizar auditorías de seguridad efectivas y cumplir con los objetivos establecidos en nuestra metodología de pentesting PTES.

## Referencias <a name="id5"></a>
[Metodología OSSTMM](https://www.ciberseguridad.eus/ciberpedia/vulnerabilidades/open-source-security-testing-methodology-manual-osstmm)  
[(OWASP)](https://owasp.org/www-project-web-security-testing-guide/)  
[Penetration Testing Execution Standard(PTES)](https://www.ciberseguridad.eus/ciberpedia/marcos-de-referencia/penetration-testing-execution-standard-ptes)   
[Tipos de Auditoría Ofensiva](https://blog.hubspot.es/website/auditoria-de-seguridad)  
[Auditoria de cumplimiento normativo](https://www.compliance-antisoborno.com/auditoria-de-cumplimiento-normativo-como-prepararse-para-superarla-con-exito/)  
[Auditoria seguridad informática](https://unirfp.unir.net/revista/ingenieria-y-tecnologia/auditoria-seguridad-informatica/#:~:text=La%20auditor%C3%ADa%20de%20seguridad%20inform%C3%A1tica,una%20empresa%20y%20ponerle%20soluci%C3%B3n.)  
[Pasos para realizar una auditoria de ciberseguridad](https://mrinformatica.es/pasos-para-realizar-una-auditoria-de-ciberseguridad/)  
[WireShark](https://openwebinars.net/blog/wireshark-que-es-y-ejemplos-de-uso/)   
[Metaesploit](https://keepcoding.io/blog/que-es-metasploit-ciberseguridad/)  

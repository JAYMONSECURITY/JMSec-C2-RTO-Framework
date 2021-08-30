# JMSec-Agent RTO
Author: Juan M. https://www.linkedin.com/in/jaymonsecuritydirector/

Command and Control Panel JMSec Agent - JAYMON SECURITY Red Team Operations.

https://jaymonsecurity.com/software-de-administracion-remota/

![DASHBOARD](https://user-images.githubusercontent.com/76411871/131404701-ff174a84-90a0-4523-8afe-f64623ec1bb8.png)


DESCRIPCIÓN

Se trata de un software diseñado específicamente para llevar a cabo Operaciones Red Team en equipos informáticos con Sistema Operativo Windows (XP/Vista/7/8/8.1/10) de arquitecturas X64/X86.

Programado por la sección “Red Team” de JAYMON SECURITY, consta de un instalador que ejecuta un binario tipo sensor en la máquina víctima para infectarla, y de un panel de control  Web multiplataforma que constituye el servidor de Mando y Control (C2), desde donde se envían órdenes a ejecutar en las máquinas infectadas. 

En resumen, consta de: 

•	El Instalador: Encargado de instalar en las máquinas infectadas un "agente" que conecta con un servidor de Mando y Control C2.

•	Servidor de Mando y Control (C2) Web: Se trata de una aplicación Web de interfaz intuitiva mediante la cual el Red Team Operator puede controlar las máquinas infectadas.

CARACTERÍSTICAS

•	Escrito en C/C++, tiene la capacidad de crear una BOTNET, ya que bajo su servidor de mando y control C2 puede llegar a controlar miles de máquinas infectadas, asignándole a cada una de ellas un número de identificación propio. 

•	Tras su ejecución, procede a realizar sus funciones en segundo plano, sin que el usuario se percate de su presencia.

•	Consta de funciones específicas para la evasión de sistemas AntiVirus, AMSI, IDS, IPS. Sus funciones están cifradas con un algoritmo propio, tras su ejecución se descodifica en memoria para evitar posibles detecciones.

•	Se auto elimina tras la primera ejecución y procede a asegurar su permanencia mediante su auto ejecución tras reinicio del sistema infectado. Posteriormente realiza la ejecución en memoria de múltiples TTPs del marco MITRE.

•	Realiza comprobaciones períodicas vía HTTP/S de la existencia de nuevas instrucciones a ejecutar en la/s máquina/s infectada/s. 

•	Las distintas funciones de las que consta se explican en la descripción del Panel de Control.


PANEL DE CONTROL (C2)

Desde el panel de control se lanzan instrucciones a las máquinas infectadas. Dichas instrucciones las podremos lanzar bien de máquina en máquina, según número de identificación propio, o bien a todas las máquinas infectadas que conforman la BOTNET.

Las distintas órdenes que podemos lanzar a las máquinas infectadas son:

•	Obtener una Shell de comandos inversa (Reverse Shell) de la máquina infectada.

•	Subir cualquier tipo de archivo de la máquina infectada al servidor C2.

•	Descargar cualquier tipo de archivo desde el servidor C2  a la máquina infectada.

•	Envío de órdenes de ejecución de comandos, pudiéndose concatenar varios de ellos mediante el parámetro "&" para ejecutarlos todos ellos en la máquina infectada.

•	Descarga de archivos del servidor C2 a la máquina infectada, y auto ejecución de los mismos.

•	Capturas de pantalla de la máquina infectada y subida de las mismas al servidor C2.

•	Exportar credenciales WiFi almacenadas en la máquina infectada y subirlas al servidor C2.

•	Exportar credenciales WEB almacenadas en la máquina infectada y subirlas al servidor C2.

•	Función de captura de teclas pulsadas por el usuario de la máquina infectada. 

•	Función para el lanzamiento de ataques de denegación de servicio (DOS) a redes específicas.

•	Función de envío de información específica de procesos, usuarios y directorios de la máquina infectada al servidor C2.

• Función de ejecución de Stager Meterpreter para recibir una sesión Meterpreter de Metasploit en otro C2 remoto, fuera de listas negras del Blue Team de la Organización a auditar.

•	Ver listado de capturas, archivos y carpetas tanto del directorio de la máquina infectada en el servidor C2, como del servidor C2 completo con todas las máquinas infectadas.

•	Ver los “logs” de la actividad de conexión de cada una de las máquinas infectada. Útil para conocer las horas de actividad de cada máquina infectada.

•	Función de auto eliminación del Software malicioso de la/s máquina/s infectada/s. 


OBJETIVOS

• No ser detectados durante la misión.

•	Exfiltrar la información necesaria de los equipos informáticos infectados para la creación de inteligencia empresarial y llevar a cabo distintas acciones sobre los objetivos.

•	Realizar inteligencia y ejecución de operaciones con garantías de éxito.

•	Finalizar la misión sin ser detectados con todas las TTPs posibles ejecutadas en memoria, y mediante inyecciones en procesos legítimos del sistema infectado.
 

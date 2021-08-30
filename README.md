# JMSec-Software RTO
Command and Control Panel JMSec Implant - JMSec Red Team Operations.


![DASHBOARD](https://user-images.githubusercontent.com/76411871/131404701-ff174a84-90a0-4523-8afe-f64623ec1bb8.png)


DESCRIPCIÓN

Se trata de un software diseñado específicamente para la creación de Ciberinteligencia mediante la administración remota de equipos informáticos con Sistema Operativo Windows.
Programado por la sección “Red Team” de JAYMON SECURITY, consta de un instalador que ejecuta un binario tipo sensor en la máquina víctima para infectarla, y de un panel de control  Web multiplataforma que constituye el servidor de Mando y Control (C2), desde donde se envían órdenes a ejecutar en las máquinas infectadas. 

En resumen, consta de: 

•	El Instalador: Encargado de instalar en las máquinas remotas a administrar (las víctimas) el sensor que conectará con el servidor C2.

•	Panel de Mando y Control (C2) Web: Se trata de una plataforma web de interfaz intuitiva programada en PHP e instalada en un servidor HTTP/S  mediante el cual el Red Team Operator puede controlar las máquinas infectadas.

CARACTERÍSTICAS

•	Presenta una función específica que lo dota de una característica de “carácter múltiple”, es decir, bajo su servidor de mando y control C2 puede llegar a controlar miles de máquinas administradas, ya que por cada una de ellas se crea un número de identificación propio. 

•	Tras su ejecución, procede a realizar sus funciones en segundo plano, sin que el usuario se percate de su presencia.

•	Consta de funciones específicas para la evasión de sistemas AntiVirus, IDS, IPS. Sus funciones están cifradas con un algoritmo propio, tras su ejecución se descodifica en memoria para evitar posibles detecciones.

•	Se auto elimina tras la primera ejecución en la máquina administrada y procede a asegurar su permanencia mediante su auto ejecución tras cualquier reinicio del sistema.

•	Tras su ejecución procede a asignar un número de identificación único e intransferible a la nueva máquina a administrar, y a crear un archivo de texto con contenido confidencial de la máquina administrada. Posteriormente exfiltra la información al servidor de mando y control.

•	Posteriormente realiza una comprobación vía HTTP/S de la existencia de nuevas instrucciones a ejecutar en la máquina administrada. En caso de no existir instrucciones a ejecutar quedará a la espera de nuevas órdenes, realizando dicha comprobación permanentemente.

•	Las distintas funciones de las que consta se explican en la descripción del Panel de Control.


PANEL DE CONTROL (C2)

Desde el panel de control podremos ejecutar instrucciones a las máquinas administradas. Dichas instrucciones las podremos lanzar bien de máquina en máquina, según número de identificación propio, o bien a todas las máquinas infectadas.

Las distintas órdenes que podemos lanzar a las máquinas víctima (infectadas) son:

•	Obtener una Shell de comandos inversa (Reverse Shell) de la máquina administrada.

•	Subir cualquier tipo de archivo de la máquina administrada al servidor C2.

•	Descargar cualquier tipo de archivo desde el servidor C2  a la máquina administrada.

•	Envío de órdenes de ejecución de comandos, pudiéndose concatenar varios de ellos mediante el parámetro "&" para ejecutarlos todos ellos en la máquina administrada.

•	Tras la ejecución de las instrucciones lanzadas, se procede a eliminar la orden lanzada del servidor C2. Esto se realiza de esta manera para que el programa no entre en un bucle infinito de ejecución de la misma orden comandada.

•	Descarga de archivos del servidor C2 a la máquina administrada, y auto ejecución del mismo.

•	Capturas de pantalla de la máquina administrada y subida de las mismas al servidor C2.

•	Exportar credenciales WiFi almacenadas en la máquina administrada y subirlas al servidor C2.

•	Exportar credenciales WEB almacenadas en la máquina administrada y subirlas al servidor C2.

•	Función de captura de teclas pulsadas por el usuario de la máquina administrada. 

•	Función para el lanzamiento de ataques de denegación de servicio (DOS) a redes específicas.

•	Función de envío de información específica de procesos, usuarios y directorios de la máquina administrada al servidor C2 a petición del propio administrador, además de hacerlo de manera automática todos los días 14 de mes.

•	Ver listado de capturas, archivos y carpetas tanto del directorio de la máquina administrada en el servidor C2 como del servidor C2 completo con todas las máquinas administradas.

•	Ver los “logs” de la actividad de conexión de cada una de las máquinas administradas. Útil para conocer las horas de actividad de cada máquina administrada.

•	Función de auto eliminación del Software malicioso de la/s máquina/s administrada/s. 
 
OBJETIVOS

•	Adquirir la información necesaria de los equipos informáticos infectados para la creación de Ciberinteligencia personal y empresarial.

•	Mantener un estrecho control de los sistemas informáticos de la empresa u organización.

•	Tener la capacidad de poder realizar inteligencia y ejecución de operaciones con garantías de éxito.
 

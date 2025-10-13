Guía de Inteligencia y Campo para PEC1: Fundamentos de Redes
PARTE 1: FUNDAMENTOS Y CONCEPTOS (Ejercicios 1-5)
Ejercicio 1: Orígenes de Internet
Intel Drop:

Origen (ARPANET): Proyecto del Departamento de Defensa de EE. UU. (años 60). Objetivo principal: crear una red de comunicaciones descentralizada y tolerante a fallos. (Fuente: Kurose, Sec. 1.7.1).

Hito 1 - E-mail (1972): Creado por Ray Tomlinson. Transformó la red de una herramienta de acceso a máquinas a una de comunicación humana. Fue la primera "killer app". (Fuente: Kurose, Sec. 1.7.1).

Hito 2 - TCP/IP (1974-1983): Vinton Cerf y Robert Kahn diseñan una arquitectura para interconectar redes ("internetworking"). El 1 de enero de 1983, ARPANET adopta oficialmente TCP/IP, creando el lenguaje común de la Internet moderna. (Fuente: Kurose, Sec. 1.7.2).

Hito 3 - World Wide Web (1989-1991): Tim Berners-Lee en el CERN inventa el HTTP y el HTML. La introducción de navegadores gráficos (como Mosaic/Netscape) hizo la red accesible para el público general, desatando su explosión comercial y social. (Fuente: Kurose, Sec. 1.7.4).

Tu Tarea: Conecta estos puntos. Explica cómo se pasó de una red militar experimental a una herramienta de comunicación global, y finalmente a una plataforma de información y servicios accesible para todos.

Ejercicio 2: Red Doméstica
Intel Drop:

Elementos: Router del ISP (combo de módem, router, switch, AP Wi-Fi), Dispositivos finales (PCs, móviles, Smart TV). (Fuente: Kurose, Sec. 1.2.1, "Home Access").

Acceso a Internet: Los dispositivos se conectan al router (vía Ethernet o Wi-Fi). El router gestiona la red local (LAN) y actúa como gateway, traduciendo direcciones (NAT) y enviando el tráfico al ISP. (Fuente: "El papel de las redes", pág. 6-8).

Características del Router: Busca en la etiqueta del dispositivo o en su interfaz web.

Conectividad WAN: ¿Es Fibra (FTTH), Cable (HFC) o Cobre (DSL)?

Estándar Wi-Fi: ¿Es Wi-Fi 5 (802.11ac), Wi-Fi 6 (802.11ax)? Esto determina la velocidad máxima teórica.

Puertos LAN: ¿Son Fast Ethernet (100 Mbps) o Gigabit Ethernet (1000 Mbps)?

Tu Tarea: Aplica estos conceptos a tu casa en Pescara. Identifica tu router, lista tus dispositivos y describe el proceso.

Ejercicio 3: Encapsulación
Intel Drop:

El proceso de añadir cabeceras en cada capa al descender por la pila de protocolos. (Fuente: Kurose, Sec. 1.5.2).

Capa de Aplicación: El dato ("23") se convierte en una Mensaje. Se añade cabecera de la aplicación (ej. HTTP).

Capa de Transporte: La Mensaje se encapsula en un Segmento. Se añade cabecera TCP/UDP con Puertos de origen/destino (para identificar la aplicación correcta).

Capa de Red: El Segmento se encapsula en un Datagrama. Se añade cabecera IP con Direcciones IP de origen/destino (para enrutamiento global).

Capa de Enlace: El Datagrama se encapsula en una Trama. Se añade cabecera Ethernet con Direcciones MAC de origen/destino (para el siguiente salto en la red local).

Tu Tarea: Describe este viaje, explicando la función de la información añadida en cada paso como si fueran direcciones en un sistema postal multinivel.

Ejercicio 4: Señales y Ancho de Banda
Intel Drop:

Una señal digital es una secuencia de pulsos de tensión. (Fuente: "El papel de las redes", pág. 15, Fig. 4).

Bits anchos (baja velocidad): Menos cambios de señal por segundo. Requiere menos ancho de banda porque usa frecuencias más bajas.

Bits estrechos (alta velocidad): Más cambios de señal por segundo. Requiere más ancho de banda porque necesita componentes de frecuencia más altas para representar esos cambios rápidos.

Límites: No se puede aumentar indefinidamente por:

Atenuación: Las frecuencias altas pierden energía más rápido con la distancia.

Ruido y Distorsión: A mayor velocidad, es más fácil que el ruido corrompa un bit o que los bits se "mezclen" (interferencia intersimbólica).

Límites del Medio Físico: Cada material (cobre, fibra) tiene una capacidad máxima (Teorema de Shannon-Hartley). (Fuente: "El papel de las redes", pág. 17).

Tu Tarea: Dibuja las ondas y explica la relación directa: más velocidad -> bits más cortos -> se necesitan frecuencias más altas -> se consume más ancho de banda.

Ejercicio 5: Atenuación WiFi (FSPL)
Intel Drop:

La fórmula PL(dB) = 20*log10(d) + 20*log10(f) - 147.55 muestra que la pérdida (PL) aumenta con la distancia (d) y la frecuencia (f).

2.4 GHz vs 5 GHz: Al ser f mayor para 5 GHz, su PL siempre será mayor a la misma distancia. Esto significa menor cobertura y peor penetración de obstáculos (paredes).

¿Por qué usar 5 GHz?

Más Canales: La banda de 5 GHz tiene muchos más canales no solapados que la de 2.4 GHz (que solo tiene 3). Esto reduce drásticamente la interferencia de redes vecinas.

Menos Congestión: La banda de 2.4 GHz está saturada por otros dispositivos (Bluetooth, microondas). 5 GHz está más "limpia".

Mayor Ancho de Banda por Canal: Los canales en 5 GHz pueden ser más anchos (40, 80, 160 MHz), permitiendo velocidades de transmisión mucho mayores. (Fuente: Kurose, Sec. 1.2.1).

Tu Tarea: Usa la calculadora del laboratorio para generar los datos, crea tu gráfica, y explica este trade-off: 2.4 GHz para cobertura, 5 GHz para velocidad y rendimiento a corta distancia.

PARTE 2: GUÍA DE CAMPO PACKET TRACER (Ejercicios 6-13)
Ejercicio 6: Vista Física
Guía de Campo:

Mover Nodos: En la vista "Physical", simplemente arrastra los iconos de los clusters a su ubicación en el mapa.

Descripción de Dispositivos: Usa el "Navigation Panel" (Shift+N). Verás Router, Switch, Server, Hub. Describe la función de cada uno (Router conecta redes, Switch conecta dispositivos en una misma red, etc.).

Montar Rack: Entra a un cluster (ej. "Netflix DC"). Arrastra un Rack desde el menú. Luego, arrastra el Router, Switch y Server a las bahías del rack. Usa los cables apropiados para reconectarlos.

Recursos DC Real: Piensa en lo que no se ve en PT: Refrigeración (HVAC), Energía Redundante (UPS, generadores), Seguridad Física (cámaras, control de acceso), Sistemas Anti-incendios.

Ejercicio 7: Análisis de Topología
Intel Drop:

La topología es distribuida o de malla parcial en la nube "INTERNET". Sin embargo, los Datacenters (Netflix, Alphabet) y tu Home se conectan de forma centralizada (topología en estrella) a un único router de borde.

Cuellos de Botella / Puntos de Fallo: RouterNetflix y RouterAlphabet son puntos únicos de fallo para sus respectivos DC. Si fallan, el DC queda aislado. El router al que conectes tu Home Router también lo será para ti.

Mejora de Resiliencia: Añadir redundancia. Conectar el RouterNetflix a un segundo router en la nube de Internet (ej. Router2). Esto se llama multihoming. Para la máxima robustez, se usarían protocolos de enrutamiento dinámico más avanzados como OSPF o BGP para gestionar las rutas redundantes.

Ejercicio 8: Hub/Repetidor
Intel Drop:

Un Hub es un dispositivo de Capa 1 (Física). Su única función es recibir una señal por un puerto y repetirla por todos los demás, regenerándola para combatir la atenuación por la distancia.

¿Por qué ahí? Didácticamente, representa una forma de extender una conexión a larga distancia (ej. un cable submarino entre la península y las Baleares) donde la señal se degradaría.

¿Sentido en una red real? No. En una red moderna se usaría un switch o simplemente enlaces de fibra óptica con amplificadores adecuados. Los hubs son tecnología obsoleta porque crean un único dominio de colisión (si dos dispositivos hablan a la vez, los datos chocan y se corrompen) y son ineficientes.

Ejercicio 9: Conexión Directa PC-PC
Guía de Campo:

Añade PC y Laptop.

Usa el rayo ("Automatically Choose Connection Type") para conectarlos. Packet Tracer seleccionará un Cable Cruzado (Crossover), representado por una línea negra discontinua.

¿Por qué cruzado? Porque en un PC, los pines de la tarjeta de red están fijos (unos para transmitir - TX, otros para recibir - RX). Para conectar dos dispositivos iguales, necesitas cruzar los cables para que el TX de un PC se conecte al RX del otro, y viceversa. Un switch hace este cruce internamente, por eso para conectar un PC a un switch se usa un cable directo (straight-through).

Configura IPs (ej. 192.168.1.2 y 192.168.1.3, máscara 255.255.255.0).

Abre el Command Prompt en el PC y escribe ping 192.168.1.3. Debería funcionar.

Ejercicio 10 y 11: Configuración de Routers y RIP
Guía de Campo:

Interfaces: Haz clic en un router, ve a la pestaña CLI. Escribe enable y luego show ip interface brief. Verás todas las interfaces y su estado. Para apagar una interfaz no usada (ej. FastEthernet0/1), entra en modo configuración (configure terminal), luego a la interfaz (interface FastEthernet0/1) y escribe shutdown.

Configurar IP: En la interfaz (interface FastEthernet0/0), escribe ip address 192.168.2.1 255.255.255.0 y luego no shutdown para activarla.

Routing RIP: RIP (Routing Information Protocol) es un protocolo simple que permite a los routers compartir las redes que conocen directamente. Al añadir una red en la configuración RIP (router rip -> network 192.168.2.0), el router empieza a "anunciar" a sus vecinos que él sabe cómo llegar a esa red. Así, los otros routers de la topología aprenden la ruta. Es crucial anunciar todas las redes directamente conectadas a un router.

Ejercicio 12: Análisis de Paquetes en Simulación
Intel Drop:

Este es uno de los conceptos más importantes de redes.

Capa 3 (IP): Las direcciones IP de origen y destino NUNCA cambian durante el viaje del paquete. Son como la dirección del remitente y del destinatario en una carta postal; identifican el inicio y el final del viaje.

Capa 2 (MAC): Las direcciones MAC de origen y destino CAMBIAN en cada salto (hop) entre routers. Son como la etiqueta de "próxima parada" que pone el cartero. La MAC de destino es siempre la del siguiente dispositivo en el camino (el siguiente router), y la MAC de origen es la del dispositivo que está enviando la trama (el router actual).

ICMP: El protocolo de los ping. Tipo 8 es echo request (la pregunta) y Tipo 0 es echo reply (la respuesta).

Tu Tarea: Sigue el sobre en modo simulación. Haz clic en él en cada salto y observa la pestaña "Outbound PDU Details". Fíjate cómo cambian los campos SRC MAC y DST MAC, mientras que SRC IP y DST IP se mantienen constantes.

PARTE 3: ANÁLISIS DE RENDIMIENTO (Ejercicios 14-15)
Ejercicio 14: Cálculo de Retardo (Stop-and-Wait)
Guía de Campo (Desglose del problema):

Calcular Nº de Paquetes: Tamaño Archivo / Datos por Paquete.

Datos por Paquete = 1500 (MTU) - 54 (Cabeceras) = 1446 Bytes.

Nº Paquetes = (10 * 10^9 Bytes) / 1446 Bytes.

Calcular Tiempo de Ida y Vuelta (RTT) de un paquete:

RTT = (h+1) * T_trans_datos + (h+1) * T_trans_ack + 2 * h * T_prop

h = nº de saltos (routers intermedios).

T_trans_datos = Tamaño Paquete (1500*8 bits) / Capacidad (10 Mbps).

T_trans_ack = Tamaño ACK (54*8 bits) / Capacidad (10 Mbps).

T_prop = Distancia (1 km) / Vel. Propagación (2e8 m/s).

Calcular Retardo Total (sin errores): Retardo = Nº Paquetes * RTT.

Cálculo con Errores (BER):

Primero, calcula la probabilidad de que un paquete llegue sin error (PER): P_exito_paquete = (1 - BER)^(Tamaño Paquete en bits).

La probabilidad de que un paquete llegue sin error a través de h+1 enlaces es: P_exito_total = (P_exito_paquete)^(h+1).

El número promedio de transmisiones por paquete es 1 / P_exito_total.

Retardo Total (con errores): Retardo = Nº Paquetes * (1 / P_exito_total) * RTT.

Ejercicio 15: Análisis de Ping (Jitter, Boxplot, PDF, CDF)
Intel Drop:

Comando Ping: ping -n 100 www.uoc.edu (en Windows) o ping -c 100 www.uoc.edu (en macOS/Linux). Copia los resultados a un editor de texto o spreadsheet.

RTT (Latencia): Es el tiempo de ida y vuelta. Depende de la distancia, la congestión y los retardos de procesamiento/transmisión. Espera un RTT mayor para rice.edu (Houston, EE.UU.) que para uoc.edu (Barcelona, España) desde tu ubicación en Pescara.

Jitter: Es la desviación estándar de los RTTs. Mide la variabilidad de la latencia. Un jitter bajo significa una conexión estable y predecible (bueno para VoIP, juegos). Un jitter alto significa que los paquetes llegan a intervalos irregulares (malo).

Boxplot: Visualiza la distribución de tus RTTs. Una caja pequeña y bigotes cortos indican bajo jitter y consistencia. Una caja ancha y bigotes largos indican alto jitter.

PDF (Función de Densidad de Probabilidad): Muestra dónde se concentran los valores de RTT. Un pico alto y estrecho indica una conexión muy estable con la mayoría de los pings agrupados en torno al valor medio.

CDF (Función de Distribución Acumulada): Muestra el porcentaje de pings que tuvieron un RTT menor o igual a un valor. Es útil para SLAs (Acuerdos de Nivel de Servicio). Por ejemplo: "El 95% de mis paquetes a la UOC tuvieron una latencia por debajo de 45ms".

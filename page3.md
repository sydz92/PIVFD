# Cooperación y comunicación

![Imagen 4](img4.png) 

A pesar de que cada drone debe ser capas de ser autonomo, toda la flotilla de drones deben formar una unidad de inteligencia. Los quadricopteros deben establecer una red de comuniación que permita intercambiar a alto nivel, la visión parcial que cada uno percibe del entorno y su estado. 

Toda esta información parcial construye una visión más completa del entorno y permite establecer objetivos de alto nivel. El trabajo en equipo permite mantener drones en vuelo mientras otros recargan su bateria, optimizar las rutas de patrullaje reduciendo los puntos ciegos y mejorar el seguimiento de posibles amenazas.

Para enviar información entre los drones, se utilizan sockets TCP que forman una red mesh a través de WIFI. De esta forma se simplifica el envio de mensajes y se asegura que estos lleguen a destino. Cada drone es responsable de notificar a los demás de su precencia y establecer conexiónes, además de notificar su estado. Este estado incluye información de su posición, estado de vuelo, precencia de intrusos, etc.

El modelo de inteligencia que se busca obtener, es de tipo destribuido. Es decir que no exista un componente maestro que tome las deciciónes. Cada drone, con la información de su estado y el de los demás drones debe determinar si debe seguir su ruta de vuelo, ir a la plataforma de carga, cubrir una nueva ruta de vuelo, perseguir o monitorear un intruso, etc. Siempre buscando optimizar la vigilancia de la zona objetivo en colaboración con los demás drones.


# Coodrinación de la flotilla

![Imagen 4](img4.png) 

A pesar de que cada dron debe ser capas de ser autonomo, toda la flotilla de drones deben trabajar De manera. El mecanismo de coordinación de la flotlla se basa en dos puntos claves: la comunicación y la toma de decicónes. 

La comunicación pemite distribuir el estado de cada dron al resto de drones de la flotilla. Esta información incluye la tarea actual, la posición, el nivel de batería, la presencia de intrusos y su ubicación, entre otras cosas. Toda esta información es resumida en un mensaje y distribuida mediante broadcast. Para pemitir la interconexión de los drones se utiliza una red inalámbrica. Esta red permite utilizar tanto una arquitectura centralizada utilizando puntos de acceso externos o utilizar la señal generada por los drone para generar una red de maya (mesh). 

La toma de decisiones permite utilizar toda la información recolectada directamente por el dron y la información recolectada mediante la comunicación con el resto de la ﬂotilla para tomar decisiónes. Estas decisiones permiten a la ﬂotilla trabajar como una unidad, colaborando para dar seguimiento a los intrusos y coordinar el uso de la plataforma de carga. Este mecanismo mecanismo se basa en dos componentes basicos: la planificación fuera de linea que permite definir las rutas de patrllaje y una maquina de estados en ejecutada en linea. Esta máquina de estados es la que determina qué tarea debe realizar el dron en cada momento y las transiciones son provocadas por eventos percibidos por el propio dron o por el resto de drones de la flotilla.


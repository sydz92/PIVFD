# Percepción del entorno

![Imagen 2](img2.png)

El proyecto emplea drones [Bebop 2 de Parrot](https://www.parrot.com/es/drones/parrot-bebop-2#parrot-bebop-2-). Cada drone posee una camara frontal de gran angular de la que obtiene información del entorno. Ademas cuenta con sensores que puermite otener la posición GPS y la altitud con respecto al suelo. Esta informaición es utilizada para la navegación, visitar los sitios de interez y perseguir intrusos. 

La imágenes obtenidas por la cámara son introducidas en algorimos de procesamiento de imágenes y vision por computadora para su anásis. El resultado de dichos algorimos permiten tener una gran percepción de los elementos y caracterísitcas del entorno. Estos resultados son utilizadas en conjunto con la información de los sensores, para estimar la posición de estos elementos y poder tomar medias sobre dicho entorno.

Para detectar instusos se utiliza un detector de personas, programado en base a liberias de OpenCV. Estos algorimos detectan en las imagenes obtenidas por el drone a potenciales intrusos. Una vez detectados mediante calculos trigonometricos que utilizan datos como el campo de vision de la cámara, el ángulo de con respecto al suelo, la altura del drone, entre otros, se utiliza trigonometría para calcular la posición relativa del instruso. Esto permite, seguir al intruso en la zona de vigililancia y notificar a los demás drones para monitorear sus acciónes.

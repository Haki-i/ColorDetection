# ColorDetection
Leds qui recopient la couleur détectée grace à un capteur

# **Objectif du projet**

L’objectif est de réaliser un cube translucide doté d’une led tricolore réagissant grâce à un capteur de couleur.

# I- **Conception électronique**

## a) Led tricolore

Nous utiliserons une led RGB à anode commune pour pouvoir obtenir une vaste plage de couleurs. Nous la connectons à 3 pins digitaux d’une Arduino Nano puis au GND.

## b) Capteur de couleur

Le capteur utilisé est le tcs34725. Afin de transmettre ses données sur notre carte, nous utilisons le protocole I2C grace aux pins SCL et SDA.

Ce module est constitué de plusieurs photodiodes, qui sont des composants électroniques convertissant la lumière en courant électrique. Lorsqu'elles sont exposées à la lumière, les photons sont absorbés par le matériau des diodes. Leur énergie excite alors les électrons, les faisant sortir du matériau et créant ainsi un courant électrique.

La quantité de courant produit est proportionnelle à l'intensité de la lumière frappant chaque photodiode. Plus la lumière est intense, plus le nombre de photons est élevé, et plus le courant généré est important.

Il est important de noter que chaque photodiode est couverte par un filtre de couleur différent – rouge, vert ou bleu. Ce filtre ne laisse passer que la lumière de la couleur correspondante. Par exemple, la photodiode sous le filtre rouge réagira principalement à la lumière rouge.

Grâce à cette configuration, nous pouvons différencier la couleur et l'intensité lumineuse de l'objet observé

## c) Alimentation

Pour alimenter notre système nous utiliserons une batterie externe de 4.5V et nous souderons un module adaptateur USB femelle pour connecter l’Arduino Nano.

# II- **Conception informatique**

Nous utiliserons la bibliothèque Adafruit_TCS34725.

Après avoir initialisé la led et le capteur, nous lisons les valeurs reçues par celui-ci.

Grace à la bibliothèque fournie, nous obtenons directement une plage de valeurs pour chaque couleur RGB.

Il est donc possible de les analyser pour les associer à différentes couleurs puis d’allumer la led en conséquence.

# III-	Rendu final

Cube par impression 3D

![ezgif com-gif-maker (3)](https://user-images.githubusercontent.com/92324336/162565028-0c61ff43-6069-46dd-a492-a36b21879c76.gif)

# ColorDetection
Leds qui recopient la couleur détectée par un capteur

# **Objectif du projet**

L’objectif est de réaliser un cube translucide doté d’une led tricolore réagissant grâce à un capteur de couleur.

# I- **Conception électronique**

## a) Led tricolore

Nous utiliserons une led RGB à anode commune pour pouvoir obtenir une vaste plage de couleurs. Nous la connectons à 3 pins digitaux d’une Arduino Nano puis au GND.

## b) Capteur de couleur

Le capteur utilisé est le tcs34725. Afin de transmettre ses données sur notre carte, nous utilisons le protocole I2C grace aux pins SCL et SDA.

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

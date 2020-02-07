### IM - Digital Trends - Heig-VD
# VR Tech - Etat de l'art      
      
### Sommaire
- [Les applications actuelles et futures de la VR](#application-vr)
- [Historique](#histo)
- [Le matériel VR](#materiel)
- Exemples d'app à succès
- Immersion
- [Déplacements](#movements)
- Performances graphiques
- Audio
- Réflexion/discussion: UX et interfaces de jeux VR

## <a name="application-vr"></a>Applications de la VR

### Quelles applications à la VR ?

- Marketing
- Jeux vidéos
- Musées
- Prototypage
- Education/formation (médecine, ...)
- Télétravail
- Cinéma (animations)

#### La VR, un média qui englobe tous les autres ?

## <a name="histo"></a> Quelques exemples historiques

XIXe s. - [Peintures panoramiques](https://fr.wikipedia.org/wiki/Panorama_(peinture))

XIXe s. - [Stéréoscopes](https://fr.wikipedia.org/wiki/St%C3%A9r%C3%A9oscope)

1929 - [Link Trainer](https://en.wikipedia.org/wiki/Link_Trainer)

1939 - [View-Master](https://fr.wikipedia.org/wiki/View-Master)

1960 - Telesphere Mask, premier head-mounted display (HMD), Morton Heilig

![Telesphere](./img/telesphere.jpg)

1961 - Headsight, premier HMD avec motion tracking, par Comeau et Bryan

![Headsight](./img/headsight.png)

1962 - [Sensorama, Morton Heilig](https://en.wikipedia.org/wiki/Sensorama)

1968 - [The Sword of Damocles](https://en.wikipedia.org/wiki/The_Sword_of_Damocles_(virtual_reality)), premier dispositif VR, par Ivan Sutherland

![The Sword of Damocles](./img/sword.jpg)

1978 - [ASPEN MOVIE MAP](https://en.wikipedia.org/wiki/Aspen_Movie_Map), propotype de cartes interactives, par le MIT

![ASPEN MOVIE MAP](./img/aspen.jpg)

1990 - [NASA-VIEW (Virtual Interface Environment Workstation)](https://www.nasa.gov/ames/spinoff/new_continent_of_ideas), casque, gants et combinaison connectés

![NASA-VIEW](./img/nasaview.jpg)

1992 - [SEGA VR/R360](https://oculusnext.com/sega-vr/)

1995 - [Virtual Boy](https://en.wikipedia.org/wiki/Virtual_Boy)

2012 - [Oculus Rift](https://en.wikipedia.org/wiki/Oculus_Rift)

2014 - [Google Cardboard](https://en.wikipedia.org/wiki/Google_Cardboard)

 ...

## <a name="materiel"></a>Le matériel VR

### Degrés de liberté

3DOF: Three Degrees Of Freedom ou suivi de rotation

6DOF: Six Degrees Of Freedom ou suivi de position

### Systèmes de  suivi de position (*positional tracking*)

- Outside-in (Oculus camera ir, Valve lighthouse, ...)
- Inside-out tracking (simultaneous localization and mapping [SLAM](https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping))

[https://uploadvr.com/how-vr-tracking-works/](https://uploadvr.com/how-vr-tracking-works/)



### Contrôleurs et systèmes d'interaction VR
- Gaze contrôleur ?
- 3DOF contrôleur
- 6DOF contrôleur
- *Tracking* des doigts
- autres systèmes

### Casques autonomes versus casques reliés


### Casques populaires récents
| Casques             | Platforme  | 6DOF | Contrôleurs | Contrôleurs 6DOF |
|:--------            |----------:|:----:|:-----------:|:----------------:|
| HTC Vive Cosmos     | PC         | ✔️    | ✔️          | ✔️                |
| Oculus Rift S       | PC         | ✔️    | ✔️          | ✔️                |
| Oculus Quest        | Standalone | ✔️    | ✔️          | ✔️                |
| Oculus Go           | Standalone | ❌   | ✔️          | ❌               |
| Google Cardboard    | Android    | ❌   | ❌         | ❌                |
| Sony Playstation VR | Playstation| ✔️    | ✔️           | ✔️                |

# Quelques applications de références

- [Beat Saber](https://beatsaber.com/)
- Inclut: musique, espace, profondeur
- Sans textes, sans déplacements du joueur (ou légers)
- Dispo: Steam, oculus store, PS, Humble bundle
- [Google earth VR](https://www.youtube.com/watch?v=SCrkZOx5Q1M&feature=youtu.be)
- Interface intéressante: déplacer le soleil (jour/nuit)
- Pas de téléportation, on amène l'endroit choisi à soi

De manière générale, une application VR ne doit pas permettre de prendre le contrôle de la caméra. Problème: [mal du voyage ou motion sickness](https://en.wikipedia.org/wiki/Virtual_reality_sickness).

# Etat de l'art: Immersion

- Le [Field of view](https://vr-lens-lab.com/field-of-view-for-virtual-reality-headsets/) (FOV) n'est pas optimal sur les casques actuels
- le FOV des devices = en moyenne 90-110°
- le FOV humain = 200-220°

![Field of view](./img/fov.png)
[*Source*](https://fr.wikipedia.org/wiki/Champ_visuel#/media/Fichier:Champ_vision.svg)

## Le casque (gênant, lourd)
- Deep Diving: jeu de plongée VR - détourne ce problème
- https://store.steampowered.com/app/1104050/Deep_Diving_VR/

## [Screen Door Effect (SDE)](https://www.howtogeek.com/404491/what-is-the-screen-door-effect-in-vr/)
- L'effet: on voit le "grillage" de pixels
- Cause: zoom sur l'écran dans le headset, en plus du fait qu'il est proche des yeux
- Solution: meilleure résolution de l'écran (8K)

![Screen Door Effect](./img/sde.jpg)
[*Source*](https://en.wikipedia.org/wiki/Screen-door_effect#/media/File:Screen-door_effect.jpg)


## [Mura Effect](https://www.roda-computer.com/technology/mura-effect/)
- L'effet: les à-plats de couleurs ne sont pas homogènes
- Cause: la composition des écran empêche une luminosité tout à fait régulière

![Screen Door Effect](https://external-preview.redd.it/lmskdQbKiWAh14j5dxhCPn-iLTx_uBkHcwZksUQz328.jpg?auto=webp&s=93735d53c775da1b0702cb0fa8126363426f9d53)

##  [Aliasing](https://fr.wikipedia.org/wiki/Anticr%C3%A9nelage)
- L'effet: les arrondis sont saccadés
- Cause: les pixels sont carré, les courbes sont pas possible sur écran
- Anti-aliasing: technique  d'"anticrénelage" (FR) pour lisser les courbes et diagonales, grâce au flou

![Aliasing](https://upload.wikimedia.org/wikipedia/commons/2/24/Antialiasing_comparaison.gif)

## [Glare ou God rays](https://3dinsider.com/vr-lenses/)
- L'effet: En cas de forts contrastes, ça "bave". On voit les rayons lumineux.
- Cause: Les lentilles dans le casques.
- Solution: limiter les forts contraste dans le design du jeu/de l'app.

![Glare](http://i.vimeocdn.com/video/569557579_1280.jpg)

# <a name="movements"></a>Déplacements

## Principales problématiques

- Mal des transports ( *cinétose* ) lorsque le déplacement visualisé est décalé de celui contrôlé par l'utilisateur.
 
- L'espace réel est souvent restreint à une petite partie d'une pièce, souvent entre 1 et 3 [m^2] alors que l'espace virtuel est d'une taille quelconque. 

- L'espace réel peut contenir des obstacles aux déplacements qui seront invisibles en VR. Et inversement, une chaise dans la réalité virtuelle ne sera peut être pas physiquement présente dans la réalité.

## Mal des transports (cinétose)

Une des principales règles pour éviter ce problème et de ne jamais prendre le contrôle de la caméra et donc de la laisser être contrôlée par les mouvements du casque VR. 

Si l'on veut tout de même déplacer l'avatar de l'utilisateur (et donc sa caméra) dans la VR sans que celui-ci se déplace dans la réalité, il va falloir trouver des "trucs" pour le faire de la manière la plus confortable possible.  Le critère de **confort** se retrouve d'ailleurs dans la plupart des magasin d'application VR (par ex. dans [l'oculus store](https://support.oculus.com/1639053389725739/)). Voilà quelques exemples de solutions :

###  La téléportation

Elle ne provoque généralement pas d’inconfort, mais elle peut casser l’immersion si elle n'est pas *scénarisée* dans l'application. C'est la solution la plus utilisée dans les applications VR d'aujourd'hui. On la retrouve sous différentes variantes dont voici quelques exemples concrets:

 - **Téléportation simple**:  l'avatar est simplement téléporté vers la destination. Elle est souvent soit **libre**: l'utilisateur choisit sa destination pour la téléportation dans l'espace VR visible (et accessible), soit **limitée**: par une série de marqueurs de téléportation disposés dans l'espace VR. La téléportation limitée est souvent utilisée lors de l'utilisation de la  [photogrammétrie](https://fr.wikipedia.org/wiki/Photogramm%C3%A9trie). L'application [Welcome to Light Fields](https://www.blog.google/products/google-ar-vr/experimenting-light-fields/) en est un bon exemple. En effet puisque l'espace VR n'est pas pleinement explorable (ce sont des *photos*), l'utilisateur se téléporte alors d'un point de vue à un autre, où les points de téléportation sont les endroits ou les *photos* ont été prises.
 
 - **Portails de téléportation**:  au lieu de téléporter l'utilisateur, on le fait passer à travers des portails reliant deux zones VR distantes. Ces portails peuvent être soit fixés par les créateurs de l'application, soit par l'utilisateur lui-même (à la manière du jeu Portal) .
 - 
 ### Flou basé sur le champ de vision (FOV) 

Toutefois, et même si l'espace VR est plus grand que l'espace réel, il existe d'autres méthodes pour éviter de devoir déplacer la caméra de l'utilisateur:

- Utiliser des **véhicules**: l'utilisateur reste sur place en réalité, c'est le véhicule qui se déplace dans le virtuel.


- **Le chaperon**: faire des murs virtuels quand y a des murs en realité. Mais qu'en est-il pour les mondes infinis ?

- **[Rediect walking](https://www.youtube.com/watch?v=u8pw81VbMUU)**: fausser la perception de l'esprit avec un décalage mouvements réels/virtuels.
- **Suites de mouvements adaptées à l'univers**, pensés pour que l'utilisateur revienne sur ses pas, et reste dans un espace restreint.

### Différentes solutions (suite)
- **Overlapping** des salles pour fausser l'esprit: jeu des distances. Difficile pour le cerveau de se représenter les distances.

![Overlapping](./img/overlapping.png)

### Différentes solutions (suite)

- **Tapis VR**: permet le déplacement infini. Le problème: ils sont dangereux, besoins de harnais, ou d'une sécurité de soutien.

![Overlapping](https://i.pinimg.com/originals/86/51/71/8651710cd1970bc5c5d6892064fcc03b.jpg)


# Etat de l'art: Performances graphiques
L'idéal serait d'avoir une résolution min. de 8k, avec un FOV de 180°, et une fréquence min. de 90Hz

Le problème: les cartes graphiques actuelles ne le permettent pas.

**Quelques solutions:**
- **[Le foveated rendering](https://en.wikipedia.org/wiki/Foveated_rendering)**: on améliore le centre de l'image, et de moins en moins en plriphérie de la vision pour réduire le temps de calcul. Avec du eye-tracking intégré aux casque cela pourrait être d'autant plus performant. 
- **[Asynchronous interleaved reprojection](https://en.wikipedia.org/wiki/Asynchronous_reprojection)**: des images sont chargées, puis adaptées avec les informations de mouvements du casque. 

Voir: [Google light field](https://www.blog.google/products/google-ar-vr/experimenting-light-fields/)
et [Light-field camera](https://en.wikipedia.org/wiki/Light-field_camera)

# Etat de l'art: le son en VR
## Le son en VR est positionnel, donc également en 3D.
En savoir plus: [VR positional Audio](https://realnewworld.com/vr-positional-audio/)

# Réflexion/discussion:
## UX/interface de jeux VR, quelles problématiques?

# Sources
- [Virtual Reality Society](https://www.vrs.org.uk/virtual-reality/history.html)
- [Geek.com](https://www.geek.com/news/the-history-of-virtual-reality-games-1652225/)
- [Changing the world: DARPA’s top inventions](https://www.extremetech.com/extreme/105117-inventing-our-world-darpas-top-inventions/2)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMDYyOTUxNjAsLTE5Nzk0ODYwMzksLT
IxMTkzMzgwMDQsNTUxNzU4NTY0LC0xMjg1NTczMzAyLDQ2NjM0
OTU1NCwtMjgwOTQwOTUwLDY3NjM0OTI3OSwxODA1MzA0Njg1LD
EzNjExMzUzNzUsMTc5MDE3NDcwNSwtMTMxMjI4ODE1MywtMTg1
NzkyMTU4OSwxNTcxMzIwMDgzLC0xNjAxNjA3MjY2LC0xOTUzNT
g0MTE3LC04MDU1MzA4OTgsLTE4ODQzODI4MDEsMjAyMzU3NDI4
MCwxODc4NzczMTRdfQ==
-->
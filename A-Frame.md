### Réalité Virtuelle - Digital Trends - IM - Heig-VD

# A-Frame : un hub VR multi-utilisateurs 

## Objectifs

- Savoir intégrer des technologies Web pour la réalisation d’une expérience VR multi-utilisateurs.
- Réaliser une application accessible via une multitude de périphériques (*responsive*).
-  S'initier au framework A-Frame et à l'architecture [Entity–component–system](https://aframe.io/docs/1.0.0/introduction/entity-component-system.html) (ECS).

## Contenu

Pour atteindre ces objectifs, nous allons développer un *Hub VR* multi-utilisateurs. Ce *hub* servira de porte d'entrée vers les projets individuels que vous développerez durant la dernière partie du cours. Il se présentera  sous la forme d'une mini expérience VR mettant en pratique les concepts de base du framework A-Frame. On y verra (entre autre) comment: 
- déplacer l'avatar de l'utilisateur (en évitant la *cinétose*)
- offrir des possibilité d'interaction avec l'environnement
- animer et déclencher des animations en fonction d'événements
- gérer les collisions pour la navigation
-  importer des *asset* 3D (*mesh*)
-  créer des *mesh* avec [three.js](https://threejs.org/) (le framework sous-jacent à A-Frame) 
- étendre le framework A-Frame via l'architecture ECS
- synchroniser des entités entres les clients connectés

## Mise en place

La version 1.0.4 du *framework* [A-Frame](https://aframe.io/docs/1.0.0/introduction/) sera utilisée. Vous pouvez donc simplement la rajouter dans votre code HTML de base (ou utiliser une des autres méthodes proposée dans la documentation officielle).

Ajoutez aussi [Aframe-Extras](https://github.com/donmccurdy/aframe-extras) à votre projet, puisque nous utiliserons certaines des fonctionnalités offertes par cet ensemble de composants.

Pour vérifier que tout fonctionne, ajouter les balises HTML nécessaires à l'affichage d'un [océan](https://github.com/donmccurdy/aframe-extras/tree/master/src/primitives) (qui servira d'environnement de base au hub VR) et tester le tout dans votre browser. Vous devriez obtenir un résultat proche de celui ci: [https://vr.chabloz.eu/ocean_base.html](https://vr.chabloz.eu/ocean_base.html).

## Environnement

### L'océan

L'océan actuelle est un peu simple, mais nous pouvons le rendre plus plaisant en faisant quelques retouches. Premièrement, agrandissez  sa taille pour qu'il couvre 100 [m^2] (toutes les distances dans A-Frame sont en **mètre** et les angles en **degré**). Ensuite, la mer est un peu trop agitée pour notre scène. Essayez donc de modifier les attributs nécessaires pour obtenir un océan plus calme (par exemple: vous pouvez réduire l'amplitude des vagues de base à 0 et leur variance à  0.1). Vous remarquerez ainsi la facilité de paramétrage des composants A-Frame grâce à l'utilisation des attributs HTML. Pour un effet intéressant, vous pouvez aussi dupliquer votre balise océan et modifier l'amplitude et la variance  du second océan. Mais bien sûr la performance sera moins bonne. Puisque nous voulons que notre scène tourne sur le plus grand nombre de périphériques, il serait utile de pouvoir la *monitorer*. A-Frame l'inclut grâce au composant [stats](https://github.com/aframevr/aframe/blob/master/docs/components/stats.md) (que vous pouvez ajouter dés maintenant). Vous trouverez des bonnes pratiques pour l'optimisation des performances ici: [A-Frame best practices](https://github.com/aframevr/aframe/blob/master/docs/introduction/best-practices.md#performance). Nous allons suivre le plus possible ces recommandations durant le développement du *hub*.  

### Le ciel

A-Frame offre le composant  [background](https://github.com/aframevr/aframe/blob/master/docs/components/background.md) afin de facilement fixer une couleur de base pour la scène. Il existe aussi un composant [a-sky](https://github.com/aframevr/aframe/blob/master/docs/primitives/a-sky.md) qui permet d'utiliser une image [cylindrique équidistante](https://fr.wikipedia.org/wiki/Projection_cylindrique_%C3%A9quidistante) comme texture intérieure pour une sphère englobant la scène. Puisque notre scène est destinée à tourner aussi sur des périphériques de faible puissance graphique, la première solution sera utilisée.

### La lumière

A-Frame ajoute par défaut une lumière d'ambiance et une lumière directionnel via le composant [light](https://github.com/aframevr/aframe/blob/master/docs/components/light.md). Vous pourriez vous contenter de ces lumières par défaut mais, pour rendre notre scène plus personnalisée, remplacez les par des lumières en accord avec le choix de couleur que vous avez fait pour votre ciel.

### Le brouillard

Afin de camoufler les bords abruptes de l'océan, vous pouvez ajouter un brouillard grâce au composant [fog](https://github.com/aframevr/aframe/blob/master/docs/components/fog.md). Voilà un exemple d'environnement obtenu après ces quelques retouches: [https://vr.chabloz.eu/ocean_quiet.html](https://vr.chabloz.eu/ocean_quiet.html)

## Pavage hexagonal

Afin de s'initier à **three.js**, le *framework* utilisé par A-Frame pour la gestion de la 3D, nous allons ajouter un nouvelle [primitive](https://aframe.io/docs/1.0.0/introduction/html-and-primitives.html) pour la création des [mesh](https://fr.wikipedia.org/wiki/Mesh_(objet)) nécessaires à un [pavage hexagonal](https://fr.wikipedia.org/wiki/Pavage_hexagonal).

Avant de commencez cette partie, il est fortement recommandé de lire cet excellent support sur l'utilisation du pavage hexagonal: [https://www.redblobgames.com/grids/hexagons/](https://www.redblobgames.com/grids/hexagons/).

Afin de simplifier la chose, nous allons nous limiter à une carte en forme d’hexagone pavé d'hexagones à sommet plat en utilisant le système des coordonnées cubiques.


### Enregistrement de la primitive et du composant

Suivez la documentation officielle pour rajouter une primitive et le composant associé nécessaire au pavage hexagonal. Pour les attributs de la primitive, implémentez au minimum les suivants:

- **size**:  la taille du pavage. Une taille de 1 signifie un seul hexagone, une taille de 2 signifie un héxagone au centre et les 6 qui l'entoure et ainsi de suite. Voila un exemple pour la taille 4: 

![Pavage hexagonal de taille 3](./img/hexagone-3.png)

- **color**: la couleur des tuiles hexagonale .
- **cellsize**: la taille des tuiles.
- **height**: la hauteur des tuiles.






<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY0NjkwNzAxNiwxODQ2MDk2MDUzLC01NT
kxNTgxMjgsMzcxNTA4ODkyLC04NDEyNzI1NTEsLTExOTA0NTcw
MDgsLTIxMjkwNzczNDcsODY4Njg0NDc2LC0xMjQwMzkwOTIwLC
0xOTIyNTQwNDAwLC0zNDE1MTU0MjMsOTY0OTQ4NzMwLC01NTk4
NjU1MDEsMjA0MjU5MDA4MiwtMTc5OTM1MDczOCwtODcxMzc4Nz
AsNTU4ODk5ODAyLC0xNDA3MjUxMDkxLC0xNjM1MDkyMzA1LC03
NzEzMzQ4MzZdfQ==
-->
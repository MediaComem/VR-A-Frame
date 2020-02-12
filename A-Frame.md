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

Pour faire un premier test, vérifiez que tout fonctionne en ajoutant les balises nécessaires à l'affichage d'un [océan](https://github.com/donmccurdy/aframe-extras/tree/master/src/primitives) (qui servira d'environnement de base au hub VR)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTYwNzA0MzI4NCwtMTYzNTA5MjMwNSwtNz
cxMzM0ODM2LC03NzM3MjUxNzAsMTAzNTIwNzgzNSwtMTI4ODI4
MjQwLC0yMDk4ODg4Njk5LC0xNzcyODQ4NTUwLDc0MjcxOTM3MC
wxOTcyMTI2OTk4XX0=
-->
### Réalité Virtuelle - Digital Trends - IM - Heig-VD

# A-Frame : Hub VR multi-utilisateurs 

## Objectifs

- Savoir intégrer des technologies Web pour la réalisation d’une expérience VR multi-utilisateurs.
- Réaliser une application accessible via une multitude de périphériques (*responsive*).
-  S'initier au framework A-Frame et à l'architecture [Entity–component–system](https://aframe.io/docs/1.0.0/introduction/entity-component-system.html) (ECS).

## Contenu

Pour atteindre ces objectifs, nous allons développer un *Hub VR* multi-utilisateurs. Ce *hub* servira de porte d'entrée vers les projets individuels que vous développerez durant la dernière partie du cours. Il se présentera  sous la forme d'une mini expérience VR mettant en pratique les concepts de base du framework A-Frame. On y verra (entre autre) comment: 
- déplacer l'avatar de l'utilisateur (en évitant la *cinétose*)
-  interagir avec l'environnement VR, synchroniser des entités entres les clients connectés
- animer et déclencher des animations en fonction d'événements
- gérer les collisions pour la navigation
-  importer des *asset* 3D (*mesh*)
-  créer des *mesh* avec [three.js](https://threejs.org/) (le framework sous-jacent à A-Frame) 
- Étendre le framework A-Frame via l'architecture ECS

## Mise en place

La version 1.0.4 du *framework* [A-Frame](https://aframe.io/docs/1.0.0/introduction/) sera utilisé. Vous pouvez donc simplement la rajouter dans votre code HTML de base ou utiliser une des autres méthodes proposée dans la documentation officielle.

Ajoutez aussi [Aframe-Extras](https://github.com/donmccurdy/aframe-extras) à votre projet, puisque nous utiliserons certaines des extensions du *framework* A-Frame offert par cet ensemble de composants.

Pour faire un premier test, vérifiez que tout fonctionne en ajoutant les balises nécessaires à l'affichage d'un océan (qui servira de 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2Nzg1NjAwMjEsLTc3MzcyNTE3MCwxMD
M1MjA3ODM1LC0xMjg4MjgyNDAsLTIwOTg4ODg2OTksLTE3NzI4
NDg1NTAsNzQyNzE5MzcwLDE5NzIxMjY5OThdfQ==
-->
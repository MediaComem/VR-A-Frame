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

L'océan actuelle est un peu simple, mais nous pouvons le rendre plus plaisant en faisant quelques simples retouches. Premièrement, agrandissez  sa taille pour qu'il couvre 100 [m^2] (toutes les distances dans A-Frame sont en **mètre** et les angles en **degré**). Ensuite, la mer est un peu trop agitée pour notre scène. Réduisez donc l'amplitude des vagues de base à 0 (attribut *amplitude*) et leur variance à  0.1


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTg5OTU5NTY5NCw1NTg4OTk4MDIsLTE0MD
cyNTEwOTEsLTE2MzUwOTIzMDUsLTc3MTMzNDgzNiwtNzczNzI1
MTcwLDEwMzUyMDc4MzUsLTEyODgyODI0MCwtMjA5ODg4ODY5OS
wtMTc3Mjg0ODU1MCw3NDI3MTkzNzAsMTk3MjEyNjk5OF19
-->
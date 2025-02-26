---
lang: fr
---

## Tâches:

- Concevoir et modéliser la base de données
- Développer le backend et le traitement de requêtes
- Implanter l'authentification d'usagers avec validation et encryption des mots de passes
- Gérer les différents modes d'accès correspondants aux rôles d'usagers
- Développer un système de code d’accès permettant la création de comptes
- Implanter l'interface graphique des étiquettes et des résultats de séquençage
- Développer le panneau d'administration
- Performer les tests avec différents cas d'utilisation

## Rapport:

### 19 Mai - 15 Juin 2022

Durant ce mois, plusieurs concepts ont été discutés lors des réunions avec l'École En Réseau et Génome Québec tel que l'utilisabilité et les fonctionnalités de l'application pour cerner l'ampleur et les besoins du projet.

Ont suivi des réunions avec l'équipe de développement du DIRO afin de discuter les technologies qui pourraient être utilisées pour le développement de l'application. Il a été décidé d'utiliser React pour implanter l'interface utilisateur. J'ai donc suggéré d'utiliser le [MERN Stack](https://www.mongodb.com/mern-stack) qui fournit tous les outils nécessaires à l'élaboration du projet utilisant un seul langage de programmation: JavaScript.

- [MongoDB](https://www.mongodb.com/) : Base de données NoSQL
- [Express](https://expressjs.com/) : Librairie JS côté serveur
- [React](https://reactjs.org/) : Librairie JS côté client
- [Node.js](https://nodejs.org/) : Serveur Web pour JavaScript

![MERN stack](https://webimages.mongodb.com/_com_assets/cms/mern-stack-b9q1kbudz0.png?auto=format%2Ccompress)

### 16 Juin - 10 Juillet

Durant cette période, on a convenu qu'on allait utiliser l'architecture [MVC](https://fr.wikipedia.org/wiki/Mod%C3%A8le-vue-contr%C3%B4leur) (Modèle-vue-contrôleur) et décidé du modèle de données dont on allait avoir besoin. Suite à quoi, j'ai:

- Créé un compte et une base de données MongoDB
- Conçu individuellement le [modèle de données](/projet-IFT3150/extra/diagramme.html) et créé les collections correspondantes

![ER diagram](https://i.imgur.com/Z6rUILV.png)

- Implanté les champs correspondant au modèle de données avec l'interface Mongoose en tenant compte de leur types et contraintes
- Développé et tester le traitement des requêtes pour les endpoint spécifiques à l'inscription et l'identification des usagers
- Traité la validation et les différents cas d'utilisation de l'authentification

## 11 Juillet - 6 Août 2022

Pendant cette période, j'ai:

- Développé la gestion des requêtes dans le backend pour performer les opérations [CRUD](https://fr.wikipedia.org/wiki/CRUD) sur les usagers et les markers
- Implanté le contexte d'authentification et mis à jour l'état correspondant au plus haut niveau de l'application pour stocker les données de l'usager identifié dans le storage du navigateur
- Implanté l'envoi de requêtes par les formulaires d'authentification et adapté quelques composantes à ce contexte
- Restructurer le code pour l'intégrer à l'architecture MVC


## 7 Août - 21 Août 2022

Pendant cette période, j'ai:
- Rajouté les codes de réponse HTTP aux traitement des requêtes
- Implanté l'envoi de requêtes pour le chargement des étiquettes de la base de donnée et leur affichage sur la carte
- Implanté l'envoi de requêtes pour l'ajout, la modification, la suppression des marqueurs et leur sauvegarde dans la base de données
- Rajouté l'interface graphique pour la visualisation des données d'une étiquette, sa modification et suppression
- Rajouté l'interface graphique et l'envoi de requêtes pour l'ajout des résultats d'analyses d'un échantillon et leur visualisation
- Adapté les opérations CRUD permises sur les étiquettes selon le type d'usager (élève, enseignant ou admin)
- Implanté l'assignation du rôle et CSS/École/Classe de l'usager avec un système de code d'accès généré par l'administrateur
- Travaillé sur divers élèments de l'interface utilisateur
- Créé les icones de Mission ADN-eau pour les utiliser comme marqueurs si besoin
- Établi un code de couleur pour les marqueurs selon leur type 

## 22 Août - 30 Août 2022

Pendant cette période, j'ai:
- Développé le panneau d'administration
- Implanté la gestion des permissions selon le type d'usager
- Implanté les modifications suggérées lors de la réunion avec Génôme Québec
- Travaillé sur divers composantes de l'interface graphique




# React-express-app

##### Prérequis pour contribuer au projet:
- Git
- Node.js

Vous pouvez les installer directement de leurs sites.

##### Récuperer le projet:
```bash
     git clone https://github.com/cjeanm11/projet-IFT3150.git
```

##### Installation des dépendances du projet:
```bash
     cd project-IFT3150
     make install
```


#### Lancer ces commandes powershell/bash dans la racine du projet pour déparer l'application dans votre environnement locale:

##### Démarrer les serveurs sur http://localhost:3000 :
```bash
     make start
```

##### Arréter les serveurs:
```bash
     make stop
```

##### Démarrer le serveur front-end sur le port 3000:
```bash
     make start-fe
```

##### Démarrer le serveur back-end sur le port 5000:
```bash
     make start-be
```


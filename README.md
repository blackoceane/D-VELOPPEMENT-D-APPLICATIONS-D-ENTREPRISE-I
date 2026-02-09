# DEVELOPPEMENT-D'APPLICATIONS-D'ENTREPRISE-I

## Description du projet
Ce projet final consiste en une application de gestion commerciale complète développée en C# / WPF utilisant une architecture DataService. 
L'objectif est de gérer le cycle de vie des commandes clients, incluant la sélection de produits, le calcul des totaux et la synchronisation avec une base de données relationnelle. Le système implémente une relation Parent/Enfant complexe entre les Commandes et les ComProds (produits commandés).

## Fonctionnalités

 ### Gestion des Commandes (CRUD)
- **Cycles complets** : Création, modification et suppression de commandes.
- **Auto-initialisation** : Dates automatiques et remise à zéro des totaux à l'ouverture.
- **Nettoyage intelligent** : Suppression en cascade des produits liés lors de la destruction d'une commande.

 ### Gestion des Produits (Items)
 - **Sélection dynamique** : Ajout de produits depuis une liste avec récupération automatique du prix.
 - **Édition flexible** : Ajustement direct des quantités et des prix dans le DataGrid.
 - **Suivi des retraits** : Gestion d'une liste ComProdsToDelete pour synchroniser la base de données.

  ### Interface Utilisateur 
  - Utilisation de ComboBox pour la sélection rigoureuse du Client et du Vendeur.
  - DataGrid synchronisé pour l'affichage en temps réel des produits ajoutés.
    
## Objectifs
- **Architecture Parent/Enfant** : Maîtriser les relations Commande ↔ ComProd.

- **Pattern DataService** : Centraliser les transactions SQL.

- **Validation** : Garantir la présence d'un client, d'un vendeur et d'au moins un produit

## Problèmes connus & Limites

- **Conception & Modélisation** : Difficultés de compréhension et d'application du MRD (Modèle Relationnel de Données) pour les relations complexes.

- **Base de Données** : La suppression en cascade (Cascade Delete) n'a pas été implémentée avec succès ; un nettoyage manuel ou des contraintes SQL restent à affiner.

- **Logique métier** :

L'exécution du calcul automatique des totaux présente des instabilités lors de la sauvegarde.

Difficulté de conception technique pour la liste de sélection des produits.

- **Manque** : Absence de la fonctionnalité d'historique financier du client ($ cumulé).

  ---------------------------------------------------------------------------------------------
  CONÇU LE 01 MAI 2025 - 20 MAI SO25
   

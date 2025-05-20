
#  TP – Gestion de Films avec Spring Boot

##  Objectif

L'objectif de ce TP est de développer une application web permettant de gérer un catalogue de **films** classés par **catégories**, en utilisant **Spring Boot** et le moteur de templates **Thymeleaf**.  
Vous devrez structurer votre application selon une **architecture clean** et séparer les responsabilités à travers des couches bien définies.

##  Modèle de données

L’application reposera sur deux entités principales :

### Film
- `id` : identifiant unique
- `titre` : titre du film
- `photogramme` : photogramme du film (à stocker comme vous voulez)
- `description` : résumé ou synopsis
- `dateDeSortie` : date de sortie du film

###  Catégorie
- `id` : identifiant unique
- `nom` : nom de la catégorie (Action, Comédie, Drame…)
- `description` : description de la catégorie

:warning: Les deux entités seront liées par une relation many-to-many :warning:

##  Fonctionnalités attendues

L’application devra permettre les opérations suivantes :

### Films
- Afficher la liste des films
- Ajouter un film
- Modifier un film existant
- Supprimer un film
- Voir le détail d’un film, incluant le nom des catégories auxquelles il est rattaché

### Catégories
- Rien, pas de CRUD pour cette partie, tout sera initialisé directement au lancement de l'application ou dans un script SQL exécuté au lancement

##  Contraintes techniques

- Utilisation de **Spring Boot** (version stable recommandée : dernière LTS)
- Utilisation de **Thymeleaf** pour les vues (ou autre s'il y en a un que vous connaissez mieux)
- Utilisation de **Spring Data JPA** et d’une base H2 ou PostgreSQL
- Application du modèle **DTO/Mapper** pour découpler les entités et les vues
- **Services abstraits** via des interfaces, pas d'accès aux **Repositories** directement depuis les **Controlleurs**
- Utilisation de Bootstrap / Tailwind ou d’un CSS simple pour rendre les pages lisibles (pas de design complexe attendu)

## Critères de réussite

- Structure du projet claire et respectant l'architecture demandée
- Fonctionnalités CRUD demandées opérationnelles
- Séparation des responsabilités effective
- Application fonctionnelle et agréable à utiliser
- Code propre et lisible

## Critères d'échec
- Vous avez copié ou partagé votre projet
- Vous avez tout fait avec une IA et ça se voit
- Vous n'avez pas suivi les instructions
- Vous n'avez pas livré votre projet à l'heure

## Livrables attendus

- Le code du projet complet sur un dépôt Github suivant **avant minuit  : [sur ce dépôt](https://classroom.github.com/a/O96KBHYS)**
- Un fichier `README.md` qui contiendra :
  - Une capture d'écran de l'interface
  - Les instructions pour exécuter l'application

:warning: Aucune fonctionnalité non demandée ne doit être réalisée :warning:

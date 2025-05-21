
# TP – API REST pour la gestion de films et de catégories

## Objectif

Dans la continuité du projet de gestion de films réalisé avec Spring Boot et Thymeleaf, vous allez désormais développer une **API REST** permettant d'exposer et de manipuler les entités `Movie` et `Category` à distance.  
L’accent sera mis sur la **propreté du code**, le **respect des conventions REST**, le **traitement explicite des erreurs**, et la **qualité des tests** via des outils comme **Postman** ou **Bruno**.

## Ressources REST

### Ressources *collection*
- `GET /api/movies` : liste tous les films
- `POST /api/movies` : ajoute un nouveau film
- `GET /api/categories` : liste toutes les catégories
- `POST /api/categories` : ajoute une nouvelle catégorie

### Ressources *singleton*
- `GET /api/movie/{id}` : récupère un film par son identifiant
- `PUT /api/movie/{id}` : met à jour complètement un film
- `PATCH /api/movie/{id}` : met à jour partiellement un film
- `DELETE /api/movie/{id}` : supprime un film

Même logique pour `/categorie/{id}`.

## Contraintes techniques

### Gestion des erreurs
- Chaque appel doit retourner un **code HTTP explicite** :
  - 200 / 201 / 204 pour les succès
  - 400 pour une requête invalide
  - 404 si l'entité demandée n'existe pas
  - 409 en cas de conflit (doublon, etc.)
- Aucune **erreur 500** ne doit être retournée à cause d’un oubli de traitement.
- Chaque réponse d’erreur doit être accompagnée d’un **message clair** indiquant l’origine du problème.

###  Interdiction
- **Pas de HATEOAS / HAL** : ne pas inclure d’objets `_links` ou de relations automatiques dans les réponses.

## Tests automatisés

Vous devez tester **l’ensemble des cas d’utilisation** de votre API via **Postman** ou **Bruno**.  
Les tests devront pouvoir être **enchaînés automatiquement** grâce à l’utilisation de **variables d’environnement**.

### Scénario de test complet
1. **Création (POST)** d’une catégorie, puis d’un film lié à cette catégorie
2. **Mise à jour (PUT/PATCH)** de ces entités
3. **Consultation (GET)** pour vérifier les modifications
4. **Suppression (DELETE)** et vérification de leur non-existence
5. **Cas d’erreurs** (liste non exhaustive) :
   - Lecture/suppression d’un ID inexistant
   - Création avec données incomplètes
   - Mise à jour d’une entité inexistante

### Consignes pour les tests
- Chaque test doit **vérifier a minima le code HTTP retourné**
- La suite de tests doit être **documentée** dans le fichier `README.md` :
  - Comment l’exécuter correctement
  - Précision sur l’ordre d’exécution
  - Variables d’environnement utilisées

## Éléments évalués

✔️ Couverture des cas de test
✔️ Robustesse des traitements et gestion des erreurs
✔️ Lisibilité et qualité du code
✔️ Cohérence des codes HTTP retournés
✔️ Rigueur dans l’organisation des scénarios de tests

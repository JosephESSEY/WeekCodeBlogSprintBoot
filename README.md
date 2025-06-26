# API Blog Personnel - Spring Boot

## Description

Cette API Spring Boot fournit un système complet de gestion de blog personnel comprenant :

* gestion des utilisateurs avec authentification JWT
* gestion des articles
* gestion des catégories
* gestion des commentaires
* pagination
* recherche textuelle

Elle est développée avec **Spring Boot** et **Spring Data JPA** (ORM).

---

## Fonctionnalités

* Authentification sécurisée via JWT
* CRUD complet sur les articles
* CRUD complet sur les catégories
* Ajout, édition, suppression de commentaires
* Pagination des articles
* Recherche plein texte sur les titres et le contenu
* Gestion des rôles utilisateurs (`ADMIN`, `AUTHOR`, `READER`)

---

## Stack technique

* Java 17+
* Spring Boot 3.x
* Spring Security
* Spring Data JPA
* JWT
* PostgreSQL ou MySQL

---

## Installation

1. **Cloner le dépôt**

```bash
git clone https://github.com/votre-utilisateur/api-blog-springboot.git
cd api-blog-springboot
```

2. **Configurer la base de données**
   Dans `src/main/resources/application.properties` :

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/blogdb
spring.datasource.username=postgres
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

3. **Configurer la clé JWT**
   Toujours dans `application.properties` :

```properties
jwt.secret=YOUR_SECRET_KEY
jwt.expiration=3600000
```

4. **Construire le projet**

```bash
./mvnw clean install
```

5. **Lancer le projet**

```bash
./mvnw spring-boot:run
```

---

## Endpoints principaux

* `POST /api/auth/register` : inscription d’un utilisateur
* `POST /api/auth/login` : connexion d’un utilisateur
* `GET /api/articles` : liste des articles avec pagination
* `GET /api/articles/search?query=motcle` : recherche d’articles
* `GET /api/articles/{id}` : consulter un article
* `POST /api/articles` : créer un article
* `PUT /api/articles/{id}` : mettre à jour un article
* `DELETE /api/articles/{id}` : supprimer un article
* `GET /api/categories` : lister les catégories
* `POST /api/comments` : ajouter un commentaire
* `GET /api/articles/{id}/comments` : lister les commentaires liés à un article

---

## Tests

Lancer les tests unitaires et d’intégration :

```bash
./mvnw test
```

---

## Sécurité

* Authentification JWT sécurisée
* Filtres de sécurité avec Spring Security
* Validation des entrées via Spring Validation

---

## Contribuer

1. Forker le projet
2. Créer une branche
3. Soumettre une pull request

---

## License

MIT License

---

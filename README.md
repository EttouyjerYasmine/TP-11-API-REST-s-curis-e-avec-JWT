# TP Spring Security avec JWT

## 📖 Résumé pédagogique
Ce TP guide pas à pas la création d’une API sécurisée avec Spring Boot en utilisant Spring Security et JWT (JSON Web Token). L’objectif est de comprendre l’authentification et l’autorisation dans une application REST sécurisée.

## 🛠 Technologies et dépendances
- **Spring Boot 3+**  
- **Spring Security 6**  
- **Spring Web**  
- **Spring Data JPA**  
- **MySQL Driver**  
- **Lombok**  
- **jjwt** (JSON Web Token library)

## ⚙️ Fonctionnalités développées
1. Authentification en mémoire des utilisateurs.  
2. Génération et validation de JWT pour sécuriser l’accès aux endpoints.  
3. Utilisation de `permitAll()` pour l’authentification (`/api/auth/**`).  
4. Implémentation d’un `JWTFilter` pour vérifier les tokens avant le traitement des requêtes.  
5. Gestion des rôles et permissions via Spring Security.  
6. Configuration de la politique `SessionCreationPolicy.STATELESS`.  

## 🗂 Structure du projet
src/
└── main/
├── java/
│ └── ma.fstg.security/
│ ├── config/ # Configuration Spring Security
│ ├── controller/ # Endpoints REST
│ ├── model/ # Entités et modèles
│ ├── repository/ # Repositories JPA
│ ├── service/ # Services métiers
│ └── security/ # JWT et gestion de l’authentification
└── resources/
├── application.properties # Configuration DB et sécurité
└── data.sql # Données initiales*

## 🔑 Points importants
- Les tokens JWT ont une durée de validité de **1 heure** par défaut.  
- Les Refresh Tokens permettent de renouveler le JWT principal sans ressaisir les identifiants.  
- Toutes les communications doivent utiliser **HTTPS** pour sécuriser les tokens.  

## 🚀 Lancer le projet
1. Configurer la base MySQL dans `application.properties`.  
2. Importer le projet dans votre IDE (IntelliJ, Eclipse, VSCode).  
3. Exécuter la classe principale `Application.java`.  
4. Tester les endpoints avec Postman ou un autre client REST.  

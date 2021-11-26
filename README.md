# Symfony eCommerce SiteWeb
[Table des matières](#symfony-ecommerce-siteweb)
  - [Pré-requis](#pré-requis)
  - [Docker-compose](#docker-compose)
  - [MySQL Databases](#mysql-databases)
  - [Commande symfony](#commande-symfony)
  - [Bootstrap template](#bootstrap-template)
  - [Espace Utilisateurs](#espace-utilisateurs)
    - [Création de l'entité User()](#création-de-lentité-user)
    - [Création d'un formulaire d'inscription](#création-dun-formulaire-dinscription)
    - [Création d'un formulaire de connexion](#création-dun-formulaire-de-connexion)
    - [Création d'un espace privé (membre)](#création-dun-espace-privé-membre)

## Pré-requis
- PHP 7.2
- Composer
- Docker et Docker-compose (mailcatcher / mysql version 8.0)
- Symfony CLI

## Docker-compose 
- Plus d'info sur les commandes: `docker-compose`
- Lancer les containers du projet:`docker-compose up -d`
- Arrêter et supprimer les containers: `docker-compose down`
- Connection mysql: `docker-compose exec database mysql -u root --password=password`

## MySQL Databases
```
mysql> show databases;
mysql> use <nom table>;
mysql> show tables;
```

## Commande symfony
- Une fois le container démarré symfony se connecte automatiquement grâce aux variables d'environnement du container: `symfony var:export --multiline`

## Bootstrap template

template utilisé: [carousel](https://getbootstrap.com/docs/5.0/examples/carousel/)

## Espace Utilisateurs

### Création de l'entité User() et la migration dans la database 'laboutiquefrancaise'

```
symfony console make:user
> [User]
> [yes]
> [email]
> [yes]
> 
> symfony console make:migration
> symfony console d:m:m
```

### Création d'un formulaire d'inscription
### Création d'un formulaire de connexion
### Création d'un espace privé (membre)
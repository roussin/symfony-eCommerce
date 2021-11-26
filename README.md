[Symfony eCommerce SiteWeb](#symfony-ecommerce-siteweb)
  - [pré-requis](#pré-requis)
  - [Docker-compose](#docker-compose)
  - [MySQL Databases](#mysql-databases)
  - [Commande symfony](#commande-symfony)

## Pré-requis
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


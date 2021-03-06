# Painter Project

Découverte du framework Symfony au travers d'un projet concret.  
[Tuto Yoan Dev](https://www.youtube.com/watch?v=HViLTaLQ1AQ)

## Mise en place de Symfony

### Création d'un projet Symfony
```sh
symfony new NomDuProjet --full
```
*`--full` permet d'avoir toutes les options*

## Docker

### Création de la base de données

```sh
symfony console make:docker:database
```
Sous Windows:
[Installer docker](https://docs.docker.com/desktop/windows/install/)  
[Mise à jour du noyaux Linux](https://docs.microsoft.com/fr-fr/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)

Après confinguration du fichier `docker-compose.yml`, on peut effectuer les commandes suivantes:
```sh
docker-compose up -d
symfony serve -d
```
## Base de données

### Création d'une entité user

```sh
symfony console make:user
```
Puis répondre aux différentes questions

On peux ajouter des propriétés avec:
```sh
symphony console make:entity
```
... puis reprendre le nom d'entité *User*

### Migration

```sh
symfony console make:migration
```
Cette commande créée le fichier de migration. Il est possible, dans le return de la fonction *getDescription()*, de spécifier un nom à cette migration.

On termine par migrer vers la base de données grace à :
```sh
symfony console d:m:m
```

## Test

```sh
symfony console make:unit-test
```

Pour installer le package
```sh
php bin/phpunit
```

Pour lancer les tests:
```sh
php bin/phpunit --testdox
```

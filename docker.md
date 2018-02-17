Docker
======

## Docker Daemon config
Add the registries in Docker daemon config.
 
```
// Registries of University of La Rochelle
http://registry.univ-lr.fr:81
https://registry.univ-lr.fr:81
```

```
// Registry mirrors
http://registry.univ-lr.fr:81
```
## Access to remote docker container
### Get container
Get a docker container.
```
// University of La Rochelle container addres   -> registry.univ-lr.fr:81/iutlr-info/devbox
docker pull [container name] 
```

### Start local server
```
/**
 * My values
 * 
 * local path               -> C:\Users\Hp\Dropbox\IUTLR\WEB\CS
 * remote path              ->/var/www/html/www
 * ports                    -> 9998:80
 * my container name        -> devbox
 * Registry of La Rochelle  -> registry.univ-lr.fr:81/iutlr-info/devbox
 */

// Option 1
docker run -it --rm -v [local path:remote path] -p [port:port] --name [container name] [registry name]

// Option 2
docker run -it -v [local path:remote path] -p [port:port] --name [container name] [registry name]
```

### Connection to local server
```
/**
 * container name   -> devbox
 */
docker exec -it [container name] bash
```

### Type in your browser 127.0.0.1:[port] 
Create a php file in your local path to test your php server installation.
```php
<?php
    echo phpInfo();
?>
```

## Add PHPUnit
Add PHPUnit to your local project.

### Install wget
Update apt-get to download wget. wget will be used to download PHPUnit.
```
apt-get update
apt-get install wget
```

### Install PHPUnit
Install phpunit.phar and change the user privileges to move the file to your global usage. 
```
wget https://phar.phpunit.de/phpunit.phar
chmod +x phpunit.phar
mv phpunit.phar /usr/local/bin/phpunit
```

### See PHPUnit version
```
phpunit --version
```

### Add PHPUnit to your project
```
composer require --dev phpunit/phpunit
```

## Build docker containers from configuration files
### Go to configuration folder
```
// my configuration path    -> C:\Users\Hp\Dropbox\IUTLR\WEB\CS\docker-machine-pull
cd [configuration path]
```

### Check docker settings
* files sharing
* daemon

### Build environment
```
docker-compose build
```

### See docker images
```
docker images
```

### Stop containers
```
docker stop $(docker ps -a -q)
```

### Delete all containers
```
docker rm $(docker ps -a -q)
```

### Delete all images
```
docker rmi $(docker images -q)
```

### Start local server
```  
docker-compose up
```

### See docker containers
```
docker ps -a
```

### Connection to local server
``` 
/*
 * LPIRM containers
 * lpirm-dfs-apachephp
 * lpirm-dfs-mysql
 */
docker exec -it [container name] bash
```

## Installer FOS
Dans le conteneur PHP-Symfony, dans le dossier du projet :
```
composer require friendsofsymfony/rest-bundle "^2.1"
```

### Activer le bundle dans Sumfony en editant le fichier AppKernel
app/AppKernel.php

### Sérialisation des réponses par FOS
#### Activer le Serializer par default de Symfony
app/config/config.yml
```yaml
framework:
	serializer:
		enabled: true
```

#### Tester la configuration
```
php bin/console debug:config fos_rest
```

### Routage automatique
Voir les routes
```
php bin/console debug:router
```

cd var/lib/mysql

mysql -D cine -p

##
$cinema                         $salles
appBundle\Entity\Salle          appBundle\Entity\Cinema


Opération souhaitée                         Verbe HTTP      URI
- Récupérer toutes les salles d'un cinéma        GET         /cinemas/{id}/salles
- Récupérer une salle d'un cinéma                GET         /cinemas/{id}/salles/{id}
- Créer une nouvelle salle pour un cinéma        POST         /cinemas/{id}/salles
- Supprimer une salle d'un cinéma                DELETE         /cinemas/{id}/salles/{id}
- MAJ complète d'une salle d'un cinéma            PUT         /cinemas/{id}/salles/{id}
- MAJ partielle d'une salle d'un cinéma            PATCH         /cinemas/{id}/salles/{id}
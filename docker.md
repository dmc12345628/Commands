Docker
======

### Insecure registries:
```
http://registry.univ-lr.fr:81
https://registry.univ-lr.fr:81
```

### Registry mirrors:
```
http://registry.univ-lr.fr:81
```

### Ouvrez un terminal
```
docker pull registry.univ-lr.fr:81/iutlr-info/devbox
```

### Lancement du container Docker sous mac
```
docker run -it --rm -v C:\Users\Hp\Dropbox\IUTLR\WEB\CS:/var/www/html/www -p 9998:80 --name devbox registry.univ-lr.fr:81/iutlr-info/devbox
```

### Lancement du nouveau container
```
docker run -it -v C:\Users\Hp\Dropbox\IUTLR\WEB\CS:/var/www/html/www -p 9998:80 --name devbox registry.univ-lr.fr:81/iutlr-info/devbox
```

### Connexion au terminal du container Docker
```
docker exec -it devbox bash
```

### Testez sur un navigateur 127.0.0.1:9998
```php
<?php
echo phpInfo();
?>
```

### Installation de wget
```
apt-get update
apt-get install wget
```

### installation de phpunit
```
wget https://phar.phpunit.de/phpunit.phar
chmod +x phpunit.phar
mv phpunit.phar /usr/local/bin/phpunit
```

### Voir la version de phpunit
```
phpunit --version
```

### Intégrer phpunit en dev sur notre projet
composer require --dev phpunit/phpunit

### Entrer au repertoire qui contient les fichier de configuration
```
cd C:\Users\Hp\Dropbox\IUTLR\WEB\CS\docker-machine-pull
```

### Verifier les settings de docker
* files sharing
* daemon

### Construction de l'envirenement
```
docker-compose build
```

### Voir les images docker
```
docker images
```

### Construction de conteneurs pour les services
```  
docker-compose up
```

### Voir les conteneurs
```
docker ps -a
```

### Entrer dans le conteneur
``` 
docker exec -it lpirm-dfs-apachephp bash
```
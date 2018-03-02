Symfony
=======

## Create symfony project
```
composer create-project symfony/framework-standard-edition [nomproject]
// or
symfony new [nomproject] 3.1
```

### During installation
```
database_host (127.0.0.1): localhost
database_port (null):
database_name (symfony): [projectname]
database_user (root): root
database_password (null): mysql
mailer_transport (stmp):
mailer_host (127.0.0.1):
mailer_user (null):
mailer_password (null):
secret (ThisTokenIsNotSoSecretChangeIt):
```

### Modify app_dev.php file (add comments)
```php
/*if (isset($_SERVER['HTTP_CLIENT_IP])
¦¦ isset($_SERVER['HTTP_X_FORWARDED_FOR'])
¦¦ !(in_array(@$_SERVER['REMOTE_ADDR'], ['127.0.0.1','::1'], true) ¦¦ PHP_SAPI === 'cli-server')
) {
	header('HTTP/1.0 403 Forbidden');
	exit('You are not allowed to access this file. Check '.basename(__FILE__).' for more information.');
}
*/
```

## Console

### See all possible commands
```
php bin/console
```

### Create new Bundle
```
php bin/console generate:bundle [Bundle]
```

// Créer un contrôleur
php bin/console generate:controller [Bundle:Entity]

// Créer une base de données
php bin/console doctrine:database:create

// Créer une entité
php bin/console doctrine:generate:entity [Bundle:Entity]

// Génère les entités en fonction du mapping qu'il connait
php bin/console doctrine:generate:entities

// Mise à jour la base de donées
php bin/console doctrine:schema:update --dump-sql

// Valider les modifications
php bin/console doctrine:schema:update --force

// Install doctrine fixtures
composer require --dev doctrine/doctrine-fixtures-bundle

// Loading Fixtures
php bin/console doctrine:fixtures:load

// Créer un Formulaire
php bin/console doctrine:generate:form [Bundle:Entity]

// see routes
php bin/console debug:router

// asstets install
bin/console assets:install --symlink

### Clear console
php bin/console cache:clear --no-warmup -e prod
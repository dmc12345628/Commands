Symfony

// Créer un projet symfony
composer create-project symfony/framework-standard-edition [nomproject]
symfony new [nomproject] 3.1

// installation
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

// Nous allons modifier le fichier app_dev.php, en mettant en commentaire
```
/*if (isset($_SERVER['HTTP_CLIENT_IP])
¦¦ isset($_SERVER['HTTP_X_FORWARDED_FOR'])
¦¦ !(in_array(@$_SERVER['REMOTE_ADDR'], ['127.0.0.1','::1'], true) ¦¦ PHP_SAPI === 'cli-server')
) {
	header('HTTP/1.0 403 Forbidden');
	exit('You are not allowed to access this file. Check '.basename(__FILE__).' for more information.');
}
*/
```

// Pour voir la liste des commandes possibles
php bin/console

// Créer un bundle
php bin/console generate:bundle [Bundle]

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
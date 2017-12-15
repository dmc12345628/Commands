Laravel

// Create new project
composer create-project laravel/laravel [roject name]
laravel new [Project name]

// create model
php artisan make:model [Model Name] -m // -m to create database migrate

// migrate database
php artisan migrate

/*If you have a problem with User table in 'email' field, you have to
go to 'AppServiceProvider.php', in boot function, write this */
'Schema::defaultStringLength(191);'

// reset database
php artisan migrate:reset

// make test datas
php artisan make:seeder [Seeder name]

// refresh seeder's files when seeders exists
composer dump-autoload -o 

// passport install
composer require laravel/passport

// refresh migration
php artisan migrate:refresh --seed

// create controller
php artisan make:controller AlumnoController [--resource]

//to have remote access

// import barryvdh/laravel-cors library to generate tokens to extarnal apps
composer require barryvdh/laravel-cors

//Files to add the libraries 
config/app.php
	write 'Barryvdh\Cors\ServiceProvider::class,' in providers array
app/Http/Kernel.php
	write '\Barryvdh\Cors\HandleCors::class,' in middleware array

//after, configurate
in terminal write:
php artisan vendor:publish --provider="Barryvdh\Cors\ServiceProvider" 

// after clone repository
// create .env file and modify the necesary
composer install
php artisan key:generate // to generate laravel key
php artisan config:clear // clean cache
php artisan migrate
php artisan passport:install
php artisan db:seed

// when edit .env
php artisan config:cache
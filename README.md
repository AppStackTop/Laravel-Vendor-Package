# Laravel 5.3 Vendor Package Example
## An Example on how-to create a Vendor Package for Composer

"Packages are the primary way of adding functionality to Laravel. Packages might be anything from a great way to work with dates like Carbon, or an entire BDD testing framework like Behat."
https://laravel.com/docs/master/packages

Use this package to rapidly develop new packages to share among your projects - or the world.

# Installation
* Clone the repo
* Rename Askedio\LaravelVendorPackage & askedio\laravelvendorpackage stuff to your namespace (search & replace all files)
* Rename shortucts for configs, lang, etc, they are "LaravelVendorPackage::", so replace "LaravelVendorPackage" in the alias loaders
* Add to a github repo
* Add to packagist.org
* Install with commands like below, but with your names and revisions

# Installation
Install a fresh copy of Laravel then require the package.

    composer require askedio/laravel-vendor-package:dev-master


## Register with config/app.php
Register the service providers to enable the package.

    Askedio\LaravelVendorPackage\Providers\AppServiceProvider::class,

    // If you plan to do routing:
    Askedio\LaravelVendorPackage\Providers\RouteServiceProvider::class,

## Test
Test the actual laravel installation.

    php artisan serv

Browse to http://localhost:8000/dashboard

## Publish
        php artisan vendor:publish
## Migrate
        php artisan migrate
## Seed
        php artisan db:seed

# Test the package itself
    composer install
    vendor/bin/phpunit

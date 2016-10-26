# Laravel MercadoLibre API Client
Laravel wrapper of the MercadoLibre API Client


# laravel-pilot
This package is a wrapper of [MercadoLibre API Client PHP Class](https://github.com/zephia/mercadolibre) for Laravel Framework.

## Installation

Run the following command and provide the latest stable version:

```bash
composer require zephia/laravel-mercadolibre
```

Then register this service provider with Laravel in config/app.php:

```php
'providers' => [
    ...
    Zephia\LaravelMercadoLibre\MercadoLibreServiceProvider::class,
    ...
]
```

Publish config file:

```bash
php artisan vendor:publish --provider="Zephia\LaravelMercadoLibre\MercadoLibreServiceProvider" --tag="config"
```

Add **MERCADOLIBRE_APP_KEY** constants to your .env file:

```
MERCADOLIBRE=YOUR-MERCADOLIBRE-APP-KEY
```

## Usage
### Create and store lead

See fields documentation at [official MercadoLibre API reference](http://developers.mercadolibre.com/api-docs/)

```php
<?php

/**
 * Create Item
 */

$user = app('ml_api')->userShow('MLA123456789');

var_dump($user);

// object(Zephia\MercadoLibre\Entity\User)
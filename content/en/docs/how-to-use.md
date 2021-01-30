---
title: "How to use"
description: "How ot use the package."
date: 2021-01-30T21:00:00+08:00
draft: false
weight: 3
---

# How to use

Just type in terminal `$ php artisan make:crud ModelName` command, it will create simple Laravel CRUD files of given **model name** completed with tests.

For example we want to create CRUD for '**App\Models\Vehicle**' model.

```bash
$ php artisan make:crud-simple Vehicle

Vehicle resource route generated on routes/web.php.
Vehicle model generated.
Vehicle table migration generated.
VehicleController generated.
Vehicle index view file generated.
Vehicle form view file generated.
lang/app.php generated.
vehicle lang files generated.
Vehicle model factory generated.
Vehicle model policy generated.
AuthServiceProvider class has been updated.
BrowserKitTest generated.
ManageVehiclesTest generated.
VehicleTest (model) generated.
VehiclePolicyTest (model policy) generated.
CRUD files generated successfully!
```

Make sure we have **set database credential** on `.env` file, then :

```bash
$ php artisan migrate
$ php artisan serve
```

Then visit our application url: `http://localhost:8000/vehicles`.

<br>

## Usage on Fresh Install Laravel 8.x

In this example, we are using the [laravel installer](https://packagist.org/packages/laravel/installer) package to install new laravel project.

```bash
# This is example commands for Ubuntu users.
$ laravel new project-directory
$ cd project-directory
$ composer require laravel/ui
$ php artisan ui bootstrap --auth
$ npm install && npm run dev # Might need to run twice, minimum requirement: NodeJS v12.x
$ vim .env # Edit your .env file to update database configuration

# Install the package
$ composer require luthfi/simple-crud-generator:^2.0

# I really suggest "git commit" your project right before you run the make:crud command
$ php artisan make:crud Vehicle # Model name in singular

$ php artisan migrate
$ php artisan serve
# Visit your route http://127.0.0.1:8000
# Register as a new user
# Visit your route http://127.0.0.1:8000/vehicles

# Run the unit tests
$ vim phpunit.xml # Remove comments on the DB_CONNECTION and DB_DATABASE lines
$ vendor/bin/phpunit
```
---
title: "About this package"
description: "This package contains artisan make:crud commands to create a simple CRUD feature with test classes on our Laravel application."
date: 2021-01-30T21:00:00+08:00
draft: false
weight: 1
---

# About this package
This package contains artisan `make:crud` commands to create a simple CRUD feature with test classes on our Laravel 5.5 (and later) application. This package is fairly simple, to **boost test-driven development** method on our laravel application.

With this package installed on local environment, we can use (e.g.) `php artisan make:crud Vehicle` command to generate some files :

- `App\Models\Vehicle.php` eloquent model
- `xxx_create_vehicles_table.php` migration file
- `VehicleController.php`
- `index.blade.php` and `forms.blade.php` view file in `resources/views/vehicles` directory
- `resources/lang/vehicle.php` lang file
- `VehicleFactory.php` model factory file
- `VehiclePolicy.php` model policy file in `app/Policies` directory
- `ManageVehiclesTest.php` feature test class in `tests/Feature` directory
- `VehicleTest.php` unit test class in `tests/Unit/Models` directory
- `VehiclePolicyTest.php` unit test class in `tests/Unit/Policies` directory

It will update some file :

- Update `routes/web.php` to add `vehicles` resource route
- Update `app/providers/AuthServiceProvider.php` to add Vehicle model Policy class in `$policies` property

It will also create this file **if it not exists** :

- `resources/lang/app.php` lang file if it not exists
- `tests/BrowserKitTest.php` base Feature TestCase class if it not exists


## Main purpose

The main purpose of this package is for **faster Test-driven Development**, it generates model CRUD scaffolds complete **with Testing Classes** which will use [Laravel Browserkit Testing](https://github.com/laravel/browser-kit-testing) package and [PHPUnit](https://packagist.org/packages/phpunit/phpunit).
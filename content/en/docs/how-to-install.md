---
title: "How to install"
description: "Install the package with composer."
date: 2021-01-30T21:00:00+08:00
draft: false
weight: 2
---

# How to install

## For Laravel 8.x

```bash
# Get the package
$ composer require luthfi/simple-crud-generator:^2.0
```

## For Laravel 5.6 to 7.x

```bash
# Get the package
$ composer require luthfi/simple-crud-generator:^1.0
```

## For Laravel 5.5

To use this package on laravel 5.5, we need to **add the package** (with browserkit) within `require-dev` in `composer.json` file, like so :


```bash
# Install required package for laravel/browser-kit-testing
$ composer require symfony/css-selector:^3.0

# Get the package
$ composer require luthfi/simple-crud-generator 1.2.* --dev
```

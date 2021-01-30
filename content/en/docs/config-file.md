---
title: "Config File"
description: "Configure the package with config file."
date: 2021-01-30T21:00:00+08:00
draft: false
weight: 8
---

# Config File

You can configure your own by publishing the config file:

```bash
$ php artisan vendor:publish --provider="Luthfi\CrudGenerator\ServiceProvider" --tag=config
```

That will generate `config/simple-crud.php` file.

By default, this package have some configuration:

```php
<?php

return [
    // The master view layout that generated views will extends
    'default_layout_view' => 'layouts.app',

    // The base test case class path for generated testing classes
    'base_test_path' => 'tests/BrowserKitTest.php',

    // The base test class full name
    'base_test_class' => 'Tests\BrowserKitTest',
];
```
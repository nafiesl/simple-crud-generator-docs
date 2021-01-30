---
title: "Generated Testing Suite"
description: "Some screenshots of the generated CRUD feature."
date: 2021-01-30T21:00:00+08:00
draft: false
weight: 11
---

# Generated Testing Suite

Next, let us try the generated testing suite. To use the generated testing classes, we can set the database environment using ***in-memory* database SQLite**. Open `phpunit.xml`. Add two lines below on the `env` :

```xml
<phpunit>
    <!-- ..... -->
    <php>
        <!-- ..... -->
        <server name="DB_CONNECTION" value="sqlite"/>
        <server name="DB_DATABASE" value=":memory:"/>
    </php>
</phpunit>
```

Then run PHPUnit

```bash
$ vendor/bin/phpunit
```

All tests should be passed.

![Generated Testing Suite on Simple CRUD Generator](images/simple-crud-generator-02.jpg)

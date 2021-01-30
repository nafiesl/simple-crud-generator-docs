---
title: "Publishing the stub files"
description: "Use your own stub files."
date: 2021-01-30T21:00:00+08:00
draft: false
weight: 9
---

# Publishing the stub files

Stub files is the templates which we use to generate the code for each model classes and files. We can customize the stub files as we needed by publishing them to our project directory.

```bash
$ php artisan vendor:publish --provider="Luthfi\CrudGenerator\ServiceProvider" --tag=stubs
```

That will generate stub files on `stubs/simple-crud` directory. Now we can change some stub files based on our project needs.

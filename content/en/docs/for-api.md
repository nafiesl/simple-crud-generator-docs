---
title: "For API"
description: "Generates API endpoints for model CRUD."
date: 2021-01-30T21:00:00+08:00
draft: false
weight: 7
---

# For API

If we want to generate API Controller with feature tests, we use following command :

```bash
$ php artisan make:crud-api Vehicle
```

By default, we use Laravel **Token Based Authentication**, so we need to update our user model.

1. Add `api_token` **column** on our **users_table_migration**.
2. Add `api_token` as **fillable** property on **User model**.
3. Add `api_token` **field** on our **UserFactory**.

<br>

#### API Usage

The generated API is a REST API, using GET and POST verbs, with a URI of `/api/modelname`.

Example code for calling the generated API, using Guzzle:

    // Read data a specific Vehicle record...
    $uri = 'http://your-domain.com/api/vehicles/'.$vehicleID;
    $headers = ['Authorization' => 'Bearer '.$apiToken];

    $client = new \GuzzleHttp\Client();
    $res = $client->request('GET', $uri, ['headers' => $headers]);
<br>

    // Create a new Vehicle record...
    $uri = 'http://your-domain.com/api/vehicles';
    $headers = ['Authorization' => 'Bearer '.$apiToken];
    $payload = json_encode([
        'title' => 'Vehicle Name 1',
        'description' => 'Vehicle Description 1',
    ]);

    $client = new \GuzzleHttp\Client();
    $res = $client->request('POST', $uri, ['body' => $payload, 'headers' => $headers]);

The generated functional tests will give you examples of how to adapt this code for other call types.
# Pimple
## Description
This module provides helper functionality for easy usage of Pimple 3 in Drupal 6.

It is basically a **Drupal 6** alternative for <https://www.drupal.org/project/pimple_container>.

## Sidenote
This module does not include/autoload Pimple for you. You still have to do this yourself.

## Usage
The usage of this module is pretty straight-forward.
```php
<?php

// Get the Pimple container.
$container = pimple_get_container();

// Register a service.
$container['api.manager'] = function () {
  return new ApiManager();
};

// Use a service.
$manager = pimple_get_service('api.manager');

// Provide a custom ServiceProvider
pimple_register_provider(new ApiServiceProvider());
```

For more information about Pimple, please visit <http://pimple.sensiolabs.org>.

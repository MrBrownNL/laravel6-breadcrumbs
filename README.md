[![Latest Stable Version](https://poser.pugx.org/creitive/laravel6-breadcrumbs/version.png)](https://packagist.org/packages/creitive/laravel6-breadcrumbs) [![Total Downloads](https://poser.pugx.org/creitive/laravel6-breadcrumbs/d/total.png)](https://packagist.org/packages/creitive/laravel6-breadcrumbs)

Laravel 6 Breadcrumbs
=====================

*A simple Laravel 6-compatible breadcrumbs package. Generates Twitter Bootstrap-compatible output.*


Installation
------------

Just run this on the command line:

```
composer require creitive/laravel6-breadcrumbs
```

Laravel 6 will use the auto-discovery function.

If using an older version of Laravel (or if you don't use auto-discovery) you will need to include the service providers / facade in `config/app.php`.

```php
return array(
    // ...

    'providers' => array(
        // ...

        Creitive\Breadcrumbs\BreadcrumbsServiceProvider::class,
    ),

    // ...

    'aliases' => array(
        // ...

        'Breadcrumbs' => Creitive\Breadcrumbs\Facades\Breadcrumbs::class,
    ),
);
```

You're all set!


Usage
-----

For usage documentation, please visit the core library that this package depends on: [creitive/breadcrumbs](https://github.com/creitive/breadcrumbs).

This particular package registers a shared instance of the breadcrumbs class, and enables you to make the calls on the provided facade, ie. instead of doing `$breadcrumbs->addCrumb('Home', '/')`, you can do `\Breadcrumbs::addCrumb('Home', '/')`.

Additionally, having this as a separate package enables us to move forward with Laravel-specific features, such as having a configuration file that enables you to more cleanly customize how the package works.


Laravel 4
---------

For Laravel 4 support, visit the [creitive/laravel4-breadcrumbs](https://github.com/creitive/laravel4-breadcrumbs) package.


Laravel 5
---------

For Laravel 5 support, visi the [creitive/laravel5-breadcrumbs](https://github.com/creitive/laravel5-breadcrumbs) package.


License
-------

The code is licensed under the MIT license, which is available in the `LICENSE` file.

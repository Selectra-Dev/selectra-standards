Selectra’s PHP coding standards
=

# Table of contents

* PHP
* Framework
    * Drupal
    * Laravel
* Composer
* Server configuration
* Coding style
* Comments
* Deployment
    * Workflow
    * Environment variables

# PHP

- Use single quotes in strings definitions
    ```php
    $foo = 'bar';
    ```
- Close last array entry with comma
    ```php
    $foo = [
        'bar' => 'baz',
    ];
    ```
- Camel case variables
    ```php
    $fooBarBaz = 'qux';
    ```
- When documenting double-precision/floating-point variable use `float` instead of `double`
    ```php
    /** @var float $fooBarBaz */
    $fooBarBaz = .5;
    ```
- Don't use short type hinting names like `bool`, `int` or `str`
- Have to use `tristanjahier/zoho-crm-php` wrapper whenever connecting to [ZohoCRM](https://crm.zoho.com/) 

# Framework

A framework **MUST** be used for the project, to make for a better code and an easier maintenance. 

In Selectra we are using **Drupal** and **Laravel** frameworks. However if the developer is more comfortable working with another framework, it may be possible - pending our CTO's approval. 

## Drupal

@ todo

## Laravel

Laravel 5 **SHOULD** be used, as most of our applications are built with it.
Laravel good practices and standard are described in details [here](php/LARAVEL.md).

# Composer

- Keep composer.json entries in correct order - follow schema [reference](https://getcomposer.org/doc/04-schema.md)
- Always keep repositories sorted when adding them manually
- When using external dependencies, explanations **SHOULD** be given and links to documentation **SHOULD** be provided.

# Server configuration

PHP >= 5.6 **MUST** be used. Ideally, PHP7 **SHOULD** be used.

# Coding style

The developer **MUST** follow the [PSR-1](http://www.php-fig.org/psr/psr-1/) and [PSR-2](http://www.php-fig.org/psr/psr-2/) specifications in order to facilitate maintenance.

Ideally developer **SHOULD** use CodeSniffer with our internal [standards repository](https://github.com/Selectra-Dev/code-sniffer).

# Comments

The code **SHOULD** be commented if the developers feels this is necessary. If the developer does choose to use comments in his code, the comments **MUST** follow the specifications of [phpDocumentor](https://www.phpdoc.org/docs/latest/index.html).

# Deployment

## Workflow

In order to optimize our workflow, our system administrator needs to be able to deploy the project without any knowledge of its inner workings. This means that the code **MUST** be shipped in such a way that it can be built easily using a well-defined procedure. This procedure **MUST** be exhaustively described in a README.md file.

## Environment variables

To avoid unnecessary re-deployments, the developer **MUST** make good use of environment variables. Below is a non-exhaustive list of what **MUST** be an environment variable:
* Data base connection information
* Api keys

In any case, the environment variables you used in your project **MUST** be listed int the README.md, along with the purpose they serve.

Credentials **MUST NOT** be stored as plain text on the repository (especially production ones). Instead, you **SHOULD** provide an example of configuration file and eventually give instructions on how to create them.

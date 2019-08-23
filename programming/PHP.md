PHP
===

This document indicates the standards we follow during PHP project development. 

It consists of **naming conventions**, **architecture patterns**, **style guidelines** and **good practices**.

# Table of contents

1. [Variables](#variables)
  
2. [Functions](#functions)
  
3. [Documentation](#documentation)

4. [Style](#style)

5. [Composer](#composer)

6. [Frameworks](#frameworks)

    6.1. [Laravel](#laravel)

# Variables

- Use single quotes in strings definitions.

    ```php
    $foo = 'bar';
    ```

    > When a string is compound it's more convenient to use sprintf or [output buffering](https://www.php.net/manual/en/book.outcontrol.php).
    
- Put trailing comma after last array element (however inline array like `$foo = ['bar' => 'baz']` is correct).

    ```php
    $foo = [
        'bar' => 'baz',
    ];
    ```
    
- Use `camelCase`.

    ```php
    function fooBarBaz() {}
    ```
    
# Functions

- Use `camelCase`.

    ```php
    $fooBarBaz = 'qux';
    ```

# Documentation

- Use short name type hinting names like `bool`, `int` or `str` instead of `boolean`, `integer`, `string`.

- When documenting floating-point variable use `float` instead of `double`.

    ```php
    /** @var float $fooBarBaz */
    $fooBarBaz = .5;
    ```

    > Float is type. `double` is alias to `float` ([reference](https://www.php.net/manual/en/language.types.php)).

# Style

The developer **MUST** follow the [PSR-1](http://www.php-fig.org/psr/psr-1/) and [PSR-2](http://www.php-fig.org/psr/psr-2/) specifications in order to facilitate maintenance.

Ideally developer **SHOULD** use CodeSniffer with our internal [configuration](https://github.com/Selectra-Dev/code-sniffer).

# Composer

Composer is a PHP package manager we use in every project its considered as inseparable part of PHP standards. 

- Keep `composer.json` configuration properties in the official order
 
    - Follow the [official schema](https://getcomposer.org/doc/04-schema.md).
    
- Keep dependencies in the alphabetical order.

- Always keep repositories sorted when adding them manually.

- When using external dependencies, explanations **SHOULD** be given and links to documentation **SHOULD** be provided.

- Have to use `tristanjahier/zoho-crm-php` wrapper whenever connecting to [ZohoCRM](https://crm.zoho.com/).

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




# Framework

A framework **MUST** be used for the project, to make for a better code and an easier maintenance. 

In Selectra we are using **Laravel** framework. However if the developer is more comfortable working with another framework, it may be possible - pending our CTO's approval. 

## Laravel

The latest **LTS** release of Laravel **MUST** be used. The latest stable release **SHOULD** be used.
Laravel good practices and standard are described in details [here](php/LARAVEL.md).

# Server configuration

PHP >= 5.6 **MUST** be used. Ideally, PHP7 **SHOULD** be used.


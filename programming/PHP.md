PHP Hypertext Preprocessor
=

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

- **MUST** use single quotes for strings

    ```php
    $foo = 'bar';
    ```

    > When a string is compound it's more convenient to use `sprintf` or [output buffering](https://www.php.net/manual/en/book.outcontrol.php).

- **MUST** put trailing comma after last array element

    ```php
    $foo = [
        'bar' => 'baz',
    ];
    ```
  > Inline arrays, like `$foo = ['bar' => 'baz']`, are correct (they seem to be __prettier__ without comma).

- **MUST** use `camelCase`

    ```php
    $fooBarBaz = 'qux';
    ```

# Functions

- **MUST** use `camelCase`

    ```php
    function fooBarBaz() {}
    ```

# Documentation

- **MUST** use short name type hinting names like `bool`, `int` or `str` instead of `boolean`, `integer`, `string`

    > Using long type names creates unnecessary overhead. Use reserved keywords.

- **MUST** use `float` instead of `double` when documenting floating-point variable

    ```php
    /** @var float $fooBarBaz */
    $fooBarBaz = .5;
    ```

    > `float` is a type and `double` is [alias](https://www.php.net/manual/en/language.types.php) to `float`.

# Style

- The developer **MUST** follow the [PSR-1](http://www.php-fig.org/psr/psr-1/) and [PSR-2](http://www.php-fig.org/psr/psr-2/) specifications in order to facilitate maintenance

- Ideally developer **SHOULD** use CodeSniffer with our internal [configuration](https://github.com/Selectra-Dev/code-sniffer)

# Composer

Composer is a PHP package manager we use in every project its considered as inseparable part of PHP standards.

- **MUST** keep `composer.json` configuration properties in the official order

    > Follow the [official schema](https://getcomposer.org/doc/04-schema.md).

- **MUST** keep dependencies (`require` and `require-dev`) in the alphabetical order

    > This is automated by `sort-packages` configuration option. If you're editing `composer.json` manually, please remember about the order.

- **MUST** keep private repositories (`repositories`) in alphabetical order

- **MUST** use [Tristan's wrapper](https://github.com/Selectra-Dev/tristanjahier/zoho-crm-php) whenever connecting to [ZohoCRM](https://crm.zoho.com/)

- **MUST** keep `authors` updated

    > Minimal necessary details are `name`, `email` and `role`.

# Comments

- The code **SHOULD** be commented if the developers feels this is necessary. If the developer does choose to use comments in his code, the comments **MUST** follow the specifications of [phpDocumentor](https://www.phpdoc.org/docs/latest/index.html).

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

- A framework **MUST** be used for the project, to make for a better code and an easier maintenance

- In Selectra we are using **Laravel** framework. However if the developer is more comfortable working with another framework, it may be possible - pending our CTO's approval

## Laravel

- The latest **LTS** release of Laravel **MUST** be used. The latest stable release **SHOULD** be used

    > Laravel good practices and standard are described in details [here](php/LARAVEL.md).

# Server configuration

- **MUST** use PHP 7.

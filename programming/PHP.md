PHP Hypertext Preprocessor
=

This document indicates the standards we follow during PHP project development.

It consists of **naming conventions**, **architecture patterns**, **style guidelines** and **good practices**.

> As a base standards (considered as a **MUST**) we use [PSR-1](http://www.php-fig.org/psr/psr-1/) specifications in order to facilitate maintenance.

# Table of contents

1. [Naming convention](#naming-convention)

2. [Style](#style)

3. [Comments and code documentation](#comments-and-code-documentation)

4. [Composer](#composer)

5. [Deployment](#deployment)

    5.1. [Workflow](#workflow)

    5.2. [Environment variables](#environment-variables)

6. [Frameworks](#frameworks)

    6.1. [Laravel](#laravel)

    6.2. [Drupal](#drupal)

7. [Server configuration](#server-configuration)

# Naming convention

- **MUST** use `camelCase` for variable and function names

    ```php
    $fooBarBaz = 'qux';
    function fooBarBaz() {}
    ```

# Style

- **SHOULD** use [PHP_CodeSniffer](https://pear.php.net/package/PHP_CodeSniffer) with our internal [configuration](https://github.com/Selectra-Dev/code-sniffer)

    > [PHP Mess Detector](https://phpmd.org/) is also good choice!

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

# Comments and code documentation

- **MUST** follow the specifications of [PSR-5: PHPDoc](https://github.com/php-fig/fig-standards/blob/master/proposed/phpdoc.md) and [phpDocumentor](https://www.phpdoc.org/docs/latest/index.html)

- **MUST NOT** comment self-explanatory methods

    > Functions like getters and setters are obvious and don't need any explanations.
    > Please also double-check its implementation in such situation. It might be badly designed.

- **SHOULD NOT** contain PhpDoc's when arguments and return type are self explicitly defined

    > They are optional for methods like `public function foo(string $bar): \baz;`

- **MUST** contain PhpDocs's when arguments and return type aren't explicitly defined

    > They are mandatory for arguments like `/** @param string|int $foo */`.
    > Please also double-check its implementation in such situation. It might be badly designed.

- **MUST** use short name type hinting names like `bool`, `int` or `str` instead of `boolean`, `integer`, `string`

    > Using long type names creates unnecessary overhead. Use reserved keywords.

- **MUST** use `float` instead of `double` when documenting floating-point variable

    ```php
    /** @var float $fooBarBaz */
    $fooBarBaz = .5;
    ```

    > `float` is a type and `double` is an [alias](https://www.php.net/manual/en/language.types.php) to `float`.

- **MUST** align variables and their comments in the PhpDocs

   ```php
   /**
    * @param        $one   The first parameter
    * @param int    $two   The second parameter
    * @param string $three The third parameter
    */
   function foo($one, int $two = 0, $three = "String"): void
   {
   }
   ```

# Composer

[Composer](https://getcomposer.org) is a PHP package manager used in modern PHP development.

> We don't ship any PHP without it so it's considered as inseparable part of PHP standards.

- **MUST** keep `composer.json` configuration properties in the official order

    > Follow the [official schema](https://getcomposer.org/doc/04-schema.md).

- **MUST** keep dependencies (`require` and `require-dev`) in the alphabetical order

    > This is automated by `sort-packages` configuration option. If you're editing `composer.json` manually, please remember about the order.

- **MUST** keep private repositories (`repositories`) in alphabetical order

- **MUST** keep `authors` in the alphabetical order and **updated**

    > Minimal necessary details are `name` (surname first), `email` and `role`. Sort by contributor **surname**.

- **MUST** use [Tristan's wrapper](https://github.com/Selectra-Dev/tristanjahier/zoho-crm-php) whenever connecting to [ZohoCRM](https://crm.zoho.com/)

# Deployment

## Workflow

In order to optimize our workflow, our system administrator needs to be able to deploy the project without any knowledge of its inner workings. This means that the code **MUST** be shipped in such a way that it can be built easily using a well-defined procedure. This procedure **MUST** be exhaustively described in a README.md file.

## Environment variables

To avoid unnecessary re-deployments, the developer **MUST** make good use of environment variables. Below is a non-exhaustive list of what **MUST** be an environment variable:
* Data base connection information
* Api keys

In any case, the environment variables you used in your project **MUST** be listed int the README.md, along with the purpose they serve.

Credentials **MUST NOT** be stored as plain text on the repository (especially production ones). Instead, you **SHOULD** provide an example of configuration file and eventually give instructions on how to create them.

# Frameworks

- A framework **SHOULD** be used for the project, to make for a better code and an easier maintenance

- In Selectra we are using **Laravel** framework. However if the developer is more comfortable working with another framework, it may be possible - pending our CTO's approval

## Laravel

- The latest **LTS** release of Laravel **MUST** be used. The latest stable release **SHOULD** be used

    > Laravel's good practices and standard are described in details [here](LARAVEL.md).

## Drupal

- Use version **8** of Drupal

    > Drupal's good practices and standard are described in details [here](DRUPAL.md).

# Server configuration

- **MUST** use PHP 7.

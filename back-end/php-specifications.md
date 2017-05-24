# Selectra’s back-end specifications

* Framework
* Server configuration
* Coding style
* Comments
* Deployment



## Framework

A framework **MUST** be used for the project, to make for a better code and an easier maintenance. Laravel 5 **SHOULD** be used, as most of our applications are built with it. However if the developer is more comfortable working with another framework, it may be possible - pending our CTO's approval.

## Server configuration

PHP >= 5.6 **MUST** be used. Ideally, PHP7 **SHOULD** be used.

## Coding style

The developer **MUST** follow the [PSR-1](http://www.php-fig.org/psr/psr-1/) and [PSR-2](http://www.php-fig.org/psr/psr-2/) specifications in order to facilitate maintenance.

## Comments

The code **SHOULD** be commmented if the developers feels this is necessary. If the developer does choose to use comments in his code, the comments **MUST** follow the specifications
of [phpDocumentor](https://www.phpdoc.org/docs/latest/index.html).

## Deployment

  In order to optimize our workflow, our system administrator needs to be able to deploy the project without any knowledge of its inner workings. This means that the code **MUST** be shipped in such a way that it can be built easily using a well-defined procedure. This procedure **MUST** be exhaustively described in a README.md file.

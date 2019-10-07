Drupal
=

**Drupal 8** - Good practices, standards and resources.

# Table of contents

1. [General information](#general-information)

2. [Standards](#standards)

3. [Good practices](#good-practices)

4. [IDE configuration](#ide-configuration)

# General information

Drupal is content management software.
It's used to make many of the websites and applications you use every day.
Drupal has great standard features, like easy content authoring, reliable performance, and excellent security.
But what sets it apart is its flexibility; modularity is one of its core principles.
Its tools help you build the versatile, structured content that dynamic web experiences need.

- [User Guide](https://www.drupal.org/docs/user_guide/en/index.html)

    > This guide was written mainly for people with minimal knowledge of the Drupal content management system.

- [Documentation for developers](https://www.drupal.org/docs/develop)

    > Documentation for developers about tools, processes, and standards that are not specific to a major version of Drupal.

- [Extending Drupal 8](https://www.drupal.org/docs/8/extending-drupal-8)

    > This documentation guide describes 'Extending' your Drupal 8 site beyond the capabilities of a standard Drupal core installation.

# Standards

Drupal coding standards are version-independent and "always-current".
All new code should follow the current standards, regardless of (core) version.
Existing code in older versions may be updated, but doesn't necessarily have to be.
Especially for larger code-bases (like Drupal core), updating the code of a previous version for the current standards may be too huge of a task.
However, code in current versions should follow the current standards.

- [Coding standards](https://www.drupal.org/docs/develop/standards/coding-standards)

- [Twig coding standards](https://www.drupal.org/docs/develop/coding-standards/twig-coding-standards)

- [SQL coding conventions](https://www.drupal.org/docs/develop/standards/sql-coding-conventions)

# Good practices

Drupal has some good practices. We'll add those in that point:

- [Services and dependency injection](https://www.drupal.org/docs/8/api/services-and-dependency-injection)

    Drupal 8 introduces the concept of services to decouple reusable functionality and makes these services pluggable and replaceable by registering them with a service container.
    As a developer, it is best practice to access any of the services provided by Drupal via the service container to ensure the decoupled nature of these systems is respected.
    The Symfony documentation has a great introduction to services.

# IDE configuration

Some configurations for each IDE:

- [Configuring Visual Studio Code](https://www.drupal.org/docs/develop/development-tools/configuring-visual-studio-code)

- [Configuring Sublime Text](https://www.drupal.org/docs/develop/development-tools/configuring-sublime-text)


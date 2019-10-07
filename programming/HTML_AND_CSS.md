HTML and CSS
=

# Table of contents

1. [Technical specifications](#technical-specifications)
    
    1.1. [Design System](#design-system)
    
    1.2. [Editor](#editor)
    
    1.3. [HTML](#html)
    
    1.4. [CSS](#css)
    
    1.5. [Deployment](#deployment)

2. [Icons and images](#icons-and-images)

3. [Useful links](#useful-links)

    3.1. [Common files](#common-files)
    
    3.1. [Menu/footer](#menu-footer-and-cookie)

# Technical specifications

## Design System

The whole process **MUST** be based on **Design system** rules:

**Basics > Components >  Templates > Features**

- Where **Basics** are the simplest html/css element you can have, like a button

- Where **Components** are a combination of two or more basics to achieve an interaction, like the search field (an input + a button)

- Where **Templates** are a combination of two or more basics to achieve complex tasks like a list of offer card with his sort fields…

- Where **Features** are a whole combination of templates which allows you to achieve your goal (different tasks)

## Editor

The developer **MUST** use our **[.editorconfig](http://editorconfig.org/)** file.

## HTML

HTML files **MUST** follow these rules:

- **MUST** be Compiled with [pug](https://pugjs.org/api/getting-started.html) **(for the big projects)**

- **MUST** be **W3C compliant**

- **MUST** be **SEO friendly**, this means a **great outline tree**

- **Accessible**, this means that a **screen reader** **MUST** be able to read pages with no error (great usage of role tag etc)

- **SHOULD** be commented if the developer feels it's necessary. (Use of unusual techniques for instance)

- **No duplication allowed**: a module **MUST** uses mobile first approach

## CSS

CSS files **MUST** these rules:

- **MUST use [bootstrap v4](https://v4-alpha.getbootstrap.com/) latest alpha/beta as basic framework**

- **MUST** be Compiled with **Sass** with **two configs**, one for **dev** (css not minified + map) and one for **dist** (css minified)

- **MUST** be **[Linted](https://github.com/sasstools/sass-lint)** with the **scss-lint.yml** file

- **SHOULD** be commented if the developer feels it's necessary. (Use of unusual techniques for instance)

- **MUST be compliant on all modern browsers including IE11**

- **No duplication allowed**: a module **MUST** uses mobile first approach

## Deployment

In order to optimize our workflow, our system administrator needs to be able to deploy the project without any knowledge of its inner workings. 

This means that the code **MUST** be shipped in such a way that it can be built easily using a well defined procedure. This procedure **MUST** be exhaustively described in a `README.md` file.

# Icons and images

Icons **MUST** follow these rules:

- **SVG** format, **compressed/optimized** with a tool like `svgo`

- You **SHOULD** Used as **sprite** where you can, called with id. (the sprite **MUST** be **called with ajax into shadow DOM**, this allow the browser to cache the file)

- The used **grid** **MUST** be **24dp by 24dp**

- **viewBox parameters SHOULD NOT contain decimals**

Images **MUST** follow these rules:

- **PNG** format, **compressed/optimized** with a tool like `tinypng`

- For **mobile, @2x/@3x** export

# Useful links

## Common files

There is common files to use in our repo called [selectra-common-files](https://bitbucket.org/elrogue/selectra-common-files)

## Menu, footer and cookie

There is a repo where you can get our menu, footer... called [selectra-app-config](https://bitbucket.org/elrogue/selectra-app-config)

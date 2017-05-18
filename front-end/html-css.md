# Selectra’s HTML/CSS specifications


* Technical specifications
  * Design System
  * Editor
  * HTML
  * CSS
  * Deployement
* Icons & Images
* Useful links
  * Common files
  * Menu/footer




## Technical specifications

### Design System

The whole process should be based on **Design system** rules :

**Basics > Components >  Templates > Features**

* Where **Basics** are the simplest html/css element you can have, like a button.
* Where **Components** are a combination of two or more basics to achieve an interaction, like the search field (an input + a button)
* Where **Templates** are a combination of two or more basics to achieve complex tasks like a list of offer card with his sort fields…
* Where **Features** are a whole combination of templates which allows you to achieve your goal (different tasks).

### Editor

The only constraint for your editor is to use our **[.editorconfig](http://editorconfig.org/)** file.

### HTML

HTML files have to follow these rules :

* Compiled with [pug](https://pugjs.org/api/getting-started.html) **(for the big projects)**
* **W3C compliant**
* **SEO friendly**, this means a **great outline tree**
* **Accessible**, this means that a **screen reader** should be able to read pages with no error (great usage of role tag etc)
* Commented to be understandable if you use some irregular technics
* **No duplication allowed** : a module should uses mobile first approach

### CSS

CSS files have to follow these rules :

* **Use [bootstrap v4](https://v4-alpha.getbootstrap.com/) latest alpha/beta as basic framework**
* Compiled with **Sass** with **two configs**, one for **dev** (css not minified + map) and one for **dist** (css minified).
* **[Linted](https://github.com/sasstools/sass-lint)** with the **scss-lint.yml** file
* Commented to be understandable if you use some irregular technics
* **Be compliant on all modern browsers including IE11**
* Use the mobile first approach**

### Deployement

  In order to optimize our workflow, our system administrator needs to be able to deploy the project without any knowledge of its inner workings. For a front-end project, it means that the code must be shipped in such a way that it can be built easily using the following procedure:


  1. **Clone the repo from GitHub**

          git clone https://github.com/Selectra-Dev/landing-page-le-bon-coin.git
          cd landing-page-le-bon-coin

  2. **Acquire build dependencies.** Make sure you have [Node.js](http://nodejs.org/) installed on your workstation. Now run:

          npm install

  3. **Run the build tool**

          grunt dist

      Now you'll find the built files in `/dist/`.

  4. **Optional: Optimize images (time consuming task)**

          grunt dist-opti-img

## Icons & Images

Icons have to follow these rules :

* **SVG** format, **compressed/optimized** with a tool like svgo.
* Used as **sprite** where you can, called with id. (the sprite should be **called with ajax into shadow DOM**, this allow the browser to cache the file).
* The used **grid** should be **24dp by 24dp**.
* **Avoid decimal for the viewBox**

Images have to follow these rules :

* **PNG** format, **compressed/optimized** with a tool like tinypng.
* For **mobile, @2x/@3x** export

## Useful links

### Common files

There is common files to use in our repo called [selectra-common-files](https://bitbucket.org/elrogue/selectra-common-files)

### Menu/footer/cookie compliance/user rating/ekomi

There is a repo where you can get our menu, footer... called [selectra-app-config](https://bitbucket.org/elrogue/selectra-app-config)

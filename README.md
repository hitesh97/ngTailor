### [Important] ngTailor has became a Yeoman generator and has moved to [https://github.com/lauterry/generator-ngtailor](https://github.com/lauterry/generator-ngtailor). This repository will not be maintained anymore. Instead, please have a look at [generator-ngtailor](http://lauterry.github.io/generator-ngtailor/)

ngTailor [![Built with Grunt](https://cdn.gruntjs.com/builtwith.png)](http://gruntjs.com/)
==================

Offers you a tailor-made workflow for your Angularjs Web App.

<img height="250" align="left" src="http://bower.io/img/bower-logo.png">

<img height="250" align="left" src="https://s3.amazonaws.com/media-p.slid.es/uploads/hugojosefson/images/86267/angularjs-logo.png">

<img height="250" align="left" src="http://gruntjs.com/img/grunt-logo.svg">

## Why is ngTailor interesting ?
You love Angularjs, Grunt and Bower ? You might be interested by ngTailor.
ngTailor scaffolds out a new Angularjs application, writing your Grunt and Bower configurations and prepare for you revelant Grunt tasks you needs.

## Features
* Let you choose the Angularjs modules you need.
* Your assets dependencies are managed by [bower](http://www.bower.io)
* Run [Brian Ford](https://twitter.com/briantford) [ng-min](https://github.com/btford/ngmin) before your minification
* Replace your scripts and stylesheets declaration with the minified version when packaging your app for production thanks to [http://yeoman.io/](Yeoman) [grunt-usemin](https://github.com/yeoman/grunt-usemin)
* Watch for you assets changes and automatically run `jshint` or `csslint` on your code and even unit tests.
* Livereload is out of the box. No F5 anymore
* Automatically output a hash in your assets file name for caching purpose.
* Set up unit and e2e tests with Karma and Jasmine and generate test coverage report.
* Automatically run `npm install && bower install && grunt bower-install` to download your project dependencies and import them in your index.html
* Compile you SASS | LESS files
* Visualize Javascript source complexity with [plato](https://github.com/es-analysis/plato). ([See an example of a plato report](http://es-analysis.github.io/plato/examples/grunt/))
* Optimize your images (png, jpeg, gif)
* Keep multiple browsers devices in sync using [grunt-browser-sync](https://github.com/shakyShane/browser-sync)

## ngTailor vs Yeoman ?
Both aim to provide you a collection of tools and best practices to improve your productivity as a modern front end developer.
Yeoman is great but in my opinion, its generator-angular provides a bloated solution to manage and build angularjs applications.
ngTailor let you choose in a much more fine-grained way, each tools or components you want to be included in your application and workflow.
Note that ngTailor do not provide generator for directives, controllers etc like yeoman and generator-angular do.

## Prerequisites
1. Install [node and npm](http://www.nodejs.org)
2. Install **Grunt** running `npm install -g grunt-cli` 
3. Install **Bower** running `npm install -g bower`
4. Install **grunt-init** running `npm install -g grunt-init`
5. Install this template in your `~/.grunt-init/` directory (`%USERPROFILE%\.grunt-init\` on Windows) 
   by running `git clone https://github.com/lauterry/ngTailor.git ~/.grunt-init/angular`

## Generate your Angular project
1. Create a new folder for your project
2. Open a terminal and run `grunt-init angular` in your project folder
3. Choose between "Fast mode" or "Advanced mode":
  * "Fast mode" : Generate an Angularjs project with the minimal options.
  * "Advanced mode" : Let you customize your scaffolding and add more features. Just answer to the prompted questions.
4. ngTaylor will generate your Angularjs application and download all the dependencies by running ```npm install && bower install```
To check that everything is ok :
5. Run `grunt dev` to serve your static assets
6. Your should see "Yeahhh ! You're ready !" displayed in your browser
7. Voilà ! Your Angular project is ready ! Next step is to discover the available Grunt tasks.

## Developement
* Run `grunt dev` to start a static web server and open your browser.
* Livereload will be automatically active meaning that you can see your modification on the browser without hitting F5.
* `jshint` and/or `csslint` will be run on your files when they change.
* If you choose to have unit tests, they will be run as your test and source files change.

## Package for Production
* Run `grunt package` to package your static assets for production.
* Your package will be generated in a `dist` folder and your javascripts and stylesheets will be concatenated, minified and versionned.
* `grunt` : launch `grunt package`, run unit tests and e2e test and generate complexity report. Use this task for continuous integration.

## Available Grunt tasks
* `grunt ls` : list and describe the available grunt tasks of your project.
* `grunt test:unit` : run karma unit tests and show test coverage in console.
* `grunt test:e2e` : run karma e2e tests
* `grunt report` : open complexity report in your browser

## Update ngTailor
* `rm -rf ~/.grunt-init/angular`
* `git clone https://github.com/lauterry/ngTailor.git ~/.grunt-init/angular`

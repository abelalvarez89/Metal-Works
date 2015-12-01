# angularjs-frontend-template

A template for creating angularjs frontends.

## Getting started

To make a new project based on this template:

* make a folder for your project
* initialize an empty git repo `git init .`
* pull in the commits from this repo:
  `git pull <url to angularjs-frontend-template> develop`
* edit `package.json` to change the package name
* edit `src/index.js` to change the angular module name
* edit `src/index.html` to match the angular module name

## Development

* run `npm start`

This will do many things:

* start a local web server serving your `src/` folder
* compile your js code into one bundle, and update that bundle automatically as you 
  edit source code
* run tests, and display a brief report on what failed and code coverage. Tests are
  automatically re-run as you edit source code. A browseable html coverage report is
  in `coverage`
* open a browser window showing your `src/index.html`, and automatically refresh the
  window as you edit source code
  
 The index.html is meant for development as a sample of how this widget gets used from
 other applications.
 
 ### Other dev commands
 
 * `npm run style` - report on code style, with rules specified in `jscs.json`
     * `npm run style:fix` - automatically fix some style problems
 * `npm run lint` - run static analysis to identify potential problems

 ## Deployment

 * per-environment configuration is managed via separate js files; see the environments
   folder
 * we `npm publish` a tested, compiled bundle to nexus, and then deploy scripts
   download our known-good code from nexus and copy it to the server with the desired
   environment config file
 * applications that consume this widget need to add two script tags, one for the bundle
   and one for the config
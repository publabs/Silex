#Silex, live web creation.

[![Build Status](https://travis-ci.org/silexlabs/Silex.png?branch=master)](https://travis-ci.org/silexlabs/Silex)
[![Dependency Status](https://gemnasium.com/silexlabs/Silex.png)](https://gemnasium.com/silexlabs/Silex)

##About Silex

Silex, is a free and open source website buidler in the cloud. Create websites directly in the browser without writing code. And it is suitable for professional designers to produce great websites without constraints. Silex is also known as the HTML5 editor.

Brought to you by Silex Labs team, promoting free software.

Current version: v2.0.0alpha3

* http://www.silex.me/

More info on Silex Labs website

* http://www.silexlabs.org/silex/

Questions and answers

* http://graphicdesign.stackexchange.com/questions/tagged/silex

Discussions

* Facebook http://www.facebook.com/silexlabs
* Twitter https://twitter.com/silexlabs
* Google plus https://plus.google.com/communities/107373636457908189681

News and tutorials

* blog http://www.silexlabs.org/category/the-blog/blog-silex/
* subscribe by email http://eepurl.com/F48q5

GPL license

* http://www.silexlabs.org/silex/silex-licensing/

Main contributors

* Alex lexoyo Hoyau @lexoyo
* Thomas zabojad Fetiveau http://www.tokom.fr/
* Pol superwup Goasdoué @superwup
* Nicolas "silex" Masson @NicoSilex‎

##Installation on your local computer

This is for developers only, since our beloved designers can use the [online version](http://www.silex.me/).

Developers you can clone this repository and start the serveur (unifile), the back end of Silex, with nodejs. See instructions bellow.

### local installation on linux or macos

Prerequisite :

* [node.js](http://nodejs.org/) installed
* [NPM installed](https://npmjs.org/)

Clone this repository, and do not forget the sub modules (cloud-explorer and unifile)

Install node modules: npm install

Start the server: node server/api-server.js
Or use: foreman start (useful on heroku platform for example)

And open http://localhost:6805/silex/ or http://localhost:5000/silex/ in a browser (depending on your computer's config) - note that 6805 is the date of sexual revolution started in paris france 8-)

### local installation on Windows

> instructions provided by Régis RIGAUD :)

Prerequisite :

* [node.js](http://nodejs.org/) installed
* Git Client installed (e.g. [windows github client](http://windows.github.com/))
* [NPM installed](https://npmjs.org/)

Installation of Silex:

* Launch the "Git Shell"
* Create a complete clone of Silex Project : git clone --recursive https://github.com/silexlabs/Silex.git
* Go to Silex's Directory.
* install depedencies  : npm install

Start Silex :

* Launch Silex from a command prompt ( Silex's Directory) : node server/api-server.js
* Open your favorite browser on http://localhost:6805/silex/ and ENJOY !!!

##dependencies

These are the upstream projects we use in Silex

* [unifile](https://github.com/silexlabs/unifile), a nodejs server which provides a unified access to cloud services. This projects uses nodejs and these modules: express, dbox, express, googleapis, logger, node-oauth, oauth, path
* [Cloud explorer](https://github.com/silexlabs/cloud-explorer), a file manager for the cloud services. It is a front end javascript app which connects to a unifile server
* [ace](http://ace.c9.me/), an excellent code editor in javascript
* google closure library and compiler
* jquery and jquery UI are included in the sites generated by Silex

##Road map

###v2.0.0alpha4

WYSIWYG

* shortcuts (suppr, arrows, save, new, open)
* set as default page (drag drop pages and change order)

Texte

* difference entre typo dans l’editeur text et sur la scene
* detecter la couleur de fond (chercher le background color ou image dans les parents)

Components

* ?? media (audio, video)
* nav bar

File

* group images on the same drive as the html page?
* export (cleanup html, make zip with .html, .js, .css, all media)? + host on github or other free hosts?

###v2.0.0alpha5

Edition

* copy/cut/paste
* undo/redo
* autosave
* multiple selection https://github.com/someshwara/MultiDraggable
* better text editor?
  http://www.webdesignerdepot.com/2008/12/20-excellent-free-rich-text-editors/
  http://mindmup.github.me/bootstrap-wysiwyg/

File properties (in the settings dialog)

* title and description and keywords
* favicon

Contextual menu on the elements (menu bar under the menu like google?)

* delete
* lock/unlock
* up/down (z-index)
* rotation

Properties

* shadows
* font-*
* cursor
* scroll?


###v2.0.0beta1

Continuous integration

* jshint, PhantomJS, jenkins, Selenium
* unit tests http://stackoverflow.com/questions/11520170/unit-testing-oauth-js-with-mocha
* functional tests

Profesionnal installation

* softaculous virtual install
* bower?

Remove handlebars.js (and use jade on the server side instead?)

Unifile archi (cf unifile readme)

Debuging

Validation

* http://validator.w3.org/

Nice to have :

* file://localhost/Users/lexa/Dropbox/fdt-workspace/Silex/libs/closure/goog/demos/onlinehandler.html

###v2.0.x

Packaging / distribution

* cf dev-notes.md
* App.js ?
* chrome app http://developer.chrome.com/apps/about_apps.html
* arvixe like service
* add "multiple ftp" to file browser
* newsletter editor or postcard editor
* mainstream CMS page, article or theme editor
* mockup tool
* banner editor

###other features and ideas for plugins

* edit local website

  * http://devcenter.kinvey.com/nodejs/guides/users
  * http://stackoverflow.com/questions/11534412/any-good-user-management-framework-for-node-js
  * http://usercake.com/docs.php#3
  * http://labs.bittorrent.com/experiments/sync/technology.htm

* edit ftp

  * http://www.goodsync.com/how-to-sync/ftp
  * https://github.com/FTPbox

* analytics

  * in the settings dialog
  * tracking code + select google, yahoo, piwik
  * track links http://www.seosite.co.uk/outgoing-links-on-google-analytics

* mobile optimized version of Silex editor

* sites dynamiques ou administrables
  Google mbaas
  Ou un cms backend only

* FB page editor

* add to publish
  
  * settings : radio buttons to choose 
    * "dropbox apps": combo box with list of services (paperplane.io etc.), combo box to choose a website => set the publish path to Apps/paperplane/the.website.com/
    *and "publish path" (advanced users), the current behavior

  * history of the versions published
  
    * ask "what's new in this version"? (=> track versions in a versions.json file)
    * .history/deleted_[date]/

  * SEO: https://developers.google.com/webmasters/ajax-crawling/docs/specification

* Expot to use in haxe with cocktail

  * port silex scripts to haxe js if needed
  * remove unsupported css styles
  * close the html tags (e.g. <img /> instead of <img>)
  * create the .hx, .hxml, .nmml files to test

* widgets 

  * widget agenda
  * widget player vidéo 
  * webgl (cf open gl editor http://stackoverflow.com/questions/7093354/any-free-open-source-webgl-editors)

* Mobile version

  * tabs in the properties toolbox: normal, mobile V, mobile H
  * mobile => bg set to 100% width, stage set to iPhone width
  * data-style-mobile-v, data-style-mobile-h complement of data-style-normal, with position and size and URL (...) data only
  * better design for the toolbox
  * view menu: iPhone, iPad, web

deployment
  
  * css 
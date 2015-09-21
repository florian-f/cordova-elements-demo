# Cordova Elements Demo

This is a very simple demo of [cordova-elements](https://github.com/florian-f/cordova-elements). The Polymer app was created with the [Yeoman Generator for Polymer projects](https://github.com/yeoman/generator-polymer). 



If you want to build and run the app yourself on a device/ emulator you first need to 

* create a cordova project `cordova create cordova-app`. 
* go to the project directory: `cd cordova-app/`
* add the android platform:  run `cordova platform add android`.
* add the plugins: run `cordova plugin add cordova-plugin-device`, `cordova plugin add cordova-plugin-network-information` and `cordova plugin add cordova-plugin-device-motion`.

Then, to build and run the app:

* `node install`
* `bower install`
* run `gulp` 
* delete this file: `rm dist/bower_components/web-animations-js/web-animations.min.js*.gz`
* empty cordova's www directory `rm -r cordova-app/www/*`
* copy the polymer app into cordova's www directory `cp -r dist/* cordova-app/www/`
* In `cordova-app/`, run `cordova run android`.

<img src="https://github.com/florian-f/cordova-elements-demo/blob/image/Screenshot_2.png" width="25%">

## Some Notes

* This doesn't work with vulcanize at the moment so I removed the vulcanize task from the gulpfile for now. 
* API level 22 is required


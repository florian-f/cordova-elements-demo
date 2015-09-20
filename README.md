# Cordova Elements Demo

This is a very simple demo of [cordova-elements](https://github.com/florian-f/cordova-elements). The Polymer app was created with the [Yeoman Generator for Polymer projects](https://github.com/yeoman/generator-polymer). The Cordova app was created by running `cordova create cordova-app`. 

If you want to try and build the app yourself you first need to 

* add the android platform: in `cordova-app/`, run `cordova platform add android`.
* add the plugins: in `cordova-app/`, run `cordova plugin add cordova-plugin-device`, `cordova plugin add cordova-plugin-network-information` and `cordova plugin add cordova-plugin-device-motion`.

Then, to build and run the app:

* run `gulp` 
* delete this file: `rm dist/bower_components/web-animations-js/web-animations.min.js*.gz`
* empty cordova's www directory `rm -r cordova-app/www/*`
* copy the polymer app into cordova's www directory `cp -r dist/* cordova-app/www/`
* In `cordova-app/`, run `cordova run android`.

## Some Notes

* This doesn't work with vulcanize at the moment so I removed the vulcanize task from the gulpfile for now. 
* API level 22 is required


Ionic

// Installer les outils CLI Cordova et Ionic via NPM
npm install -g cordova ionic
// Verifier les versions
cordova -v
ionic -v

// Créer un projet
ionic start [projet_name]

// Add page
ionic generate page

// Ajouter la plateforme Android à l'application
ionic cordova platform add android

// Tester l'application dans le navigateur
ionic serve

// Déployer l'application sur android
ionic cordova run android

// Déployer l'application sur android
ionic cordova run android --device --livereload

// Installer angular google map
npm install @ngui/map @types/googlemaps --save

// Installer le module geolocation
ionic plugin add cordova-plugin-geolocation
npm install --save @ionic-native/geolocation

// Installer le module camera
ionic cordova plugin add cordova-plugin-camera
npm install --save @ionic-native/camera

// Installer firebase
ionic cordova plugin add cordova-plugin-firebase
npm install --save @ionic-native/firebase

npm cache clean -f
npm install npm -g

// add facebook plugin
ionic cordova plugin add cordova-plugin-facebook4 --variable APP_ID="2035037336775348" --variable APP_NAME="DevOps"
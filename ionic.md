Ionic
=====

## Quick started
### Install Cordova et Ionic
Install Cordova and Ionic CLI with NPM
```
npm install -g cordova ionic
```

### Check versions
```
cordova -v
ionic -v
```

### Create a project
```
ionic start [projet_name]
```

### Add page
```
ionic generate page
```

## Android platform

### Add android platform
```
ionic cordova platform add android
```

### Run project in android device
```
ionic cordova run android
ionic cordova run android --device --livereload
```

## Web platform 

### Run web app
```
ionic serve
```

## Angular Google Map

### Install @ngui/map
```
npm install @ngui/map @types/googlemaps --save
```

### Install geolocation
```
ionic plugin add cordova-plugin-geolocation
npm install --save @ionic-native/geolocation
```

## Angular Camera

### Install Camera
```
ionic cordova plugin add cordova-plugin-camera
npm install --save @ionic-native/camera
```

## Angular Firebase

### Install Firebase
```
ionic cordova plugin add cordova-plugin-firebase
npm install --save @ionic-native/firebase
```

## Angular Facebook

### Add Facebook plugin
```
ionic cordova plugin add cordova-plugin-facebook4 --variable APP_ID="2035037336775348" --variable APP_NAME="DevOps"
```

## Extras

### Clean cache
```
npm cache clean -f
```

### ?
```
npm install npm -g
```

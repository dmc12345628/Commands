Ionic
=====

## Quick started

### Install Cordova and Ionic
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
ionic start myApp tabs --type=angular // ionic 4
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
ionic cordova run android --prod --release
ionic cordova run android --device --livereload
ionic cordova build android --prod --release
ionic cordova run android --prod --release -- -- --keystore=my-release-key.keystore --alias=my-alias
```
### Sign Android APK
```
keytool -genkey -v -keystore my-release-key.keystore -keyalg RSA -keysize 2048 -validity 10000 -alias my-alias
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.keystore app-release-unsigned.apk my-alias
zipalign -v 4 app-release-unsigned.apk HelloWorld.apk
apksigner verify HelloWorld.apk
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

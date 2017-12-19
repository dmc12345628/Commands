Android Gradle Dependencies
===============

### [Butterknife](http://jakewharton.github.io/butterknife/)

Field and method binding for Android views and callbacks.

#### Owner
[Jake Wharton](https://github.com/JakeWharton)

#### Usage
```gradle
dependencies {
    compile 'com.jakewharton:butterknife:8.8.1'
    annotationProcessor 'com.jakewharton:butterknife-compiler:8.8.1'
}
```

### [FloatingActionButton](https://github.com/Clans/FloatingActionButton)
Android Floating Action Button based on Material Design specification.

#### Owner
[Clans](https://github.com/Clans)

#### Usage
```gradle
dependencies {
    compile 'com.github.clans:fab:1.6.2'
}
```

## [Support Library Packages](https://developer.android.com/topic/libraries/support-library/packages.html)
### [RecyclerView](https://developer.android.com/topic/libraries/support-library/packages.html#v7-recyclerview)
A widget for efficiently displaying large data sets by providing a limited window of data items. 

#### Usage
```gradle
dependencies {
    compile 'com.android.support:recyclerview-v7:26.1.0'
}
```

### [CardView](https://developer.android.com/topic/libraries/support-library/packages.html#v7-cardview)
This library lets you show information inside cards that have a consistent look on any app.

#### Usage
```gradle
dependencies {
    compile 'com.android.support:cardview-v7:26.1.0'
}
```

### [Spectrum](https://github.com/the-blue-alliance/spectrum)
A color selection library for Android.

#### Owner
[The blue alliance](https://github.com/the-blue-alliance)

#### Usage
```gradle
dependencies {
    compile 'com.thebluealliance:spectrum:0.7.1'
}
```

### [Room Persistence Library](https://developer.android.com/topic/libraries/architecture/room.html)
The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite.

#### Usage
```gradle
dependencies {
    implementation "android.arch.persistence.room:runtime:1.0.0"
    annotationProcessor "android.arch.persistence.room:compiler:1.0.0"
}
```

## Firebase
### Realtime Database
Save and retrieve data stored in a JSON tree structure.

#### Add the Realtime Database to your app
* build.gradle (project-level)
Add Firebase Gradle buildscript dependency
```
classpath 'com.google.gms:google-services:3.1.0'
```

* app/build.gradle
Add Firebase plugin for Gradle
```
apply plugin: 'com.google.gms.google-services'
```

* build.gradle will include these new dependencies:
```
compile 'com.google.firebase:firebase-database:11.6.2'
```
# pesantrian-app
pesantrian application image for desktop and mobile

# requirements
- a java keystore file, *.jks file is generated on play console directly by google itself
- npm from nodejs
- cordova from npm
- openjdk v17
- android sdk
- gradle

```
apt install npm openjdk-17-jdk snapd
npm install -g cordova
snap install core
snap install androidsdk
snap install gradle
```

# configuration
add to ```~/.bashrc```
```
export ANDROID_HOME=/opt/android-sdk
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
```

# cordova plugin list
```
cordova-plugin-camera
cordova-plugin-battery-status
cordova-plugin-device
cordova-plugin-dialogs
cordova-plugin-file
cordova-plugin-geolocation
cordova-plugin-inappbrowser
cordova-plugin-media
cordova-plugin-media-capture
cordova-plugin-screen-orientation
cordova-plugin-vibration
cordova-plugin-statusbar
cordova-plugin-navigationbar-color
cordova-plugin-qrscanner-11
cordova-plugin-network-information
cordova-plugin-in-app-updates
```

# closing
alhamdulillaah, thats all there is to it.



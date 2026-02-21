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

# path configuration
add to ```~/.bashrc```
```bash
export ANDROID_HOME=/opt/android-sdk
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
```

# android-sdk configuration
its required 3 of a kind library, depends on what version of cordova its used, for example cordova 14 requires:
- platforms 35
- build-tools 26
- platform-tools 35

just make sure check the avaiablity using ```sdkmanager --list```

and execute with
```
cordova build android
```

# electron configuration
choose one of the current platform
```json
{
    "electron": {
        "linux": {
            "package": [
                "AppImage",
            ],
            "arch": [ "x64" ]
        },
        "mac": {
            "package": [
                "dmg",
            ],
            "arch": [ "arm64" ]
        },
        "windows": {
            "package": [
                "portable",
            ],
            "arch": [ "x64" ]
        }
    }
}
```
on the file ```config.xml``` add,
```xml
<platform name="electron">
    <preference name="ElectronSettingsFilePath" value="res/electron/settings.json" />
</platform>
```
on the file ```res/electron/settings.json``` should be,
```json
{
    "browserWindow": {
        "width": 1024,
        "height": 768,
        "resizable": true,
        "fullscreen": true,
        "webPreferences": {
            "nodeIntegration": false
        }
    }
}
```
and execute with
```
cordova build electron
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



# Cordova plugin GTM

A plugin to install GTM on iOS and Android.

## Installation
`cordova plugin add git+https://github.com/florentlandure/cordova-plugin-gtm.git`

## Config
Add your GTM container configuration in config.xml

```xml
<plaform name="ios">
  ...
  <resource-file src="path/to/ios/config/files/GTM-XXXXXX.json" target="container/GTM-XXXXXX.json" />
  ...
</platform>

<platform name="android">
  ...
  <resource-file src="path/to/android/config/files/GTM-XXXXXX.json" target="app/src/main/container/GTM-XXXXXX.json" />
  ...
</platform>
```

Note: When using `resource-file` for iOS your config will be copied to `platforms/ios/Solocal/Resources/container/GTM-XXXXXX.json`. It is recommended to copy the config file to `platforms/ios/container/GTM-XXXXXX.json`. To do that you can create a hook that copies it there for you.

## Usage

This plugin is meant to be use alongside [Firebase analytics](https://github.com/chemerisuk/cordova-plugin-firebase-analytics) or [Firebase](https://github.com/arnesson/cordova-plugin-firebase) plugin.

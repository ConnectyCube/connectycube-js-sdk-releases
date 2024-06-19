# Changelog

## 3.30.0

### Updated

- [Video Calling][Conference Video Calling] "session.getUserMedia(mediaParams)" and "session.getDisplayMedia(mediaParams)" have been updated to correctly update an existed stream (track) when it needs to be replaced with a new one;

### Removed

- [Video Calling][Conference Video Calling] "session.stopLocalStreamTracks()" method was removed;

### Upgraded

- react-native-connectycube SDK (react-native-webrtc v124.0.1);

### Added

- react-native-connectycube.podspec.


## 3.29.0

### Upgraded

- connectycube SDK ("crypto-js", "fbemitter", "form-data", "node-fetch" and devDependencies);
- react-native-connectycube SDK ("crypto-js", "fbemitter", "js-base64", "react-native-webrtc");
- webpack config in connectycube JavaScript SDK;
- lerna for repository.

## 3.28.0

### Added

- the "ConnectyCube.data.readPermissions" method to get permissions by record's ID;
- [JS Custom Data documentation](https://developers.connectycube.com/js/custom-data);
- [React Native Custom Data documentation](https://developers.connectycube.com/reactnative/custom-data);
- [Cordova Custom Data documentation](https://developers.connectycube.com/cordova/custom-data);
- [NativeScript Custom Data documentation](https://developers.connectycube.com/nativescript/custom-data); 

### Updated

- the "ConnectyCube.data.update" method to have the ability to update by search_criteria;
- the "ConnectyCube.data.list" method to get records by ID/IDs/filters instead of only filters;
- DataSpec tests to support updated Custom Data API features.

## 3.27.4

### Bug Fixes

- "react-native-connetycube": fixed the error "ERROR TypeError: Cannot read property 'enumerateDevices' of undefined" if the "react-native-webrtc" isn't supported.

## 0.0.1

### Important Notes

- **Important**: Removed something
- **Important**: Updated something
- App now requires something

### Maintenance

- Removed a redundant feature
- Added a new functionality
- Improved overall performance
    - Enhanced user interface responsiveness

### Features

- :tada: Implemented a new feature
    - This feature allows users to...
- Added a user profile customization option

### Bug Fixes

- Fixed a critical issue that caused...

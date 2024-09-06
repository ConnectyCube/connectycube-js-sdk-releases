# Changelog

## 3.33.1

### Fixed

- typescript declarations for ConnectyCube.videochat;
- typescript declarations for ConnectyCube.videochatconference.

## 3.33.0

### Upgraded

- _@xmpp/client_ from 0.9.2 to 0.13.1 in all packages;
- _react-native-webrtc_ from 124.0.1 to 124.0.4 in _react-native-connectycube_;
- all "devDependencies" in _connectycube_ package;

### Fixed

- reassign const error (\*\*/lib/videocalling_conference/JanusVideoConferencingWrapper.js);
- typescript declarations.

## 3.32.0

### Added

- `session.restartIce(userID)` to restore WebRTC peer connection;
- `ConnectyCube.chat.pingWithTimeout(msTimeout).then(() => {...}).catch((e) => {...});`

### Fixed

- [Chat] prevent presence error from XMPP chat

Usage flow:

```javascript
ConnectyCube.videochat.onSessionConnectionStateChangedListener = function (session, userID, connectionState) {
  if (connectionState === 'failed') {
    if (onLine && session.canInitiateIceRestart(userID)) {
      session.restartIce(userID);
    }
  }
};
```

```javascript
ConnectyCube.chat
  .pingWithTimeout()
  .then(() => {})
  .catch((error) => {});
```

## 3.31.0

### Added

- prettifier;
- typescript declarations (types/\*\*/\*.d.ts);

### Updated

- [React Native][videocalling][videocalling conference] `getDisplayMedia` may not accept parameters

### Removed

- warnings about deprecated code.

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

# Changelog

## 4.1.3

### Updated

- the `ConnectyCube.chat.privacylist.setAsDefault` method can take null to deactivate the default list;
- the `CHANNEL` property was renamed to `BROADCAST` in `enum DialogType`;
- now `enum`s are exported in the same way as types.

## 4.1.2

### Updated

- `Dialogs.Dialog` types;

### Fixed

- fixed `ConnectyCube.users.listOnline` test to compare users results without strict order.

## 4.1.1

### Updated

- `Users` and `Messages.Attachment` types.

## 4.1.0

### Added

- new API to get online users:

```typescript
ConnectyCube.users.listOnline({limit?: number, offset?: number}): Promise<{users: array<User>}>;
```

### Removed

- Contact List (XMPP Roster) was removed as deprecated;

### Fixed

- Dialog types.

## 4.0.2

### Fixed

- now `ConnectyCube.setSession(session)` uses correct context;

## 4.0.1

### Upgraded

- `xmpp.js` libraries were upgraded;
- [react-native-connectycube] SpecRunner was upgraded migrated to the latest React Native 0.76.5

### Updated

- fixed TypeScript issues;
- checks the connection status when sending a message;
- defines SDK version from `package.json`;
- [connectycube] UMD bundle was optimized to decrease output size;
- [react-native-connectycube] `rollup` was replaces by `typescript` build;
- [react-native-connectycube] `react-native-webrtc` library is now supported as peerDependency;

### Deprecated

- `ConnectyCube.login(user)` was deprecated. Use `ConnectyCube.createSession(user)` or `ConnectyCube.auth.login(user)` instead;
- `ConnectyCube.logout()` was deprecated. Use `ConnectyCube.destroySession()` or `ConnectyCube.auth.logout()` instead.

## 4.0.0

### Added

- Full TypeScript source code;

### Updated

- Webpack bundler was replaced by Rollup module bundler (ECMAScript Module, CommonJS, and UMD);
- the `fbemitter` was replaced by the `eventemitter3` dependency;
- Contact List (XMPP Roster) marked as deprecated and will be removed in next major release;
- the `ConnectyCube.users.get(params)` method marked as deprecated and will be removed in next major release.

### Removed

- the `nativescript-connectycube` package was removed and will no longer be supported;
- removed the `crypto-js` dependency.

## 3.35.3

### Fixed

- [node.js] reverted to 'node-fetch' instead of internal 'fetch' to avoid file upload issue;

## 3.35.2

❗️ This release has issues with `ConnectyCube.storage.createAndUpload(params)` method in node.js environment. Update to 3.35.3.

### Fixed

- [node.js] it tries to use internal `fetch` first instead of `require('node-fetch').default`;
- parameters for `ConnectyCube.createSession(params)` are optional;
- fixed error when trying to overwrite a const;

## 3.35.1

[Types] Second argument is optional in `ConnectyCube.init(credentials, config)` (`ConnectyCube.init(credentials: any, configMap: any): void` > `ConnectyCube.init(credentials: any, configMap?: any): void`)

## 3.35.0

_@xmpp/client_ was upgraded from 0.9.2 to 0.13.1 in all packages. ConnectyCube SDK uses custom build of the _xmpp.js_ library to get rid of _@xmpp/stream-management_ package, which was replaced by ConnectyCube stream-management implementation

## 3.34.0

### Fixed

- [ConnectyCube.videochat] session.getUserMedia(mediaOptions) returns undefined;

### Updated

- [react-native-connectycube] "react-native-webrtc" has been replaced from dependencies to peerDependencies to support autolinking

```bash
yarn add react-native-connectycube react-native-webrtc
```

or

```bash
npm install react-native-connectycube react-native-webrtc --save
```

## 3.33.2

### Fixed

- the "@xmpp/client" dependency was reverted to version 0.9.2 to prevent errors with XMPP chat (streamManagement - "[Chat] ERROR: TypeError: Cannot read properties of undefined (reading 'catch')").

## 3.33.1

❗️ This release has XMPP chat issues. Upgrade to 3.33.2 or dump to 0.32.0.

### Fixed

- typescript declarations for ConnectyCube.videochat;
- typescript declarations for ConnectyCube.videochatconference.

## 3.33.0

❗️ This release has XMPP chat issues. Upgrade to 3.33.2 or dump to 0.32.0.

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

### Updated

- the "ConnectyCube.data.update" method to have the ability to update by search_criteria;
- the "ConnectyCube.data.list" method to get records by ID/IDs/filters instead of only filters;
- DataSpec tests to support updated Custom Data API features.

## 3.27.4

### Bug Fixes

- "react-native-connectycube": fixed the error "ERROR TypeError: Cannot read property 'enumerateDevices' of undefined" if the "react-native-webrtc" isn't supported.

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

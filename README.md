[![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/banner2-direct.svg)](https://stand-with-ukraine.pp.ua)

# ConnectyCube JS SDK Releases

This repository contains changelog and links to JS products released by ConnectyCube.

If you have any questions, comments, or issues related to any products distributed via this repository then please raise an issue here on GitHub repository or contact the team by emailing [support@connectycube.com](mailto:support@connectycube.com).

## SDK overview

ConnectyCube helps you implement real-time chat, video chat, push notifications and user authorization to any app with ease - no server side implementation required. You can concentrate fully on your mobile app development. Our JS SDK provides you with many helpful methods to build the chat and video chat from the client side.

This page presents a quick overview of the SDK’s functionalities and logic, then let you go through the easy steps of implementing ConnectyCube in your own app.

ConnectyCube Javascript SDK can be used on the following environments:

- Browser
- [Node.js](https://nodejs.org/)
- [React Native](https://facebook.github.io/react-native/)
- [NativeScript](https://www.nativescript.org/)
- [Apache Cordova](https://cordova.apache.org/)
- [Electron](https://www.electronjs.org/)

Original JS developers page https://developers.connectycube.com/js/

## Create ConnectyCube app

Register a FREE ConnectyCube account at [https://connectycube.com/signup](https://connectycube.com/signup), then create your 1st app and obtain an app credentials. These credentials will be used to identify your app.

All users within the same ConnectyCube app can communicate by chat or video chat with each other, across all platforms - iOS, Android, Web, etc.

## When building a new app

If you are just starting your app and developing it from scratch, we recommend to use our Code Samples projects.

[Download Code Samples](https://developers.connectycube.com/js/code-samples)

These code samples are ready-to-go apps with an appropriate functionality and simple enough that even novice developers will be able to understand them.

## When integrating SDK into existing app

If you already have an app, do the following for integration.

### Connect SDK

#### Browser

Simply connect the JS file as a normal script:

```html
<script src="https://cdn.jsdelivr.net/npm/connectycube@x.x.x/dist/connectycube.min.js"></script>
```

where **x.x.x** is the desired JS SDK version (check for [Releases page](https://github.com/ConnectyCube/connectycube-js-sdk-releases/releases) for all available versions).

The latest version is available here https://www.npmjs.com/package/connectycube

Then a window scoped variable called `ConnectyCube` is created.

Or install the package as NPM module:

```bash
npm install connectycube --save
```

And add script to HTML file from the 'node_modules' folder (as a relative path):

```html
<script src="~/node_modules/connectycube/dist/connectycube.min.js"></script>
```

See [an example of simple application based on Webpack build](https://github.com/ConnectyCube/connectycube-js-samples/tree/master/sample-webpack-build-app)

#### Node.js/NPM, Native Script

Simply install the package in a normal way:

```bash
npm install connectycube --save
```

and you're ready to go:

```javascript
const cubeClient = require("connectycube");
```

#### React Native

Simply install the package in a normal way:

```bash
npm install react-native-connectycube --save
```

and you're ready to go:

```javascript
import ConnectyCube from "react-native-connectycube";
```

### Initialize

Initialize framework with your ConnectyCube application credentials:

```javascript
const CREDENTIALS = {
  appId: 21,
  authKey: "hhf87hfushuiwef",
  authSecret: "jjsdf898hfsdfk",
};

ConnectyCube.init(CREDENTIALS);
```

### Configuration

An additional set of configs can be passed as a 2nd argument in `init` function:

```javascript
const CONFIG = {
  debug: { mode: 1 }, // enable DEBUG mode (mode 0 is logs off, mode 1 -> console.log())
};
ConnectyCube.init(CREDENTIALS, CONFIG);
```

## SDK Changelog

The complete SDK changelog is available on [ConnectyCube Javascript Releases GitHub page](https://github.com/ConnectyCube/connectycube-js-sdk-releases/releases)

## Have an issue?

Join our [Discord](https://discord.com/invite/zqbBWNCCFJ) for quick answers to your questions

## Community

- [Blog](https://connectycube.com/blog)
- X (twitter)[@ConnectyCube](https://x.com/ConnectyCube)
- [Facebook](https://www.facebook.com/ConnectyCube)

**Want to support our team**:<br>
<a href="https://www.buymeacoffee.com/connectycube" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

## License

ConnectyCube SDK for JS is licensed under the ConnectyCube SDK License.

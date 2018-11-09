# ConnectyCube JS SDK Releases

This repository contains changelog and links to JS products released by ConnectyCube.

If you have any questions, comments, or issues related to any products distributed via this repository then please raise an issue here on GitHub repository or contact the team by emailing [support@connectycube.com](mailto:support@connectycube.com).

# ConnectyCube SDK

This repository contains releases of the JS SDK for interacting with the ConnectyCube communications cloud.

It provides a simple interface to the messaging, video calling (WebRTC), push notifications, users management and cloud files storage capabilities provided by the platform.

[Getting Started with ConnectyCube JS SDK](https://developers.connectycube.com/js/)

# Installation

## Browser

Simply connect the JS file as a normal script:

```html
<script src="https://cdn.jsdelivr.net/npm/connectycube@x.x.x/dist/connectycube.min.js"></script>
```

Then a window scoped variable called `ConnectyCube` is created.

Check for [Releases page](https://github.com/ConnectyCube/connectycube-js-sdk-releases/releases) for available versions.

## Node.js/NPM, Native Script integration

Simply install the package in a normal way:

```bash
npm install connectycube --save
```

and you're ready to go:

```javascript
var cubeClient = require('connectycube');
```

## React Native integration

Simply install the package in a normal way:

```bash
npm install connectycube-reactnative --save
```

and you're ready to go:

```javascript
import {ConnectyCube} from 'connectycube-reactnative';
var CB = new ConnectyCube();
```

# Contact

You can reach the ConnectyCube team at any time by emailing [support@connectycube.com](mailto:support@connectycube.com).

# Licence

ConnectyCube SDK for JS is licensed under the ConnectyCube SDK License.

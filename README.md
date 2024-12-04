# Cordova screen pinning plugin

Cordova plugin that exposes screen pinning APIs on Android (API 21+).

## Installation

Run the following command inside your project's folder:

```sh
npm install https://github.com/yokowasis/cordova-plugin-screen-pinning/
```

## Usage

### enterPinnedMode()

Function that makes the app enter pinned mode. It accepts the following parameters:

- **successCallback:** [Function optional] - Success callback function.
- **errorCallback:** [Function optional] - Error callback function, takes the message string as the only parameter.

```js
cordova.plugins.screenPinning.enterPinnedMode(successCallback, errorCallback);
```

#### Example

```js
// Enter pinned mode
cordova.plugins.screenPinning.enterPinnedMode(
  function () {
    console.log("Pinned mode activated!");
  },
  function (errorMessage) {
    console.log("Error activating pinned mode:", errorMessage);
  }
);
```

### exitPinnedMode()

Function that makes the app exit pinned mode. It accepts the following parameters:

- **successCallback:** [Function optional] - Success callback function.
- **errorCallback:** [Function optional] - Error callback function, takes the message string as the only parameter.

```js
cordova.plugins.screenPinning.exitPinnedMode(successCallback, errorCallback);
```

#### Example

```js
// Exit pinned mode
cordova.plugins.screenPinning.exitPinnedMode(
  function () {
    console.log("Pinned mode de-activated!");
  },
  function (errorMessage) {
    console.log("Error exiting pinned mode:", errorMessage);
  }
);
```

### isPinned()

Function that check whether the app is currently in pinned mode. It accepts the following parameters:

- **successCallback:** [Function optional] - Success callback function.
- **errorCallback:** [Function optional] - Error callback function, takes the message string as the only parameter.

```js
cordova.plugins.screenPinning.isPinned(successCallback, errorCallback);
```

#### Example

```js
// Check if pinned
cordova.plugins.screenPinning.exitPinnedMode(
  function (r) {
    if (r) {
      console.log("App is in pinned mode!");
    } else {
      console.log("App is not in pinned mode!");
    }
  },
  function (errorMessage) {
    console.log("Error exiting pinned mode:", errorMessage);
  }
);
```

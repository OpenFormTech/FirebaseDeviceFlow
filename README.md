# Firebase Device Flow

[![forthebadge](https://forthebadge.com/images/badges/open-source.svg)](https://forthebadge.com) [![forthebadge](https://forthebadge.com/images/badges/powered-by-coffee.svg)](https://forthebadge.com)

Firebase authentication via [OAuth2 'Device Flow'](https://www.oauth.com/oauth2-servers/device-flow/) for Node.js CLI applications on limited input devices (i.e. IoT).

[![Build Status](https://travis-ci.com/UTAgritech/FirebaseDeviceFlow.svg?branch=master)](https://travis-ci.com/UTAgritech/FirebaseDeviceFlow)

## Providers Currently Implemented

- GitHub [(Docs)](https://docs.github.com/en/free-pro-team@latest/developers/apps/authorizing-oauth-apps#device-flow)
- Google [(Docs)](https://developers.google.com/identity/protocols/oauth2/limited-input-device)

## Example Usage

See [test.ts](./test.ts).

1. Import `FirebaseDeviceFlow`.
2. Initialize your Firebase app.
3. Pass Firebase app reference and OAuth config object to `DeviceFlowUI` constructor. If any parameters are absent from the OAuth config object, the relevant auth provider will be excluded from the UI.
4. Execute `DeviceFlowUI.signIn()`. This will return a **Promise\<UserCredential\>**.

## How It Works

Google has a great resource on ["OAuth 2.0 for TV and Limited-Input Device Applications"](https://developers.google.com/identity/protocols/oauth2/limited-input-device#obtaining-oauth-2.0-access-tokens).

![Device Flow Diagram](https://developers.google.com/identity/protocols/images/oauth2/device/flow.png)

# Development

Build and test with the usual `npm run build`, `npm run test`. For testing, you will have to initialize your own Firebase app and provider support.

## Requirements

- Node.js and `npm`
- Dependencies (install with `npm install`)

## Todo

- [X] Convert to Typescript
- [X] Change package structure for easier import (currently `import { DeviceFlowUI } from 'FirebaseDeviceFlow/dist/FirebaseDeviceFlow';`)
- [X] Fix testing
- [ ] 'Slow down' error code handling?
- [ ] Add more providers?

[![firebase](https://firebase.google.com/downloads/brand-guidelines/SVG/logo-built_white.svg)](https://firebase.google.com/)
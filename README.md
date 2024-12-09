# React Native Dimensions API Undefined Bug

This repository demonstrates a bug where `Dimensions.get('window')` or `Dimensions.get('screen')` in React Native unexpectedly returns `undefined`. This can cause layout problems and app crashes.

## Problem Description

The `Dimensions` API is used to retrieve screen dimensions. However, under certain circumstances (rapid orientation changes, app initialization), it can return `undefined`, leading to errors in calculations or component rendering.

## Solution

The solution involves using the `Dimensions` API in conjunction with the `useEffect` hook to ensure the dimensions are retrieved reliably.  We also add error handling to gracefully handle cases where dimensions are not immediately available.

## How to reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install`
3. Run the app on an Android or iOS emulator/device.
4. Quickly change the device's orientation multiple times to observe the potential issue.

## License

MIT
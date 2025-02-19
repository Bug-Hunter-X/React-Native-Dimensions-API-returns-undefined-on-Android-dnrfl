# React Native Dimensions API Undefined on Android

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native on Android. The problem arises because the `Dimensions` API may return `undefined` initially, before the dimensions are fully loaded, leading to runtime errors.

## Problem

The code attempts to access `Dimensions.get('window').width` or `Dimensions.get('window').height` before the dimensions are available, resulting in a runtime error because you're trying to access properties of `undefined`.

## Solution

The solution uses the `useEffect` hook and the `Dimensions` API's event listener to ensure that the dimensions are available before accessing them.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run the app on an Android emulator or device.
4. Observe the error in the console.
5. Implement the solution to fix the error.

## License

MIT
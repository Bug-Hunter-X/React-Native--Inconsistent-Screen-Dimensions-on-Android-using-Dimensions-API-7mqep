# React Native Inconsistent Screen Dimensions on Android

This repository demonstrates a common issue in React Native where the `Dimensions.get('window')` API returns inaccurate screen dimensions, particularly on Android.  The problem often manifests as 0 or incorrect values, leading to layout problems.

## Problem

The `Dimensions` API doesn't always provide the correct screen dimensions immediately, especially after the app has been in the background and returns to the foreground. This leads to components being rendered with the wrong dimensions.

## Solution

The solution involves using the `onLayout` event of the root view to detect when the dimensions have stabilized. This ensures the accurate dimensions are available before rendering components that depend on screen size.

## Setup

1. Clone the repository.
2. Run `npm install`.
3. Run the app on an Android device or emulator.
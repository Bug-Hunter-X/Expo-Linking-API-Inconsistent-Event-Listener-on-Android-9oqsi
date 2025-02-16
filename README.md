# Expo Linking API Inconsistent Event Listener on Android

This repository demonstrates a bug in Expo's `Linking` API where the `Linking.addEventListener` method for handling deep links is unreliable on Android.  The app sometimes fails to register and respond to external URL intents.

## Bug Description

The `Linking.addEventListener` fails to consistently trigger the callback function when a deep link is opened on Android devices. This can cause the app to miss important URL intents and fail to perform the expected actions.

## Reproduction

1. Clone the repository.
2. Run the app using `expo start`.
3. Try opening a deep link that the app is designed to handle (specified in the code).
4. Observe that the event listener does not always fire on Android (it usually works on iOS).

## Solution

The solution involves ensuring that the event listener is properly attached and that there are no conflicts with other event listeners or asynchronous operations.
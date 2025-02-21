# Expo Constants.deviceId undefined in Async Functions

This repository demonstrates a common issue encountered when using `Constants.deviceId` from Expo within asynchronous functions.  The `deviceId` may be undefined if accessed before it's fully loaded, causing unexpected errors.

The `bug.js` file shows the problem. The `bugSolution.js` file provides a solution.

## Problem

Accessing `Constants.deviceId` within an asynchronous operation (like a network request) before Expo has fully initialized may result in `undefined` being returned, leading to crashes or unexpected behavior.

## Solution

The recommended approach is to ensure that the `Constants.deviceId` is accessed only after Expo's `AppLoading` or a similar mechanism guarantees that the device information has been fully retrieved.
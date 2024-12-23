# Expo Camera: `takePictureAsync` Error Before Camera Initialization

This repository demonstrates a common error when using the Expo Camera API: calling `takePictureAsync` before the camera has fully initialized.  This leads to crashes or unexpected behavior.

The solution leverages the `onCameraReady` prop to ensure the `takePictureAsync` method is called only after the camera is ready.

## Bug Description
Attempting to use `takePictureAsync` immediately after mounting the `Camera` component can cause errors because the camera needs time to initialize. The code in `bug.js` illustrates this issue.

## Solution
The corrected code in `bugSolution.js` utilizes the `onCameraReady` prop of the `Camera` component.  This ensures that the `takePictureAsync` function is executed only after the camera is prepared, preventing the error.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe the behavior of the original `bug.js` and the corrected `bugSolution.js`.
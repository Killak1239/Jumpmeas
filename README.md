# AI Object Measure

An Android application that uses artificial intelligence to measure objects through a mobile device camera without requiring AR technology.

## Features

- **Real-time Object Detection**: Detects common objects using TensorFlow Lite
- **Size Measurements**: Calculates dimensions using a reference object
- **No AR Required**: Works on all Android devices without special AR capabilities
- **Measurement History**: Saves past measurements for future reference
- **Multiple Units**: Support for mm, cm, and inches

## How It Works

1. The app uses the device camera to capture an image
2. A TensorFlow Lite model detects objects in the image
3. A credit card (or similar sized object) is used as a reference
4. The app calculates real-world dimensions based on the reference
5. Measurements are displayed on screen and can be saved

## Technical Implementation

- **Camera**: Uses CameraX API for modern camera access
- **Object Detection**: TensorFlow Lite with COCO-SSD model
- **UI**: Material Design components for a clean interface
- **Storage**: Local storage for saving measurement history

## Requirements

- Android 5.0 (API level 21) or higher
- Camera permission
- Storage permission (for saving measurements)

## Build Instructions

See the included `Termux_APK_Guide.md` for detailed instructions on building the APK in Termux.

## Usage

1. Open the app and grant necessary permissions
2. Ensure you have a credit card or similar-sized object for reference
3. Place the reference object alongside the item you want to measure
4. Capture the image using the camera button
5. The app will detect objects and display their measurements
6. Save measurements you want to keep for future reference

## Limitations

- Accuracy depends on the quality of the reference object placement
- Best results are achieved with good lighting conditions
- Works best when objects are on the same plane as the reference
- Requires a known reference object in the frame

## Future Improvements

- Add support for more reference objects
- Implement 3D measurements
- Add cloud backup for measurement history
- Improve accuracy with multiple reference points
- Add measurement annotation tools
# AI Object Measure: Complete User Guide

## Introduction

AI Object Measure is a smartphone application that uses artificial intelligence to measure objects through your device's camera without requiring AR technology. This makes it compatible with virtually any Android smartphone. This guide covers all features and provides tips for getting the most accurate measurements.

## Getting Started

### Installation

1. Install the APK file on your Android device
2. Grant all requested permissions (camera, storage)
3. Complete the initial calibration process

### Main Interface

The app has four primary screens:
- **Camera**: For capturing images of objects to measure
- **Measure**: For analyzing captured images and displaying measurements
- **Points**: For making precise point-to-point measurements
- **History**: For viewing saved measurements

### Basic Workflow

1. Place a reference object (credit card, business card, etc.) next to the object you want to measure
2. Capture the image using the camera
3. The app detects objects and displays their dimensions
4. Save or share measurements as needed

## Camera Mode

### Controls

- **Capture Button**: Takes a photo
- **Switch Camera**: Toggles between front and rear cameras
- **Model Selection**: Changes the AI model used for detection
- **Flash**: Toggles camera flash (if available)

### Tips for Best Photos

- Ensure good, even lighting (natural light works best)
- Place objects on a plain, non-reflective background
- Keep the camera steady and parallel to the surface
- Ensure the reference object is clearly visible
- Keep objects on the same plane for accurate measurements

## Measurement Modes

### Auto Detection Mode

This mode automatically detects common objects in the scene and calculates their dimensions based on the reference object.

1. Ensure a known reference object (like a credit card) is in the frame
2. Capture the image
3. The app will highlight detected objects with their dimensions
4. Tap on any object to see more detailed measurements

### Point-to-Point Mode

This mode allows you to manually select points for measurement, ideal for:
- Objects not automatically detected
- Measuring specific parts of objects
- Measuring distances between objects

To use:
1. Tap the "Points" tab
2. Select two points on the image
3. The distance between points will be calculated and displayed
4. You can adjust points by dragging them
5. Save the measurement if desired

## Calibration

Proper calibration is essential for accurate measurements. See the detailed [Calibration Guide](Calibration_Guide.md) for complete instructions.

### Quick Calibration Steps

1. Go to Settings > Calibration
2. Select your reference object type
3. Verify or update the dimensions
4. Complete the calibration process
5. Test with an object of known size to verify accuracy

## AI Model Selection

The app includes multiple AI detection models optimized for different scenarios:

- **EfficientDet-Lite**: Balanced accuracy and speed for most objects
- **MobileNet SSD**: Fastest detection suited for mobile devices
- **YOLOv5**: Highest accuracy but slower processing

To change models:
1. Tap the AI model button in the camera view
2. Select your preferred model
3. Wait for the model to load (this may take a few seconds)

## Measurement History

The app saves your measurement history for future reference.

Features:
- View past measurements with images
- Sort by date, size, or object type
- Delete individual measurements
- Export measurements as CSV
- Share measurement images

## Advanced Features

### Reference Objects

The app supports several standard reference objects:
- Credit Card (85.6 × 53.98 mm)
- Business Card (89 × 51 mm)
- A4 Paper (297 × 210 mm)
- Custom reference objects (with known dimensions)

### Measurement Units

Switch between:
- Millimeters (mm)
- Centimeters (cm)
- Inches (in)

Units can be changed globally in settings or on-the-fly when viewing measurements.

### Manual Correction Factor

Fine-tune measurements with a correction factor:
1. Go to Settings > Advanced
2. Adjust the correction factor as needed:
   - Values < 1.0: Decrease all measurements
   - Values > 1.0: Increase all measurements

## Troubleshooting

### Common Issues

1. **Poor Detection Accuracy**
   - Ensure good lighting
   - Use a contrasting background
   - Try changing AI models
   - Recalibrate using a known reference

2. **App Crashes**
   - Ensure you have sufficient storage space
   - Update to the latest version
   - Restart your device

3. **Inaccurate Measurements**
   - Check calibration settings
   - Ensure the reference object is properly detected
   - Verify objects are on the same plane
   - Try changing AI models

4. **Slow Performance**
   - Use a simpler AI model (MobileNet)
   - Close background apps
   - Ensure your device has adequate free memory

## Tips for Best Results

1. **Optimal Distance**: 30-60cm from objects works best
2. **Surface**: Use a non-reflective, flat surface
3. **Lighting**: Even, diffused lighting minimizes shadows
4. **Angle**: Keep camera parallel to the surface
5. **References**: Larger references work better for larger objects
6. **Calibration**: Recalibrate when changing environments or lighting

## Privacy and Data Usage

- All processing happens on-device
- No images are uploaded to servers
- You control all data storage and sharing
- Measurements are stored only locally on your device
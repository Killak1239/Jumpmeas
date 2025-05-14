# Calibration Guide for AI Object Measure

This guide explains how to use the calibration feature to improve measurement accuracy in the AI Object Measure app.

## Why Calibration Matters

The app uses reference objects (like credit cards) and AI to calculate real-world measurements. However, several factors can affect accuracy:

1. Camera lens distortion
2. Viewing angle
3. Lighting conditions
4. Distance from objects
5. Surface reflections

Calibration helps compensate for these variables and provides more accurate measurements.

## Calibration Options

### Reference Object Selection

The app offers several standard reference objects:

- **Credit Card** (85.6 × 53.98 mm): The default reference object
- **Business Card** (89 × 51 mm): Common alternative reference
- **A4 Paper** (297 × 210 mm): Useful for measuring larger objects
- **Custom Reference**: When you have an object with known precise dimensions

Choose the reference object that's most appropriate for your measurement needs. Larger reference objects generally work better for measuring larger items.

### Fine-Tuning with Correction Factor

The correction factor adjusts all measurements by a specific multiplier. This helps when you notice that the app consistently over or under-measures objects by a certain percentage.

- **Values less than 1.0**: Reduce all measurements (use when app overestimates sizes)
- **Values greater than 1.0**: Increase all measurements (use when app underestimates sizes)
- **Default value is 1.0**: No adjustment

### Known Object Calibration

For the most precise calibration:

1. Measure an object of known dimensions with the app
2. Enter the actual dimensions
3. The app will automatically calculate the optimal correction factor

This is the recommended approach for maximum accuracy.

## Best Practices for Accurate Measurements

1. **Surface and Positioning**:
   - Place objects on a flat, non-reflective surface
   - Position the reference object at the same height as the object you're measuring
   - Keep the camera perpendicular to the surface (overhead view)

2. **Lighting**:
   - Use consistent, even lighting
   - Avoid harsh shadows and bright reflections
   - Natural, diffused daylight works best

3. **Distance and Framing**:
   - Keep a consistent distance between measurements
   - Include both the reference object and the item being measured in the same frame
   - Don't zoom in/out between calibration and measurement

4. **Recalibrate When Needed**:
   - Different environments may require different calibration settings
   - Recalibrate when changing locations or lighting conditions
   - Create multiple calibration profiles for different scenarios if needed

## Troubleshooting

If measurements seem inaccurate after calibration:

1. **Try a different reference object**: Some references work better in certain situations
2. **Adjust the correction factor manually**: Make small adjustments (±0.05) and test results
3. **Check lighting and surface**: Eliminate shadows and reflections
4. **Ensure proper detection**: Make sure the app is correctly identifying object boundaries
5. **Reset to defaults**: If things get worse, reset calibration settings and start over

Remember that physical measurement tools (rulers, calipers) still provide the most accurate measurements for critical applications.

## Advanced Calibration Techniques

For expert users who need maximum precision:

1. **Multi-object calibration**: Calibrate with multiple known objects of different sizes
2. **Environment-specific profiles**: Create and save different calibration settings for different environments
3. **Angle compensation**: Measure at consistent angles or use geometric correction
4. **Regular verification**: Periodically check calibration against known measurements

By taking time to properly calibrate the app, you can achieve measurement accuracy within 1-3% of actual dimensions in most cases.
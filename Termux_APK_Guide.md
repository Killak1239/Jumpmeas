# Building an APK in Termux: Step-by-Step Guide

This guide will walk you through the process of setting up your development environment in Termux and compiling the AI Object Measurement app into an APK file.

## Prerequisites

1. Termux app installed on your Android device (available from F-Droid)
2. Internet connection for downloading packages
3. At least 4GB of free storage space

## Step 1: Install essential packages

Open Termux and run the following commands:

```bash
# Update package list
pkg update -y

# Install essential build tools
pkg install -y git wget curl openssh

# Install Java Development Kit
pkg install -y openjdk-17

# Install build tools
pkg install -y gradle

# Install Android SDK tools (this will take some time)
pkg install -y android-tools

# Check Java installation
java -version
```

## Step 2: Set up environment variables

Set up the necessary environment variables:

```bash
# Create a directory for Android SDK
mkdir -p $HOME/Android/Sdk

# Set environment variables in .bashrc
echo 'export ANDROID_HOME=$HOME/Android/Sdk' >> $HOME/.bashrc
echo 'export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin:$ANDROID_HOME/platform-tools' >> $HOME/.bashrc
source $HOME/.bashrc
```

## Step 3: Install Android SDK components

Download and install the SDK components:

```bash
# Create an sdkmanager script
mkdir -p $HOME/Android/Sdk/tools/bin
wget https://dl.google.com/android/repository/commandlinetools-linux-8512546_latest.zip
unzip commandlinetools-linux-8512546_latest.zip
mv cmdline-tools/* $HOME/Android/Sdk/
rm -rf cmdline-tools
rm commandlinetools-linux-8512546_latest.zip

# Accept licenses and install required components
yes | $HOME/Android/Sdk/bin/sdkmanager --licenses
$HOME/Android/Sdk/bin/sdkmanager "platform-tools" "platforms;android-33" "build-tools;33.0.0"
```

## Step 4: Download the AI Object Measure project

Clone this project into Termux:

```bash
# Create a directory for your project
mkdir -p ~/projects
cd ~/projects

# Clone the repository (or transfer project files to your device)
git clone https://github.com/yourusername/ai-object-measure.git
cd ai-object-measure
```

## Step 5: Build the APK

Build the APK using Gradle:

```bash
# Navigate to the project folder
cd ~/projects/ai-object-measure

# Build the APK
./gradlew assembleDebug
```

If you don't have a gradle wrapper, create one:

```bash
gradle wrapper
./gradlew assembleDebug
```

## Step 6: Locate the built APK

After successful build, find your APK at:

```
~/projects/ai-object-measure/app/build/outputs/apk/debug/app-debug.apk
```

## Step 7: Install APK on your device

You can install the APK directly from Termux:

```bash
# Enable installation from unknown sources in your device settings first
# Then install the APK
adb install ~/projects/ai-object-measure/app/build/outputs/apk/debug/app-debug.apk
```

If adb doesn't work within Termux, you can copy the APK to a shared folder and install manually:

```bash
# Copy the APK to your Downloads folder
cp ~/projects/ai-object-measure/app/build/outputs/apk/debug/app-debug.apk /storage/emulated/0/Download/
```

Then navigate to the Downloads folder using your file manager and tap on the APK to install.

## Troubleshooting

### Limited storage in Termux
If you encounter storage issues, consider using Termux-storage:

```bash
pkg install termux-storage
termux-setup-storage
```

### Permission issues
If you encounter permission issues:

```bash
chmod +x gradlew
```

### Java memory issues
If you encounter Java memory issues, add the following to your gradle.properties file:

```
org.gradle.jvmargs=-Xmx1024m
```

### Building from scratch
If you prefer to build from scratch using only source files:

```bash
# Create base project structure
mkdir -p app/src/main/java/com/aicamerameasure
mkdir -p app/src/main/res/layout
mkdir -p app/src/main/res/values
mkdir -p app/src/main/res/drawable

# Copy source files
# (Copy all Java files to app/src/main/java/com/aicamerameasure)
# (Copy XML layouts to app/src/main/res/layout)
# (Copy Android Manifest to app/src/main)

# Build project
gradle init
# Configure build.gradle and settings.gradle
./gradlew assembleDebug
```

## Advanced: Adding TensorFlow Lite Model

For object detection, you need to add the TensorFlow Lite model to the assets folder:

```bash
# Create assets directory
mkdir -p app/src/main/assets

# Download a pre-trained model (example: COCO SSD)
wget https://storage.googleapis.com/download.tensorflow.org/models/tflite/coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip
unzip coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip -d temp_model
cp temp_model/detect.tflite app/src/main/assets/model.tflite
rm -rf temp_model
rm coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip
```

## Next Steps

- Add additional measurement features to the app
- Implement cloud backup of measurements
- Add support for more reference objects
- Enhance the UI with more intuitive controls
- Test on various Android device models for compatibility
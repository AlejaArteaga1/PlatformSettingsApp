# Platform-Specific Settings App

A React Native mobile application demonstrating platform-specific UI components and design patterns for iOS and Android.

## Project Overview

This lab project showcases the implementation of platform-specific user interfaces following Apple's Human Interface Guidelines and Google's Material Design principles. The app features a settings screen with platform-appropriate styling, components, and interactions.

## Lab Details

- **Course:** CPAN 213 - Cross-Platform Mobile Application Development
- **Lab:** #05 - Implementing Platform-Specific Features
- **Student:** Alejandra Arteaga Diaz
- **Student ID:** n01710855
- **Date:** October 23 2025

## Features

### Platform-Specific Implementations

- **iOS Design:**
  - Rounded buttons (12pt border radius)
  - Shadow effects for depth
  - SF Pro typography style
  - iOS-style switches and headers
  - Normal case button text

- **Android Design:**
  - Sharp buttons (4pt border radius)
  - Elevation for depth
  - Roboto typography style
  - Material Design switches
  - UPPERCASE button text

### Components
- Platform-aware buttons with variants (primary/secondary)
- Settings toggle rows with platform-appropriate switches
- Platform information display section
- Responsive header with platform-specific styling

## Technical Implementation

### Platform Detection
// Platform-specific file loading

const PlatformButton = Platform.select({

  ios: () => require('./PlatformButton.ios').default,
  
  android: () => require('./PlatformButton.android').default,
  
})();

// Platform-specific colors and styles

export const PLATFORM_COLORS = {

  ios: { primary: '#007AFF', background: '#f2f2f7' },
  
  android: { primary: '#2196F3', background: '#f5f5f5' }
  
};

### Project Structure
PlatformSettingsApp/

├── src/

│   ├── components/

│   │   └── PlatformButton/

│   │       ├── index.js

│   │       ├── PlatformButton.ios.js

│   │       └── PlatformButton.android.js

│   ├── screens/

│   │   └── SettingsScreen.js

│   └── utils/

│       └── platform.js

├── App.js

└── package.json

### Installation and Setup
1. Clone the repository

git clone https://github.com/your-username/PlatformSettingsApp.git

cd PlatformSettingsApp

2. Install dependencies
   
npm install

3. Install iOS dependencies (macOS only)
   
cd ios && pod install && cd ..

Run the application

# Android
npx react-native run-android

# iOS (macOS only)
npx react-native run-ios

### Testing
The app has been tested on:

-Android (Emulator & Physical Device)

-iOS (via Expo Snack - Windows development environment limitation)

### Learning Objectives Achieved
-Implement platform-specific UI components using file naming conventions

-Apply Platform.OS and Platform.select() for conditional styling

-Handle basic platform-specific permissions

-Create components that follow iOS and Android design guidelines

### Dependencies
React Native 0.82

react-native-vector-icons

Platform API (built-in)

### Development Notes
Development Environment: Windows (Android focus)

iOS Testing: Conducted via Expo Snack due to platform limitations

Code Quality: Follows React Native best practices with proper component separation

# Crop Guard AI - Early Plant Disease Detection App

An Android application for early plant disease detection using simulated AI analysis. Built with Kotlin, Jetpack Compose, and MVVM architecture.

## Features

### Core Functionality
- **Image Capture & Upload**: Use CameraX to capture plant leaf images or select from gallery
- **Simulated Disease Detection**: Random disease detection with confidence scores (60-100%)
- **Comprehensive Results**: Disease name, symptoms, treatment options (organic & chemical), prevention tips
- **Detection History**: Local storage of all past detections using Room database
- **Offline-First Design**: All functionality works without internet connection

### Additional Features
- **Regional Outbreak Alerts**: Randomly generated disease outbreak notifications by region
- **Educational Content**: Plant health information categorized by disease, prevention, and treatment
- **Farmer-Friendly UI**: Simple, intuitive interface with green color scheme
- **MVVM Architecture**: Clean separation of concerns for maintainability

## Technical Stack

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose with Material 3
- **Architecture**: MVVM (Model-View-ViewModel)
- **Camera**: CameraX for image capture
- **Database**: Room for local storage
- **Navigation**: Navigation Compose
- **Image Loading**: Coil
- **Permissions**: Accompanist Permissions

## Project Structure

```
app/src/main/java/com/example/earlyplantdiseasedetectionapp/
├── data/
│   ├── database/          # Room database, DAOs, converters
│   ├── model/            # Data models (DetectionResult, OutbreakAlert, etc.)
│   └── repository/       # Repository pattern for data access
├── ui/
│   ├── navigation/       # Navigation setup
│   ├── screens/         # Compose screens (Home, Camera, Results, etc.)
│   ├── theme/           # Material 3 theming
│   └── viewmodel/       # ViewModels for MVVM
├── utils/               # Utility classes (CameraUtils)
└── MainActivity.kt      # Main activity with navigation
```

## Screens

1. **Home Screen**: Quick actions and recent alerts overview
2. **Camera Screen**: Image capture with CameraX integration
3. **Results Screen**: Detailed detection results with treatment recommendations
4. **History Screen**: List of all past detections with delete functionality
5. **Alerts Screen**: Regional disease outbreak notifications
6. **Education Screen**: Plant health educational content with categories

## Simulated Disease Detection

The app simulates AI disease detection by randomly selecting from common plant diseases:
- Early Blight
- Late Blight
- Leaf Spot
- Powdery Mildew
- Rust
- Bacterial Wilt
- Mosaic Virus
- Anthracnose

Each detection includes realistic symptoms, treatment options, and prevention tips.

## Future Integration Ready

The architecture is designed to easily integrate real AI models and datasets:
- Repository pattern allows swapping simulated detection with real API calls
- UI components are model-agnostic and will work with real detection results
- Database schema supports additional fields for real detection metadata

## Setup Instructions

1. Clone the repository
2. Open in Android Studio
3. Sync Gradle dependencies
4. Run on Android device or emulator (API 24+)
5. Grant camera and storage permissions when prompted

## Permissions Required

- `CAMERA`: For capturing plant images
- `READ_EXTERNAL_STORAGE`: For selecting images from gallery
- `WRITE_EXTERNAL_STORAGE`: For saving captured images

## Dependencies

Key dependencies include:
- Jetpack Compose BOM
- CameraX libraries
- Room database
- Navigation Compose
- Coil for image loading
- Accompanist Permissions
- Gson for JSON parsing

## License

This project is for educational and demonstration purposes.
# Applications

This directory contains all client-side applications for the Hospital Management System.

## Structure

```
app/
├── web/           # Web application (React/Vue/Angular)
├── mobile-app/    # Mobile applications
│   ├── ios/       # iOS (Swift)
│   └── android/   # Android (Kotlin)
└── desktop/       # Desktop application (Electron)
```

## Web Application

### Technology
- React/Vue/Angular
- Tailwind CSS or Material-UI
- Redux/Vuex for state management
- Axios for API calls

### Setup
```bash
cd web
npm install
npm start
```

Access at: `http://localhost:3000`

See `web/README.md` for detailed instructions.

## Mobile Application

### iOS
- Language: Swift
- IDE: Xcode
- Deployment Target: iOS 12.0+

Setup:
```bash
cd mobile-app/ios
pod install
# Open in Xcode and run
```

### Android
- Language: Kotlin
- IDE: Android Studio
- Minimum SDK: API 21

Setup:
```bash
cd mobile-app/android
./gradlew build
# Open in Android Studio and run
```

Both platforms share common business logic via shared code or API calls to backend.

## Desktop Application

### Technology
- Electron
- Same frontend as web app (React/Vue)
- Electron API for native features

### Setup
```bash
cd desktop
npm install
npm start
```

### Build for Distribution
```bash
npm run build
# Creates installers for Windows, macOS, Linux
```

## Shared Resources

Common features across all platforms:
- Authentication
- API communication
- Data validation
- Error handling
- Notification system

See `/docs/guides/DEVELOPER_GUIDE.md` for more information.

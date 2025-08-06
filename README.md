# Sonargaon University ERP Mobile App

A comprehensive Enterprise Resource Planning (ERP) mobile application built with Flutter for Sonargaon University to streamline academic and administrative operations.

## 🎓 About Sonargaon University

Sonargaon University is a leading private university in Bangladesh, committed to providing quality higher education and fostering academic excellence. This Flutter-based ERP mobile app aims to digitize and optimize the university's operations with a modern, cross-platform solution.

## 📱 Flutter Features

### Cross-Platform Compatibility

- **iOS & Android** - Single codebase for both platforms
- **Responsive Design** - Adapts to different screen sizes
- **Native Performance** - Smooth animations and interactions
- **Offline Capability** - Works without internet connection

## 🚀 App Features

### Student Module

- **📚 Student Dashboard** - Overview of academic progress
- **📝 Course Registration** - Easy enrollment in courses
- **📊 Grade Tracking** - Real-time academic performance
- **📅 Class Schedule** - Daily/weekly timetable view
- **💰 Fee Management** - Payment history and pending fees
- **📋 Attendance Record** - Track class attendance
- **🎯 Assignments & Exams** - Upcoming deadlines and results

### Faculty Module

- **👨‍🏫 Faculty Dashboard** - Teaching overview
- **📖 Course Management** - Manage assigned courses
- **✅ Attendance Taking** - Quick student attendance
- **📝 Grade Entry** - Input and manage student grades
- **📢 Announcements** - Send updates to students
- **📊 Performance Analytics** - Track student progress
- **🗓️ Schedule Management** - View teaching schedule

### Administrative Module

- **🏛️ Admin Dashboard** - University overview
- **👥 User Management** - Manage students and faculty
- **📋 Course Catalog** - Maintain course information
- **💼 Department Management** - Organize academic departments
- **📈 Reports & Analytics** - Generate various reports
- **🔔 Notification Center** - Send university-wide updates

### Common Features

- **🔐 Secure Authentication** - Biometric and PIN login
- **🌐 Multi-language Support** - Bengali and English
- **🌙 Dark/Light Theme** - User preference themes
- **📱 Push Notifications** - Real-time updates
- **💬 In-App Messaging** - Communication between users
- **📄 Document Viewer** - View PDFs and images
- **🔍 Search Functionality** - Quick content search

## 🛠️ Technology Stack

### Frontend (Flutter)

- **Flutter SDK** - Cross-platform framework
- **Dart** - Programming language
- **Material Design 3** - Modern UI components
- **Provider/Riverpod** - State management
- **Flutter Bloc** - Business logic component pattern

### Backend Integration

- **REST APIs** - HTTP client integration
- **GraphQL** - Advanced data fetching
- **Socket.io** - Real-time communication
- **Firebase** - Authentication and push notifications

### Local Storage

- **SQLite** - Local database
- **Hive** - Lightweight key-value storage
- **Shared Preferences** - App settings storage
- **Secure Storage** - Sensitive data encryption

### Additional Packages

- **cached_network_image** - Image caching
- **pdf_viewer** - Document viewing
- **charts_flutter** - Data visualization
- **camera** - Image capture
- **biometric_auth** - Fingerprint/Face ID
- **connectivity_plus** - Network status

## 📋 Prerequisites

Before running this Flutter application, make sure you have:

- **Flutter SDK** (3.16.0 or higher)
- **Dart SDK** (3.2.0 or higher)
- **Android Studio** or **VS Code** with Flutter extensions
- **Android SDK** (for Android development)
- **Xcode** (for iOS development - macOS only)
- **Git**

## 🚀 Installation & Setup

1. **Clone the repository**

```bash
git clone https://github.com/MilonChandraDas/SU_App.git
cd SU_App
```

2. **Install Flutter dependencies**

```bash
flutter pub get
```

3. **Check Flutter setup**

```bash
flutter doctor
```

4. **Environment Configuration**
   Create `lib/config/app_config.dart`:

```dart
class AppConfig {
  static const String baseUrl = 'https://api.sonargaonuniversity.edu.bd';
  static const String apiVersion = 'v1';
  static const String appName = 'SU ERP';
  static const bool debugMode = true;
}
```

5. **Run the application**

```bash
# Debug mode
flutter run

# Release mode
flutter run --release

# Specific device
flutter run -d <device_id>
```

6. **Build for production**

```bash
# Android APK
flutter build apk --release

# Android App Bundle
flutter build appbundle --release

# iOS (macOS only)
flutter build ios --release
```

## 📱 Supported Devices

### Android

- **Minimum SDK**: Android 21 (5.0 Lollipop)
- **Target SDK**: Android 34 (14.0)
- **Architecture**: ARM64, ARMv7, x86_64

### iOS

- **Minimum Version**: iOS 12.0
- **Architecture**: ARM64 (iPhone 5s and newer)
- **Supported Devices**: iPhone, iPad

## 🏗️ Project Structure

```
lib/
├── main.dart                 # App entry point
├── core/                     # Core functionality
│   ├── constants/           # App constants
│   ├── utils/              # Utility functions
│   ├── services/           # API services
│   └── themes/             # App themes
├── models/                  # Data models
│   ├── user.dart
│   ├── student.dart
│   └── course.dart
├── screens/                 # App screens
│   ├── auth/               # Authentication screens
│   ├── student/            # Student module screens
│   ├── faculty/            # Faculty module screens
│   └── admin/              # Admin module screens
├── widgets/                 # Reusable widgets
│   ├── common/             # Common widgets
│   └── custom/             # Custom widgets
└── providers/               # State management
    ├── auth_provider.dart
    ├── student_provider.dart
    └── course_provider.dart
```

## 🔐 Authentication Flow

1. **Splash Screen** - App initialization
2. **Login Screen** - Credentials input
3. **Biometric Authentication** - Fingerprint/Face ID
4. **Role-based Dashboard** - Student/Faculty/Admin
5. **Session Management** - Auto-login and logout

## 🌐 API Integration

### Base Configuration

```dart
class ApiService {
  static const String baseUrl = 'https://api.sonargaonuniversity.edu.bd/v1';
  static const Map<String, String> headers = {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
  };
}
```

### Main Endpoints

- `/auth/login` - User authentication
- `/students` - Student data management
- `/faculty` - Faculty information
- `/courses` - Course catalog
- `/grades` - Academic records
- `/attendance` - Attendance tracking

## 🧪 Testing

```bash
# Run all tests
flutter test

# Run widget tests
flutter test test/widgets/

# Run integration tests
flutter test integration_test/

# Generate test coverage
flutter test --coverage
```

## 📦 Building & Deployment

### Android Deployment

1. **Generate keystore**

```bash
keytool -genkey -v -keystore upload-keystore.jks -keyalg RSA -keysize 2048 -validity 10000 -alias upload
```

2. **Configure signing in `android/app/build.gradle`**

3. **Build release APK**

```bash
flutter build apk --release
```

### iOS Deployment (macOS only)

1. **Configure Xcode project**
2. **Set up provisioning profiles**
3. **Build release IPA**

```bash
flutter build ios --release
```

## 🔧 Configuration Files

### pubspec.yaml Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  provider: ^6.1.1
  http: ^1.1.0
  sqflite: ^2.3.0
  shared_preferences: ^2.2.2
  cached_network_image: ^3.3.0
  firebase_messaging: ^14.7.6
  local_auth: ^2.1.7
  pdf_viewer_plugin: ^2.0.1
```

## 🤝 Contributing

We welcome contributions to the Sonargaon University Flutter ERP app!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Follow Flutter coding conventions
4. Write tests for new features
5. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
6. Push to the branch (`git push origin feature/AmazingFeature`)
7. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support & Contact

For technical support or inquiries:

- **Email**: support@sonargaonuniversity.edu.bd
- **Phone**: +880-2-XXXXXXXX
- **Address**: Sonargaon University, Dhaka, Bangladesh
- **Developer**: Milon Chandra Das

## 🙏 Acknowledgments

- Sonargaon University Administration
- Flutter Community for amazing packages
- Faculty and Staff for valuable feedback
- Student community for testing and suggestions

---

**Built with Flutter 💙 for Sonargaon University**

_Last updated: August 2025_

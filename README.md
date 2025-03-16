# Buy & Earn App

A fully functional mobile application for Buy and Earn website, where users can earn coins by completing tasks, playing games, and participating in giveaways.

## Features

- User Authentication (Email, Phone, Google Sign-in)
- Task Completion System
- Mini Games
- Giveaways
- Software Purchase with Coins
- Coin Withdrawal System
- Profile Management
- Dark/Light Theme
- Push Notifications
- Referral System

## Getting Started

### Prerequisites

- Flutter SDK (2.17.0 or higher)
- Android Studio / VS Code
- Firebase Account
- Google AdMob Account

### Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/buy_and_earn_app.git
cd buy_and_earn_app
```

2. Install dependencies:
```bash
flutter pub get
```

3. Configure Firebase:
   - Create a new Firebase project
   - Add Android & iOS apps in Firebase console
   - Download and add configuration files:
     - Android: `google-services.json` to `android/app/`
     - iOS: `GoogleService-Info.plist` to `ios/Runner/`

4. Configure AdMob:
   - Create an AdMob account
   - Add your app in AdMob console
   - Update the AdMob app ID in:
     - Android: `AndroidManifest.xml`
     - iOS: `Info.plist`

5. Create keystore for release build:
```bash
keytool -genkey -v -keystore android/app/upload-keystore.jks -keyalg RSA -keysize 2048 -validity 10000 -alias upload
```

6. Create `key.properties` in `android/` folder:
```properties
storePassword=<your-keystore-password>
keyPassword=<your-key-password>
keyAlias=upload
storeFile=upload-keystore.jks
```

### Running the App

For development:
```bash
flutter run
```

For release build:
```bash
flutter build apk --release
# or
flutter build appbundle --release
```

## Project Structure

```
lib/
  ├── constants/      # App constants, themes, etc.
  ├── models/         # Data models
  ├── screens/        # UI screens
  │   ├── auth/       # Authentication screens
  │   ├── tabs/       # Main tab screens
  │   └── ...
  ├── services/       # Business logic services
  ├── utils/          # Utility functions
  ├── widgets/        # Reusable widgets
  └── main.dart       # App entry point
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Flutter Team
- Firebase
- All package authors used in this project 
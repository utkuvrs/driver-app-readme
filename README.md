# SFT Driver iOS Android

SFT Driver is a Flutter project.

## Installation

To install the project, follow these steps:

1. Clone this repository: `git clone https://github.com/SFT-Logistics/driver-app.git`
2. Install the dependencies: `flutter pub get`

## Build

To get build files, use the following command:

```dart
/// Get Android build files.
flutter clean && flutter pub get && flutter build apk

/// Get iOS build files.
flutter clean && flutter pub get && flutter build ipa

/// Also feel free to use:

/// Windows
build_apk.bat
/// Mac
build_ipa.sh
build_apk.sh
```

Sometimes, you might get "Unable to process request - PLA Update available" error while trying to get a build for iOS. To fix this, agree to terms & conditions on https://developer.apple.com/account/ .

If you are unable to run and/or build the project, see Stepfront Utilities.

## Stepfront Utilities

See: https://github.com/Stepfront1/stepfront-utilities/

## Features

This project includes the following features:

- Barcode scan
- Camera
- BLoC, Cubit
- Location
- Push notifications
- Chat using signalr socket
- Language support for: English, Danish, Serbian and Swedish.

## Architecture

This project uses the following architecture:

- View -> Screen (Handling the UI elements and what should be shown to the end-user on which state, State Management.)
- Control -> Cubit (Handling the "Endpoint" calls and also setting the states when necessary.)
- Endpoint -> endpoint (Handling the necessary API calls using the API Provider class)
- Since an endpoint can be used in various screens & cubits, for DRY principles, we have separated the endpoint calls from the cubit.
- API Provider -> (Handles GET, POST, PUT, PUTIMAGE calls to the API as well as authentication tokens.)

## Libraries

This project uses the following libraries:

- `dio` for making API requests
- `get_storage` for storing access & refresh tokens.
- `flutter_bloc` for implementing the BLoC pattern
- `onesignal_flutter` for push notifications.
- `signalr_netcore` for support chat.

## Testing

This project includes unit tests. To run the tests, see test/, use the following command:
Front-end unit tests

```dart
flutter test
```

Back-end unit tests

```dart
/// example device name: emulator-5554
flutter run test/back_end.dart/ -d <device-name-here>
```

Back-end unit tests

```dart
/// example device name: emulator-5554
flutter run test/back_end.dart/ -d <device-name-here>
```

## Contributing

If you'd like to contribute to the project, feel free to submit a pull request. Here are some ways you can contribute:

- Add a new feature
- Fix a bug
- Improve the documentation
- Write tests

## License

See LICENSE.md

## Acknowledgments

- Developed by [Utku AYDOS](https://github.com/21kkfy).
- Thanks to [Ahmet SERDAR](https://github.com/ahmetserdar00) for translations and testing the application on iOS physical devices.

## Dart, Flutter Version

SFT was designed Dart 2.18.6 (stable) and Flutter 3.3.10 versions in mind.
At the time of development, Dart 3 wasn't released.
Flutter version was upgraded to 3.7.12 as of 20/04/2023 (EU)
<br>However, SFT Driver is fully compatible with sound null safety and **MUST** stay as such, because Dart 3 doesn't support no sound null safety.

# Semantic Versioning (SemVer)

Semantic Versioning, or SemVer, is a standard for versioning software that helps developers communicate the changes made to their codebase. The standard is described on semver.org, and it follows a `major.minor.patch` format.

## Versioning

The `major` version is incremented when there are breaking changes to the API or functionality of the software.

The `minor` version is incremented when new features are added to the software, but the existing functionality remains unchanged.

The `patch` version is incremented when bug fixes are made to the software, but no new features or functionality are added.

## Pre-release versions

Pre-release versions can be denoted by appending a hyphen and a series of dot-separated identifiers to the version number. For example, `1.0.0-beta.1`.

## Build metadata

Build metadata can be denoted by appending a plus sign and a series of dot-separated identifiers to the version number. For example, `1.0.0+build.1234`.

## Conclusion

By following the standards described on semver.org, developers can communicate the changes made to their software in a clear and concise way. This makes it easier for users of the software to understand the impact of each version and make informed decisions about when to upgrade.

## Package Versions

- cupertino_icons: ^1.0.2
- get: ^4.6.5
- flutter_screenutil: ^5.6.0
- flutter_svg: ^1.1.6
- flutter_bloc: ^8.1.1
- confetti: ^0.7.0
- camera: ^0.10.0+4
- dio: ^4.0.6
- http: ^0.13.5
- get_storage: ^2.0.3
- google_maps_flutter: ^2.2.1
- flutter_polyline_points: ^1.0.0
- geolocator: ^9.0.2
- motion_tab_bar_v2: ^0.2.6
- mobile_scanner: 2.1.0
- signature: ^5.3.0
- intl: ^0.18.0
- validators: ^3.0.0
- animated_bottom_navigation_bar: ^1.1.0
- vibration: ^1.7.6
- syncfusion_flutter_charts: ^20.4.38
- path_provider: ^2.0.12
- qr_code_scanner: ^1.0.1
- flutter_phone_direct_caller: ^2.1.1
- signalr_netcore: ^1.3.3
- onesignal_flutter: ^3.5.1
- url_launcher: ^6.1.10
- flutter_dotenv: ^5.0.1
- package_info_plus: ^3.1.0

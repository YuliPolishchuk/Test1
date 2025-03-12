# Production Build & Release Process

Female Invest uses [Expo Application Services](https://expo.dev) to automate the release process. To gain access to EAS, reach out to a fellow mobile app developer.

### Build Process

Login to Expo

```bash
expo login
```

Create a Production Build

For iOS:

```bash
eas build -p ios --profile production
```

For Android:

```bash
eas build -p android --profile productions
```

Using the --local Flag

For local builds that do not require remote Expo servers, you can use the --local flag:

Android:
```bash
eas build -p android --profile development --local
```

iOS:

```bash
eas build -p ios --profile development --local
```
This will build the app locally on your machine instead of using Expo's cloud services.

#  Deployment & Distribution

Android Release

Submit the app to Google Play using:

```bash
eas submit -p android --track production
```

iOS Release

Submit the app to the App Store using:

```bash
eas submit -p ios
```

# Testing & QA

Internal Testing (Development Build)

To test the development build locally, install it on devices using:

```bash
eas build -p android --profile development
```

For iOS:

```bash
eas build -p ios --profile development
```

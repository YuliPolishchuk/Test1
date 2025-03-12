# Production Build & Release Process

Female Invest uses [Expo Application Services](https://expo.dev) to automate the release process. To gain access to EAS, reach out to a fellow mobile app developer.

### Build Process

**Install the latest EAS CLI**

```bash
npm install -g eas-cli
```

**Log in to your Expo account**

```bash
eas login
```

You can check whether you are logged in by running `eas whoami`.

### Create a Production Build

For iOS:

```bash
eas build -p ios --profile production
```

For Android:

```bash
eas build -p android --profile production
```

Alternatively, you can use `--platform` all option to build for Android and iOS at the same time:

```bash
eas build --platform all --profile production
```


### Using the `--local` Flag

For local builds that do not require remote Expo servers, you can use the `--local` flag:

**Android:**

```bash
eas build -p android --profile production --local
```

**iOS:**

```bash
eas build -p ios --profile production --local
```

This will build the app locally on your machine instead of using Expo's cloud services.

#  Deployment & Distribution

If you have made it to this step, congratulations! Depending on which path you chose, you now either have a build that is ready to upload to an app store, or you have a build that you can install directly on an Android device/iOS Simulator.

**Android Release**

Submit the app to Google Play using:

```bash
eas submit -p android --profile production
```

**iOS Release**

Submit the app to the App Store using:

```bash
eas submit -p ios --profile production
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

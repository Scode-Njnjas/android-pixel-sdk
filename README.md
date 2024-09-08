# ConvertedIn Pixel SDK for Android

## Overview

ConvertedIn Pixel SDK is a powerful tool for Android applications that enables tracking and analysis of user events, push notifications management, and integration with the ConvertedIn platform.

## Features

- User identification
- Event tracking
- Push notification handling
- Automatic app open event logging
- Various e-commerce events (Add to Cart, Purchase, etc.)

## Installation

Add the following to your project's `build.gradle` file:

```gradle
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

Then, add the dependency to your app's `build.gradle`:

```gradle
dependencies {
    implementation 'com.github.Scode-Njnjas:android-pixel-sdk:latest_version'
}
```

## Usage

### Initialization

Initialize the SDK in your application's onCreate method:

```kotlin
ConvertedInSdk().initialize(context, "YOUR_PIXEL_ID", "YOUR_STORE_URL")
```

### User Identification

Identify a user with their email or phone number:

```kotlin
ConvertedInSdk().identifyUser(email = "user@example.com", phone = "1234567890", countryCode = "US")
```

### Tracking Events

Track custom events:

```kotlin
val products = arrayListOf(EventContent(/* product details */))
ConvertedInSdk().addEvent("custom_event", "USD", "10.99", products)
```

### Push Notifications

Handle push notification clicks:

```kotlin
ConvertedInSdk().onPushNotificationClicked("campaign_id_from_payload")
```

Save device token for push notifications:

```kotlin
ConvertedInSdk().saveDeviceToken("device_token")
```

## License

MIT

## Support

For any issues or questions, please contact [support@scodenjnja.store](support@scodenjnja.store).

# Forme — workout companion

A light workout tracker for web and Android. The web interface is bundled with Vite and packaged for Android with Capacitor.

## Run the web app

```sh
npm install
npm run dev
```

Open the local Vite URL printed by the command.

## Build the Android app

Install Android Studio and an Android SDK, then run:

```sh
npm run android
```

This builds the web assets, syncs them into the Capacitor Android project and opens Android Studio. To only refresh the Android project after web changes, run `npm run cap:sync`.

## Notifications

- Water reminders use scheduled local Android notifications, so reminders can arrive while the app is closed. Android notification permission is requested when reminders are enabled.
- Remote notifications use Capacitor Push Notifications and Firebase Cloud Messaging. Add your Firebase project's `google-services.json` to `android/app/`, then sync the Android project. A trusted server or Firebase Cloud Function is still needed to send production messages; never put Firebase Admin credentials in this app.
- This project uses the Android package ID registered in its Firebase config. The provided config is ignored by Git so it stays out of the public repository. After registering an Android device, use **Copy Firebase test token** in Settings to send a manual test from the Firebase console.

## What's included

- Personal workout split based on goals, experience, equipment and weekly availability.
- Session logging, small exercise illustrations, weekly progress and history.
- Daily water and step tracking, with manual steps and a foreground motion-sensor option in the web app.
- Installable web app and an Android Capacitor project.

## Account and device storage

The current sign-in and fitness data are stored in the browser/WebView on the current device. There is no secure server login, cloud backup or cross-device sync yet. Do not reuse a password from another service. Connect a backend authentication provider and server-side storage before using this as a multi-user product.

Workout suggestions are general fitness templates, not medical advice. Adapt them to your ability and seek qualified guidance for injuries or health concerns.


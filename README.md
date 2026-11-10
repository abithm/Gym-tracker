# Forme — workout companion

A light, installable web app for personal workout planning, workout logging, water tracking and steps. It is built with browser-native HTML, CSS and JavaScript, so it runs on the web and adapts to Android phone screens.

## Run it

Serve this folder over HTTPS or from `localhost` (service workers, installation and motion sensors need a secure browser context). For example, with Python installed:

```sh
python -m http.server 8000
```

Open `http://localhost:8000` on your computer. On Android, deploy the folder to an HTTPS static host and open it in Chrome. Use Chrome's **Install app** or **Add to Home screen** option to install it.

## What's included

- Create an account and sign in on the current device.
- Personalize goals, experience, available equipment and training days. The plan generates 2–6 weekly sessions with exercise, set and rep suggestions.
- Mark exercises and log completed gym sessions.
- Track daily water and step totals. Steps can be entered manually or counted from motion while the app is open on supported phones.
- Set hydration reminders while the app is open. Browser notification support varies.
- View weekly workout history and progress. The app shell is cached for offline access after its first visit.

## Account and device storage

This starter stores accounts, password digests and workout data in browser local storage. Accounts are local to one browser on one device; there is no server, cloud backup or cross-device sign-in. Do not use a password here that you rely on for another service. Before offering this as a multi-user product, connect a backend authentication provider and server-side data storage.

Workout suggestions are general fitness templates, not medical advice. Users should adapt them to their ability and seek qualified guidance for injuries or health concerns.


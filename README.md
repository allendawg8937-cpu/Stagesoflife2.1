# StagesOfLife 2.0

A clean, new foundation for the StagesOfLife platform. This project is independent of the original repository; no existing user data or code is modified.

## Project layout
- `android/` — Kotlin + Jetpack Compose Android application.
- `web/` — Angular + Firebase web application.
- `firebase/` — Firestore rules and Firebase configuration.
- `.github/workflows/` — separate Android and web CI workflows.

## First setup
1. Create a new Firebase project.
2. Enable Email/Password authentication.
3. Add a web app and copy its Firebase config into `web/src/environments/environment.ts`.
4. Register an Android app and provide its `google-services.json` in `android/app/` (never commit production secrets).
5. Review `firebase/firestore.rules`, then deploy with `firebase deploy --only firestore:rules`.
6. Build the web app with `cd web && npm ci && npm run build`.
7. Build Android with `cd android && ./gradlew assembleDebug`.

## Important
This is a secure starter foundation, not a migration of production accounts or a claim that Firebase is already configured. Do not copy real user data into a test Firebase project. Keep production secrets out of Git.

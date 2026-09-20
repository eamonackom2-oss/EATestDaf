# DeutschSprint — Build & verification

## Project
- 28 weeks / 168 lessons
- A1 → A2 → B1 → B2 + TestDaF preparation
- Course data is embedded in `app/src/main/assets/index.html` for offline use.
- Progress is stored locally with `localStorage`.
- Backup supports JSON export/import; automatic email/cloud sync is not included without a backend account.

## Android build
The project uses Android Gradle Plugin 8.7.3, Gradle 8.9, Java 17, compile/target SDK 35, and min SDK 23.

### Android Studio
Open the folder containing `settings.gradle`, wait for Gradle sync, then choose **Build → Build Bundle(s) / APK(s) → Build APK(s)**.

### GitHub Actions
The included `.github/workflows/build-apk.yml` builds the debug APK in the cloud. Push the project to a GitHub repository, open **Actions**, run **Build DeutschSprint APK**, then download the `DeutschSprint-debug-apk` artifact.

## Important test limitation
Static/project validation can be performed here, but a real Android emulator/device is required for final UI, audio, storage and installation validation.

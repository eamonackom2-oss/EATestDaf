# Easiest APK build — no Android Studio required

If you have a GitHub account, GitHub can build the APK for you in the cloud.

1. Create a new GitHub repository.
2. Upload the contents of this folder (`DeutschSprint_Expanded_Android`) to the repository.
3. Open the repository's **Actions** tab.
4. Select **Build DeutschSprint APK** and run it (or push to `main`, which starts it automatically).
5. Wait for the workflow to finish with a green check.
6. Open the completed workflow run and scroll to **Artifacts**.
7. Download **DeutschSprint-debug-apk** and unzip it. The APK is `app-debug.apk`.
8. Transfer the APK to an Android phone and install it.

This project contains a GitHub Actions workflow at `.github/workflows/build-apk.yml` that installs Java, Gradle, and Android SDK 35 automatically and builds the debug APK.

For a normal release APK suitable for wider distribution, a signing key is required; the workflow currently builds a debug APK for easy testing.


### Automated inspection (2026-09-19)
The project was inspected before packaging: 28 weeks / 168 lessons were validated; each lesson contains the expanded course schema (goal, grammar focus, vocabulary, model sentences, reading, listening, exercises, writing, speaking, self-check and answer key). The Android manifest, Gradle configuration, Java launcher and bundled assets were also checked. The web lesson renderer was corrected to match the expanded course schema and the course data is now embedded in the HTML so the APK does not depend on a fetch of a separate local asset.

Note: this environment does not have Android SDK/Gradle/ADB/emulator, so an actual APK build and device UI test could not be executed here.

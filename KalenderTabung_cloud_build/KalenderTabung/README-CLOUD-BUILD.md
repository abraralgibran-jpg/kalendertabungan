# Kalender Tabung — Cloud APK build

This package contains the original Android project plus a GitHub Actions workflow. It builds a debug APK in GitHub's cloud; Android Studio is not required on your laptop.

## Build steps
1. Create a **public** repository on GitHub (public repositories can use standard GitHub-hosted runners without consuming private-repository minutes, subject to GitHub policy/limits).
2. Upload the contents of this ZIP to the repository root, keeping the `KalenderTabung/` folder and `.github/` folder.
3. Open the repository's **Actions** tab and enable workflows if prompted.
4. Run **Build Kalender Tabung APK** using **Run workflow**, or push a commit to `main`.
5. Open the completed run and download the artifact named `KalenderTabung-debug-apk`.
6. Extract the artifact; install `app-debug.apk` on the Android phone.

The debug APK is for testing and is not a Play Store release. Keep the repository public only if you are comfortable making its source code public. Do not upload personal savings data; the ZIP contains source code, not your app's private runtime data.

The source project already includes Android WebView's `onShowFileChooser` callback and a JavaScript `Android.pickImage()` bridge. The workflow only automates cloud compilation; test photo selection on the phone after installing the APK.

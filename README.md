# Stock Book (Android)

Catering inventory app: stock (rice, oil, ghee and more), equipment, events, suppliers.
Data is stored on the phone only. It does not sync with the web page.

## Get the APK without installing anything (GitHub)
1. Create a free GitHub account and a new empty repository.
2. Upload every file in this folder to it, keeping the folder structure
   (including `.github/workflows/build-apk.yml`).
3. Open the repository's Actions tab, pick "Build APK", press Run workflow.
4. When it finishes (about 5 minutes), open the run and download `stock-book-apk`.
   Unzip it to get `app-debug.apk`.
5. Send the APK to your phone, open it, and allow "Install unknown apps" if asked.

## Build on your own computer instead
Needs Node 20+, JDK 21 and Android Studio.

    npm install
    npx cap add android
    npx cap sync android
    npx cap open android

In Android Studio use Build > Build APK(s). The file is in
`android/app/build/outputs/apk/debug/`.

## Changing the app
Everything lives in `www/index.html`. After editing, run `npx cap sync android` and rebuild.

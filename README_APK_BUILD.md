# Mashooque Diary Book — Native Android Project

**Package Name:** `com.mashooque.diarybook`  
**Target SDK:** Android 34 (Android 14)  
**Min SDK:** Android 26 (Android 8.0 Oreo)  
**Language:** Kotlin  
**UI Framework:** Jetpack Compose (Material 3)  
**Database:** Room (SQLite) with AES-256 EncryptedSharedPreferences  

---

## 🚀 How to Build the APK

### Method 1: Instant Cloud Build via GitHub (Easiest - 100% Free)
1. Push or upload this extracted folder to a new repository on [GitHub](https://github.com).
2. The pre-configured file `.github/workflows/build-apk.yml` will automatically build both:
   - `MashooqueDiaryBook-Debug.apk`
   - `MashooqueDiaryBook-Release.apk`
3. Go to the **Actions** tab on your GitHub repository.
4. Download the ready-to-install APK directly to your phone!

---

### Method 2: Android Studio (Windows / Mac / Linux)
1. Download & open [Android Studio](https://developer.android.com/studio).
2. Choose **Open** and select this directory.
3. Allow Gradle to sync dependencies.
4. Connect your Android phone with USB Debugging enabled, or select an emulator.
5. Click the green **Run (▶)** button, or go to **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. Android Studio will generate the APK at:  
   `app/build/outputs/apk/debug/app-debug.apk`.

---

### Method 3: Direct Build on Android Phone via Termux (No PC needed)
If you only have an Android phone:
1. Install **Termux** from F-Droid.
2. Run:
   ```bash
   pkg update && pkg install openjdk-17 git
   ```
3. Navigate to this folder in Termux and run:
   ```bash
   ./gradlew assembleDebug
   ```
4. Install the output APK directly from your phone's file manager!

---

## 🔒 Security Architecture
- **Room SQLite**: Structured offline diary storage.
- **MasterKey & EncryptedSharedPreferences**: AES256-GCM encryption for PIN & cryptographic seeds.
- **Zero Cloud Uploads**: 100% offline, private, and secure.

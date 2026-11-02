# Lift Log

Track weights (weight, reps and sets per set), walks and runs, with estimated calories burned,
weekly sets per muscle and a rough muscle gain or loss estimate. Plus a weekly training plan.

Standalone Capacitor app (iOS + Android), built the same way as NutriSnap. No server and no account:
everything is stored on the device. Use **Setup → Back up my data** to save a file you can restore later.

## iOS
```bash
npm install
npm run ios
```
Pick your phone, set your Team under Signing & Capabilities, press Run.

## Android
```bash
export JAVA_HOME="/Applications/Android Studio.app/Contents/jbr/Contents/Home"
export ANDROID_HOME=$HOME/Library/Android/sdk
cd android && ./gradlew assembleDebug
adb install -r app/build/outputs/apk/debug/app-debug.apk
```
Or `npm run android` and press Run in Android Studio.

## After editing `www/`
`npx cap sync`

## Link to NutriSnap
**Setup → Send to NutriSnap** saves a NutriSnap backup file with your workouts (one entry per day for weights,
one per walk or run). In NutriSnap open Profile → Restore and pick the file. Entries NutriSnap already has are skipped.

## Notes
- Calories use MET values and your body weight. Muscle change uses weekly hard sets per muscle. Both are estimates, not medical advice.
- The Android app uses Capacitor's default launcher icon.

တောင်သူ့အိမ် MM Crop Yield Calculator - Android Project

ပြင်ဆင်ထားသော Version
- versionCode: 3
- versionName: 1.2
- compileSdk: 36
- targetSdk: 36
- minSdk: 23
- Android Gradle Plugin: 8.13.2
- Gradle: 8.13
- Java: 17

မူရင်း HTML တွက်ချက်မှု၊ မှတ်တမ်း၊ မြန်မာ/English စနစ်နှင့် App Logo ကို မပြောင်းထားပါ။

GitHub Actions
- Push to main သို့မဟုတ် Actions > Build Android APK and Play Store AAB > Run workflow ဖြင့် Build လုပ်နိုင်သည်။
- Signing key မထည့်ရသေးလျှင် Debug APK တစ်ခုသာ ထုတ်ပေးမည်။
- Signing secrets ထည့်ပြီးလျှင် Signed Release APK နှင့် Play Store အတွက် AAB နှစ်မျိုးလုံး ထုတ်ပေးမည်။

Release signing အတွက် GitHub Repository > Settings > Secrets and variables > Actions တွင် အောက်ပါ Repository secrets ၄ ခု ထည့်ရန်လိုသည်။
1. ANDROID_KEYSTORE_BASE64
2. ANDROID_KEYSTORE_PASSWORD
3. ANDROID_KEY_ALIAS
4. ANDROID_KEY_PASSWORD

သတိပြုရန်
- release-key.jks / keystore ဖိုင်ကို GitHub repository ထဲသို့ မတင်ပါနှင့်။
- Keystore နှင့် password များကို လုံခြုံစွာ Backup ထားပါ။
- Password များကို Chat ထဲတွင် မပို့ပါနှင့်။
- Google Play တင်ရာတွင် AAB ကို အသုံးပြုပါ။ APKPure အတွက် Signed Release APK ကို အသုံးပြုပါ။

Local build command:
  gradle --no-daemon assembleDebug
  gradle --no-daemon assembleRelease bundleRelease

Output paths:
  app/build/outputs/apk/debug/app-debug.apk
  app/build/outputs/apk/release/app-release.apk
  app/build/outputs/bundle/release/app-release.aab

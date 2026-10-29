# मेरा Voice Assistant — Android प्रोजेक्ट

यह शुरुआती Android ऐप है। इसमें:
- हिंदी/अंग्रेज़ी SpeechRecognizer आधारित वॉइस कमांड
- स्क्रीन लॉक होने पर सुनने के लिए foreground service और स्थायी notification
- YouTube, WhatsApp, Instagram खोलने और Google पर खोजने के उदाहरण
- GitHub Actions से Debug APK बनाने की workflow

## ज़रूरी बात
- पहली बार ऐप खोलकर माइक्रोफ़ोन और नोटिफ़िकेशन की अनुमति दें।
- स्क्रीन लॉक होने से पहले ऐप में **Listening चालू करें** दबाएँ। Notification दिखाई देनी चाहिए।
- Xiaomi/Redmi में Settings → Apps → Manage apps → Mera Voice Assistant → Battery saver में **No restrictions** चुनना पड़ सकता है।
- Android/फोन की नीतियों के कारण लगातार माइक्रोफ़ोन सुनना हर डिवाइस पर गारंटी नहीं है। ऐप बंद/Force stop होने, फोन रीस्टार्ट होने या सिस्टम द्वारा सेवा रोके जाने पर फिर से चालू करना पड़ सकता है।
- कॉल करना, SMS भेजना, फोन लॉक करना जैसी संवेदनशील सुविधाएँ इस शुरुआती संस्करण में नहीं जोड़ी गई हैं। इन्हें अलग से सुरक्षित तरीके से जोड़ना होगा।
- SpeechRecognizer का ऑन-डिवाइस/नेटवर्क व्यवहार फोन और भाषा सेवाओं पर निर्भर करता है।

## APK GitHub से बनाना
1. इस ZIP को Extract करें।
2. नई GitHub repository बनाएँ।
3. ZIP के अंदर की फ़ाइलें और फ़ोल्डर repository के root में upload करें (`app`, `.github`, `build.gradle.kts`, `settings.gradle.kts` आदि)।
4. GitHub → Actions → Android APK Build workflow → Run workflow चलाएँ।
5. सफल run खोलें → Summary → Artifacts → `MeraVoiceAssistant-debug-apk` डाउनलोड करें।
6. ZIP extract करके `app-debug.apk` फ़ोन में कॉपी करें।

## लोकल बिल्ड
Android Studio में इस फ़ोल्डर को Open करें और Gradle Sync के बाद Build → Build APK(s) चुनें।

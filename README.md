# Route Tracker APK

## بناء الـ APK (من غير ما تنزّل Android Studio)
1. اعمل repo جديد على GitHub وارفع محتوى المجلد ده كله (الـ `.github` لازم يترفع).
2. افتح تبويب **Actions** ← **Build APK** ← **Run workflow** (بيشتغل لوحده كمان مع أي push على `main`).
3. بعد ما يخلص (~5-8 دقايق) نزّل **route-tracker-apk** من قسم Artifacts، فك الـ zip وهتلاقي `app-debug.apk`.
4. انقله للموبايل وثبّته (فعّل "تثبيت من مصادر غير معروفة").

## لو عدّلت الكود
عدّل `www/index.html` بس. لو غيّرت كلاسات Tailwind شغّل `npm install && npm run build:css` محليًا (الـ workflow بيعملها تلقائيًا).

## ملاحظات
- التطبيق بيشتغل أوفلاين بالكامل (Tailwind والخطوط محلية). الحفظ في `localStorage` على الجهاز.
- مزامنة Google/Firebase مش شغالة في الـ APK؛ استخدم **تصدير/استيراد JSON** من تبويب الإحصائيات للنسخ الاحتياطي ونقل البيانات.
- الـ APK ده Debug للاستخدام الشخصي. للنشر على Play Store محتاج Release APK/AAB موقّع.

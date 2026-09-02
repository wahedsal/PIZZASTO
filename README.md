# نشر موقع بيتزاستو على GitHub Pages

هذه الحزمة مفصولة إلى واجهتين:

- `index.html`: نسخة العملاء فقط، ولا تحتوي على لوحة الإدارة أو رمز دخول لها.
- `admin/index.html`: نسخة الإدارة فقط لتحديث توفر الآيس كريم.
- `availability.json`: ملف التوفر المشترك الذي تقرؤه نسخة العملاء.
- `omani-rial-symbol.png`: رمز الريال العُماني.

## 1. رفع الموقع

1. أنشئ مستودع GitHub عامًا، مثل `pizzasto-order`.
2. ارفع **محتويات هذه الحزمة** إلى جذر المستودع مع المحافظة على مجلد `admin`.
3. افتح إعدادات المستودع ثم `Pages`.
4. اختر `Deploy from a branch`، ثم الفرع `main` والمجلد `/(root)`، وبعدها احفظ.
5. انتظر حتى يظهر رابط GitHub Pages.

مرجع GitHub الرسمي: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

إذا كان اسم المستخدم `USERNAME` واسم المستودع `pizzasto-order`، فستكون الروابط:

- العملاء: `https://USERNAME.github.io/pizzasto-order/`
- الإدارة: `https://USERNAME.github.io/pizzasto-order/admin/`

لا يوجد في نسخة العملاء رابط ينقل إلى صفحة الإدارة.

## 2. إعداد صلاحية الإدارة

حتى تستطيع صفحة الإدارة تحديث `availability.json`:

1. من إعدادات حساب GitHub أنشئ **Fine-grained personal access token**.
2. اجعل وصول الرمز إلى مستودع `pizzasto-order` فقط.
3. امنح صلاحية المستودع `Contents: Read and write` فقط.
4. افتح رابط الإدارة، والصق الرمز في الحقل، وحدد الأنواع المتوفرة ثم اضغط الحفظ.

مرجع GitHub الرسمي: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens

رمز الوصول لا يُحفظ في المتصفح. لا ترسله إلى أي شخص، واحفظ رابط الإدارة لدى الإدارة فقط. وجود رابط الإدارة وحده لا يسمح بالتعديل من دون رمز GitHub الصالح.

## 3. تحديث التوفر اليومي

1. افتح رابط `/admin/`.
2. حدد أنواع الآيس كريم المتوفرة.
3. أدخل رمز GitHub واضغط `حفظ ونشر توفر اليوم`.
4. قد يستغرق ظهور التحديث في موقع العملاء من دقيقة إلى ثلاث دقائق.

لوحة الإدارة تحفظ اسم المستخدم واسم المستودع والفرع فقط لتسهيل الاستخدام التالي؛ لا تحفظ رمز الوصول.

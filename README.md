# LaslesVPN

صفحة هبوط متجاوبة لخدمة VPN، مبنية باستخدام HTML وSCSS، مع واجهة نظيفة وقائمة جانبية للجوال تعمل بـ CSS فقط بدون JavaScript.

## المميزات

- تصميم متجاوب مع مختلف أحجام الشاشات.
- هيدر ثابت `sticky` أثناء التمرير.
- قائمة برجر للجوال تعمل باستخدام `:target` في CSS.
- خلفية معتمة للقائمة الجانبية، وإغلاق تلقائي عند اختيار رابط أو النقر خارجها.
- أيقونات وشعارات SVG محلية داخل مجلد `images`.
- لا توجد سكربتات JavaScript داخل الصفحة.
- تنظيم التنسيقات في ملفات SCSS منفصلة لتسهيل الصيانة.

## التقنيات المستخدمة

- HTML5
- SCSS / Sass
- Bootstrap 5 عبر CDN للتنسيقات فقط
- خط Rubik من Google Fonts

## هيكل المشروع

```text
.
├── index.html
├── style.css
├── scss/
│   ├── style.scss
│   ├── _variables.scss
│   ├── _mixins.scss
│   ├── _base.scss
│   ├── _buttons.scss
│   ├── _components.scss
│   ├── _utilities.scss
│   └── _responsive.scss
├── images/
├── package.json
├── package-lock.json
└── .gitignore
```

## التشغيل

تثبيت الاعتماديات:

```bash
npm install
```

بناء ملف CSS:

```bash
npm run build:css
```

أو تشغيل المراقبة أثناء التطوير:

```bash
npm run watch:css
```

ثم افتح ملف `index.html` في المتصفح.

## ملاحظات

- `style.css` هو الملف الناتج عن تجميع SCSS، لذا يُفضّل التعديل على ملفات `scss/` ثم إعادة البناء.
- مجلد `node_modules` غير مرفوع إلى المستودع.
- الصور والأيقونات موجودة جميعها داخل مجلد `images`.

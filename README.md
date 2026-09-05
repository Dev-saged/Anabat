<div align="center">

# 🌟 أنيرا — Anira
### نظام تسجيل الإنابات الإنساني | Humanitarian Proxy Registration System

<img src="https://img.shields.io/badge/version-1.4.0-gold?style=for-the-badge"/>
<img src="https://img.shields.io/badge/offline-100%25-green?style=for-the-badge&logo=wifi"/>
<img src="https://img.shields.io/badge/zero-dependencies-blue?style=for-the-badge"/>
<img src="https://img.shields.io/badge/RTL-Arabic-red?style=for-the-badge"/>
<img src="https://img.shields.io/badge/mobile-first-orange?style=for-the-badge&logo=android"/>

</div>

---

## 🇸🇦 عربي

نظام ويب متكامل لتسجيل الإنابات في عمليات توزيع المساعدات الإنسانية — يعمل أوفلاين 100٪ كملف HTML واحد، بدون أي اعتمادية خارجية.

### ✨ المميزات الرئيسية

| الميزة | التفاصيل |
|--------|----------|
| 📝 **تسجيل سريع** | إدخال بيانات المستفيد والمنيب مع التنقل بـ Enter |
| 🔍 **كشف التكرار** | تحذير فوري عند إدخال هوية مسجّلة سابقاً |
| ↩️ **تراجع عن الحذف** | حذف فوري مع نافذة تراجع 5 ثوانٍ |
| 📂 **فلاتر متقدمة** | تصفية بالصلة، البلد، الشهر |
| 📄 **تصدير Excel / PDF** | للشهر الحالي أو تقرير شامل لكل الأشهر |
| ☁️ **نسخ تيليجرام** | رفع تلقائي عبر Bot API |
| 🌙 **وضع ليلي** | مع منع وميض عند الفتح |
| 💾 **مسودة تلقائية** | حفظ النموذج فوراً — لا تضيع البيانات |
| ♾️ **ترقيم صفحات ذكي** | 60 سجلاً ثم تحميل بالتمرير (IntersectionObserver) |
| 📊 **إحصائيات المنيبين** | Top 5 منيبين الأكثر استلاماً |
| 🌍 **خارج البلاد** | دعم تصنيف المستفيد خارج البلاد |
| 🔄 **مزامنة الأجهزة** | تصدير / استيراد JSON مع دمج ذكي |

---

## 🇬🇧 English

A complete offline-first web application for registering humanitarian aid proxy recipients. Single HTML file, zero dependencies, works 100% offline.

### ✨ Key Features

| Feature | Details |
|---------|---------|
| 📝 **Fast Entry** | Beneficiary & deputy data entry with Enter-key navigation |
| 🔍 **Duplicate Detection** | Real-time warning when an ID is already registered |
| ↩️ **Undo Delete** | Instant delete with 5-second undo toast |
| 📂 **Advanced Filters** | Filter by relation, country status, or month |
| 📄 **Excel / PDF Export** | Current month or comprehensive all-months report |
| ☁️ **Telegram Backup** | Automatic upload via Bot API |
| 🌙 **Dark Mode** | With FOUC-free persistence |
| 💾 **Auto-Draft Save** | Form persisted on every keystroke |
| ♾️ **Smart Pagination** | 60 records + IntersectionObserver lazy loading |
| 📊 **Deputy Statistics** | Top 5 most active field recipients |
| 🌍 **Abroad Flag** | Mark beneficiaries outside the country |
| 🔄 **Cross-Device Sync** | JSON export/import with smart deduplication merge |

---

## 🗂️ ملفات المشروع | Project Files

```
anira/
├── 📄 anira-system.html     ← التطبيق بالكامل (الملف الوحيد)
└── 📖 README.md             ← هذا الملف
```

---

## 🚀 نشر التطبيق على GitHub Pages

### الطريقة 1 — رفع مباشر من الهاتف (الأسهل)

```
1. افتح github.com من المتصفح
2. سجّل دخول ← انقر + New repository
3. اسم المستودع: anira  ← Public ← Create repository
4. انقر "uploading an existing file"
5. ارفع ملف anira-system.html
6. Commit changes
7. Settings ← Pages ← Branch: main ← Save
8. رابطك: https://USERNAME.github.io/anira/anira-system.html
```

### الطريقة 2 — عبر GitHub CLI (للمتقدمين)

```bash
# تثبيت gh CLI ثم:
gh repo create anira --public
git init && git add .
git commit -m "feat: Anira v1.4.0"
git push origin main
gh api repos/{owner}/anira/pages -X POST -f source[branch]=main
```

### الطريقة 3 — نشر على Vercel / Netlify (بديل)

```
1. vercel.com أو netlify.com
2. Import from GitHub ← اختر المستودع
3. يتم النشر تلقائياً مع رابط مخصص
```

> **⚠️ ملاحظة:** GitHub Pages مجاني للمستودعات العامة (Public).
> لحماية البيانات الحساسة، يُفضّل المستودع الخاص (Private) مع Vercel المجاني.

---

## ⚙️ المتطلبات التقنية | Tech Requirements

```
✅ متصفح حديث (Chrome 80+, Firefox 78+, Safari 14+)
✅ لا يوجد server، لا npm، لا build step
✅ يعمل كـ PWA قابل للتثبيت على الهاتف
```

---

## 🏗️ المكدس التقني | Tech Stack

```
HTML5 / CSS3 / Vanilla JavaScript
├── 🗄️  IndexedDB (تخزين أساسي) + localStorage (fallback)
├── 📦  محرك ZIP/DEFLATE مبني يدوياً (قراءة/كتابة XLSX)
├── 📡  Telegram Bot API (نسخ احتياطية)
├── 👁️  IntersectionObserver (ترقيم صفحات)
└── 📱  WebToApp (تغليف Android)
```

---

## 📱 تغليف كتطبيق Android

استخدم [WebToApp](https://github.com/shiaho777/web-to-app) لتحويل الملف لـ APK:

```yaml
targetSdk: 28
file: anira-system.html
permissions:
  - INTERNET (للنسخ عبر تيليجرام فقط)
```

---

## 📋 سجل الإصدارات | Changelog

| الإصدار | التاريخ | التغييرات |
|---------|---------|-----------|
| **v1.4.0** | 2026 | تراجع الحذف، فلاتر، ترقيم صفحات، إحصائيات، تصدير شامل، مسودة تلقائية |
| v1.3.0 | 2025 | وضع ليلي، تيليجرام، تحذير checksum، "نفس آخر منيب"، قفل ضغطة مزدوجة |
| v1.2.0 | 2025 | خارج البلاد، تخطيط متجاوب، إصلاح أرشفة عبر الأجهزة |

---

## 👨‍💻 المطوّر | Developer

**م. ساجد العبادلة** — تطوير حصري من الهاتف، بلا حاسوب أو IDE.

---

<div align="center">
<sub>مبني بـ ❤️ لخدمة العمل الإنساني الميداني</sub>
<br>
<sub>Built with ❤️ for humanitarian field operations</sub>
</div>

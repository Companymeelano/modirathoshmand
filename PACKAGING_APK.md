# 📱 راهنمای بسته‌بندی PWA به APK با PWABuilder

این پروژه (MeeLano V78) به‌عنوان یک **PWA پیشرفته** آماده شده و قابل نصب بر روی Android/iOS است.

---

## روش اول: سریع‌ترین راه (پیشنهادی) — PWABuilder وب

۱. وارد سایت [https://www.pwabuilder.com/](https://www.pwabuilder.com/) شوید.
۲. آدرس پروژه خود را وارد کنید (مثلاً: `https://your-domain.com/admin/`).
۳. PWABuilder به‌صورت خودکار `manifest.webmanifest` و `sw.js` را تحلیل می‌کند.
۴. گزینه **«Generate APK / AAB»** را انتخاب کنید.
۵. فایل APK دانلود و بر روی دستگاه اندروید نصب می‌شود.

---

## روش دوم: خط فرمان (CLI) — PWABuilder / Bubblewrap

### پیش‌نیازها (هم‌اکنون نصب شده):
- Node.js (`v22.22.3`)
- npm (`10.9.8`)
- pwabuilder CLI (`npm install -g @pwabuilder/cli`)

### مراحل:
```bash
# ۱. ورود به پوشه پروژه
cd meelano-v78-final-enhanced.zip  (پس از استخراج)

# ۲. تولید APK با PWABuilder
npx pwabuilder --platform android --start-url /admin/ --manifest /pwa/manifest.webmanifest --output ./apk-output/

# ۳. فایل APK در پوشه apk-output/ تولید می‌شود.
```

---

## فایل‌های آماده‌شده برای بسته‌بندی

| فایل | توضیح |
|---|---|
| `pwa/manifest.webmanifest` | مشخصات اپ (نام، آیکون، رنگ، start_url) |
| `pwa/sw.js` | Service Worker برای کار آفلاین |
| `pwa/icon-192.png` | آیکون ۱۹۲×۱۹۲ (تولید شده با AI) |
| `pwa/icon-512.png` | آیکون ۵۱۲×۵۱۲ (تولید شده با AI) |

---

## ⚠️ توجه مهم

این پروژه یک **سیستم PHP تحت وب** است. تبدیل آن به APK نیتیو (بدون مرورگر) نیازمند بازنویسی کامل با Flutter / Kotlin است. روش فوق بهترین و سریع‌ترین راه نصب موبایلی است.

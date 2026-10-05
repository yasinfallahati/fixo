<p align="center"><img src="docs/assets/hero.png" width="100%" alt="Fixo"></p>

# Fixo
### The local AI desk for Android repair counters

<p align="center">
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black">
<img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white">
<img src="https://img.shields.io/badge/ADB-3DDC84?style=for-the-badge&logo=android&logoColor=white">
<img src="https://img.shields.io/badge/pnpm-F69220?style=for-the-badge&logo=pnpm&logoColor=white">
</p>

<p align="center">
<img src="docs/assets/hero.png" width="48%">
<img src="docs/assets/features.png" width="48%">
</p>
<p align="center">
<img src="docs/assets/bench.webp" width="48%">
<img src="docs/assets/bench-tools.webp" width="48%">
</p>

Plug a phone over USB. Fixo talks ADB so the shop can flip Wi‑Fi, push Play installs, provision Pasargad VPN (`phone@id`), assist Gmail signup, run category diagnostics, and back up media/contacts to `Desktop/Fixo-Backups` — with chat + mic for hands-free steps. Themes: Galaxy · Emerald · Ice. Persian-first, English locale ready.

## Monorepo start

```bash
pnpm install
pnpm dev          # desktop + helpers
pnpm build && pnpm test && pnpm typecheck
```

Packages under `apps/desktop` + `packages/*`. Agent/MCP network helpers via `pnpm dev:mcp`.

| Bench job | Fixo action |
|-----------|-------------|
| Shop Wi‑Fi | Connect / forget / mobile-data gate |
| Apps | Play grid + APK / GitHub / URL |
| VPN | Lookup · create · renew · delete |
| Backup | Pause / resume / cancel |

---

## فارسی — فیکسو

**میزکار هوش‌مصنوعی برای تعمیرگاه موبایل اندروید.** گوشی را با USB وصل کنید؛ فیکسو از ADB برای وای‌فای فروشگاه، نصب اپ، VPN پاسارگاد، کمک ساخت جیمیل، عیب‌یابی دسته‌بندی‌شده و بکاپ عکس/ویدیو/مخاطب استفاده می‌کند. چت و میکروفون برای دستورات بدون دست؛ سه تم بصری.

### اجرا

```bash
pnpm install && pnpm dev
```

### ارزش برای پیشخوان

- کمتر جابه‌جایی بین ابزارهای پراکنده  
- UI فارسی برای تکنسین  
- داده و بکاپ روی همان سیستم فروشگاه می‌ماند  

نسخه فعلی: `1.0.3` در `package.json`.

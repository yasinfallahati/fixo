<p align="center">
  <img src="docs/assets/hero.png" alt="Fixo — Android Repair Desk" width="100%" />
</p>

<h1 align="center">Fixo</h1>

<p align="center">
  <strong>EN:</strong> Local AI desk for Android phone repair shops<br/>
  <strong>FA:</strong> میزکار هوش‌مصنوعی برای مغازه‌های تعمیرات اندروید
</p>

<p align="center">
  <a href="#english">English</a> ·
  <a href="#persian--فارسی">فارسی</a> ·
  <a href="#install--نصب">Install / نصب</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Android-ADB-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android ADB" />
  <img src="https://img.shields.io/badge/Node.js-22+-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/UI-Galaxy%20%7C%20Emerald%20%7C%20Ice-0EA5E9?style=for-the-badge" alt="Themes" />
  <img src="https://img.shields.io/badge/Locale-FA%20%2B%20EN-F59E0B?style=for-the-badge" alt="Bilingual" />
</p>

---

<p align="center">
  <img src="docs/assets/bench.webp" alt="Fixo Bench panel" width="48%" />
  &nbsp;
  <img src="docs/assets/bench-tools.webp" alt="Fixo tools and backup" width="48%" />
</p>

<p align="center">
  <img src="docs/assets/features.png" alt="Wi-Fi · VPN · Backup" width="92%" />
</p>

---

<a id="english"></a>

## English

### What is Fixo?
**Fixo** is a local desktop agent for Android repair counters. Connect a phone over USB (ADB), then manage shop Wi‑Fi, install apps from Play, provision Pasargad VPN (`phone@id`), assist Gmail signup, run phone diagnostics, and back up photos / videos / contacts — with Persian-first UI and English locale support.

### Highlights
| Area | What you get |
|------|----------------|
| **Shop network** | Toggle Wi‑Fi, connect/forget shop SSID, mobile-data gate before Play install |
| **Apps** | One-tap Play install grid + manual sources (model search, APK, GitHub, URL) |
| **VPN** | Pasargad lookup / create / renew / delete · sequential suggested shop id · username `0912…@id` |
| **Gmail** | Assisted signup flow on the connected phone |
| **Phone settings** | Category diagnostics: detect / fix / technician guides |
| **Backup** | Media + contacts to `Desktop/Fixo-Backups` with pause / resume / cancel |
| **Agent** | Chat + voice mic for hands-free repair commands |
| **Themes** | Galaxy · Emerald · Ice |

### Stack
```
apps/desktop          Express API + Vite React UI + local agent
packages/mcp-network  ADB network / Wi-Fi / mobile data
packages/mcp-apps     Play install, backup, Pasargad, Gmail, phone settings
packages/shared       Shared Zod schemas
```

### Quick start
```bash
git clone https://github.com/yasinfallahati/fixo.git
cd fixo
pnpm install
cp .env.example .env   # fill keys
pnpm --filter @fixo/desktop build
pnpm --filter @fixo/desktop start
```
Open **http://127.0.0.1:8787**

### Update later
```bash
cd fixo
git pull origin main
pnpm install
pnpm --filter @fixo/desktop build
pnpm --filter @fixo/desktop start
```

### Environment (`.env`)
| Variable | Purpose |
|----------|---------|
| `OPENAI_API_KEY` | Chat agent |
| `SHOP_WIFI_SSID` / `SHOP_WIFI_PASSWORD` | Shop Wi‑Fi connect / forget |
| `PASARGAD_BASE_URL` / `PASARGAD_API_KEY` | Pasargad / PasarGuard panel |
| `PORT` | Optional API port (default `8787`) |

> Never commit real secrets. Keep `.env` local.

### Requirements
- Node.js **22+** and **pnpm 9+**
- `adb` on `PATH` (Android platform-tools)
- USB debugging enabled on the phone

---

<a id="persian--فارسی"></a>

## فارسی

### فیکسو چیست؟
**Fixo** میزکار محلی برای کانتر تعمیرات اندروید است. گوشی را با USB (ADB) وصل کن؛ بعد وای‌فای مغازه، نصب از پلی، VPN پاسارگاد (`شماره@شناسه`)، کمک ساخت جیمیل، عیب‌یابی تنظیمات گوشی و بک‌آپ عکس/فیلم/مخاطبین را از یک UI فارسی (با زبان انگلیسی) مدیریت کن.

### قابلیت‌ها
| بخش | کار |
|-----|-----|
| **شبکه مغازه** | روشن/خاموش وای‌فای، وصل/فراموش SSID مغازه، چک اینترنت قبل از نصب |
| **برنامه‌ها** | گرید نصب سریع از پلی + نصب دستی |
| **VPN** | جستجو / ساخت / تمدید / حذف · چیپ شناسه ترتیبی · نام `۰۹۱۲…@شناسه` |
| **جیمیل** | کمک ساخت حساب روی گوشی وصل‌شده |
| **تنظیمات گوشی** | تشخیص / رفع / راهنمای تعمیرکار |
| **بک‌آپ** | رسانه + مخاطبین در `Desktop/Fixo-Backups` با توقف/ادامه/لغو |
| **ایجنت** | چت و میکروفون برای دستورهای تعمیر |
| **تم** | کهکشان · زمردی · یخی |

### اجرای سریع
```bash
git clone https://github.com/yasinfallahati/fixo.git
cd fixo
pnpm install
cp .env.example .env   # کلیدها را پر کن
pnpm --filter @fixo/desktop build
pnpm --filter @fixo/desktop start
```
آدرس: **http://127.0.0.1:8787**

### آپدیت بعدی
```bash
cd fixo
git pull origin main
pnpm install
pnpm --filter @fixo/desktop build
pnpm --filter @fixo/desktop start
```

---

<a id="install--نصب"></a>

## Install / نصب

### Windows (CMD)
```cmd
winget install --id Git.Git -e --source winget --accept-package-agreements --accept-source-agreements
winget install --id OpenJS.NodeJS.LTS -e --source winget --accept-package-agreements --accept-source-agreements
```
بستن و باز کردن CMD، سپس:
```cmd
npm install -g pnpm@9
cd %USERPROFILE%\Desktop
git clone https://github.com/yasinfallahati/fixo.git
cd fixo
pnpm install
copy .env.example .env
notepad .env
pnpm --filter @fixo/desktop build
pnpm --filter @fixo/desktop start
```

### Linux (Ubuntu)
```bash
sudo apt update && sudo apt install -y git curl
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs
sudo npm install -g pnpm@9
cd ~/Desktop
git clone https://github.com/yasinfallahati/fixo.git
cd fixo
pnpm install
cp .env.example .env
nano .env
pnpm --filter @fixo/desktop build
pnpm --filter @fixo/desktop start
```

### ADB
Install [Android platform-tools](https://developer.android.com/tools/releases/platform-tools) and put `adb` on your `PATH`.

---

## License / مجوز
Private repair-shop tooling — keep API keys and shop Wi‑Fi passwords out of git.

<p align="center">
  <sub>Built for the bench · ساخته‌شده برای میز تعمیرات</sub>
</p>

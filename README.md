# TradeX Desktop

**Download:** [macOS](https://github.com/omiraclex/TradeX-downloads/raw/main/TradeX-User-mac.zip) · [Windows](https://github.com/omiraclex/TradeX-downloads/raw/main/TradeX-User-windows.zip)

For active TradeX members only — sign in at https://tradex-members.web.app first.


## English

TradeX User runs on **your own computer** (Mac or Windows) and places TradeX signals on **your own IBKR account**. It never sees your IBKR password: you sign in to IBKR yourself, and TradeX only talks to IB Gateway / TWS running on your computer.

### One-time setup
Nothing to install except IBKR's own app — Python and everything TradeX needs is already inside this folder.

1. **IB Gateway** (recommended) or TWS — https://www.interactivebrokers.com/en/trading/ibgateway-stable.php
2. In IB Gateway: **Configure → Settings → API → Settings**
   - tick **Enable ActiveX and Socket Clients**
   - untick **Read-Only API**
   - keep **Socket port** as is (4001 live · 4002 paper)
   - add `127.0.0.1` to **Trusted IPs**
3. Sign in on **https://tradex-members.web.app** and link your subscription (the `/link` step with the Telegram bot).
4. On the website, set your trading settings: SPX and/or company signals, contracts, daily limits, and exit mode.

### Every trading day
1. Open IB Gateway and log in (**paper** first is recommended).
2. Start TradeX User:
   - **Mac:** double-click `start.command`. If macOS says it can't be opened: **System Settings → Privacy & Security**, scroll down, click **Open Anyway** next to the blocked item, then start `start.command` again (repeat once if it asks again for `python3`).
   - **Windows:** double-click `start.bat`. If SmartScreen appears: **More info → Run anyway**.
3. The first time, enter your member email and the code it sends you. After that you stay signed in.
4. Leave the window open during the session. Your status shows on the website.

### How it trades
- **Entry:** a limit order near the live price — never a market order. It skips the trade if the price is more than 15% above the signal price or the spread is too wide.
- **Exit, auto mode:** you exit together with TradeX's central manager (the same rules the owner's executor uses), whether or not the owner takes the trade.
- **Exit, manual mode:** your own take-profit / stop-loss / trailing stop from the website.
- **Safety net:** −50% hard stop, flat at 15:55 ET on expiry day, and your own rules if the central manager goes silent.

Close it with **Ctrl+C**. Sign out: run `start.command --logout` (Mac) or `start.bat --logout` (Windows).

---

## العربية

يعمل TradeX User على **جهازك أنت** (ماك أو ويندوز) وينفّذ إشارات TradeX على **حسابك في IBKR**. لا يطّلع البرنامج على كلمة مرور IBKR أبداً: أنت تسجّل الدخول بنفسك، والبرنامج يتصل فقط بـ IB Gateway / TWS على جهازك.

### الإعداد لأول مرة
لا تحتاج تثبيت أي شيء سوى برنامج IBKR نفسه — Python وكل ما يحتاجه TradeX موجود داخل هذا المجلد.

1. ثبّت **IB Gateway** (يُنصح به) أو TWS.
2. في IB Gateway افتح: **Configure → Settings → API → Settings**
   - فعّل **Enable ActiveX and Socket Clients**
   - ألغِ **Read-Only API**
   - اترك رقم المنفذ كما هو (4001 حقيقي · 4002 تجريبي)
   - أضف `127.0.0.1` إلى **Trusted IPs**
3. سجّل الدخول في **https://tradex-members.web.app** واربط اشتراكك (خطوة `/link` مع بوت تيليجرام).
4. من الموقع اضبط إعداداتك: إشارات SPX و/أو الشركات، عدد العقود، الحد اليومي، وطريقة الخروج.

### كل يوم تداول
1. افتح IB Gateway وسجّل الدخول (يُنصح بالحساب **التجريبي** أولاً).
2. شغّل البرنامج:
   - **ماك:** انقر مرتين على `start.command`. إذا ظهرت رسالة أن الملف لا يمكن فتحه: افتح **إعدادات النظام ← الخصوصية والأمان**، انزل للأسفل واضغط **Open Anyway** بجانب العنصر المحظور، ثم شغّل `start.command` مرة أخرى (كرّر مرة إذا طلبها لـ `python3`).
   - **ويندوز:** انقر مرتين على `start.bat`. إذا ظهرت رسالة SmartScreen: **More info ← Run anyway**.
3. في المرة الأولى أدخل بريدك والرمز الذي يصلك، وبعدها يبقى الدخول محفوظاً.
4. اترك النافذة مفتوحة طوال الجلسة، وستظهر حالتك في الموقع.

### طريقة التنفيذ
- **الدخول:** أمر محدد السعر قريب من السعر الحالي، وليس أمراً بسعر السوق أبداً. يتجاوز البرنامج الصفقة إذا ارتفع السعر أكثر من 15% فوق سعر الإشارة أو كان الفارق واسعاً.
- **الخروج التلقائي:** تخرج مع المدير المركزي لـ TradeX، وهي القواعد نفسها التي يستخدمها منفّذ المالك، سواء أخذ المالك الصفقة أم لا.
- **الخروج اليدوي:** هدف الربح ووقف الخسارة والوقف المتحرك الخاص بك من الموقع.
- **شبكة الأمان:** وقف إجباري عند −50%، وإغلاق الصفقات الساعة 15:55 بتوقيت نيويورك في يوم الانتهاء، وتُطبَّق قواعدك أنت إذا توقف المدير المركزي عن الإرسال.

للإيقاف اضغط **Ctrl+C**. لتسجيل الخروج: `start.command --logout` (ماك) أو `start.bat --logout` (ويندوز).

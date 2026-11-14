# TradeX Desktop

**Download:** [macOS](https://github.com/omiraclex/TradeX-downloads/raw/main/TradeX-User-mac.zip) · [Windows](https://github.com/omiraclex/TradeX-downloads/raw/main/TradeX-User-windows.zip)

For active TradeX members only — sign in at https://tradex-members.web.app first.


## English

TradeX Desktop runs on **your own computer** (Mac or Windows) and places TradeX signals on **your own IBKR account**. It never sees your IBKR password: you sign in to IBKR yourself, and TradeX only talks to IB Gateway / TWS running on your computer.

### One-time setup
Nothing to install except IBKR's own app — everything TradeX needs is already inside the app.

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
2. Open TradeX:
   - **Mac:** double-click **TradeX** (drag it to Applications first if you like). The first time macOS says it can't verify it: click **Done**, then **System Settings → Privacy & Security**, scroll down, click **Open Anyway** → **Open**. Only needed once.
   - **Windows:** double-click **TradeX.bat**. If SmartScreen appears: **More info → Run anyway**.
3. The first time, enter your member email and the code it sends you in the TradeX window. After that you stay signed in.
4. Keep the window open during the session. Four green lights = signed in, IB Gateway connected, TradeX signals online, auto-trading on.

### How it trades
- **Entry:** a limit order near the live price — never a market order. It skips the trade if the price is more than 15% above the signal price or the spread is too wide.
- **Exit, auto mode:** you exit together with TradeX's central manager (the same rules the owner's executor uses), whether or not the owner takes the trade.
- **Exit, manual mode:** your own take-profit / stop-loss / trailing stop from the website.
- **Safety net:** −50% hard stop, flat at 15:55 ET on expiry day, and your own rules if the central manager goes silent.

Press **Stop** or close the window to stop. **Sign out** is at the bottom of the window.

---

## العربية

يعمل TradeX Desktop على **جهازك أنت** (ماك أو ويندوز) وينفّذ إشارات TradeX على **حسابك في IBKR**. لا يطّلع البرنامج على كلمة مرور IBKR أبداً: أنت تسجّل الدخول بنفسك، والبرنامج يتصل فقط بـ IB Gateway / TWS على جهازك.

### الإعداد لأول مرة
لا تحتاج تثبيت أي شيء سوى برنامج IBKR نفسه — كل ما يحتاجه TradeX موجود داخل التطبيق.

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
2. افتح TradeX:
   - **ماك:** انقر مرتين على **TradeX** (يمكنك سحبه إلى مجلد التطبيقات أولاً). في المرة الأولى سيقول النظام إنه لا يستطيع التحقق منه: اضغط **تم**، ثم **إعدادات النظام ← الخصوصية والأمان**، انزل للأسفل واضغط **Open Anyway** ← **Open**. مرة واحدة فقط.
   - **ويندوز:** انقر مرتين على **TradeX.bat**. إذا ظهرت رسالة SmartScreen: **More info ← Run anyway**.
3. في المرة الأولى أدخل بريدك والرمز الذي يصلك داخل نافذة TradeX، وبعدها يبقى الدخول محفوظاً.
4. اترك النافذة مفتوحة طوال الجلسة. أربعة أضواء خضراء = تم الدخول، IB Gateway متصل، إشارات TradeX تعمل، التداول الآلي يعمل.

### طريقة التنفيذ
- **الدخول:** أمر محدد السعر قريب من السعر الحالي، وليس أمراً بسعر السوق أبداً. يتجاوز البرنامج الصفقة إذا ارتفع السعر أكثر من 15% فوق سعر الإشارة أو كان الفارق واسعاً.
- **الخروج التلقائي:** تخرج مع المدير المركزي لـ TradeX، وهي القواعد نفسها التي يستخدمها منفّذ المالك، سواء أخذ المالك الصفقة أم لا.
- **الخروج اليدوي:** هدف الربح ووقف الخسارة والوقف المتحرك الخاص بك من الموقع.
- **شبكة الأمان:** وقف إجباري عند −50%، وإغلاق الصفقات الساعة 15:55 بتوقيت نيويورك في يوم الانتهاء، وتُطبَّق قواعدك أنت إذا توقف المدير المركزي عن الإرسال.

للإيقاف اضغط **Stop** أو أغلق النافذة. **Sign out** في أسفل النافذة.

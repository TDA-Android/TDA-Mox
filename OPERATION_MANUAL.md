# TDA Mox V1 - Operation Manual & Guidelines / دليل التشغيل والإرشادات

> **Notice / تنويه هام:** 
> **[EN]:** This manual is for reference only. The user has full freedom and absolute authority to set up, transfer, and work with the environment, tools, and applications inside `/data/local/tmp` or any path that suits their device structure without being forced to copy heavy tools into the main repository.
> **[AR]:** هذا الدليل مرجعي فقط. المستخدم له مطلق الحرية وكامل الصلاحية في إعداد، نقل، والعمل بالبيئة والأدوات والتطبيقات داخل مسار `/data/local/tmp` أو أي مسار يناسب هيكلة جهازه دون إجبار على نسخ أدوات ضخمة داخل المستودع الأساسي.

---

## 1. Environment Setup & Core Tools / إعداد البيئة والأدوات الأساسية
* **[EN]:** The platform integrates essential binaries and tools including Python, Java, Llama, Dumpsys, Toybox, and Busybox.
* **[AR]:** تدمج المنصة الملفات التنفيذية والأدوات الأساسية بما في ذلك Python و Java و Llama و Dumpsys و Toybox و Busybox.
* **[EN]:** Busybox is manually installed in `/data/local/tmp/busybox` and mapped via environment variable `B`.
* **[AR]:** يُفضل تثبيت Busybox يدوياً في `/data/local/tmp/busybox` وربطه عبر متغير البيئة `B`.
* **[EN]:** Toybox is located at `/system/bin/toybox` and can be mapped via environment variable `T`.
* **[AR]:** يوجد Toybox في `/system/bin/toybox` ويمكن ربطه عبر متغير البيئة `T`.
* **[EN]:** System data collection tool `dumpsys` can be configured as an alias to `/system/bin/dumpsys`.
* **[AR]:** يمكن تكوين أداة جمع بيانات النظام `dumpsys` كاسم مستعار (alias) لـ `/system/bin/dumpsys`.

## 2. Phase 1: Exploration & Work Environment Preparation / المرحلة 1: الاستكشاف وإعداد بيئة العمل
* **[EN]:** Environment variables and paths can be verified using commands like `echo $B` and `echo $T`.
* **[AR]:** يتم التحقق من متغيرات البيئة والمسارات باستخدام أوامر مثل `echo $B` و `echo $T`.
* **[EN]:** File types and characteristics are inspected using `$T file` or `$B file`.
* **[AR]:** فحص أنواع الملفات وخصائصها يتم باستخدام `$T file` أو `$B file`.
* **[EN]:** Directory contents and listings are managed using commands such as `$T ls -la`, `$B ls -la`, and `$B ls -lhS`.
* **[AR]:** إدارة محتويات الدليل والقوائم باستخدام أوامر مثل `$T ls -la`، `$B ls -la`، و `$B ls -lhS`.
* **[EN]:** Process status and system uptime are monitored using `ps aux` and `uptime`.
* **[AR]:** مراقبة حالة العمليات وقت تشغيل النظام باستخدام `ps aux` و `uptime`.

## 3. Android Package Management & System Operations (PM & AM) / إدارة حزم أندرويد والعمليات النظامية
* **[EN]:** Installed packages are listed using `pm list packages`, and package installation paths are retrieved with `pm path`.
* **[AR]:** سرد الحزم المثبتة باستخدام `pm list packages`، واسترجاع مسارات تثبيت الحزم بـ `pm path`.
* **[EN]:** Permissions and states of the application package `com.maestro.tda` are inspected using `dumpsys package` queries.
* **[AR]:** فحص الأذونات وحالات حزمة التطبيق `com.maestro.tda` باستخدام استعلامات `dumpsys package`.
* **[EN]:** System hardware metrics and app resource consumption are tracked via `dumpsys battery` and `dumpsys meminfo com.maestro.tda`.
* **[AR]:** تتبع مقاييس أجهزة النظام واستهلاك موارد التطبيق عبر `dumpsys battery` و `dumpsys meminfo com.maestro.tda`.
* **[EN]:** Global settings and activities are manipulated using `settings put global airplane_mode_on` and Activity Manager commands like `am start`.
* **[AR]:** التلاعب بالإعدادات العامة والأنشطة باستخدام `settings put global airplane_mode_on` وأوامر مدير الأنشطة مثل `am start`.

## 4. File Operations, Compression, & Search / عمليات الملفات، الضغط، والبحث
* **[EN]:** Disk blocks and large files are copied efficiently using `dd if=/source of=/dest bs=4M`.
* **[AR]:** نسخ كتل القرص والملفات الكبيرة بكفاءة باستخدام `dd if=/source of=/dest bs=4M`.
* **[EN]:** Archives are compressed and extracted using standard `tar -czf`, `tar -xzf`, and `unzip` utilities.
* **[AR]:** ضغط الأرشيفات واستخراجها باستخدام أدوات `tar -czf`، `tar -xzf`، و `unzip`.
* **[EN]:** File searching and pattern matching across directories are performed using `find /sdcard -name "*.apk"` and `grep -r`.
* **[AR]:** البحث عن الملفات ومطابقة النماذج عبر الدلائل باستخدام `find /sdcard -name "*.apk"` و `grep -r`.
* **[EN]:** File integrity and verification are ensured using `sha256sum`.
* **[AR]:** ضمان سلامة الملفات والتحقق منها باستخدام `sha256sum`.

## 5. Binary Analysis & Reverse Engineering / تحليل الملفات الثنائية والهندسة العكسية
* **[EN]:** Shared libraries and binaries are analyzed for strings and embedded endpoints using `strings /path/to/lib.so`.
* **[AR]:** تحليل المكتبات المشتركة والملفات الثنائية للنصوص ونقاط النهاية المضمنة باستخدام `strings /path/to/lib.so`.
* **[EN]:** API keys and URLs are extracted using regex patterns with `strings` and `grep`.
* **[AR]:** استخراج مفاتيح API وعناوين URLs باستخدام أنماط التعبيرات المنتظمة (regex) مع `strings` و `grep`.
* **[EN]:** Custom unpacking workflows combine `cp`, `gunzip`, and `tar` to process compressed binary containers.
* **[AR]:** دمج `cp` و `gunzip` و `tar` في مسارات العمل الخاصة بفك الحاويات الثنائية المضغوطة.

## 6. Local Artificial Intelligence & Llama Integration / الذكاء الاصطناعي المحلي وتكامل Llama
* **[EN]:** Local GGUF models are executed via command-line inference using `./llama-cli` with `LD_LIBRARY_PATH=.`.
* **[AR]:** تنفيذ نماذج GGUF المحلية عبر الاستدلال من سطر الأوامر باستخدام `./llama-cli` مع `LD_LIBRARY_PATH=.`.
* **[EN]:** Local background API servers are launched using `./llama-server` on port `8080` with background persistence (`nohup` and `&`).
* **[AR]:** إطلاق خوادم API المحلية في الخلفية باستخدام `./llama-server` على المنفذ `8080` مع استمرارية الخلفية (`nohup` و `&`).
* **[EN]:** Server endpoints are tested using HTTP POST requests via `wget`, and processes can be terminated using `pkill -f llama-server`.
* **[AR]:** اختبار نقاط نهاية الخادم باستخدام طلبات HTTP POST عبر `wget`، وإنهاء العمليات باستخدام `pkill -f llama-server`.

## 7. System Monitoring & Diagnostics / مراقبة النظام والتشخيص
* **[EN]:** Active network connections are monitored using `netstat -an | grep ESTABLISHED`.
* **[AR]:** مراقبة اتصالات الشبكة النشطة باستخدام `netstat -an | grep ESTABLISHED`.
* **[EN]:** Top CPU-consuming processes are sorted and displayed using customized `ps` commands.
* **[AR]:** فرز وعرض العمليات الأكثر استهلاكاً للوحدة المركزية باستخدام أوامر `ps` المخصصة.
* **[EN]:** Device thermal status is monitored by reading temperature zones from `/sys/class/thermal/thermal_zone*/temp`.
* **[AR]:** مراقبة حالة حرارة الجهاز عن طريق قراءة مناطق الحرارة من `/sys/class/thermal/thermal_zone*/temp`.
* **[EN]:** System load averages and logs are tracked using `uptime`, `cat /proc/loadavg`, and `logcat`.
* **[AR]:** تتبع متوسطات حمل النظام والسجلات باستخدام `uptime`، `cat /proc/loadavg`، و `logcat`.

## 8. Environment Tools, Python, & GitHub Integration / أدوات البيئة، Python، وتكامل GitHub
* **[EN]:** Runtime versions can be verified via `java -version`, `python3 --version`, and `pip list`.
* **[AR]:** التحقق من إصدارات بيئات التشغيل عبر `java -version`، `python3 --version`, و `pip list`.
* **[EN]:** Rely on downloading files, scripts, and software resources directly from GitHub repositories instead of local package installation.
* **[AR]:** الاعتماد على تنزيل الملفات، السكربتات، والموارد البرمجية مباشرة من مستودعات GitHub بدلاً من تثبيت الحزم محلياً.
* **[EN]:** APK badging and metadata are inspected using `aapt2 dump badging`.
* **[AR]:** فحص شارات APK والبيانات الوصفية باستخدام `aapt2 dump badging`.
* **[EN]:** Code repositories and file paths are queried programmatically via GitHub Search API endpoints using `wget` and `grep`.
* **[AR]:** الاستعلام عن مستودعات الكود ومسارات الملفات برمجياً عبر نقاط نهاية API لبحث GitHub باستخدام `wget` و `grep`.

## 9. Reference Directory Structure & Suggested Paths / هيكل الدليل المرجعي والمسارات المقترحة
* **[EN]:** **Package Identity:** `com.maestro.tda`
* **[AR]:** **معرف الحزمة:** `com.maestro.tda`
* **[EN]:** **Busybox Binary:** `/data/local/tmp/busybox`
* **[AR]:** **ملف Busybox الثنائي:** `/data/local/tmp/busybox`
* **[EN]:** **Llama Binaries:** `/data/local/tmp/inspect/llama_extracted/`
* **[AR]:** **ملفات Llama الثنائية:** `/data/local/tmp/inspect/llama_extracted/`
* **[EN]:** **Android Toolchain:** `/data/local/tmp/toolchain/android-tools/`
* **[AR]:** **أدوات أندرويد:** `/data/local/tmp/toolchain/android-tools/`
* **[EN]:** **Predefined Shell Aliases:** Custom shortcuts such as `top_cpu`, `check_temp`, `netwatch`, and `clean_logs` for rapid execution.
* **[AR]:** **الأسماء المستعارة لسطر الأوامر:** اختصارات مخصصة مثل `top_cpu`، `check_temp`، `netwatch`, و `clean_logs` للتنفيذ السريع.

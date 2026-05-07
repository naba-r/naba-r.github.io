# دليل فهم مديري الحزم في لينكس

## من حفظ الأوامر إلى فهم المنطق

مديرو الحزم في لينكس لا ينبغي التعامل معهم كقائمة أوامر للحفظ، لأن هذا يخلق معرفة هشة تنهار عند أول اختلاف بين التوزيعات. الفهم الحقيقي يبدأ عندما تدرك أن هذه الأدوات ليست أوامر متفرقة، بل أنظمة تفكير مختلفة تؤدي الوظيفة نفسها.

**القاعدة الذهبية:** إذا فهمت المنطق، فلن تحتاج إلى الحفظ.

## لماذا توجد عدة مديري حزم؟

السؤال الطبيعي الذي يطرحه كل مبتدئ هو: لماذا لا يوجد مدير حزم واحد فقط لكل توزيعات لينكس؟

الجواب يشبه تمامًا سبب وجود لغات متعددة بين البشر: ليست المشكلة في عدم الاتفاق، بل في اختلاف البيئات والاحتياجات التي نشأت فيها هذه الأدوات.

كل مدير حزم وُلد داخل:

- مجتمع مختلف
- احتياجات مختلفة  
- فلسفة مختلفة في التعامل مع النظام

## الفلسفات الأربع الكبرى

### APT في Debian و Ubuntu

**البيئة:** الاستقرار، الوضوح، التدرّج، تجنّب المفاجآت

**الفلسفة:** الأفضل أن يكون الأمر واضحًا وآمنًا، لا سريعًا وغامضًا.

لماذا يستخدم كلمات كاملة؟

```
apt install
apt remove
apt update
```

لأن الوضوح أهم من الاختصار.

### DNF في Fedora و RHEL

**البيئة:** الشركات، الخوادم، البيئات الإنتاجية

**الفلسفة:** لا يكفي أن تعمل، يجب أن تعرف ماذا حدث وكيف تعود للخلف.

الميزة المميزة:

```
dnf history
dnf history undo last
```

التتبع والتراجع بسهولة.

### Zypper في openSUSE

**البيئة:** الدقة، الهندسة، المعاملات المحسوبة

**الفلسفة:** ليس كل تحديث هو نفس الشيء.

التفريق الواضح:

```
zypper patch
zypper update
zypper dup
```

عقلية المحاسب الدقيق.

### Pacman في Arch Linux

**البيئة:** البساطة، الشفافية، السيطرة الكاملة

**الفلسفة:** المستخدم مسؤول، لا سحر، لا إخفاء.

الاختصار الشديد:

```
pacman -S
pacman -Q
pacman -R
```

الجرّاح لا يشرح، بل ينفذ مباشرة.

## العالم الخارجي والداخلي

### النموذج العقلي الأساسي

هناك دائمًا عالمان:

**العالم الخارجي:** المستودعات على الإنترنت - الحزم المتاحة للتنزيل

**العالم الداخلي:** جهازك - الحزم المثبتة فعليًا وقاعدة البيانات المحلية

### المخطط البصري

```
الإنترنت - المستودعات
        |
        | المزامنة والتنزيل
        v
جهازك - الحزم المثبتة
      - قاعدة البيانات المحلية
```

### السؤال الذهبي قبل أي أمر

**هل أتعامل مع الخارج أم الداخل؟**

هذا السؤال وحده يفسر معظم الأوامر.

## استعارة Windows للقادمين من بيئة Microsoft

إذا كنت معتادًا على Windows Update:

**apt update** يساوي الضغط على Check for updates

**apt upgrade** يساوي الضغط على Install now

**الفرق:** لينكس يعطيك التحكم بالخطوتين بشكل منفصل.

## الفلاسفة الأربعة - التفصيل الكامل

### 1. Pacman - الجرّاح

#### الفلسفة

أفترض أنك تعرف ما تفعل. لا أشرح كثيرًا، لا أجمّل، لا أخفي.

#### المنطق

```
pacman -[ACTION][modifiers]
```

#### الأفعال الأساسية

**-S** يعني Sync - التعامل مع الخارج

**-Q** يعني Query - التعامل مع الداخل

**-R** يعني Remove - الحذف

**-U** يعني Upgrade - تثبيت ملف محلي

#### قاعدة اليد اليمنى واليسرى

اليد اليمنى تمتد للخارج: S

اليد اليسرى تبقى بالداخل: Q






#### الأوامر الأساسية

أمر النجاة - تحديث كامل:

```
sudo pacman -Syu
```

البحث في المستودعات (خارج):

```
pacman -Ss firefox
```

البحث في المثبت (داخل):

```
pacman -Qs firefox
```

التثبيت:

```
sudo pacman -S firefox
```

الحذف الكامل مع التبعيات والإعدادات:

```
sudo pacman -Rns firefox
```

#### معلومات الحزم

معلومات من المستودعات (خارج):

```
pacman -Si firefox
```

معلومات الحزمة المثبتة (داخل):

```
pacman -Qi firefox
```

قائمة ملفات حزمة مثبتة:

```
pacman -Ql firefox
```

من يملك هذا الملف:

```
pacman -Qo /usr/bin/firefox
```

#### العمليات المتقدمة

**التراجع لنسخة أقدم**

من الكاش المحلي:

```
sudo pacman -U /var/cache/pacman/pkg/firefox-120.0-1.pkg.tar.zst
```

باستخدام أداة downgrade:

```
sudo pacman -S downgrade
sudo downgrade firefox
```

**قفل حزمة (منع تحديثها)**

تحرير ملف الإعدادات:

```
sudo nano /etc/pacman.conf
```

أضف تحت options:

```
IgnorePkg = firefox
```

**السجلات**

آخر 30 عملية:

```
tail -30 /var/log/pacman.log
```

البحث عن التثبيتات:

```
grep "installed" /var/log/pacman.log | tail -20
```

### 2. APT - أمين المكتبة المحافظ

#### الفلسفة

الوضوح أهم من الاختصار. نستخدم كلمات كاملة لا رموزًا غامضة.

#### الفرق بين apt و apt-get

**apt** للاستخدام اليومي - ملون ومختصر وللبشر

**apt-get** للسكربتات والأتمتة - مستقر وقديم

**تحذير:** في السكربتات استخدم apt-get لأن apt قد يتغير مستقبلاً.

#### الرقصة الثنائية الشهيرة

الخطوة الأولى - تحديث الفهرس (لا يثبت شيئاً):

```
sudo apt update
```

الخطوة الثانية - الترقية الفعلية:

```
sudo apt upgrade
```

**لماذا خطوتان؟** لأن Debian تقدّس الاستقرار - تنظر أولاً، ثم تقرر.

#### الأوامر الأساسية

التثبيت:

```
sudo apt install firefox
```

الحذف مع الاحتفاظ بالإعدادات:

```
sudo apt remove firefox
```

الحذف الكامل مع الإعدادات:

```
sudo apt purge firefox
```

حذف الحزم اليتيمة:

```
sudo apt autoremove
```

البحث:

```
apt search firefox
```

#### معلومات متقدمة

معلومات تفصيلية:

```
apt show firefox
```

الإصدارات المتاحة والمثبتة:

```
apt policy firefox
```

قائمة ملفات حزمة (يستخدم dpkg):

```
dpkg -L firefox
```

من يملك هذا الملف:

```
dpkg -S /usr/bin/firefox
```

#### إدارة المستودعات

إضافة PPA في Ubuntu:

```
sudo add-apt-repository ppa:username/ppa-name
sudo apt update
```

حذف PPA:

```
sudo add-apt-repository --remove ppa:username/ppa-name
```

#### التراجع لنسخة أقدم

عرض الإصدارات المتاحة:

```
apt policy firefox
```

تثبيت إصدار محدد:

```
sudo apt install firefox=120.0+build1-0ubuntu1
```

#### قفل حزمة

قفل حزمة (منع تحديثها):

```
sudo apt-mark hold firefox
```

فك القفل:

```
sudo apt-mark unhold firefox
```

عرض الحزم المقفلة:

```
apt-mark showhold
```

#### السجلات

تاريخ العمليات:

```
tail -30 /var/log/apt/history.log
```

سجل dpkg (أكثر تفصيلاً):

```
tail -30 /var/log/dpkg.log
```

### 3. DNF - المصلح الحديث

#### الفلسفة

YUM كان جيدًا لكنه أصبح قديمًا. أنا النسخة الأذكى والأسرع.

#### السلاح السري

عرض تاريخ كل العمليات:

```
dnf history
```

تفاصيل عملية معينة:

```
dnf history info 5
```

التراجع عن آخر عملية:

```
sudo dnf history undo last
```

إعادة تنفيذ عملية:

```
sudo dnf history redo 5
```

الرجوع لنقطة زمنية:

```
sudo dnf history rollback 5
```

**ملاحظة مهمة:** كل مديري الحزم يحتفظون بسجلات، لكن DNF يجعل التعامل معها تفاعليًا وسهلاً.

#### الأوامر الأساسية

التحديث الكامل:

```
sudo dnf upgrade
```

التحديث مع refresh:

```
sudo dnf upgrade --refresh
```

التثبيت:

```
sudo dnf install firefox
```

الحذف:

```
sudo dnf remove firefox
```

البحث:

```
dnf search firefox
```

من يوفّر هذا الملف:

```
dnf provides /usr/bin/firefox
```

#### المجموعات Groups

عرض المجموعات المتاحة:

```
dnf group list
```

معلومات عن مجموعة:

```
dnf group info "Development Tools"
```

تثبيت مجموعة كاملة:

```
sudo dnf group install "Development Tools"
```

#### إدارة المستودعات

عرض المستودعات:

```
dnf repolist
```

تفعيل مستودع:

```
sudo dnf config-manager --set-enabled repo-name
```

إضافة COPR (مستودعات المجتمع):

```
sudo dnf copr enable username/project
```

#### التراجع لنسخة أقدم

عرض كل الإصدارات:

```
dnf list firefox --showduplicates
```

التراجع التلقائي للإصدار السابق:

```
sudo dnf downgrade firefox
```

#### قفل حزمة

تثبيت إضافة versionlock:

```
sudo dnf install python3-dnf-plugin-versionlock
```

قفل حزمة:

```
sudo dnf versionlock add firefox
```

عرض المقفلة:

```
dnf versionlock list
```

فك القفل:

```
sudo dnf versionlock delete firefox
```

### 4. Zypper - المحاسب الدقيق

#### الفلسفة

ليس كل تحديث هو نفس الشيء. كل شيء يجب أن يكون محسوبًا ودقيقًا.

#### ثلاث درجات للتحديث

المستوى 1 - تحديثات أمنية فقط:

```
sudo zypper patch
```

المستوى 2 - تحديث يومي عادي:

```
sudo zypper update
```

أو المختصر:

```
sudo zypper up
```

المستوى 3 - ترقية التوزيعة الكاملة:

```
sudo zypper dup
```

**متى تستخدم ماذا؟**

patch للخوادم (تحديثات حرجة فقط)

update للاستخدام اليومي

dup عند الانتقال بين إصدارات openSUSE

#### الأوامر الأساسية

تحديث الفهرس:

```
sudo zypper refresh
```

المختصر:

```
sudo zypper ref
```

التثبيت:

```
sudo zypper install firefox
```

المختصر:

```
sudo zypper in firefox
```

الحذف:

```
sudo zypper remove firefox
```

المختصر:

```
sudo zypper rm firefox
```

البحث:

```
zypper search firefox
```

المختصر:

```
zypper se firefox
```

#### الأنماط Patterns - السلاح السري

**الأنماط:** مجموعات منظمة من الحزم لمهام محددة.

عرض الأنماط المتاحة:

```
zypper search -t pattern
```

تثبيت نمط التطوير الأساسي:

```
sudo zypper in -t pattern devel_basis
```

أنماط مفيدة - أدوات C/C++:

```
sudo zypper in -t pattern devel_C_C++
```

أنماط مفيدة - أدوات Python:

```
sudo zypper in -t pattern devel_python3
```

أنماط مفيدة - خادم LAMP:

```
sudo zypper in -t pattern lamp_server
```

أنماط مفيدة - بيئة KDE:

```
sudo zypper in -t pattern kde_plasma
```

أنماط مفيدة - بيئة GNOME:

```
sudo zypper in -t pattern gnome
```

معلومات عن نمط:

```
zypper info -t pattern devel_basis
```

**لماذا الأنماط مهمة؟** بدل تثبيت 50 حزمة يدويًا، تثبت نمطًا واحدًا وتحصل على كل ما تحتاجه.

#### إدارة المستودعات

عرض المستودعات:

```
zypper lr
```

مع التفاصيل (URLs، الأولويات):

```
zypper lr -u
```

إضافة مستودع:

```
sudo zypper addrepo https://example.com/repo repo-name
```

المختصر:

```
sudo zypper ar https://example.com/repo repo-name
```

حذف مستودع:

```
sudo zypper rr repo-name
```

تفعيل مستودع:

```
sudo zypper mr -e repo-name
```

تعطيل مستودع:

```
sudo zypper mr -d repo-name
```

تغيير الأولوية (الأقل يعني الأعلى):

```
sudo zypper mr --priority 50 repo-name
```

#### التراجع لنسخة أقدم

عرض كل الإصدارات:

```
zypper search -s firefox
```

التثبيت لنسخة قديمة:

```
sudo zypper install --oldpackage firefox=120.0-1
```

السماح بتغيير المُوفّر:

```
sudo zypper install --allow-vendor-change firefox
```

#### قفل حزمة

قفل حزمة:

```
sudo zypper addlock firefox
```

المختصر:

```
sudo zypper al firefox
```

عرض المقفلة:

```
zypper locks
```

المختصر:

```
zypper ll
```

فك القفل:

```
sudo zypper removelock firefox
```

المختصر:

```
sudo zypper rl firefox
```

#### السجلات

عرض السجل:

```
tail -30 /var/log/zypp/history
```

أو في الإصدارات الحديثة:

```
zypper history
```

## حجر رشيد - الجدول الشامل

### نفس المهمة بأربع لغات

| المهمة | Pacman | APT | DNF | Zypper |
|:---|:---|:---|:---|:---|
| تحديث الفهرس | -Sy | update | check-update | refresh |
| ترقية النظام | -Syu | upgrade | upgrade | update |
| التثبيت | -S pkg | install pkg | install pkg | in pkg |
| الحذف | -R pkg | remove pkg | remove pkg | rm pkg |
| حذف كامل | -Rns | purge | remove | rm -u |
| البحث | -Ss | search | search | se |
| معلومات حزمة | -Si / -Qi | show | info | info |
| قائمة ملفات | -Ql | dpkg -L | rpm -ql | rpm -ql |
| من يملك ملف | -Qo | dpkg -S | provides | se --provides |
| إضافة مستودع | Edit config | add-apt-repository | copr enable | ar URL |
| قفل حزمة | IgnorePkg | apt-mark hold | versionlock add | addlock |
| تراجع لنسخة | -U old.pkg | install pkg=ver | downgrade | in --oldpackage |
| مجموعات/أنماط | Groups | Tasks | group install | in -t pattern |
| تراجع عن عملية | يدوي | يدوي | history undo | يدوي |

## الأخطاء الشائعة وكيفية تجنبها

### 1. التثبيت دون تحديث الفهرس

خطأ شائع:

```
sudo apt install firefox
```

الصحيح:

```
sudo apt update && sudo apt install firefox
```

**لماذا؟** قد تحصل على نسخة قديمة من الفهرس القديم.

### 2. التحديث الجزئي في Arch

خطير جداً - لا تفعل هذا أبداً:

```
sudo pacman -Sy firefox
```

الصحيح - دائماً:

```
sudo pacman -Syu firefox
```

**لماذا خطير؟** لأن قاعدة البيانات تصبح محدثة لكن بقية النظام قديم مما يؤدي لكسر التبعيات.

### 3. تجاهل تنظيف الكاش

في Arch:

```
sudo pacman -Sc
```

في Ubuntu:

```
sudo apt clean
sudo apt autoclean
```

في Fedora:

```
sudo dnf clean all
```

في openSUSE:

```
sudo zypper clean
```

**لماذا؟** الكاش يملأ المساحة في `/var/cache/`

### 4. عدم فهم إدارة المستودعات

كل توزيعة لها طريقتها الخاصة:

**Arch:** تعديل `/etc/pacman.conf`

**Ubuntu:** استخدام `add-apt-repository`

**Fedora:** استخدام `copr enable`

**openSUSE:** استخدام `zypper ar`

## سيناريوهات واقعية

### السيناريو 1: تثبيت Firefox

في Arch:

```
sudo pacman -Syu firefox
```

في Ubuntu:

```
sudo apt update && sudo apt install firefox
```

في Fedora:

```
sudo dnf install firefox
```

في openSUSE:

```
sudo zypper in firefox
```

### السيناريو 2: من يملك ملف معين

معرفة من يملك `/usr/bin/python3`

في Arch:

```
pacman -Qo /usr/bin/python3
```

في Ubuntu/Debian:

```
dpkg -S /usr/bin/python3
```

في Fedora/RHEL:

```
dnf provides /usr/bin/python3
```

في openSUSE:

```
zypper se --provides python3
```

### السيناريو 3: تثبيت كل أدوات التطوير دفعة واحدة

في Arch:

```
sudo pacman -S base-devel
```

في Ubuntu:

```
sudo apt install build-essential
```

في Fedora:

```
sudo dnf group install "Development Tools"
```

في openSUSE (الأقوى):

```
sudo zypper in -t pattern devel_basis devel_C_C++
```

## قاعدة I.S.R.Q للحفظ السريع

كل مدير حزم يفعل أربع وظائف:

**I** يعني Install - تثبيت

**S** يعني Search - بحث

**R** يعني Remove - حذف

**Q** يعني Query/Update - استعلام وتحديث

## طريقة التعلّم الصحيحة

### لا تفعل

حفظ 50 أمرًا مرة واحدة.

### افعل

ابدأ بـ 5 أوامر فقط:

1. تحديث النظام
2. تثبيت برنامج
3. البحث عن برنامج
4. حذف برنامج
5. معرفة ما هو مثبت

بعد إتقان الخمسة، انتقل للمستوى التالي.

## اختبر فهمك

### الأسئلة

**س1:** هل Firefox مثبت عندي؟ (داخل أم خارج؟)

**س2:** لديك ملف `file.pkg.tar.zst` في Arch، كيف تثبته؟

**س3:** كيف تعرف من يملك ملف `/usr/bin/python3` في كل توزيعة؟

**س4:** كيف تثبت كل أدوات تطوير Python دفعة واحدة في openSUSE؟

### الإجابات

**س1:** داخل - Query المثبت محليًا

في Pacman:

```
pacman -Qs firefox
```

في APT:

```
apt list --installed | grep firefox
```

**س2:** استخدم -U

```
sudo pacman -U file.pkg.tar.zst
```

**س3:** حسب التوزيعة

في Arch:

```
pacman -Qo /usr/bin/python3
```

في Ubuntu:

```
dpkg -S /usr/bin/python3
```

في Fedora:

```
dnf provides /usr/bin/python3
```

في openSUSE:

```
zypper se --provides python3
```

**س4:** استخدم الأنماط Patterns

```
sudo zypper in -t pattern devel_python3
```

## الواجهات الرسومية والإدارة الموحدة

### الفرق المهم

**مراكز البرامج** مثل GNOME Software وKDE Discover:

- للاستخدام اليومي البسيط
- واجهة مشابهة للمتاجر
- ليست مديري حزم تقنيًا

**مديرو الحزم الرسوميون** مثل Shelly وDNFDragora وYaST وSynaptic:

- تفاصيل تقنية كاملة
- إدارة المستودعات والتبعيات
- هي مديرو حزم حقيقيون

### التوصيات حسب التوزيعة

**Arch:**

للمبتدئين: Shelly أو Pamac

للمحترفين: Pamac مع CLI

**openSUSE:**

للمبتدئين: Myrlin

للمحترفين: YaST

**Fedora:**

للمبتدئين: DNFDragora

للمحترفين: DNFDragora مع CLI

**Ubuntu:**

للمبتدئين: Ubuntu Software

للمحترفين: Synaptic

### تفاصيل الأدوات

**Arch - Shelly (الأحدث 2024)**

التثبيت:

```
yay -S shelly
```

الموقع: https://shellyalpm.com/

المميزات: عصرية، سريعة، دعم AUR مدمج

**Arch - Pamac (الأشهر)**

التثبيت:

```
yay -S pamac-aur
```

المميزات: مستقرة، موثوقة، واجهة نظيفة

**openSUSE - Myrlin (الحديثة)**

التثبيت:

```
sudo zypper in myrlin
```

المميزات: واجهة حديثة Qt6، دعم الأنماط

**openSUSE - YaST (الأقوى)**

التشغيل:

```
sudo yast2 sw_single
```

المميزات: أقوى واجهة رسومية لإدارة الحزم في لينكس - تحكم كامل بالمستودعات والأنماط والأقفال والأولويات وشجرة التبعيات

**Fedora - DNFDragora (الرسمية)**

التثبيت:

```
sudo dnf install dnfdragora
```

المميزات: واجهة رسمية لـ DNF، إدارة COPR والمجموعات

**ملاحظة:** Fedora لا تستخدم GNOME Software لإدارة حزم RPM، بل DNFDragora.

**Ubuntu - Synaptic (للمحترفين)**

التثبيت:

```
sudo apt install synaptic
```

المميزات: فلترة قوية جدًا، سريعة وموثوقة، تفاصيل كاملة

### Cockpit - لوحة التحكم الموحدة

**واجهة ويب شاملة** لإدارة النظام بالكامل (ليس فقط الحزم)

التثبيت في Arch:

```
sudo pacman -S cockpit
```

التثبيت في Ubuntu:

```
sudo apt install cockpit
```

التثبيت في Fedora:

```
sudo dnf install cockpit
```

التثبيت في openSUSE:

```
sudo zypper in cockpit
```

التشغيل:

```
sudo systemctl enable --now cockpit.socket
```

الوصول عبر المتصفح:

```
https://localhost:9090
```

**ما يوفره Cockpit:**

- إدارة الحزم والتحديثات
- مراقبة أداء النظام CPU وRAM وDisk
- إدارة الخدمات systemd
- إدارة الشبكة والجدران النارية
- إدارة التخزين والأقراص
- إدارة الحاويات Podman وDocker
- إدارة عدة خوادم من مكان واحد
- Terminal مدمج في المتصفح

**متى تستخدم Cockpit:**

- تدير خوادم أو VPS
- تريد واجهة واحدة لكل شيء
- لا تريد تثبيت بيئة سطح مكتب كاملة
- تحتاج للوصول عن بُعد بأمان

## Fish vs Zsh - Shell الأذكى

### المشكلة مع Bash العادي

في Bash عند الكتابة:

```
sudo pacman -S fire<TAB>
```

تحصل على:

```
fire  firebird  firefox  firewalld
```

مجرد قائمة بدون شرح

### الحل: Fish أو Zsh

عند الكتابة:

```
sudo pacman -S fire<TAB>
```

تحصل على (مع أوصاف):

```
firefox    -- متصفح ويب
firewalld  -- برنامج جدار ناري
firejail   -- أداة عزل تطبيقات
```

### Fish - الأفضل للمبتدئين

#### التثبيت

في Arch:

```
sudo pacman -S fish
```

في Ubuntu:

```
sudo apt install fish
```

في Fedora:

```
sudo dnf install fish
```

في openSUSE:

```
sudo zypper in fish
```

جعلها Shell الافتراضية:

```
chsh -s /usr/bin/fish
```

#### لماذا Fish؟

**1. اقتراحات تلقائية من السجل**

سبق أن كتبت:

```
sudo pacman -Syu
```

المرة القادمة، اكتب فقط:

```
sudo pac
```

Fish تقترح (بخط رمادي): sudo pacman -Syu

اضغط السهم الأيمن للقبول

**2. تكملة ذكية مع وصف**

اكتب:

```
pacman -<TAB>
```

يعرض:

```
-S   -- تثبيت حزمة
-Q   -- الاستعلام عن قاعدة البيانات
-R   -- حذف حزمة
-U   -- ترقية أو تثبيت ملف محلي
```

**3. تكملة أسماء الحزم**

```
sudo pacman -S <TAB>
```

يعرض الحزم المتاحة

```
sudo pacman -R <TAB>
```

يعرض المثبتة فقط

**4. تلوين الأوامر**

```
sudo pacman -S firefox
```

أخضر (أمر صحيح)

```
sudo pacman -Z firefox
```

أحمر (علَم خاطئ)

**5. تعمل من الصندوق**

لا تحتاج إعداد معقد - ثبّت واستخدم مباشرة.

### Zsh - للمستخدمين المتقدمين

#### التثبيت مع Oh-My-Zsh

تثبيت Zsh:

```
sudo pacman -S zsh
```

تثبيت إطار Oh-My-Zsh:

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

جعلها الافتراضية:

```
chsh -s /usr/bin/zsh
```

#### الإضافات المفيدة

عدّل ملف الإعدادات:

```
nano ~/.zshrc
```

أضف الإضافات:

```
plugins=(
    git
    ubuntu
    archlinux
    dnf
    sudo
    command-not-found
)
```

**ubuntu:** اختصارات apt (إن كنت على Ubuntu)

**archlinux:** اختصارات pacman (إن كنت على Arch)

**dnf:** اختصارات dnf

**sudo:** اضغط ESC مرتين لإضافة sudo

**command-not-found:** اقتراح الحزمة للتثبيت

#### اختصارات مدمجة

**للـ Arch:**

```
pacin = sudo pacman -S
pacr = sudo pacman -R
pacsyu = sudo pacman -Syu
pacss = pacman -Ss
```

**للـ Ubuntu:**

```
agi = sudo apt install
agr = sudo apt remove
agu = sudo apt update && sudo apt upgrade
acs = apt search
```

#### إضافة sudo السحرية

كتبت:

```
pacman -Syu
```

اضغط Enter ثم تحصل على: permission denied

اضغط ESC مرتين بسرعة

الأمر يتحول تلقائياً إلى:

```
sudo pacman -Syu
```

### المقارنة

| الميزة | Fish | Zsh | Bash |
|:---|:---|:---|:---|
| جاهزة للاستخدام | نعم | تحتاج إعداد | نعم |
| اقتراحات تلقائية | مدمجة | تحتاج إضافة | لا |
| تكملة ذكية | ممتازة | ممتازة | بسيطة |
| تلوين الأوامر | مدمج | تحتاج إضافة | لا |
| توافق POSIX | لا | نعم | نعم |
| توافق السكربتات | صيغة مختلفة | جيد | كامل |
| منحنى التعلم | سهل جداً | متوسط | سهل |
| التخصيص | جيد | ممتاز | محدود |

### التوصية النهائية

**للمبتدئين والاستخدام اليومي:** Fish

**للمطورين والمستخدمين المتقدمين:** Zsh

**للخوادم والسكربتات:** Bash

## المرجع السريع للطباعة

### الأوامر اليومية الأساسية

```

Arch      Ubuntu           Fedora         openSUSE
-Syu      update&&upgrade  upgrade        up
-S pkg    install pkg      install pkg    in pkg
-R pkg    remove pkg       remove pkg     rm pkg
-Ss       search           search         se
-Si/-Qi   show             info           info
-Ql       dpkg -L          rpm -ql        rpm -ql
-Qo       dpkg -S          provides       se --provides
```

نصيحة: احتفظ بهذا الجدول حتى تعتاد على المنطق

## الخاتمة - المبادئ الأساسية

إذا فهمت شيئين فقط، فأنت فهمت كل شيء:

### 1. الداخل والخارج

كل أمر يتعامل مع:

- الخارج: المستودعات
- الداخل: المثبت محليًا
- أو كليهما: التثبيت والتحديث

### 2. الفلسفة قبل الأمر

لا تسأل: ما هو الأمر الصحيح؟

بل اسأل: كيف يفكر هذا النظام؟

- APT يفكر بالوضوح
- DNF يفكر بالتتبع
- Zypper يفكر بالدقة
- Pacman يفكر بالبساطة

### الآن أنت جاهز

أنت الآن تفهم مديري الحزم، لا تحفظ أوامرهم.

وهذا هو الفرق بين المستخدم المبتدئ والمستخدم الواثق.

بالتوفيق.

---

ملاحظة أخيرة: هذا الدليل حي - مديرو الحزم يتطورون. تابع التحديثات الرسمية لكل توزيعة.
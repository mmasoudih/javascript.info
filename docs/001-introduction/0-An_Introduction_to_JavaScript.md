
# مقدمه‌ای بر جاوا اسکریپت
خب بیاین ببینیم جاوا اسکریپت چه چیزای خفنی برامون داره، چه کارایی میتونیم باهاش انجام بدیم و چه تکنولوژی هایی ازش استفاده میکنن.

### جاوا اسکریپت چیه؟



جاوا اسکریپت اول برای «زنده کردن صفحات وب» ساخته شد

برنامه هایی که با این زبان نوشته میشن اسمشون اسکریپت (script) هست، میشه اونا رو توی HTML یک صفحه وب نوشت و موقعی که صفحه بارگذاری میشه به صورت خودکار اجرا بشن

اسکریپت ها به صورت متن ساده نوشتن میشن و مراحل پیچیده‌ای برای اجرا شدن لازم نیست انجام بشه (میشه با یک ویرایشگر متن به راحتی اسکریپت نوشت)

پس بذارین یه نکته‌ای همینجا بهتون بگم جاوااسکریپت(JavaScript) با یه زبان دیگه‌ای که اسمش جاوا(Java) هست خییییلی فرق میکنه

> چرا بهش میگیم جاوا اسکریپت؟ زمانی که جاوا اسکریپت ساخته شد، اوایل اسمش LiveScript بود. اما اون زمان جاوا خیلی محبوب بود پس تصمیم گرفتن که از جایگاه جاوا استفاده کنن و اسمش رو گذاشتن "برادر کوچکتر جاوا" تا از محبوبیت جاوا استفاده کنه. اما بیشتر که تکامل پیدا کرد جاوا اسکریپت به یه زبان کاملا مستقل تبدیل شد با ویژگی های خاص خودش به نام ECMAScript

جاوا اسکریپت نه تنها توی مرورگر بلکه توی سرور یا هر جایی که موتور جاوا اسکریپت وجود داشته باشه میتونه اجرا بشه

مرورگر توی خودش یه موتور جاوا اسکریپت داره که با استفاده از اون میتونه اسکریپت‌ها رو اجرا کنه که بعضیا بهش «ماشین مجازی جاوا اسکریپت هم میگن»

موتور های مختلف، اسمای مخفف متفاوتی دارن که چند تاشون رو براتون میگم و جلوش هم مرورگر هایی که از این موتور ها استفاده میکنن مینویسم براتون :‌

-   [V8](https://en.wikipedia.org/wiki/V8_(JavaScript_engine)) - Chrome & Opera
    
-   [SpiderMonkey](https://en.wikipedia.org/wiki/SpiderMonkey) - Firefox
    
-   یه سری دیگه از موتور ها هستن مثل "Chakra" که برای مرورگر Internet Explorer خدابیامرزه
    
-   موتور "ChakraCore" برای مرورگر Microsoft Edge
    
-   موتور "Nitro" و "SquirrelFish" برای مرورگر Safari
    
-   و ...
    

این اصطلاحات بالا رو سعی کنین که یادتون بمونه، چون توی مقاله هایی که توسعه دهنده‌ها مینویسن از این چیزا زیاد استفاده میکنن مثلا اگه جایی خوندین که فلان ویژگی توی V8 فقط پشتیبانی میشه احتمالا توی مرورگر های Chrome و Opera کار میکنه

### خب این موتور هایی که راجع بهشون صحبت کردیم چطوری کار میکنن؟



موتور‌ها خیلی پیچیده هستن ولی اصول اولیه‌ خیلی راحته

۱− موتوری که توی مرورگر هست میاد و اسکریپت رو میخونه یا parse‌اش میکنه

۲− بعد میاد اسکریپت رو تبدیلش میکنه به زبان ماشین (منظورم همون compile کردنه)

۳− و بعد از کامپایل خیلی سریع اجراش میکنه

موتورها توی هر کدوم از مراحل بهینه سازی هم انجام میدن، حتی اسکریپتی که کامپایل شده رو موقع اجرا بررسی میکنه و اطلاعاتی که از اول تا اخر برنامه رد و بدل میکنه رو تجزیه و تحلیل میکنه فرایند بهینه سازیش اینجوریه

### جاوا اسکریپت توی مروگر چه کارایی میتونه انجام بده؟



جاوا اسکریپت کنونی یه زبان برنامه نویسی «امن» هست، دسترسی سطح پایین یعنی کار با مموری یا CPU رو نمیده بهمون برای این که اوایل جاوا اسکریپت برای مرورگر ها ساخته شد و نیازی به این چیزا نداشت

قابلیت های جاوا اسکریپت بستگی داره به این که کجا اجرا بشه به عنون مثال Node.js از توابعی پشتیبانی می کنه که به جاوا اسکریپت امکان خوندن و نوشتن فایل ها ، انجام درخواست های شبکه و ... رو میده

جاوا اسکریپت توی مرورگر می‌تونه همه کارهایی که مربوطه به دستکاری صفحه وب، تعامل با کاربر و سرور رو انجام بده.

خب بذارین چند تا مثال براتون بزنم تا بهتر متوجه بشین:

-   اضافه کردن تگ HTML جدید به صفحه، ویرایش کردن محتوای توی صفحه، یا تغییر دادن استایل‌ها
    
-   به کارایی که کاربر توی صفحه انجام مثل کلیک‌کردن، تکون دادن ماوس یا فشار دادن کلیدها
    
-   درخواست ها رو از طریق شبکه به سرور میفرسته برای دانلود و اپلود (اصطلاحا تکنولوژی های AJAX و COMET)
    
-   گرفتن و تنظیم کردن کوکی‌ها، پرسیدن سوال از کاربر و نشون دادن پیغام
    
-   نگهداری اطلاعات روی مرورگر کاربر (با استفاده از local storage)
    

### جاوا اسکریپت توی مروگر چه کارایی نمی‌تونه انجام بده؟



دست و پای جاوا اسکریپت توی مرورگر بسته هست اونم به خاطر اینه که اطلاعات کاربر توسط سایت های مخرب لو نره و به خطر نیوفته

چند تا از این محدودیت ها رو براتون میگم :

-   جاوااسکریپت توی مرورگر نمیتونه به فایل های روی هاردتون دسترسی داشته باشه و اونا رو بخونه یا یه چیزی بنویسه یا کپیشون کنه و دسترسی مستقیمی به توابع سیستم عامل نداره
    
-   مرورگر های به‌روز اجازه کار با فایل‌ها رو بهش میدن اما با اجازه کاربر و با دسترسی محدود شده و کاربر میتونه فایلش رو انتخاب کنه یا این که بِکشه بیاره بندازه توی پنجره مرورگر
    
-   روش هایی برای کار کردن با دوربین و میکروفن هست که نیاز به اجازه کاربر داره پس جاوا اسکریپت نمیتونه خودش بیاد دوربین و باز کنه و ببینه چیکار میکنین و بعدش فیلمتون رو بفرسته برای آژانس امنیت ملی (NSA)
    
-   تب ها یا پنجره های مختلف مرورگر با هم دیگه ارتباطی ندارن برای مثال بعضی وقتا یک پنجره از جاوا اسکریپت استفاده میکنه تا یک پنجره دیگه رو باز کنه اما توی این حالت هم اگر ادرس های سایتها فرق کنن ممکنه که نتونه دسترسی داشته باشه (از یه دامنه، پورت، یا پروتکل دیگه) اصطلاحا این ویژگی رو میگن "Same Origin Policy" برای حل این مسئله ، هر دو صفحه باید برای تبادل داده توافق کنن و یک کد جاوا اسکریپت خاص هست که اینو مدیریت می کنه. توی آموزش های بعدی میگم چی هست. این محدودیت، برای ایمنی کاربره مثلا یه صفحه از سایت http://anysite.com که یک کاربر باز کرده نباید بتونه به یک تب مرورگر دیگه به ادرس http://gmail.com دسترسی پیدا کنه و اطلاعات رو از اونجا بدزده
    
-   جاوا اسکریپت می تونه به راحتی از طریق شبکه با سروری که صفحه فعلی از اونجا اومده ارتباط برقرار کنه اما نمیتونه از یه دامنه یا سایت دیگه اطلاعات رو دریافت کنه، ولی این کار ممکنه و لازمه که سرور داخل HTTP header ها اون رو قبول کنه، این محدودیت ها برای امنیت هستش
    

  

![](https://files.virgool.io/upload/users/217114/posts/ubjrf30ckg0f/xjgfscneyy70.png)

  

بعضی از این محدودیت بستگی به این داره که جاوا اسکریپت کجا اجرا بشه مثلا اگه روی سرور اجرا بشه این محدودیت ها وجود نداره، مرورگرهای جدید هم اجازه میدن به افزونه هایی که ممکنه مجور های زیادی بخوان

### چی جاوا اسکریپت رو منحصر به فرد می‌کنه؟



حداقل سه نکته جالب در مورد جاوا اسکریپت وجود داره:

-   یکپارچگی کامل با HTML / CSS
    
-   کار های ساده به راحتی انجام میشن
    
-   توسط مرورگر های اصلی پشتیبانی میشه و به صورت پیش‌فرض هم فعاله
    

جاوا اسکریپت تنها فناوری هستش که این سه تا رو با هم دیگه ترکیب می‌کنه

این چیزیه که جاوا اسکریپت رو منحصر به فرد می‌کنه به همین دلیل گسترده ترین ابزار برای ایجاد رابط های مرورگره

جاوا اسکریپت همچنین امکان ایجاد سرور و برنامه برای موبایل و ... هم بهمون میده

### زبان هایی که روی جاوا اسکریپت هستن



سینتکس(نحوه نوشتن کد) جاوا اسکریپت مناسب نیاز همه نیست، افراد مختلف ویژگی های مختلفی میخوان برای پروژه‌هاشون

این اواخر زبان های زیادی به وجود اومدن که قبل از اجرا شدن توی مرورگر تبدیل میشن به جاوا اسکریپت، ابزار های جدید این عمل تبدیل کردن رو خیلی سریع انجام میدن و به توسعه دهنده‌ها این اجازه رو میدن که توی یه زبان دیگه کد بزنن و در نهایت به صورت خودکار اون رو به جاوا اسکرپت تبدیل کنن

چند تا از این زبان رو براتون مینویسم :

-   CoffeeScript : یه ترکیب شیرینه برای جاوا اسکریپت نحوه نوشتن کدها رو کوتاه تر کرده ، و به ما اجازه میده که کد های تمیز تر و بهتری بنویسیم معمولا توسعه دهنده های روبی دوسش دارن
    
-   TypeScript : تمرکز تایپ‌اسکریپت اضافه کردن نوع داده های مختلفه به صورت سخت گیرانه تا فرایند توسعه و پشتیبانی سیستم های پیچیده رو راحت تر کنه و مایکروسافت هم توسعه‌اش داده
    
-   Flow: هم کارش مثل تایپ‌اسکریپته اما یه جور دیگه این کار رو انجام میده و فیسبوک توسعه دهنده‌اش هست
    
-   Dart: یه زبان مستقله که موتور خاص خودش رو داره که توی محیط های غیر از مرورگر اجرا میشه مثل اپلیکیشن های موبایل اما همچنان میتونه به جاوا اسکریپت تبدیل بشه، توسعه دهنده‌اش هم گوگل هست
    
-   Brython: یه تبدیل کننده کد به جاوا اسکریپت هست که با پایتون کار میکنه و این اجازه رو میده که با پایتون خالص بدون استفاده از جاوا اسکریپت برنامه بنویسین
    
-   Kotlin: یک زبان برنامه نویسی جدیده که مختصره و امن که میتونه مرورگر یا Node رو هدف قرار بده
    

البته خیلی بیشتر از این ها هستن ولی اگه بخوایم از هر کدوم از این زبان های تبدیل کننده استفاده کنیم باید جاوا اسکریپت رو بلد باشیم تا واقعا بفهمیم داریم چیکار میکنیم

  

### خلاصه



-   جاوا اسکریپت اون اوایل به عنوان یه زبان برای مرورگر ایجاد شد ، اما الان توی خیلی از محیط های دیگه هم ازش استفاده می‌شه.
    
-   امروزه جاوا اسکریپت جایگاه منحصر به فردی به عنوان گسترده ترین زبان مرورگر با یکپارچگی کامل با HTML / CSS داره
    
-   زبانهای زیادی وجود دارن که به جاوا اسکریپت "منتقل میشن" و ویژگیهای خاصی را ارائه می‌دن. توصیه می‌شه بعد از تسلط به جاوا اسکریپت، حداقل به طور خلاصه یه نگاهی بهشون بندازین.
    

  

  

  

اگر توی این مقاله مشکلی بود یا خواستین توی این پروژه مشارکت کنین این لینک گیت‌هابش هست.

[منبع](https://javascript.info/intro)

[گیت‌هاب](https://github.com/mmasoudih/javascript.info)
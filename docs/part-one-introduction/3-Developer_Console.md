# کنسول توسعه دهنده در مرورگر (Developer Console) | عیب‌یابی کد های جاوا اسکریپت

![](https://files.virgool.io/upload/users/217114/posts/ajnctbqq5dyf/sq1x3nedq4y5.png)

  

برنامه‌نویسی همیشه توش خطا هست. شما به احتمال زیاد اشتباه می‌کنین ... اوه من دارم از چی صحبت میکنم ؟!!

اشتباه کردن یه چیزیه توی برنامه نویسی که حداقل اگه یه انسان بخواد یه برنامه‌ بنویسه اشتباه میکنه، مگه این که یه ربات بخواد این کار و انجام بده.

اما توی مرورگر کاربرا به صورت پیش فرض هیچ خطایی نمی‌بینن پس اگه یه چیزی اشتباه باشه توی اسکریپتی که نوشتیم، ما نمیتونم ببینیم مشکل از چیه تا بتونیم حلش کنیم

برای دیدن خطاها و استفاده از اطلاعات مفید درباره اسکریپت‌ها قسمت "developer tools" (ابزارهای توسعه) توی مرورگرا جاسازی شده

بیشتر توسعه دهنده‌ها برای توسعه میرن سمت Chrome یا Firefox چون این مرورگرا بهترین ابزارهای توسعه رو دارن بقیه مرورگرا هم ابزارهای توسعه رو دارن، بعضی وقتا یه سری ویژگی خاص اضافه کردن اما معمولا با Chrome و Firefox بازی میکنن و زیاد فرق خاصی ندارن

بنابراین بیشتر توسعه دهنده‌ها یه مرورگر مورد علاقه دارن و اگه یه مشکل توی یه مرورگر خاص وجود داشته باشه از بقیه مرورگرا استفاده میکنن

ابزارهای توسعه خیلی قوی هستن، اونا خیلی قابلیت زیادی دارن برای شروع میریم سراغ این که چطوری بازشون کنیم و به خطاها یه نگاهی بندازیم و بعدشم چند تا دستور جاوا اسکریپت اجرا کنیم

  

### گوگل کروم (Google Chrome)

این صفحه رو باز کنین ([لینک](https://mmasoudih.github.io/javascript.info/examples/bug.html))

> اگه توی باز کردنش مشکی داشتین از یه پروکسی یا فیلترشکن استفاده کنین

یه ارور جاوا اسکریپت توی این صفحه هست. اما بازدید کننده سایت نمیتونه اون رو ببینه پس بیاین تا ابزار های توسعه رو باز کنیم و اروره رو ببینیم

دکمه `F12` یا اگه از مک(_Mac_) استفاده میکنین`Cmd+Opt+J` رو بزنین ابزار های توسعه به صورت پیش‌فرض روی سر‌برگ `Console` باز میشه یه چیزی شبیه به این عکس باید باشه:

  

![عکسی از ارور داخل کنسول مرورگر کروم](https://files.virgool.io/upload/users/217114/posts/ajnctbqq5dyf/lsv7ywg3qwlt.png)

عکسی از ارور داخل کنسول مرورگر کروم

  

این شکل بستگی داره به نسخه مرورگرتون ممکنه فرق کنه اما به عکس بالا باید شبیه باشه

اینجا ما میتونیم یه پیغام قرمز رنگ ببینیم، اسکریپت یه دستور ناشناخته "_lalala_" رو داره نشون میده سمت راست یه لینک قابل کلیک شدن هست که به جایی که این خطا رخ داده داره اشاره می‌کنه که توی عکس بالا گفته `bug.html:12` و این یعنی توی خط 12 فایل `bug.html` یه مشکلی هست

  

زیر متن خطا یه علامت آبی `<` هست که داره محیط متنی (`command line`) رو نشون میده جایی که ما میتونیم دستورات جاوا اسکریپت رو تایپ کنیم و با زدن دکمه `Enter` اونا رو اجرا کنیم

حالا ما میتونیم خطا ها رو ببینیم، و برای شروع این کافیه، ما بعدا به ابزار های توسعه بر می‌گردیم و توضیحات بیشتری رو توی قسمت (عیب یابی در کروم) بهتون میدیم

> هنوز این قسمت رو ترجمه نکردم به محض این که ترجمه‌اش تموم شد لینکش رو میذارم

  

### اگه بخوام چند خط بنویسم و بعد اجرا کنم چیکار کنم ؟

معمولا وقتی ما یه خط کد توی کنسول مینویسیم و دکمه`Enter` رو میزنیم و کدی که نوشتیم اجرا میشه

برای این که بخوایم چند خط بنویسم و بعد اجراش کنیم باید `Shift+Enter` بزنیم و اینجوری میتونیم کد های طولانی تری بنویسم

  

### فایرفاکس(Firefox)، اج(Edge) و بقیه مرورگرا

توی بیشتر مرورگرا با استفاده از `F12` میشه ابزار های توسعه رو باز کرد ظاهر اونا کاملا مشابه هست وقتی که یکی از این ابزار ها رو بدونین (_میتونین با کروم شروع کنین_) بعدش خیلی راحته براتون تا با بقیه مرورگرا هم کار کنین

### سَفاری (Safari)

سَفاری (_مرورگری برای مک هست و توسط ویندوز/لینوکس پشتیبانی نمیشه_) یه مقدار اینجا فرق میکنه ما نیاز داریم تا گزینه "`Develop menu`" رو فعال کنیم

اول `Preferences` رو باز کنین و به سربرگ `Advanced` برین یه تیک پایین صفحه هست اون رو باید فعال کنین حالا برای باز و بسته کردن کنسول میتونین از دکمه های `Cmd+Opt+C` استفاده کنین

![عکسی از تنظیمات مرورگر سَفاری](https://files.virgool.io/upload/users/217114/posts/ajnctbqq5dyf/mkrypxkgfbbc.png)

عکسی از تنظیمات مرورگر سَفاری

  

همچنین، توجه کنین که منوی بالا به نام "`Develop`" ظاهر میشه و اون دستورات و گزینه های زیاده داره

### خلاصه

-   ابزار های توسعه به ما اجازه میدن تا بتونیم خطاها رو ببینیم، دستورات رو اجرا کنیم، متغیرها رو بررسی کنیم و خیلی چیزای دیگه ...
-   ابزار های توسعه رو توی بیشتر مرورگرا روی ویندوز میشه با `F12` باز کرد و کروم برای مک رو با فشردن `Cmd+Opt+J` و همچنین مرورگر سَفاری هم با `Cmd+Opt+C` (_البته باز اول فعالش کنین_) میشه باز کرد

  

#### خب خب بالاخره محیط کاریمون آماده شد. توی قسمت بعدی میریم سراغ جاوا اسکریپت

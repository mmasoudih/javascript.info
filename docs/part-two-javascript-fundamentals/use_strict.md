# حالت جدید سخت‌گیرانه (use strict)

برای مدت طولانی جاوا اسکریپت بدون مشکل سازگار پذیری توسعه داده می‌شد و امکانات جدید بدون اینکه نیازی به تغییر در امکانات قبلی باشه، به این زبان اضافه می‌شد.

مزیت این موضوع این بود که هیچوقت توی کدهای قدیمی اشکالی به‌وجود نمیومد اما مشکل اینجا بود که اگر اشکالی در طراحی زبان، توسط خالقان جاوا اسکریپت رخ داده بود، تا ابد بجا میموند

این موضوع تا سال 2009 که ECMAScript 5 (ES5) معرفی شد، ادامه داشت.ES5 قابلیت‌های جدیدی رو به زبان اضافه کرد و اصلاحاتی رو هم روی امکانات فعلی انجام داد.

برای اینکه کدهای قدیمی کار کنن، بیشتر تغییراتی که در ES5 اتفاق افتاد، به صورت پیش‌فرض غیر فعاله، و برای فعال کردن اونا باید از طریق عبارت `"use strict"` این کارو انجام داد.

### حالت سخت‌گیرانه یا همون  "use strict" 

عبارت دستوری (directive) `"use strict"` یا `'use strict'` شبیه به یه رشته هست که زمانیکه اول اسکریپت قرار می‌گیره، تمام اسکریپت روی حالت مدرن کار خواهد کرد. برای نمونه :

```
"use strict";

//  این کد ها توی حالت مدرن کار میکنن
...
```

در مورد فانکشن‌ها (روشی برای گروه‌بندی کردن دستورات) در آینده خواهیم آموخت.

در اینجا صرفا اینو بدونین که میتونیم اول بیشتر فانکشن‌ها `"use strict"` رو بذاریم تا قواعد مدرن فقط روی کد های فانکشن اعمال بشه


مطمئن بشین که `use strict` رو اول کداتون گذاشتین در غیر این صورت حالت مدرن فعال براتون فعال نمیشه 

```

alert("some code");

"use strict";

// حالت سخت‌گیرانه اینجا غیر فعاله
```


فقط توضیحات میتونن بالای `"use strict"` قرار بگیرن


هیچ راه برای غیرفعال کردن `use strict` وجود نداره هیچ دستوری مثل `no use strict` وجود نداره تا به موتور جاوا اسکریپت دستور بده که به روش قدیمی کار کنه. زمانی‌که `use strict` رو قرار می‌دیم، راه برگشتی وجود نداره



### کنسول مرورگر

وقتی از کنسول توسعه دهنده برای اجرا کردن کد استفاده می‌کنین حواستون به این باشه که به صورت پیش‌فرض از `use strict` استفاده نمیکنه

بعضی وقتا `use strict` یه تفاوت هایی ایجاد میکنه که شما ممکنه نتیجه اشتباهی بگیرین

پس واقعا چجوری از `use strict` توی کنسول مرورگر استفاده کنیم؟
از دکمه های `Shift+Enter` استفاده کنین تا بتونین توی چند خط کد بنویسین، و `use strict` رو بالای کداتون بذارین مثل مثال زیر :‌

```
'use strict'; <Shift+Enter برای خط جدید>
//  ...کداتون
<Enter برای اجرا شدن>
```


این روش توی اکثر مرورگرها یعنی Firefox و Chrome کار می کنه ولی اگه کار نکرد مثلا مرورگرتون قدیمی بود یا هر چیز دیگه‌ای یه روش هست براش اما روش زشتیه، اما خب میشه مطمئن شد که حتما `use strict` کار میکنه :

```

(function() {
  'use strict';

  // کداتون رو اینجا بذارین 

})()

```

### اصلا باید از use strict استفاده کنیم یا نه؟

ممکنه این سوال واضح به نظر برسه ولی اینطور نیست
توصیه میکنم از `use strict` اول کداتون استفاده کنین، اما میدونین چی جالبه؟

جاوا اسکریپت مدرن از کلاس ها و ماژول ها و ساختار های پیشرفته زبان (که توی آموزش های بعدی بهشون میرسیم) پشتیبانی میکنه که `use strict` رو به صورت خودکار فعال میکنه، پس اگه از اونا استفاده کنیم لازم نیست از `use strict` استفاده کنیم

فعلا `use strict` رو به عنوان یک مهمون بالای اسکریپت هاتون استفاده کنین بعدا که به ماژول ها و کلاس ها رسیدم میتونیم این مهمون رو بفرستیم بره خونه خودش :)

توی قسمت های بعدی ویژگی های زبان رو یاد میگیریم و تفاوت های حالت سخت‌گیرانه و حالت قدیمی رو میبینیم، خوشبختانه تعدادشون زیاد نیست و در واقع زندگی ما بهتر میکنن :)
 

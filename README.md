# اسلایدر محصول واکنش‌گرا

این یک اسلایدر محصول واکنش‌گرا است که از ابتدا و بدون هیچ چارچوب یا کتابخانه‌ای ساخته شده است. این اسلایدر چند خط کد دارد، بنابراین سبک و سریع است. من از کلاسی استفاده کردم که به شما امکان می‌دهد هر تعداد اسلایدری که می‌خواهید در یک صفحه وب ایجاد کنید. همه تصاویر استفاده شده رایگان هستند و از [Unsplash](https://unsplash.com/) گرفته شده است.

## نحوه استفاده از آن

ابتدا این مخزن (repository) را دانلود کنید. سپس مراحل بعدی را انجام دهید.

### بخش HTML

در فایل **index.html** از **پوشه ریشه مخزن**، می‌توانید کدهای HTML اسلایدر را پیدا، ویرایش یا اضافه کنید.

فقط برچسب `div` را با مقدار ویژگی کلاس `slider-container` کپی و جایگذاری کنید و مقدار ویژگی `id` آن را به مقدار مناسب خود تغییر دهید.

هر برچسب `li` با کلاس `slider-item` یک اسلاید واحد است. می‌توانید اسلایدهای بیشتری اضافه کنید، برخی از آنها را حذف کنید و اسلاید را (`slide-link-url` و `slide-image-file-url` و `image alternative text`) به دلخواه ویرایش کنید.

#### نمونه کد:

```
<div class="slider-container" id="sample-slider">
  <div class="slides-wrapper">
    <div class="slides-container">
      <ul class="slider-list">
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
        <li class="slider-item">
          <a href="slide-link-url">
            <img src="slide-image-file-url" alt="image alternative text" />
          </a>
        </li>
      </ul>
    </div>
  </div>
  <div class="slider-arrows">
    <button type="button" class="slider-arrow-prev">Prev</button>
    <button type="button" class="slider-arrow-next">Next</button>
  </div>
</div>
```

### بخش جاوا اسکریپت

در پوشه **assets** > پوشه **js**، فایل **slider.js** قرار دارد. می‌توانید کدهای جاوا اسکریپت اسلایدر را پیدا، ویرایش یا اضافه کنید.

برای ایجاد هر اسلایدر جدید، در پایین کد قبل از `{`، خط کد زیر را اضافه کنید و مقادیر را تغییر دهید:

```
new Slider('sample-slider', [576, 768, 992]).run();
```

به جای `sample-slider`، شناسه `id` تگ div با کلاس `slider-container` خود را با که قبلاً در قسمت HTML وارد کرده‌اید، بنویسید.

`[992 ,768 ,576]` آرایه‌ای از کوئری‌های رسانه‌ای (نقاط شکست) است که در آن تعداد اسلایدهای نمایش داده شده همزمان، افزایش می‌یابد. در صورت نیاز آن را تغییر دهید.

فایل‌ها را ذخیره کنید. همین! شما یک اسلایدر جدید ایجاد کردید.

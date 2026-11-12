# تحلیل فروش و رفتار مشتریان Olist

## ساختار فایل‌ها

- `olist_analysis.ipynb`: نوت‌بوک اصلی تحلیل (فارسی) — **با خروجی‌های اجرای کامل** (۳۰ نمودار و همه جداول)
- `olist_management_report.pdf`: گزارش مدیریتی فارسی (۶ صفحه)
- `olist_analysis_en.ipynb`: نسخه انگلیسی نوت‌بوک (متن‌های توضیحی انگلیسی؛ کدها عیناً همان است)
- `olist_management_report_en.pdf`: نسخه انگلیسی گزارش مدیریتی
- `Olist-data/`: داده‌های خام
- `requirements.txt`: فهرست وابستگی‌ها
- `.gitignore`: فایل‌های نادیده‌گرفته‌شده در گیت

## داده‌ها

فایل‌های زیر با همین نام‌ها در پوشه `Olist-data/` (در ریشه پروژه، هم‌سطح نوت‌بوک) قرار می‌گیرند:

```text
olist_orders_dataset.csv
olist_customers_dataset.csv
olist_order_items_dataset.csv
olist_order_payments_dataset.csv
olist_order_reviews_dataset.csv
olist_products_dataset.csv
olist_sellers_dataset.csv
olist_geolocation_dataset.csv
product_category_name_translation.csv
```

## اجرا

```bash
python -m pip install -r requirements.txt
jupyter notebook olist_analysis.ipynb
```

نوت‌بوک از ریشه پروژه اجرا می‌شود و داده‌ها را از `Olist-data/` می‌خواند. همه سلول‌ها به‌ترتیب با گزینه `Restart & Run All` اجرا می‌شوند؛ در پایان، جدول 16.1 («کنترل محاسبات») باید بدون خطا اجرا شود.

نسخه انگلیسی (`olist_analysis_en.ipynb`) فقط متن‌های توضیحی را ترجمه می‌کند؛ کدها و در نتیجه اعداد و نمودارها (با برچسب‌های فارسی) با نسخه فارسی یکسان‌اند.

## نتایج کلیدی (خلاصه)

- سفارش‌های دو دوره هم‌ماه از 22,968 به 53,991 رسید (+135.1%)؛ پرمخاطب‌ترین ماه نوامبر 2017 با 7,544 سفارش.
- از 96,096 مشتری یکتا، پنج ایالت نخست 77.1% را دارند؛ سائوپائولو به‌تنهایی 15.6%.
- نرخ تأخیر تحویل از 3.5% به 7.7% رسید (+4.2 واحد درصد)؛ مارس 2018 با 19.0% بدترین ماه بود.
- میانگین امتیاز نظرهای سفارش‌های دیرکرددار 2.27 در برابر 4.29 گروه بدون تأخیر است.
- ده فروشنده نخست 13.3% ارزش کالای تحویل‌شده را دارند؛ فروش متمرکز نیست.

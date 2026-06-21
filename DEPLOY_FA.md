# راهنمای انتشار پورتفولیو در GitHub Pages

## روش ساده از داخل سایت GitHub

1. وارد اکانت GitHub خودت شو.
2. روی علامت `+` بالا سمت راست بزن و `New repository` را انتخاب کن.
3. نام Repository را دقیقاً این قرار بده:

   `mobinababarashani.github.io`

4. حالت Repository را `Public` بگذار.
5. Repository را بساز.
6. داخل صفحه Repository روی `Add file` و بعد `Upload files` بزن.
7. **محتویات داخل پوشه** `mobinababarashani.github.io` را آپلود کن؛ خود پوشه را به‌عنوان یک پوشه اضافه نکن. فایل `index.html` باید مستقیماً در ریشه Repository دیده شود.
8. پایین صفحه روی `Commit changes` بزن.
9. وارد `Settings` شو.
10. از منوی سمت چپ `Pages` را باز کن.
11. در بخش `Build and deployment`:
    - Source: `Deploy from a branch`
    - Branch: `main`
    - Folder: `/(root)`
12. روی `Save` بزن.
13. بعد از چند دقیقه سایت از این آدرس باز می‌شود:

    `https://mobinababarashani.github.io/`

## روش خط فرمان

بعد از ساخت Repository خالی، در PowerShell وارد پوشه سایت شو و این دستورات را اجرا کن:

```powershell
git init
git add .
git commit -m "Create personal portfolio website"
git branch -M main
git remote add origin https://github.com/mobinababarashani/mobinababarashani.github.io.git
git push -u origin main
```

سپس از `Settings > Pages` انتشار از شاخه `main` و پوشه `/(root)` را فعال کن.

## نکته‌های مهم

- نام Repository باید دقیقاً با نام کاربری GitHub تو هماهنگ باشد.
- فایل `index.html` نباید داخل یک پوشه اضافه قرار گرفته باشد.
- پس از هر تغییر، فقط فایل‌ها را Commit و Push کن؛ سایت خودکار به‌روزرسانی می‌شود.
- برای عوض‌کردن عکس پروفایل، فایل جدید را با نام `mobina-profile.webp` داخل `assets/images` جایگزین کن.
- برای عوض‌کردن تصویر پروژه توربین، فایل جدید را با نام `wind-turbine-power-calculator.webp` داخل `assets/images` جایگزین کن.
- برای عوض‌کردن سایر عکس‌های پروژه، فایل جدید را با همان نام داخل `assets/images` جایگزین کن.
- برای جایگزین‌کردن PDF رزومه، فایل جدید را با نام `Mobina-Babarashani-Resume.pdf` داخل `assets/files` قرار بده.

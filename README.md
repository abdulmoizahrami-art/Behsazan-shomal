# بهسازان شمال — وب‌سایت (SvelteKit)

## اجرا
```bash
npm install
npm run dev        # نمایش در مرورگر: http://localhost:5173
npm run build      # ساخت نسخهٔ نهایی در پوشهٔ build
npm run preview    # دیدن نسخهٔ نهایی
```
پوشهٔ `build` را روی هر هاستی می‌توانید بگذارید (نیازی به سرور نیست).

## ساختار
```
static/images/            لوگو و عکس‌ها (عکس پروژه‌ها را اینجا بگذارید)
src/app.html              پوستهٔ HTML (زبان فارسی، راست‌به‌چپ)
src/app.css               فقط استایل‌های عمومی را وارد می‌کند
src/lib/styles/           tokens.css (رنگ‌ها) · base.css · utilities.css
src/lib/data/site.ts      همهٔ متن‌ها و اطلاعات تماس  ← محتوا را اینجا عوض کنید
src/lib/components/       هر بخش یک پوشه: X.svelte (ساختار) + X.css (ظاهر)
  Nav · Hero · About · Services · Portfolio · Process · Pledge · Contact · Footer
  Button · Icon           اجزای تکراری
src/routes/+page.svelte   ترتیب بخش‌های صفحه
```

## کارهای رایج
- **تغییر شماره و ایمیل:** `src/lib/data/site.ts` ← بخش `contact`
- **اضافه کردن پروژه:** عکس را در `static/images/projects/` بگذارید و در `site.ts` به `projects` اضافه کنید:
  `{ title: '...', text: '...', image: '/images/projects/p1.jpg' }`
- **تغییر رنگ طلایی:** `src/lib/styles/tokens.css`

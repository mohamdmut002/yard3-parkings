# ساعد للأنظمة المرورية – ساحات الحجز (SAAED Impound Yard)

خريطة تفاعلية ثلاثية الأبعاد (isometric) لساحة الحجز 3. بدون Backend، والبيانات تنحفظ في LocalStorage.

## التشغيل محلياً
```bash
npm install
npm run dev
```

## البناء
```bash
npm run build   # الناتج في مجلد dist
```

## النشر على GitHub + Cloudflare Pages
1. ارفع المجلد على مستودع GitHub.
2. في Cloudflare: Workers & Pages ← Create ← Pages ← Connect to Git، واختر المستودع.
3. Framework preset: Vite (أو None)
   - Build command: `npm run build`
   - Build output directory: `dist`
4. Save and Deploy.

(Vercel: Import Project ويتعرف على Vite تلقائياً.)

## الملفات
- `index.html`: هيكل الصفحة
- `src/main.js`: المنطق (الخريطة، المواقف، السيارات، البحث، الحفظ)
- `src/styles.css`: التصميم

لتغيير بيانات البداية عدّل `ROWS` في `src/main.js`، ولتغيير مفتاح الحفظ عدّل `KEY` (البيانات المحفوظة في المتصفح تتجاهل التعديل على ROWS ما لم تغيّر المفتاح).

Developed by Mohammed Mutasim (4223) & Mohammed Tareq (4224)

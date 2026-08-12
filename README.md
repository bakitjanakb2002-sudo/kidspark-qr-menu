# Kids Park QR Menu — Өскемен

Kids Park Өскеменнің QR-мәзіріне арналған production source package.

## Құрылым

- `index.html` — негізгі клиенттік сайт. Қазіргі жұмыс істейтін нұсқаның сақталған source көшірмесі.
- `vercel.json` — Vercel static deployment конфигурациясы.
- `supabase/functions/site-render/index.ts` — Supabase Edge Function-ның ағымдағы source көшірмесі.
- `backup/app-extracted.js` — frontend JavaScript-тің жеке backup көшірмесі; production `index.html` ішінде код inline сақталған.
- `docs/DEPLOYMENT.md` — GitHub → Vercel қосу нұсқаулығы.

## Маңызды

Бұл репозиторийге `SUPABASE_SERVICE_ROLE_KEY`, admin кодтары және басқа private secrets кірмейді.
Frontend Supabase-тың public/publishable access-ін қолданады. Supabase-тағы мәзір деректері мен Storage файлдары бөлек сақталады және бұл repo-ға автоматты түрде көшірілмейді.

## Жұмыс тәртібі

1. Өзгерісті GitHub-қа commit/push жасау.
2. Vercel preview deployment-ты тексеру.
3. Preview дұрыс болса ғана Production-ға шығару.
4. Production бұзылса — Git commit немесе Vercel deployment арқылы rollback жасау.

## Қазіргі негізгі домен

`kidspark-qr-menu.vercel.app`
    Git deploy test — 2026-08-12

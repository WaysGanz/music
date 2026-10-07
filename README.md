# WayssMusify

Web music player (PWA) — frontend statis, siap deploy ke Vercel.

## Deploy
1. Push repo ini ke GitHub.
2. Vercel → Add New → Project → pilih repo → Framework: **Other** → Deploy.

## Catatan Backend
Frontend memanggil endpoint berikut (tidak termasuk di repo ini):

`/api/search` `/api/suggest` `/api/artist` `/api/album` `/api/lyrics` `/api/ytplay` `/api/proxy-audio` `/api/proxy-image`

Tanpa backend, tampilan tetap muncul tapi pencarian & pemutaran tidak jalan.
Jika backend ada di server lain, tambahkan di `vercel.json`:

```json
"rewrites": [{ "source": "/api/:path*", "destination": "https://BACKEND-KAMU/api/:path*" }]
```

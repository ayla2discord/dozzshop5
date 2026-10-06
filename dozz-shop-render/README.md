# dozz shop — serveur Node

Backend multi-utilisateurs (API REST + WebSocket) + frontend.

## Lancer en local

```bash
cd dozz-shop-server
npm install
npm start
```

Ouvre **http://localhost:3000**

## Deploy sur Render (gratuit)

1. Crée un compte sur [render.com](https://render.com)
2. New → **Web Service**
3. Connecte ton repo GitHub (push ce dossier)
4. Settings :
   - **Build command :** `npm install`
   - **Start command :** `npm start`
   - **Instance type :** Free
5. Deploy → tu reçois une URL `https://xxx.onrender.com`

## Comptes admin

| pseudo | mdp |
|--------|-----|
| admin | dozz2026 |
| ayla | aylaHalloween26 |
| AceOfEloan | AceDozz2026! |

## API (résumé)

- `POST /api/register` `{ username, email, password }`
- `POST /api/login` `{ username, password }` → `{ token, user }`
- `GET /api/state` (Bearer token) → users, servers, dms
- `POST /api/servers/:id/channels/:ch/messages` `{ content, file? }`
- `WebSocket /ws?token=...` → events live

Données persistées dans `data/db.json`.

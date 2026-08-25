# Vercel deployment

Import `prathmesh8889/Itcybertechnologiespvtltd` into Vercel with the repository
root as the Root Directory. Vercel reads `vercel.json`, runs `npm run build`,
and serves `dist` with SPA rewrites for React Router routes.

Configure these variables for Production, Preview and Development:

```text
VITE_SUPABASE_URL=https://hmzxkhofrxvrylixxijx.supabase.co
VITE_SUPABASE_ANON_KEY=<Supabase publishable key>
VITE_SITE_URL=https://www.itcyber.in
```

Never add a Supabase service-role or secret key to a `VITE_` variable.

After Vercel provides the deployment hostname, add its exact origin to the
Supabase `ALLOWED_ORIGINS` secret and redeploy the four public Edge Functions.

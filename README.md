# Fashion Tryon investor website

A static website: four HTML pages and a shared stylesheet. No dependencies,
backend, environment variables, or build step are needed.

## Deploy to Vercel

1. Push this folder, including `vercel.json`, to a GitHub repository.
2. In Vercel, choose **Add New > Project** and import that repository.
3. Set **Root Directory** to the folder containing `index.html` and
   `vercel.json`. If these files are at the repository root, leave the default.
4. Select **Other** for Framework Preset. The included `vercel.json` sets:
   - Build Command: empty (skip build).
   - Install Command: empty (skip installation).
   - Output Directory: `.` (this folder).
5. Click **Deploy**.

Do not select Next.js or Vite, or set the output directory to `dist`, `build`,
or `public`. This project serves its existing files directly.

Alternatively, from this folder with Node.js installed:

```powershell
npx vercel
```

Sign in and follow the prompts to create/link a project and deploy a preview.
When the preview looks correct, deploy to production:

```powershell
npx vercel --prod
```

## Check after deployment

Open `/`, `/market/index.html`, `/projections/index.html`, and
`/funding/index.html`. Check the navigation and confirm `/styles.css` loads.
The original `.html` links are preserved, so the same files also work when
opening `index.html` locally.

If the homepage returns 404, check that Root Directory contains `index.html`
and Output Directory is `.`. Redeploy after fixing project settings.

Official configuration reference:
https://vercel.com/docs/project-configuration/vercel-json

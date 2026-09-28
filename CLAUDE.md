# mail-assets

Billeder og skabeloner til WeZimplify-mailsignaturer, hostet via GitHub Pages på
https://assets.wezimplify.com/ (`7a/mail.png` → `https://assets.wezimplify.com/7a/mail.png`).
Et push er et deploy.

**Repoet er offentligt:** ingen persondata eller kundedata i git - historikken er også
offentlig. Udfyldte signaturer ligger i `personal/`, som er gitignored.

- `7a/` - signatur 7a "Præcision": `index.html` er skabelonen, billederne ligger ved siden af.
- Opsætning af en signatur i Outlook: [signature-setup.md](signature-setup.md).

## Regler

- **Overskriv aldrig en fil der er i brug** - mailklienter cacher billeder nærmest
  permanent. Nyt design = ny mappe (`7b/`); den gamle bliver liggende.
- Absolutte https-URL'er i signaturen, aldrig relative stier eller `data:`-billeder.
- PNG eller JPG, gemt i 2x og vist i 1x med `width`/`height` som HTML-attributter, `alt` på
  alle billeder, under ~100 KB pr. fil. Ingen tracking-pixels.

## Hosting

- GitHub Pages fra `main`, roden. `CNAME` skal blive liggende.
- DNS hos Simply: `assets` som CNAME til `wezimplify.github.io`. Andre records røres ikke.
- "Enforce HTTPS" under Settings → Pages slås til når GitHub har udstedt certifikatet.
- Tjek: `curl -I https://assets.wezimplify.com/7a/mail.png` skal svare 200.

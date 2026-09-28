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
- **HTTPS mangler stadig (2026-09-28).** Domænet blev gemt i GitHub 2026-09-23, men
  DNS-recorden fandtes først 2026-09-27, så de første tjek kunne kun fejle. Domænet er gemt
  igen, og Settings → Pages viser "DNS check in progress". Når "Enforce HTTPS" kan klikkes:
  slå det til og slet denne linje. Står den stadig fast efter 24 timer: fjern domænet under
  Settings → Pages og gem det igen. Indtil da loader billederne ikke over https, og
  signaturen virker ikke.
- Tjek: `curl -I https://assets.wezimplify.com/7a/mail.png` skal svare 200.

# mail-assets

Statiske billeder til mailsignaturer. Hostet via GitHub Pages på
**https://assets.wezimplify.com/**, så en URL i en signatur bliver ved med at virke
uafhængigt af hjemmesiden.

Filerne ligger i roden af repoet: `linkedin.png` bliver
`https://assets.wezimplify.com/linkedin.png`. Et push er et deploy — der går typisk under
et minut før filen er ude.

## Regler

- **Overskriv aldrig en fil der er i brug.** En signatur ligger i alle tidligere
  afsendte mails, og mailklienter cacher billedet nærmest permanent — Gmail henter det
  gennem sin egen proxy og beholder kopien. Nyt udtryk = nyt filnavn
  (`linkedin-v2.png`), og den gamle fil bliver liggende.
- **Kun PNG eller JPG i en signatur.** SVG renderer ikke i Outlook og bliver strippet i
  Gmail. Ligger der en SVG her, er den kilde til rasterisering, ikke til brug direkte.
- **Gem i 2x og vis i 1x.** Et ikon på 48×48 vises som `width="24" height="24"`. Sæt
  altid `width`/`height` som HTML-attributter — Outlook regner ikke CSS, og uden dem
  fylder billedet sin fulde pixelstørrelse.
- **Sæt `alt` på alt.** Billeder er slået fra som standard i mange klienter, og alt-teksten
  er det modtageren ser i stedet.
- **Hold filerne små.** En signatur hentes ved hver visning, også på mobil; under ~100 KB
  pr. fil er en fornuftig grænse.
- **Tænk på dark mode.** Et mørkt motiv på transparent baggrund forsvinder når klienten
  vender baggrunden. Enten nok kontrast til begge, eller to varianter.
- Ingen tracking-pixels. Ingen kunde- eller persondata — repoet er offentligt.

## Opsætning

- GitHub Pages: kilde er `main`, roden af repoet.
- `CNAME` holder domænet og skal blive liggende i repoet — ellers falder det custom
  domæne af ved næste deploy.
- DNS: `assets` som CNAME til `wezimplify.github.io`. Kun det subdomæne; apex, www og
  mail-records røres ikke.
- HTTPS-certifikatet udstedes automatisk et par minutter efter at DNS peger rigtigt.

## Test

Send en mail med signaturen til en Gmail-adresse og se at billederne vises. Gmail er den
klient der beviser at et billede kan hentes gennem en billed-proxy.

# Sæt din signatur op

## Lav din egen signatur

1. Kopiér `7a/index.html` til `personal/7a-<dine initialer>.html`. `personal/` er
   gitignored, så din udfyldte signatur bliver aldrig committet.
2. Udskift pladsholderne:
   - `{{navn}}` - fulde navn
   - `{{titel}}` - titel (vises med versaler)
   - `{{mail}}` - står to steder, i linket og i teksten
   - `{{mobil}}` - 8 cifre uden +45, står to steder; +45 er en del af skabelonen
   - `{{linkedin}}` - fuld URL til din LinkedIn-profil
3. Åbn filen i en browser og se at alle billeder vises.

Eller bed Claude om at lave den ud fra 7a og giv den dine oplysninger.

## Ind i Outlook

Brug altid din fil herfra, ikke eksporten fra Claude Design: eksporten har billederne
indlejret, og dem fjerner Outlook og Gmail typisk. Din fil henter dem fra
`https://assets.wezimplify.com`.

**Nyt Outlook (Windows) og Outlook på nettet**
1. Åbn din fil fra `personal/` i Edge eller Chrome, marker alt (Ctrl+A) og kopiér (Ctrl+C).
2. Indstillinger (tandhjulet) → Konti → Signaturer → Ny signatur.
3. Sæt ind (Ctrl+V), giv den et navn og gem.
4. Vælg den som standard for nye mails og for svar.

Nyt Outlook og Outlook på nettet deler signaturer via din Microsoft 365-konto, så den skal
kun sættes op ét af stederne.

**Klassisk Outlook (Windows)**
1. Kopiér fra browseren som ovenfor.
2. Filer → Indstillinger → E-mail → Signaturer → Ny, sæt ind, gem, og vælg standard.

Falder layoutet fra hinanden ved indsætning: luk Outlook, kopiér din fil til
`%APPDATA%\Microsoft\Signatures\WeZimplify.htm`, og start Outlook igen - så står den på
listen over signaturer.

**Outlook til Mac**
1. Åbn din fil i Safari eller Chrome, marker alt (Cmd+A) og kopiér (Cmd+C).
2. Outlook → Indstillinger → Signaturer → + → sæt ind (Cmd+V) → gem.
3. Vælg den som standard for kontoen samme sted.

## Test før du bruger den

Send en mail til en Gmail-adresse og en til en kollega i Outlook. Se at billederne vises og
at layoutet holder - også på mobil og i mørk tilstand, hvor Outlook kan vende farverne.
Gmail beviser at billederne kan hentes gennem en billed-proxy.

**Ikke testet i Outlook endnu** (2026-09-27). Den første der har sat 7a op i Outlook på
Windows eller Mac, retter den linje med hvad der virkede.

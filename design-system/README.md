# Aftalt

Aftalt er dokumentationslaget bag håndværkergarantien. Det fanger fire ting, mens arbejdet sker: hvad der blev aftalt, hvad der kom til, hvad der blev lukket inde, og hvad kunden kvitterede for. Identiteten skal få det til at ligne det, det er: et bevis, ikke en app til at gøre ting pænere.

Tagline: **Det aftalte, dokumenteret.**

## Tre principper

**1. Rolig og udramatisk.** Aftalt står mellem en håndværker og en boligejer, ofte når de er uenige. Ingen udråbstegn, ingen konfetti, ingen "Fantastisk!". Tonen er den rolige fyr på pladsen, der siger "det er noteret" og går videre.

**2. Stemplet er signaturen.** Alt, der gælder som bevis, sættes i `stamp` (monospace): tidsstempler, positioner, sagsnumre, SMS-koder. Når noget er låst, ses hængelåsen. Det er den ene detalje, kun Aftalt har, og den går igen fra telefonen til PDF'en i klagesagen.

**3. Læsbart med beskidte hænder.** Mindste brødtekst er 15 px, mindste berøringsflade 44 px, kontrast 4.5:1 overalt, også i sol. Én primær handling pr. skærm, nederst, inden for tommelfingerens rækkevidde.

## Navn og ordmærke

Navnet skrives **Aftalt**, kun stort A. Aldrig AFTALT, aldrig aftalt.dk som brand.

Ordmærket sættes i `display` (Bricolage Grotesque) vægt 700 med -0.015em tegnafstand, i `ink-900` på lys grund eller `ground-100` på mørk. Der er endnu ingen ordmærke-fil; mærket er nedenfor.

Mærket er et A, der også er et flueben: tre streger i en firkant med `radius-sm`-hjørner. Det findes i to versioner under Assets › Logo: blåt (`snor-700`) til app og web, enfarvet (`ink-900`) til tryk og mørke flader. Mindste størrelse 20 px. Fri luft omkring mærket: en kvart af dets bredde.

## Farver

Paletten er hentet fra byggepladsen, ikke fra en app-butik.

- **Puds** (`ground-100`, `surface-100`, `surface-200`): varm, lys grund. Kort er hvide. Grå er aldrig neutral grå; den trækker mod varmt.
- **Tjære** (`ink-900`, `ink-600`, `ink-400`): tekst i tre styrker. Sagsmappens hoved, som foreningen ser, er `ink-900` med lys tekst: det eneste sted, der er mørkt med vilje.
- **Snor** (`snor-700`, `snor-100`, `on-snor`): kridtsnorens blå. Brandfarven og håndværkerens farve. Den eneste farve til primære handlinger, links og aktive faner, undtagen på kundens side. Én primær knap pr. skærm.
- **Lyng** (`lyng-700`, `lyng-100`, `on-lyng`): lyngens lilla. Kundens farve. Når håndværker og kunde vises over for hinanden, er håndværkeren Snor og kunden Lyng, så man altid kan se, hvem der handler. Kundens primære handling (Godkend, Kvittér) er Lyng. Bruges aldrig som pynt eller til tilstande; Markering og Kvit betyder det samme på begge sider.
- **Markering** (`markering-600`, `markering-100`): sprayorange. Betyder altid "et menneske skal gøre noget": afventer kundens godkendelse, mangel med frist, obligatorisk foto der mangler. Bruges aldrig som pynt, hero eller knap.
- **Kvit** (`kvit-600`, `kvit-100`): godkendt, kvitteret, dokumenteret, låst. Et grønt flueben er altid koblet til et tidsstempel.
- **Stop** (`stop-600`, `stop-100`): ikke med i aftalen, afvist. Sparsomt.

Regler: Tilstande skelnes på mere end farve (ikon plus tekst: "Godkendt 11:02", ikke kun grøn). Blå og orange er hovedparret, fordi de kan skelnes af alle. Rød og grøn står aldrig som eneste forskel ved siden af hinanden. Ingen gradienter, ingen farvede venstrekanter på kort.

## Typografi

Tre familier, hver med ét job:

- `display`, Bricolage Grotesque: titler og tal. Bred, selvsikker, lidt håndværkeragtig. Aldrig under 20 px.
- `sans`, IBM Plex Sans: alt, der skal læses. Tydelige æ, ø, å og tal, der står lige i kolonner (`font-variant-numeric: tabular-nums` overalt, hvor tal mødes).
- `mono`, IBM Plex Mono: stemplet. Tidsstempler, positioner, sagsnumre, koder. Brug den ikke til andet; så mister den sin betydning.

Skalaen står under Typography. `label` er altid versaler med 0.07em afstand og i `ink-400`. Overskrifter får `text-wrap: balance`.

Alle tre hentes fra Google Fonts (css2, display=swap) med rigtige fallback-stakke; ingen fontfiler endnu.

## Stemplet

Et stempel er en linje i `stamp` med tre dele, adskilt af en midterprik: dag, klokkeslæt, og hvad der låste det (position, SMS-kode eller bruger).

`3. nov 2026 · 09:14 · position bekræftet`

Et låst stempel får hængelås-ikonet foran. Et stempel ændres aldrig med farve; det er altid `ink-400` på lys og `ink-600` på mørk, så det ligner det samme i appen, i SMS'en og i PDF'en til nævnet. Stemplet er komponenten `Stamp`.

## Ikoner

Stregikoner, 2 px streg, runde ender og hjørner (Lucide-stil), 20 px i lister og 24 px i knapper. Farve arves fra teksten. Ingen fyldte ikoner, ingen emoji. Fem ikoner bærer produktet: kamera, mikrofon, hængelås, position, flueben.

## Layout og afstande

4-pixel-skala (`space-1` til `space-8`). Søskende lægges med flex eller grid og `gap`; ingen marginer på enkeltelementer. Telefonens gutter er `space-4`, desktopens `space-5`. Kort har `radius-md`, 1 px `line-100`-kant og ingen skygge; skygge (`shadow-float`) er kun til dialoger og toasts.

På telefon: én kolonne, titel øverst, primær handling i en fast bund. På desktop: sidenavigation 224 px, indhold i to kolonner (1.25 : 1), og kundens telefon som panel til højre, når noget afventer.

## Komponenter

Tre komponenter definerer udtrykket: `Button` (én primær pr. skærm, 46 px høj), `StatusPill` (tilstande med ikon og tekst, aldrig farve alene) og `Stamp` (tidsstemplet). Checkpoint-kort, SMS-bobler og tjeklister er sammensat af disse og af tokens; de får egne komponenter, når der er kode at bygge dem fra.

## Tone i tekster

Korte sætninger. Aktivt sprog: "Send til kunden", "Godkend aftalen", "Kvittér". En knap siger, hvad der sker, og toasten bekræfter det samme ord: "Sendt". Tilstande skrives som fakta med tid: "Godkendt 11:02 · låst". Ingen udråbstegn, ingen "Du er næsten i mål", ingen tanke-streger. Kunden tiltales med du; firmaet nævnes ved navn, ikke som "håndværkeren".

## Det må du ikke

- Bruge Markering (orange) som brandfarve, knap eller hero.
- Sætte et flueben uden et tidsstempel.
- Lave en primær knap mere pr. skærm.
- Bruge `mono` til brødtekst, eller `display` under 20 px.
- Gradienter, skygger på kort, farvede venstrekanter, emoji.
- Skrive AFTALT eller aftalt.

# Salgsside

`index.html` er en one-pager til salgsmødet med Dansk Håndværk. Én fil, ingen build. Åbn den direkte i browseren. Knapperne "Se prototypen" linker til `../prototype/index.html`.

Sektioner: Hero, Problemet, Det fanger Aftalt (fire ting), Ét forløb, to telefoner (håndværkeren i Snor over for kunden i Lyng), Sagsmappen, Det får foreningen (kundens tryghed), Tre parter, Pilot.

Samme regler som i roden (`README.md`) og designsystemet (`design-system/README.md`): kun værdier fra `tokens.json`, stemplet er signaturen, rolig tone, dansk tekst, ingen emojis.

## Billeder (til Codex)

Siden har fem billedpladser. Hver er et element som dette:

```html
<figure class="billedplads" data-billede="hero" data-format="hoej" data-prompt="...">
  <div class="pladstekst">...</div>
</figure>
```

Sådan udfyldes en plads:

1. Generér billedet ud fra `data-prompt`. Format: `data-format="hoej"` er 4:5, `"bred"` er 16:9, ingen værdi er 4:3.
2. Gem det som `salgsside/billeder/<data-billede>.jpg` (f.eks. `billeder/hero.jpg`). Maks. ca. 400 KB pr. billede.
3. Indsæt `<img src="billeder/hero.jpg" alt="...">` som første barn i `<figure>`. Pladsteksten skjules automatisk, og rammen bliver fast.
4. Skriv en kort, saglig `alt`-tekst på dansk.

| `data-billede` | Format | Motiv | Status |
|---|---|---|---|
| `hero` | 4:5 | Tømrer fotograferer vådrumsmembranen med telefonen, før der sættes fliser op | Midlertidigt: `membran.jpg` |
| `sagsmappe` | 16:9 | Sagsbehandler i foreningen åbner en sag på en bærbar | `sagsmappe.jpg` |
| `forening` | 4:3 | To fra foreningen gennemgår en sag ved et mødebord | `forening.jpg` |
| `haandvaerker` | 4:3 | Håndværkerhænder med telefon, talenote på byggepladsen | `haandvaerker.jpg` |
| `boligejer` | 4:3 | Par i deres nyrenoverede badeværelse kigger på en telefon | Midlertidigt: `aflevering.jpg` |

### Sagens fotos

`billeder/bjaelke.jpg`, `roer.jpg`, `membran.jpg` og `aflevering.jpg` er de fire AI-illustrationer fra mødesiden (`moede/`). De bruges i kundens telefon (tillægget) og som miniaturer i sagsmappen, og midlertidigt i `hero` og `boligejer`, indtil der er billeder til de motiver. Erstattes et midlertidigt billede, så gem det nye som `<data-billede>.jpg` og ret `src`.

### Sagens fakta (samme på salgsside, mødeside og prototype)

Kunde Mette Lund, Ved Søen 8, 3450 Allerød. Tømrerfirma Holm ApS (Thomas Holm). Sag 2026-0142. Aftale 69.576 kr. inkl. moms, godkendt 28. okt kl. 19:35 med kode 482 917. Rådden bjælke fundet 3. nov kl. 08:10; tillæg med prisloft 6.500 kr. inkl. moms godkendt 3. nov kl. 09:42 med kode 306 118. Rør før lukning 4. nov kl. 11:10. Membran før fliser 5. nov kl. 14:30. Aflevering kvitteret 12. nov kl. 15:20 med kode 771 240. Prototypens ur er simuleret, så dens tidspunkter flytter sig, når man klikker.

Prototypen har også en tag-sag, når man vælger fagtypen Tag (kun i prototypen, ikke på salgssiden eller mødesiden): samme kunde og adresse, sag 2026-0157, nyt tegltag for 286.250 kr. inkl. moms. Obligatoriske checkpoints: undertag før lægter og inddækning ved skorsten før tagsten. Tillæg: rådne spærfødder ved tagfod, prisloft 9.800 kr. Aflevering 20. nov; mangel: rygningssten ved østgavlen, frist 27. nov.

Og en køkkensag (Inde, Køkken; kun i prototypen): samme kunde og adresse, sag 2026-0163, nyt køkken for 158.750 kr. inkl. moms. Obligatoriske checkpoints: eksisterende køkken før nedrivning, vand og afløb før lukning, el til komfur og emhætte før lukning. Tillæg: rådden gulvplade under vask, prisloft 4.800 kr. Aflevering 18. nov kl. 14:10; mangel: skabslåger skal justeres, frist 25. nov. Køkkenets tjekliste bygger på `noter/research-koekken.md` (BR18 § 443 og § 406, autorisationer, tæthedskontrol); punkter mærket [verificér] er endnu ikke kontrolleret i kilderne.

I prototypen vælges fagtypen via "Ny sag" i fem trin (kontakt, hvor, hvad, fag og garanti, tjekliste): badeværelse giver vådrumssagen, køkken giver køkkensagen, og tag giver tag-sagen. Stue, facade og terrasse er endnu ikke bygget. Opsætningen pr. fag står i `FAG` øverst i prototypens script.

Stil for alle billeder: dokumentarisk, naturligt dagslys, varme og dæmpede farver, der passer til puds-grunden (`ground-100`). Danske omgivelser. Ingen tekst eller logoer i billedet, intet poseret smil, ingen stockfoto-stemning. Ingen skærme med læsbart indhold.

Billederne skal ikke ændre layoutet. Rør ikke telefonen, sagsmappen og stemplerne; de er bygget i HTML og skal forblive tekst.

## Kendte huller

- Logomærket er tegnet direkte i siden (`<symbol id="mark">`, samme tegning som i prototypen), fordi `aftalt-mark.svg` og `aftalt-mark-ink.svg` endnu ikke ligger i `design-system/assets/Logo/`. Når filerne findes, skal de erstatte symbolet.
- Fontene hentes fra Google Fonts. Skal siden køre på en projektor uden net, skal de indlejres (se regel 6 i roden).
- Citatet i Problemet er gengivet fra en samtale med Dansk Håndværk. Ret ordlyden, hvis den skal være mere præcis.

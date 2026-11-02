# Salgsside

`index.html` er en one-pager til salgsmødet med Dansk Håndværk. Én fil, ingen build. Åbn den direkte i browseren. Knapperne "Se prototypen" linker til `../prototype/index.html`.

Sektioner: Hero, Problemet, Det fanger Aftalt (fire ting), En sag (Ved Søen 8 med kundens telefon), Sagsmappen, Tre parter, Pilot.

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

| `data-billede` | Format | Motiv |
|---|---|---|
| `hero` | 4:5 | Tømrer fotograferer vådrumsmembranen med telefonen, før der sættes fliser op |
| `sagsmappe` | 16:9 | Sagsbehandler i foreningen åbner en sag på en bærbar |
| `forening` | 4:3 | To fra foreningen gennemgår en sag ved et mødebord |
| `haandvaerker` | 4:3 | Håndværkerhænder med telefon, talenote på byggepladsen |
| `boligejer` | 4:3 | Par i deres nyrenoverede badeværelse kigger på en telefon |

Stil for alle billeder: dokumentarisk, naturligt dagslys, varme og dæmpede farver, der passer til puds-grunden (`ground-100`). Danske omgivelser. Ingen tekst eller logoer i billedet, intet poseret smil, ingen stockfoto-stemning. Ingen skærme med læsbart indhold.

Billederne skal ikke ændre layoutet. Rør ikke telefonen, sagsmappen og stemplerne; de er bygget i HTML og skal forblive tekst.

## Kendte huller

- Logomærket er tegnet direkte i siden (`<symbol id="mark">`), fordi `aftalt-mark.svg` og `aftalt-mark-ink.svg` endnu ikke ligger i `design-system/assets/Logo/`. Når filerne findes, skal de erstatte symbolet.
- Fontene hentes fra Google Fonts. Skal siden køre på en projektor uden net, skal de indlejres (se regel 6 i roden).
- Citatet i Problemet er gengivet fra en samtale med Dansk Håndværk. Ret ordlyden, hvis den skal være mere præcis.

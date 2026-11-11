# Aftalt

Dokumentationslag til håndværkere ("Det aftalte, dokumenteret."). Kunde: Dansk Håndværk (garantiordningen).

Live (GitHub Pages fra `main`): https://ralf-commits.github.io/aftalt/ sender videre til salgssiden. Prototypen ligger på https://ralf-commits.github.io/aftalt/prototype/ og viser Dansk Håndværk-udgaven som standard; Aftalts egen stil ligger på `prototype/?brand=aftalt`.

## Indhold
- `demo/index.html`: vælg mellem Aftalt og Dansk Håndværk-medlemsudgaven.
- `dansk-haandvaerk/index.html`: indgang til prototypen (samme som standardudgaven). Se `demo/README.md` for brandstatus.
- `index.html`: sender videre til `salgsside/`, så salgssiden er forsiden.
- `prototype/index.html`: interaktiv prototype i én fil (mobil/desktop, simuleret ur, kundens telefon). Åbn direkte i browseren. Ingen build.
- `moede/index.html` og `moede/Aftalt-salgsmoede.pdf`: mødesiden. Sagen fortalt kapitel for kapitel som præsentation, med fire AI-illustrationer. Live på `/aftalt/moede/`.
- `salgsside/index.html`: one-pager til salgsmødet med Dansk Håndværk. Har billedpladser til genererede billeder; se `salgsside/README.md`.
- `design-system/tokens.json` og `design-system/README.md`: farver, typografi, afstande og brandbog. Kilden til alt visuelt.
- `design-system/dansk-haandvaerk/`: Dansk Håndværks farver, font og logo til medlemsudgaven. Se mappens README for regler.

## Til AI-værktøjer (ChatGPT, Claude m.fl.)
Opgave: gør prototypen visuelt skarpere til et salgsmøde med Dansk Håndværk.

Regler:
1. Behold flowet og skærmene: Sag, Aftale, Byggedag, Aflevering, Sagsmappe, samt kundens SMS-godkendelse.
2. Brug kun værdier fra `design-system/tokens.json`. Opfind ikke nye farver. Fonte: Bricolage Grotesque (display), IBM Plex Sans, IBM Plex Mono.
3. Stemplet (mono-linje: dag · klokkeslæt · kilde, med hængelås når låst) er signaturen. Bevar det.
4. Tonen er rolig og udramatisk. Intet pral, ingen emojis. Tekst på dansk.
5. Fotos i prototypen er pladsholdere; rigtig kameraadgang kommer i det rigtige produkt.
6. Hold det som én HTML-fil uden build, så den kan åbnes på en mødeprojektor uden net (fonte kan indlejres).
7. Ændringer leveres som pull request mod main (aldrig gh-pages). Ralf ser ændringen og merger. Main går live på GitHub Pages få minutter efter merge.
8. Sagens fakta (navne, beløb, datoer, koder) står i `salgsside/README.md` og skal være ens på alle sider.

# Aftalt

Dokumentationslag til håndværkere ("Det aftalte, dokumenteret."). Kunde: Dansk Håndværk (garantiordningen).

## Indhold
- `prototype/index.html`: interaktiv prototype i én fil (mobil/desktop, simuleret ur, kundens telefon). Åbn direkte i browseren. Ingen build.
- `design-system/tokens.json` og `design-system/README.md`: farver, typografi, afstande og brandbog. Kilden til alt visuelt.

## Til AI-værktøjer (ChatGPT, Claude m.fl.)
Opgave: gør prototypen visuelt skarpere til et salgsmøde med Dansk Håndværk.

Regler:
1. Behold flowet og skærmene: Sag, Aftale, Byggedag, Aflevering, Sagsmappe, samt kundens SMS-godkendelse.
2. Brug kun værdier fra `design-system/tokens.json`. Opfind ikke nye farver. Fonte: Bricolage Grotesque (display), IBM Plex Sans, IBM Plex Mono.
3. Stemplet (mono-linje: dag · klokkeslæt · kilde, med hængelås når låst) er signaturen. Bevar det.
4. Tonen er rolig og udramatisk. Intet pral, ingen emojis. Tekst på dansk.
5. Fotos i prototypen er pladsholdere; rigtig kameraadgang kommer i det rigtige produkt.
6. Hold det som én HTML-fil uden build, så den kan åbnes på en mødeprojektor uden net (fonte kan indlejres).
7. Ændringer som pull request, aldrig direkte på main.

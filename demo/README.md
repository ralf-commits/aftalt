# To prototypeudgaver

- `../prototype/`: Aftalt, som hidtil.
- `../dansk-haandvaerk/`: indgang til Dansk Håndværk-udgaven.
- `./`: præsentationsside med begge udgaver.

Begge indgange bruger `prototype/index.html`. Den eneste særlige URL-parameter er
`brand=dansk-haandvaerk`; ukendte værdier falder tilbage til Aftalt. Der gemmes
hverken brandvalg eller sagsdata på tværs af indlæsninger. Nulstilling bevarer den
valgte afsender, og en ny indlæsning starter en frisk demonstrationssag.

Brandkonfiguration og navnetræk ligger under `shared brand presentation` i HTML-filen.
Det særskilte tema ligger under `Whitelabel concept`. Fag, handlinger, validering,
simuleret tid og sagsdata er fælles. Ingen build eller ekstra runtime-afhængigheder.

Dansk Håndværks afsender vises i præsentationshoved, navigation, mobilhoved,
kundens telefon, SMS-kvitteringer og sagsmappe-dialog. Tømrerfirma Holm er fortsat
aftalepart og afsender på arbejdet. Der opfindes ingen officielle SMS-domæner.

## Brandstatus

Dette er en foreløbig visuel medlemsudgave, ikke en verificeret gengivelse af
Dansk Håndværks designmanual. Miljøets netværk blokerede www.dhv.dk under arbejdet.
Navnet vises som tekst; der er ikke tegnet et uofficielt logo. Farverne kommer fra
det eksisterende tokensæt. Officielle farver, typografi og logo skal verificeres,
når brandmateriale eller netværksadgang er tilgængelig.

Leveres til review mod main. Ingen af disse routes bliver live før merge.

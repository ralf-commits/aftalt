# To prototypeudgaver

- `../prototype/`: Aftalt, som hidtil.
- `../dansk-haandvaerk/`: indgang til Dansk Håndværk-udgaven.
- `./`: præsentationsside med begge udgaver.

Begge indgange bruger `prototype/index.html`. Den eneste særlige URL-parameter er
`brand=dansk-haandvaerk`; ukendte værdier falder tilbage til Aftalt. Der gemmes
hverken brandvalg eller sagsdata på tværs af indlæsninger. Nulstilling bevarer den
valgte afsender, og en ny indlæsning starter en frisk demonstrationssag.

Brandkonfiguration og navnetræk ligger under `shared brand presentation` i HTML-filen.
Det særskilte tema følger `design-system/dansk-haandvaerk/tokens.json`. Fag, handlinger, validering,
simuleret tid og sagsdata er fælles. Ingen build eller ekstra runtime-afhængigheder.

Dansk Håndværks afsender vises i præsentationshoved, navigation, mobilhoved,
kundens telefon, SMS-kvitteringer og sagsmappe-dialog. Tømrerfirma Holm er fortsat
aftalepart og afsender på arbejdet. Der opfindes ingen officielle SMS-domæner.

## Brandstatus

Udgaven bruger logoet, garantimærket og designværdierne fra
`design-system/dansk-haandvaerk/`. Materialet er aflæst fra dhv.dk og er ikke en
officiel designmanual; se mappens README for kilder og anvendelsesregler.

Logoet er indlejret uændret og vises på hvide flader med korrekt billedforhold.
Garantimærket vises kun i medlemsudgavens garantiafsnit i sagsmappen. Ingen af
logoerne vises i Aftalt-udgaven, på salgssiden eller på vælger-siden.
Lexend Latin er indlejret med licens og kildefiler i brandmappens `fonts/`.
Primærfarven er blue-01 (#005489), sidegrunden blue-03-40 (#F4F6F9), den mørke
sagsmappeflade navy (#013B60), og brødtekstfarven ink (#1D1D1B). De eksisterende
semantiske farver til godkendt, afventer og afvist er fælles for de to udgaver.

Leveres til review mod main. Ingen af disse routes bliver live før merge.

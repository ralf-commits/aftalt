# Feedback fra Rasmus (10. nov 2026)

Givet på Dansk Håndværk-udgaven af prototypen (`main`, efter PR #7). Arbejdet foregår på branchen `feedback/rasmus`, så `main` er urørt, indtil ændringerne er set og godkendt.

## Hvad han sagde

1. **Ny sag er for generisk.** Først kontaktoplysninger, derefter en definition af, hvad der skal aftales. Snævr opgaven ind (inde/ude, bad/køkken/stue), så man ved, om det er VVS- eller tømrerarbejde, tjek certifikater og garanti, og først derefter selve opgaven, prisen og hvad der ikke er med.
2. **Tjeklister ud fra branchens regler.** Find SOP'er og "lærebøger", f.eks. Bygningsreglementet (BR18), som tjeklisterne trækkes ud fra.
3. **To farver til to oplevelser.** Håndværker i blå, kunde i lilla.
4. **Vis udvekslingen i ét forløb.** På siden: håndværkerens og kundens telefon over for hinanden, skridt for skridt (som Skiftr-eksemplet).
5. **Skærmene vandret i rækkefølge.** F.eks. fem skærme side om side.
6. **Det, han kan lide:** godkendelsesprocessen og de dokumenterede billeder.
7. **Forretningsmodel:** 0,5 % af transaktionen.

## Opgaver

- [x] Ny sag som trin-for-trin: kontakt, hvor (inde/ude, rum), hvad (spørgsmål der afgør fag), autorisationer og garanti, tjekliste, pris og "ikke med".
- [x] Research-notat for vådrum: `noter/research-vaadrum.md`. BR18, SBi-anvisning 252, Byg-Erfa, autorisationer og Dansk Håndværk Garanti. GVK viste sig at være Gulvbranchens Vådrumskontrol (kun vinyl). Punkter mærket [verificér] skal tjekkes mod kilderne.
- [x] Tjekliste i prototypen udvidet fra notatets 23 punkter: 11 checkpoints med kilde pr. punkt (notatets A- og C-punkter dækkes af aftale- og afleveringsskærmene).
- [x] Farve til kundens side. Lyng (`lyng-700`/`lyng-100`/`on-lyng`) er tilføjet designsystemet efter Ralfs ok.
- [x] Salgsside: udvekslingsflow med to telefoner i zigzag.
- [x] Salgsside: filmstrimmel med de fem skærme vandret (sektionen "Fem skærme").
- [x] Salgsside: sektion "Bygget på branchens regler" med link til research-notatet.
- [x] Forretningsmodeller: 0,5 % af transaktionen er regnet ind som model 6 på forretningsmodel-siden til Julius (privat Claude-side, ikke i repoet, da repoet er offentligt). Beløbet kendes fra de godkendte aftaler og tillæg i Aftalt.

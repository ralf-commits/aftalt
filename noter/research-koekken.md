# Research: krav ved køkkenrenovering som grundlag for Aftalt-tjeklisten

Dato: 11. november 2026

## Indledning

Notatet samler de krav, køkken-tjeklisten i prototypen bygger på, efter samme metode som `noter/research-vaadrum.md`. Et køkken er ikke et vådrum i reglernes forstand (medmindre det har gulvafløb), så regelgrundlaget er tyndere end for badeværelser: det vigtigste er vandinstallationer, el, ventilation og autorisationer. Resten er producentanvisninger og god montageskik.

Kildetyper som i vådrumsnotatet:

- **Lovkrav**: BR18 og autorisationsreglerne. Skal overholdes.
- **Anvisning / god praksis**: BR18's vejledninger, Rørcenter-anvisning 027, Byg-Erfa. Målestok for "fagmæssigt korrekt".
- **Brancheordninger**: Dansk Håndværk Garanti (se vådrumsnotatet, afsnit 5; gælder uændret for køkkensager hos private).

### Metode og forbehold

Som ved vådrumsnotatet er indholdet hentet via websøgning, der gengiver uddrag af kilderne, ikke ved læsning af de fulde kildesider. Flere af de centrale udsagn kommer fra sekundære kilder (Bolius, Tænk, leverandørsider). Punkter markeret **[verificér]** skal kontrolleres i kilden, før tjeklisten låses.

---

## 1. Bygningsreglementet BR18 (lovkrav)

**Køkken er ikke vådrum.** § 339 (vådrum) gælder rum med gulvafløb. Et almindeligt køkken uden gulvafløb er ikke omfattet; de generelle fugtkrav i kapitel 14 gælder stadig.

**Ventilation, § 443:** Køkkener i boliger skal have emhætte med mekanisk udsugning over kogepladerne og afkast til det fri. Udsugningen skal være regulerbar og kunne forøges til mindst 20 l/s. Emhætter med recirkulation (kulfilter) opfylder normalt ikke kravet. Sekundære kilder nævner højere tal afhængigt af køkkenets udformning (40 l/s i lukket køkken, 120 l/s i åbent) **[verificér tallene i gældende § 443 og vejledning]**. Ved udskiftning og ombygning må ventilationen ikke blive dårligere end før **[verificér grænsen for hvornår kravet udløses ved renovering]**.

**Vandinstallationer, § 406:** Vandinstallationer skal projekteres og udføres, så der er sikkerhed mod udsivning og udstrømning, og så utætheder let kan konstateres. Det er samme princip som vådrummets meldesystem: skjulte dele skal kunne "melde" en utæthed, før den gør skade (fx tomrør bag indbyggede armaturer).

**Kilder:**
- BR18 § 443 (ventilation i boliger): https://www.lovguiden.dk/loven/br18/443,444
- BR18 vejledning om vand (PDF): https://www.bygningsreglementet.dk/media/sgpdo2bl/vejledning_vand.pdf
- Bolius om emhættekrav: https://www.bolius.dk/koeb-af-emhaette-18975 og https://www.bolius.dk/emhaette-med-kulfilter-36183

---

## 2. Vand og afløb (lovkrav og anvisning)

1. **Skjulte samlinger:** Siden 1990 har det ikke været lovligt at udføre skjulte rør med utilgængelige samlinger. Samlinger skal være tilgængelige, eller der skal bruges rør-i-rør med koblingsdåse og tomrør, så en utæthed bliver synlig. (Sikkerhedsstyrelsens håndbog om VVS-installationer; BR18 § 406)
2. **DS 439 (vandnormen):** 2009-udgaven er delvist forældet, og BR18 henviser kun til dele af den som niveau. Dimensioneringsreglerne er under opdatering. **[verificér hvilken udgave der er gældende, og om en 2024-revision er udkommet]**
3. **Tryk- og tæthedsprøvning:** BR18's grundlag for tæthedskontrol af brugsvandsinstallationer er Rørcenter-anvisning 027, med særskilte afsnit for metal- og plastrørsystemer. Prøvningen bør dokumenteres med manometer i billedet, som i vådrums-tjeklisten. **[verificér prøvetryk og metode i anvisning 027]**
4. **Opvaskemaskine:** Skal have stophane, og tilslutningen skal kunne lukkes. En boligejer må selv tilslutte en opvaskemaskine til eksisterende stophane; nye rør og indgreb i den faste installation kræver autoriseret VVS. I en håndværkersag udføres tilslutningen af VVS, og stophanen fotograferes synlig.
5. **Afløb:** Nye afløbstilslutninger og ændringer i faste afløbsinstallationer kræver autoriseret VVS-installatør (DS 432 som norm).

**Kilder:**
- Sikkerhedsstyrelsen, håndbog: VVS-installationer (PDF): https://dev.sik.dk/sites/default/files/2021-01/11_-_vvs-installationer.pdf
- BR18 vejledning om vand: https://www.bygningsreglementet.dk/media/sgpdo2bl/vejledning_vand.pdf
- Rørcenter-anvisning 027, Vandinstallationer: https://bygningsreglementet.dk/-/media/Br/Kap_21_Vand/anvisning-027-Vandinstallationer.pdf
- Bolius, montér selv vask og armatur (grænser for eget arbejde): https://www.bolius.dk/monter-selv-din-nye-koekkenvask-og-armatur-35728
- Bolius, reparation af skjulte samlinger: https://www.bolius.dk/reparation-af-skjulte-samlinger-paa-vandroer-99852

---

## 3. El (lovkrav)

1. **Kræver autoriseret elinstallatør:** Nye elinstallationer, udvidelse af eksisterende (fx ny komfurgruppe, nye stikkontakter, ny fast tilslutning til emhætte), ændringer i gruppetavlen, og fast tilslutning af komfur, ovn eller emhætte uden stikprop.
2. **Må udføres uden autorisation:** Tilslutning af komfur, ovn og emhætte med stikprop i eksisterende stikkontakt.
3. **Installationsregler:** DS/HD 60364-serien (via installationsbekendtgørelsen), herunder HPFI-beskyttelse. Prototypens checkpoint "El til komfur og emhætte før lukning" dokumenterer føringsveje, før de skjules bag elementer, plus HPFI-test.
4. I køkkener gælder ingen særlige zonekrav som i badeværelser; placering ved vask følger de almindelige regler. **[verificér om DS/HD 60364 stiller særkrav ved køkkenvask]**

**Kilder:**
- Tænk, hårde hvidevarer, må du selv tilslutte: https://taenk.dk/forbrugerliv/bolig/haarde-hvidevarer-maa-du-selv-tilslutte
- Bolius, nyt køkken: 8 ting du ikke må lave selv: https://www.bolius.dk/nyt-koekken-8-ting-du-ikke-maa-lave-selv-20936
- Bolius, love og regler om gør det selv-arbejde: https://www.bolius.dk/love-og-regler-om-goer-det-selv-arbejde-17478

---

## 4. Byg-Erfa og skadeserfaring (god praksis)

Der blev **ikke fundet** et Byg-Erfa-blad specifikt om køkkener. Relevante blade fra vådrumsnotatet gælder tilsvarende for skjulte installationer bag køkkenelementer: rørgennemføringer (53) og rør-i-rør med meldesystem. Typiske skader i køkkener ifølge forsikrings- og skadeskilder: utætte koblinger under vask, afløbsslanger fra opvaskemaskine og skjulte samlinger bag elementer. **[verificér på byg-erfa.dk om der findes blade om installationsskakte/indbyggede installationer, og suppler med skadesstatistik fra DH's garantisager]**

**Kilder:**
- Byg-Erfa, gennemføring af rør: https://byg-erfa.dk/gennemfoering-af-roer-vaadrumsgulve-og-vaegge
- Tekniq, Bedre installationer (PDF): https://www.tekniq.dk/media/b3wjp5hf/bedre_installationer_2018.pdf

---

## 5. Dansk Håndværk Garanti

Som for vådrum: ordningen dækker håndværksarbejde for private op til 150.000 kr. inkl. moms pr. sag, prisklager er undtaget, og fra 2026 går tvister først gennem DH's hurtige tvistløsning (30 dage). Se `noter/research-vaadrum.md`, afsnit 5 og 8. Dokumentation af skjulte installationer bag køkkenelementer rammer samme bevisproblem som i vådrum: skjult arbejde kan ikke fotograferes bagefter.

---

## 6. Tjeklisten i prototypen, holdt mod grundlaget

| Checkpoint | Grundlag |
|---|---|
| Før nedrivning: eksisterende køkken | God praksis: beskytter mod tvist om forudbestående skader |
| Vand og afløb før lukning | BR18 § 406, DS 439/432, autoriseret VVS. Stophane til opvaskemaskine i billedet |
| El til komfur og emhætte før lukning | Autoriseret el, DS/HD 60364, HPFI |
| Emhættens aftræk til det fri | BR18 § 443: mekanisk udsugning, afkast til det fri |
| Vægge lukket og spartlet | Montageforudsætning (producentanvisning) |
| Elementer monteret i lod og vater | Producentens monteringsvejledning |
| Bordplade: udskæringer forseglet | Producentens anvisning; fugt ved vask og kogeplade er en kendt skadesårsag |
| Vask og maskiner tilsluttet, tæthedstjek | Rørcenter-anvisning 027 (tæthedskontrol); autoriseret VVS |

Aftryk fra researchen: checkpointet "Emhættens aftræk til det fri" er tilføjet prototypen sammen med notatet, fordi det er et direkte lovkrav, der ofte overses ved renovering (recirkulation opfylder det ikke).

---

## 7. Autorisationer, opsummeret for køkkensagen

- **Autoriseret VVS:** Nye vandrør og afløb, flytning af vask, indgreb i faste installationer.
- **Autoriseret el:** Ny komfurgruppe, nye stik, fast tilslutning af emhætte eller komfur, ændringer i tavlen.
- **Uden autorisation:** Udskiftning af armatur og vask med vandlås på eksisterende tilslutning, tilslutning af hvidevarer med stikprop, tilslutning af opvaskemaskine til eksisterende stophane.
- **Gaskomfur:** Alt arbejde på gasinstallationer kræver autoriseret VVS/gas. Ikke med i demosagen. **[verificér om DH's medlemmer typisk møder gas i køkkensager]**
- **Tjek i Aftalt:** Autorisationsnumre slås op i Sikkerhedsstyrelsens autorisationsregister (som i vådrumsnotatet, afsnit 7).

---

## 8. Åbne spørgsmål

1. Gældende udgave af DS 439 og status for revisionen af dimensioneringsreglerne.
2. De præcise luftmængdekrav i gældende § 443 og vejledning (20, 40 eller 120 l/s afhængigt af køkkentype), og hvornår kravet udløses ved renovering.
3. Findes der Byg-Erfa-blade om skjulte installationer bag inventar, og kan DH levere anonymiserede køkkensager fra garantiordningen til at prioritere tjeklisten?
4. Prøvetryk og metode for tæthedskontrol i Rørcenter-anvisning 027.
5. Skal gaskomfur-varianten med i prototypen?

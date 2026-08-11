---
id: 76aa6153-518c-40b5-bb51-bfa588d8001a
title: Oppgavestyring
weight: 10
lastmod: 2026-08-12T01:53:53+02:00
last_editor: Erik Hagen

---

Utkast, august 2026. Skrevet som grunnlag for diskusjon, ikke som anbefaling.

## Situasjonen i dag

Prosjektet styrer oppgaver to steder samtidig:

- **Kjerneteamet bruker MS Planner**, som er lett tilgjengelig i det
  Microsoft-miljøet deltakerne bruker til daglig.
- **Pilotene bruker GitHub issues** i et felles repo, `Oppgaver`, der hver sak
  merkes med hvilken pilot den hører til.

`Oppgaver` ble opprettet for pilot 1 i februar 2026 og har siden vokst inn i
rollen som felles backlog. I august 2026 ligger det 62 saker der – 6 merket
pilot 1, 14 pilot 2 og 24 pilot 3. Pilot 4 har fått en etikett, men ikke tatt
den i bruk.

## Spørsmålet

Ville GitHub-prosjekter vært et bedre valg enn Planner – og i så fall, hva er
det egentlig som gjør dem bedre?

Argumentet er ikke at GitHub er et bedre oppgaveverktøy. Planner er
sannsynligvis enklere for den som ikke koder. Argumentet er at oppgavene da
ligger *samme sted som arbeidet*: dokumentasjonen, forslagene og
beslutningene. En sak kan peke på en konkret endring, og en endring kan lukke
en sak.

Motargumentet er like reelt: verktøyet må passe dem som skal bruke det. Et
oppgavesystem ingen åpner er verdiløst, uansett hvor godt det er koblet til
resten. Dette er ikke et spørsmål om hvilket verktøy som er best, men om hvor
terskelen skal ligge – og for hvem.

## Felles backlog eller én per pilot?

Pilotene har egne repoer for innhold, men deler backlog. Det kan se
inkonsekvent ut, og gir samtidig noe verdifullt: man oppdager at flere piloter
holder på med det samme.

Her ligger et skille som er lett å bomme på:

- **Samme oppgave for flere piloter** – ett stykke arbeid, flere som har nytte
  av det. Felles begrepsapparat, overordnet arkitektur, metodikk og
  arbeidsform.
- **Samme oppgavetype i hver pilot** – parallelle instanser med hvert sitt
  innhold. ROS- og personvernvurderinger må gjøres per pilot: ulike
  opplysninger, ulike hjemler, ulike risikoer. De kan ikke slås sammen.

Den første typen taler for en `Tverrgående`-etikett. Den andre taler for felles
**maler**, ikke felles saker – gjenbruksverdien ligger i sjekklisten, ikke i
oppgaven.

Prisen ved felles backlog er at varsling ikke lar seg skille per pilot. GitHub
har ingen abonnering på etikett; man følger alt eller ingenting. Det er samme
skille mellom *ansvar* og *interesse* som gjelder ellers i prosjektet, og her
er det ikke løsbart med dagens verktøy.

## Hvorfor dette er en leveranse, ikke bare husholdning

Et økosystem består av aktører som ikke er underordnet hverandre. Da kan ingen
pålegge de øvrige et verktøy, og heller ikke en arbeidsmåte. Spørsmålet om
hvordan felles arbeid koordineres uten felles linjeledelse er derfor et
generelt problem, ikke en intern detalj – og erfaringene herfra er noe andre
kan bruke.

## Åpne spørsmål

- Bør oppgavene ligge i pilotenes egne repoer, med et prosjektbrett på
  organisasjonsnivå som henter saker fra flere repoer? Da får man både lokal
  kobling mellom sak og endring, og tverrgående utsyn.
- Hva skal til for at et verktøyskifte ikke bare flytter arbeidet til et sted
  der færre ser det?
- Hvordan skal oppgaver som gjelder flere piloter merkes – og hvem eier dem?
- Kan to verktøy leve side om side over tid, eller er delt oppgavestyring en
  tilstand som alltid forfaller?

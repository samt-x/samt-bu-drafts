---
id: 76aa6153-518c-40b5-bb51-bfa588d8001a
title: Oppgavestyring
weight: 10
lastmod: 2026-08-12T02:59:34+02:00
last_editor: Erik Hagen

---

Hvordan bør oppgaver styres i et samarbeid der flere organisasjoner deltar, og
ingen av dem er overordnet de andre?

Dette er en drøfting av hva som ser ut til å være god praksis, med erfaringene
fra SAMT-BU som grunnlag. Et konkret forslag for dette prosjektet finnes under
[Innspill om utvidet bruk av GitHub for oppgavestyring](https://docs.samt-bu.no/utkast/diverse/github-oppgavestyring/).

Eksemplene er hentet fra GitHub, som SAMT-BU bruker. Prinsippene er ikke
bundet til den plattformen – se avsnittet om verktøy nederst.

Utkast, august 2026.

## Oppgaver bør ligge der arbeidet ligger

Når en oppgave og resultatet av den ligger på hvert sitt sted, må noen holde
dem sammen manuelt. Det er arbeid ingen er tildelt, og det stopper den uka
vedkommende har annet å gjøre.

Ligger de samme sted, kan en oppgave vise til en konkret endring, og en endring
kan lukke oppgaven den svarte på. Sporet blir stående av seg selv, uten at noen
vedlikeholder det.

Dette er ikke et argument for et bestemt verktøy. Det er et argument for at
avstanden mellom «det vi skal gjøre» og «det vi gjorde» bør være kort.

## Tverrgående arbeid trenger et hjem som ikke tilhører noen

I et samarbeid med flere parter finnes det alltid arbeid som ikke tilhører noen
enkelt del: felles begreper, felles arkitektur, felles arbeidsform.

Uten et eget sted havner slikt arbeid ett av tre steder. Det merkes med én
tilfeldig valgt del av prosjektet. Det legges hos den mest sentrale parten, der
de andre ikke ser det. Eller det blir ikke skrevet ned.

Alle tre er tap, men det siste er verst, fordi det ikke etterlater spor.

## Verktøyvalg som følger organisasjonskartet, befester organisasjonskartet

Det vanlige rådet mot å bruke to systemer samtidig er at slikt forfaller: ett
vinner stille, og det andre blir liggende med gamle saker ingen har lukket.

Men når delingen følger en organisatorisk skillelinje – én gruppe her, en annen
der – forfaller den ikke. Den er tvert imot ganske stabil, nettopp fordi de to
gruppene sjelden trenger hverandres oppgaveliste til daglig.

Og det er der problemet ligger. En stabil deling langs en organisasjonsgrense
gjenskaper den siloen samarbeidet skulle bryte ned. Risikoen er ikke at
ordningen slutter å virke, men at den virker – og at den gjør arbeidet på den
andre siden usynlig uten at noen merker det.

Det betyr ikke at alle må bruke samme verktøy til alt. Intern
oppgavefordeling i én organisasjon er noe annet enn felles arbeid. Men det
felles arbeidet bør ligge et sted alle deltakerne faktisk ser.

## To slags «felles» som er lette å blande

Når flere parter gjør noe av det samme, er det verdt å skille mellom to
tilfeller:

**Samme oppgave for flere.** Ett stykke arbeid, flere som har nytte av
resultatet. Et felles begrepsapparat lages én gang. Her er delt eierskap
riktig, og oppgaven bør merkes som tverrgående.

**Samme oppgavetype hos hver.** Parallelle oppgaver med hvert sitt innhold. En
risiko- og personvernvurdering må gjøres for hver enkelt løsning: ulike
opplysninger, ulike hjemler, ulike risikoer. De kan ikke slås sammen.

Blandes de to, ender man enten med å duplisere arbeid som burde vært gjort én
gang, eller med å slå sammen vurderinger som måtte vært gjort hver for seg.

For det andre tilfellet ligger gjenbruksverdien i **malen**, ikke i oppgaven.
En god sjekkliste er verdt mer enn en delt sak.

## Prisen: varsling kan ikke skilles fint nok

Samler man alt på ett sted, får man synlighet på tvers – men mister muligheten
til å følge bare sin egen del. Verktøyene skiller i dag på arbeidsområde, ikke
på merkelapp. Man følger alt, eller ingenting.

Det treffer et skille som betyr mye i praksis: forskjellen mellom **ansvar** –
hvem må handle – og **interesse** – hvem vil vite. Ansvar tildeles og kan ikke
velges bort. Interesse velges selv og skal være lett å melde seg av.

Blandes de, drukner de ansvarlige i støy, eller de interesserte får varsler de
ikke kan skru av. Da skrur folk av alt, og mister også det de burde fått med
seg.

Dette er en reell kostnad ved felles arbeidsflater, og den er verdt å kjenne
til på forhånd. Den forsvinner ikke ved å velge et annet verktøy.

## Verktøy

### Hva som kreves

Skal samskaping fungere i et stort økosystem, på tvers av organisasjoner og
land, må verktøyet ha noen egenskaper som ikke er selvsagte:

- **Åpent å lese uten konto eller lisens.** Den som vurderer å delta, må kunne
  se arbeidet først.
- **Lav terskel for å bidra på tvers av organisasjonsgrenser.** Man må kunne
  foreslå en endring uten å være innmeldt hos noen andre først.
- **Varig historikk og opphav.** Hvem foreslo hva, når, og hva det ble til.
  Uten dette forsvinner sporbarheten som gjør et innspill etterprøvbart.
- **Ingen enkelt deltaker eier flaten.** Legges arbeidet i én parts
  lisensmiljø, er de andre gjester der.
- **Mulig å flytte.** Innholdet må kunne tas med til en annen plattform uten å
  skrives om.

### Git-plattformer

Git-baserte plattformer er i dag den eneste familien som har alle fem samtidig,
i praktisk bruk og i stor skala. Det er også grunnen til at internasjonalt
standardiseringsarbeid har flyttet dit: W3C utvikler nå spesifikasjoner i åpne
arbeidsområder på GitHub, der hvem som helst kan kommentere.

SAMT-BU bruker GitHub, men tilsvarende løsninger kan realiseres andre steder:

- **GitLab** – samme modell, og kan driftes i egen regi. EU-kommisjonen driver
  sin egen GitLab-tjeneste for åpen kildekode.
- **Forgejo og Gitea** – lettere alternativer beregnet på egen drift. Codeberg
  er en europeisk, ideell tjeneste bygget på Forgejo.

For offentlig sektor kan valget mellom driftet og selvdriftet ha betydning for
digital suverenitet. Arbeidsformen er den samme uansett.

### Hvorfor ikke de vanlige prosjektverktøyene

Jira, Confluence, Planner og Notion er ofte bedre på oppgavefordeling isolert
sett. Men de er bygget for én organisasjon: lesetilgang krever lisens,
deltakelse krever å bli lagt til, og innholdet er tungt å ta med seg ut.

De bryter dermed med de tre første kravene over – og det er ikke en innstilling
som kan endres. De egner seg godt til intern fordeling av arbeid, og dårlig som
felles flate i et økosystem.

### Terskelen løses med et lag oppå, ikke ved å bytte ut

Innvendingen mot git-plattformer er reell: de er laget for utviklere, og for
mange er de fremmede.

Men innvendingen treffer grensesnittet, ikke modellen. Det finnes
redigeringsverktøy som legger seg oppå og skjuler maskineriet – dette
nettstedet er selv et eksempel. Den som retter en side her, skriver i en vanlig
teksteditor i nettleseren og trenger verken å kjenne git eller å ha sett
GitHub. Samtidig kan den som vil, arbeide direkte mot repoet som før.

Det er trolig den riktige veien: behold en åpen og etterprøvbar kjerne, og senk
terskelen med lag oppå – framfor å velge et lukket verktøy fordi det er lettere
å komme i gang med.

## Det vi ikke vet ennå

- Om et samlebrett som henter saker fra flere arbeidsområder – i GitHub kalt et
  Project – gir nok oversikt i praksis, eller om det bare blir enda en flate
  ingen åpner.
- Hvor mye av verdien som ligger i verktøyet, og hvor mye som ligger i at noen
  faktisk holder oversikten ved like.
- Om terskelen for å delta senkes eller heves når arbeidet flyttes til åpne
  flater. Åpenhet gir innsyn, men åpne verktøy er ikke nødvendigvis enkle å ta
  i bruk for alle.

---
id: 76aa6153-518c-40b5-bb51-bfa588d8001a
title: Oppgavestyring
weight: 10
lastmod: 2026-08-12T03:29:44+02:00
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
  [code.europa.eu](https://code.europa.eu/) på GitLab, forvaltet av deres Open
  Source Programme Office og åpent for EU-institusjoner, utviklere og
  samarbeidende organisasjoner.
- **Forgejo og Gitea** – lettere alternativer beregnet på egen drift. Codeberg
  er en europeisk, ideell tjeneste bygget på Forgejo.

For offentlig sektor kan valget mellom driftet og selvdriftet ha betydning for
digital suverenitet. Arbeidsformen er den samme uansett.

### Prosjektverktøyene

Jira, Confluence, Planner og Notion er ofte bedre på oppgavefordeling isolert
sett. Men de er bygget for én organisasjon: lesetilgang krever lisens,
deltakelse krever å bli lagt til, og innholdet er tungt å ta med seg ut.

**OpenProject viser at disse tre ikke henger uløselig sammen.** Det er åpen
kildekode under GPL-3.0, kan driftes i egen regi eller i EU-basert sky, retter
seg uttrykkelig mot offentlig forvaltning, og brukes blant annet av
Europakommisjonen. Det oppfyller også WCAG 2.1, som er et selvstendig poeng for
offentlig sektor. Lisenskravet og innelåsingen faller dermed bort. I tillegg
integrerer det mot både GitHub og GitLab, slik at en oppgave kan kobles til den
konkrete endringen som løser den.

Det som likevel gjenstår, er bidragsmodellen. **Ingen av disse verktøyene har
en ekvivalent til fork og pull request.** For å bidra må du få en konto av en
administrator på den installasjonen. Det er en arkitektonisk forskjell, ikke en
innstilling.

Skillet går altså ikke mellom åpen og lukket kildekode, men mellom verktøy som
forutsetter at deltakerne allerede er innmeldt, og verktøy der en fremmed kan
foreslå noe uten å bli medlem av noe først.

Prosjektverktøyene egner seg derfor godt til intern fordeling av arbeid – og
OpenProject er et reelt alternativ for den som vil ha det på åpne premisser.
Som felles flate i et økosystem kommer de til kort.

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

## Utfordringer – og hvor løsningene ligger

Ingen av disse er grunner til å la være. Det er ting man bør kjenne til på
forhånd, og for hver av dem finnes det en kjent retning.

### Ett brett blir fort enda en flate ingen åpner

**Utfordringen.** Samler man alt på ett sted, kan resultatet bli en liste så
lang at den ikke gir oversikt, bare dårlig samvittighet.

**Retningen.** Skill mellom to nivåer, slik Altinn gjør – med GitHub som
verktøy i begge:

- **Porteføljenivå.** Få saker, grov oppløsning. Svarer på «hvordan går det med
  de fire pilotene».
- **Prosjektnivå.** Mange saker, fin oppløsning. Svarer på «hva gjør jeg nå».

Feilen er å blande dem i ett brett. Da blir det for detaljert for den som vil ha
oversikt, og for grovt for den som skal arbeide. To brett med ulik oppløsning
dekker begge behov, uten at saken må ligge to steder.

### Varsling kan ikke skreddersys

**Utfordringen.** Som beskrevet over: man følger et arbeidsområde, ikke en
merkelapp.

**Retningen.** Slutt å løse det med varsler. Varsler er *push* – de kommer til
deg, og kan bare skrus av eller på. Oversikt er *pull* – du oppsøker den når du
trenger den.

Et personlig utsyn på tvers – «hva er tildelt meg», «hva har endret seg i det
jeg følger» – dekker mesteparten av behovet uten en eneste e-post. Slike
spørringer på tvers av arbeidsområder finnes i verktøyene allerede.

Her er det også rimelig å vente at assistenter blir en reell hjelp: å få «dette
har skjedd siden sist som angår deg» oppsummert, framfor tjue varsler man skal
sortere selv. Da er ikke finmasket varslingsstyring lenger det som avgjør om
man henger med.

### Noen må holde oversikten ved like

**Utfordringen.** Et brett som ikke stemmer er verre enn ingen brett, fordi
folk stoler på det en stund før de slutter.

**Retningen.** Utled status av arbeidet i stedet for å vedlikeholde den. Lukkes
en sak av seg selv når endringen den gjelder er tatt inn, er brettet oppdatert
uten at noen har gjort noe. Det er også grunnen til at koblingen mellom oppgave
og endring er verdt å prioritere.

### Terskelen for dem som ikke koder

**Utfordringen.** Git-plattformer er fremmede for mange.

**Retningen.** Legg noe oppå framfor å bytte ut – se avsnittet om verktøy. Det
gjelder oppgavesiden like mye som innholdet: et brett kan brukes gjennom et
enklere grensesnitt uten at kjernen endres.

---

Det gjenstår å prøve dette ut i praksis i SAMT-BU. Retningene over er hentet fra
andre som har gjort det, ikke fra egne erfaringer ennå.

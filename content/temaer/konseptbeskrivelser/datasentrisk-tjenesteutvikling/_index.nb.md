---
id: 39286298-056f-4d68-9fe0-cdea507f59cb
# id: auto-generert – kopierte verdier overskrives automatisk ved push
title: "Datasentrisk tjenesteutvikling"
linkTitle: "Datasentrisk tjenesteutvikling"
weight: 10
lastmod: 2026-05-31T13:48:42+02:00
last_editor: Erik Hagen

---

*Konseptbeskrivelse for SAMT-BU – utkast til arkitekturgruppa*

---

## 1. Sammendrag

Datasentrisk tjenesteutvikling er en arkitektonisk forpliktelse til at data – med felles, eksplisitt mening – er det stabile, mens applikasjoner er utskiftbare projeksjoner mot dataene. Denne konseptbeskrivelsen forplikter SAMT-BU til den retningen, og til å realisere den gjennom en virtuell, lagdelt kunnskapsgraf med dataproduktorientering.

Bakgrunnen er lett å formulere og vanskelig å løse: sammenhengende tjenester for barn og unge på tvers av barnehage, skole, kommune og stat forutsetter at de involverte forstår de samme begrepene på samme måte – at «elev», «vedtak», «samtykke» og «bosted» betyr det de skal, også når data hentes fra ulike etater. Dagens applikasjonssentriske landskap legger denne forståelsen i kode, spredt på hvert fagsystem, der den må vedlikeholdes på nytt for hver integrasjon. Datasentrisk arkitektur flytter meningen ut av koden og inn i et delt semantisk lag som applikasjonene – og etter hvert KI-agentene – bygger mot.

Konseptet hviler på tre ben: *datasentrisk* som arkitekturvalg (data, ikke applikasjoner, er det stabile), *dataproduktorientering* som organisering (data leveres som produkter med tydelig forvaltningsansvar, kontrakter og semantisk annotasjon), og en *virtuell kunnskapsgraf* som realisering (data forblir hos sine autoritative kilder, og en lagdelt ontologi binder dem sammen gjennom mapping). Den avgjørende egenskapen er at grafen vokser monotont: nye begreper kan legges til uten å bryte det som allerede virker. Det er denne egenskapen som gjør at verdi kan hentes gradvis, pilot for pilot, uten å vente på en ferdig modell.

Konseptet er forankret i internasjonale rammeverk – særlig EUs operative interoperabilitetsmekanismer ([MIMs Plus](#mims-plus)) og [SEMICs Core Vocabularies](#semic-core-vocabularies) – slik at norsk offentlig sektor kan kobles på det europeiske økosystemet av delte begreper framfor å bygge en særvariant.

Like viktig er hva konseptet *ikke* gjør. Det sentraliserer ikke data, det bytter ikke ut eksisterende fagsystemer, og det velger ikke teknologi, produkter eller leverandører – slike valg hører til målbildearkitekturen og arkitekturgruppas videre arbeid. Konseptbeskrivelsen forplikter retningen, ikke beslutningene under.

Dokumentet kan leses lineært eller oppslagsvis: konseptvalget med de vurderte alternativene (seksjon 3), den arkitektoniske realiseringen (seksjon 4), sammenhengen med søknadens eget språk (seksjon 5), den internasjonale forankringen (seksjon 6), implikasjonene for piloter, partnere og KI (seksjon 7), og til slutt avgrensningen og de åpne spørsmålene som hører til det videre arbeidet (seksjon 8).

---

## 2. Innledning

Dette dokumentet er en konseptbeskrivelse for **datasentrisk tjenesteutvikling** i SAMT-BU. Det er et utkast, plassert under [Konseptbeskrivelser](../), og er ment som innspill til arkitekturgruppa i prosjektet. Det er ikke en fasit, og det erstatter ikke målbildearkitekturen eller den videre arkitekturdiskusjonen prosjektet skal gjennomføre. Det er et arbeidsdokument som forplikter retningen, slik at de neste skrittene kan tas på begrunnet grunnlag.

### Bakgrunn

Søknaden som ligger til grunn for SAMT-BU bruker uttrykk som "mellomlag", "felles informasjonsmodeller", "tjenestekatalog" og "datavirtualisering" som plassholdere for noe det ikke fantes en etablert norsk betegnelse for da søknaden ble skrevet. Disse begrepene peker i en bestemt arkitektonisk retning, men de er ikke selvbeskrivende i den forstand at de forteller hvordan retningen skal realiseres. Det er den jobben denne konseptbeskrivelsen tar tak i.

Når en arkitekturgruppe er etablert og prosjektet er i operativ fase, er det også på tide å introdusere det presise språket konseptet krever – datasentrisk paradigme, dataproduktorientering, virtuell kunnskapsgraf, lagdelt ontologi. Disse begrepene er ikke nye for det internasjonale faglige fellesskapet, men de er ikke enda etablert i norsk offentlig-sektor-vokabular. En del av denne konseptbeskrivelsens jobb er å gjøre koblingen mellom prosjektets eksisterende språk og det presise faglige språket eksplisitt.

### Hva dette dokumentet er

Dokumentet er:

- En **arkitektonisk forpliktelse** til datasentrisk paradigme realisert gjennom dataproduktorientering og en gradvis utbyggbar virtuell kunnskapsgraf
- En **forankring i internasjonale rammeverk** – særlig MIMs Plus, SEMICs Core Vocabularies, og dataproduktorientering med semantisk anker
- En **bro** mellom søknadens språk og det presise faglige språket konseptet krever
- Et **utkast og innspill** som arkitekturgruppa kan diskutere, forfine eller forkaste

### Hva dette dokumentet ikke er

Det er likeledes viktig å være eksplisitt om hva dokumentet ikke er, slik at det leses riktig:

- *Ikke en målbildearkitektur.* Konkrete teknologivalg, leverandørvalg, infrastrukturoppsett og produktvalg hører til målbildet og kommer senere.
- *Ikke en sentralisert dataløsning.* Virtuell kunnskapsgraf betyr at data forblir hos sine autoritative kilder; integrasjonen skjer på det semantiske laget over.
- *Ikke "vent på den store grafen før vi leverer".* Den arkitektoniske retningen er gradvis utbyggbar – pilotene gir verdi underveis, ikke ved en stor fullføring.
- *Ikke at eksisterende fagsystemer skal byttes ut.* Konseptet beskriver hvordan eksisterende systemer kan kobles inn i den semantiske infrastrukturen, ikke at de skal erstattes.
- *Ikke en kritikk av enkeltløsninger.* Vi nevner FINT, Felles datakatalog og Bergen-utredningen ved navn fordi de er konkrete referansepunkter, men formålet er posisjonering, ikke nedvurdering.
- *Ikke en akademisk øvelse.* Hver del av konseptet er valgt for å fungere operativt på offentlig-sektor-skala, ikke for å oppfylle et fagteoretisk ideal.
- *Ikke en beskrivelse av nåsituasjonen.* En grundig kartlegging av eksisterende fagsystemer, dataforvaltning og samhandlingsmønstre i berørte sektorer er en del av arkitekturgruppas eget arbeid og hører ikke hjemme her.

### Hvordan dokumentet er bygget opp

Dokumentet kan leses lineært, men det er også strukturert slik at lesere kan gå direkte til den delen som er mest relevant:

- **Konseptvalg** for den som vil vite hvilke alternativer som er vurdert og hvorfor vi lander der vi gjør
- **Realiseringen** for den tekniske kjernen: virtuell kunnskapsgraf, lagdelt ontologi, dataprodukter, applikasjoner
- **Sammenheng med konsept skissert i søknaden** for koblingen mellom søknadens språk og konseptet vi presenterer
- **Internasjonal forankring** for tilkoblingen til EUs operative interoperabilitetsrammeverk (MIMs Plus, Core Vocabularies)
- **Implikasjoner** for hva konseptet betyr for piloter, partnere og KI-strategi
- **Avgrensning og åpne spørsmål** for det som hører til arkitekturgruppas videre arbeid

Konseptbeskrivelsen er skrevet med ambisjon om å være lesbar for ledere og fagfolk uten semantisk-web-bakgrunn i de første avsnittene av hver seksjon, og presis nok for arkitekter lenger ned. Hver seksjon avsluttes typisk med peker mot hva som er overlatt til arkitekturgruppa eller målbildearkitekturen.

---

## 3. Konseptvalg

Konseptvalget skal ikke være tatt før det er begrunnet. I dette avsnittet viser vi hvilke alternative konsepter vi har vurdert, hvilke krav vi har målt dem mot, og hvorfor vi lander der vi lander. Hensikten er at leseren skal kunne være uenig i konklusjonen på begrunnet grunnlag, ikke avvise den fordi alternativene aldri ble nevnt.

### Kravene ambisjonen stiller

Ambisjonen om sammenhengende, tverrsektorielle tjenester – på tvers av alt det offentlige har ansvar for – stiller disse kravene:

**1. Data nås der de eies.** Søknaden er eksplisitt på at vi ikke skal kopiere eller flytte data ut av kontekst. Folkeregisteret, Enhetsregisteret, Matrikkelen og fagsystemene i kommunene blir værende der de er.

**2. Semantisk interoperabilitet på tvers.** Det skal være mulig å vite om "samboer" i NAV, Skatteetaten og folkeregisteret refererer til samme entitet, og hvor de skiller seg. Dette gjelder hundrevis av tilsvarende begreper.

**3. Gradvis utvidelse uten brudd.** Nye begreper må kunne legges til uten at eksisterende data eller tjenester invalideres. Bakoverkompatibilitet skal være en grunnleggende egenskap ved arkitekturen, ikke en operasjonell øvelse hver gang noe endres.

**4. Internasjonal samhandling.** EUs operative rammeverk – Single Digital Gateway, Once-Only Technical System, Data Spaces og MIMs Plus – bygger på felles semantiske datamodeller (SEMICs Core Vocabularies, CPSV-AP, CCCEV, DCAT-AP og beslektede standarder). Disse modellene er RDF-baserte, selv der utvekslingsformatet på linja er XML eller JSON. Norge må kunne kobles på dette økosystemet av delte begreper, ikke bygge en særvariant. *Detaljert mapping mot MIMs Plus følger i seksjon 6.*

**5. AI-etterrettelighet.** Hvis offentlig sektor skal bruke AI-agenter i tjenesteyting, må svarene kunne etterprøves og forankres i autoritative kilder med eksplisitt mening.

**6. Felles begreper for sammenhengende brukerreiser.** Brukerreisene på tvers av etater forutsetter at samme begrep forstås konsistent. Dette er hele rasjonalen bak prosjektet.

### Vurderte alternativer

Vi har vurdert syv konsepter, fra de mest tradisjonelle til de mest ambisiøse:

**A. Sentralisert datalager (data warehouse, data lake).** Klassisk BI-tilnærming der data kopieres til ett sentralt lagringssted. Fungerer godt for analyse, men bryter direkte med kravet om at data nås der de eies. På cross-sektor-skala blir kopiering, oppdateringssyklus og governance uhåndterlig, og personopplysninger reiser betydelige juridiske spørsmål.

**B. Master Data Management (MDM) alene.** Sterkt for et avgrenset sett kjernebegreper (person, virksomhet, adresse). Men MDM er ikke i seg selv et arkitekturparadigme – det adresserer ikke det bredere spørsmålet om hvordan tjenester og applikasjoner skal forholde seg til hverandre. Vi vil bruke prinsipper fra MDM på utvalgte grunndata, men kan ikke bygge hele konseptet på det.

**C. ESB med kanonisk datamodell (hub-and-spoke / FINT-stilen).** Velprøvd tilnærming der en sentral integrasjonsbuss og en felles datamodell bringer systemer sammen. Novaris FINT er en moderne realisering for fylkeskommunene og en del av prosjektets inspirasjonsgrunnlag. Men erfaringen viser to gjentakende problemer: den kanoniske modellen blir et flaskehalspunkt som er vanskelig å evolvere, og endringer bryter ofte bakoverkompatibilitet med påkoblede systemer. Dette skaleres ikke til alle offentlige tjenester over tiår.

**D. API-mesh eller "data fabric" uten semantisk lag.** Moderne API-orientert integrasjon (REST, GraphQL, hendelser) løser tekniske koblinger, men semantikken ligger fortsatt implisitt i koden hos hver konsument. Hver ny integrasjon krever ny tolkning av hva begrepene betyr. N²-problemet flyttes, ikke fjernes.

**E. Data mesh uten kunnskapsgraf.** Dataprodukter med eierskap, kontrakter og federert governance løser mye organisatorisk. Men data mesh i sin opprinnelige form adresserer ikke den semantiske fragmenteringen mellom domener. Konsumenter må fortsatt normalisere semantikken selv ved hver kobling.

**F. Datasentrisk på relasjonsmodeller.** [McComb](#mccomb-2019) argumenterer i [*The Data-Centric Revolution*](#mccomb-2019) (kap. 8–9) for at datasentrisk arkitektur i prinsippet er mulig også med tradisjonelle relasjonsmodeller. Det er fagteknisk riktig. Men kompleksiteten vokser eksponentielt med antall virksomheter, begreper og endringstempo. Den monotone utvidelses-egenskapen som linked data gir, er vanskelig å oppnå når skjemaer er strikte. På norsk offentlig-sektor-skala blir denne varianten teoretisk farbar, men praktisk forsinkende.

**G. Datasentrisk med virtuell kunnskapsgraf.** Datasentrisk paradigme realisert gjennom en virtuell, lagdelt ontologi som refererer dataene der de eies. Dataprodukter eksponerer data med semantiske koblinger til ontologien. Dette er konseptet vi anbefaler.

### Sammenstilling

| Konsept | Data der de eies | Semantisk interop. | Gradvis utvidelse | EU-kompatibilitet | AI-etterrettelighet | Brukerreiser |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| A. Datalager / datasjø | ✗ | △ | ✗ | ✗ | △ | ✗ |
| B. MDM alene | △ | △ | ✗ | ✗ | △ | △ |
| C. ESB / kanonisk modell (FINT-stil) | ✓ | △ | ✗ | ✗ | ✗ | △ |
| D. API-mesh uten semantikk | ✓ | ✗ | △ | ✗ | ✗ | ✗ |
| E. Data mesh uten kunnskapsgraf | ✓ | ✗ | △ | △ | ✗ | △ |
| F. Datasentrisk på relasjonsmodeller | ✓ | △ | △ | △ | △ | △ |
| **G. Datasentrisk + virtuell kunnskapsgraf** | **✓** | **✓** | **✓** | **✓** | **✓** | **✓** |

Tegnforklaring: ✓ oppfyller, △ delvis, ✗ oppfyller ikke. Vurderingene er kvalitative og er gjenstand for diskusjon. Tabellens verdi ligger i å vise *mønsteret*, ikke i å være presis i hver enkelt rute.

### Konvergens, ikke maksimering

Argumentet for alternativ G er ikke at det er "best" på hver enkelt dimensjon. Argumentet er at det er det eneste konseptet som **simultant** oppfyller alle kravene, gitt ambisjonsnivået. Alternativene A–F er gode på noen kriterier hver, og noen er gode på flere – men ingen håndterer kombinasjonen.

Dette skal ikke leses som at relasjonsmodeller er dårlige, at API-er er overflødige, eller at MDM er feil. Tvert imot vil flere av disse elementene inngå i den faktiske realiseringen: data forblir typisk lagret i relasjonsdatabaser hos eierne, integrasjoner skjer ofte via API-er, og MDM-prinsipper anvendes for utvalgte grunndata. Konseptvalget G handler om det *semantiske laget over* dette, og om hvordan dataprodukter eksponerer mening – ikke om å erstatte underliggende teknologi.

### Hva konseptvalget *ikke* gjør

Det er viktig å være eksplisitt på hva dette valget innebærer og ikke. Vi har valgt et **paradigme** (datasentrisk tjenesteutvikling) og et **arkitektonisk mønster** (virtuell kunnskapsgraf med føderert lagdelt ontologi og dataprodukteierskap). Vi har **ikke** valgt:

- Konkrete teknologier (f.eks. [RDF](#rdf-og-sparql) vs. property graph, [SPARQL](#rdf-og-sparql) vs. Cypher, valg av triplestore)
- Konkrete verktøy for ontologimodellering og governance
- Konkret infrastruktur (sky vs. on-prem, hvilke fellesløsninger som utvides)
- Konkrete leverandører

Slike valg hører hjemme i målbildearkitekturen, hos arkitekturgruppa, og i pilotene. Konseptbeskrivelsen forplikter retningen, ikke beslutningene under.

---

## 4. Realiseringen: virtuell kunnskapsgraf med lagdelt ontologi

Denne seksjonen beskriver hvordan datasentrisk tjenesteutvikling skal realiseres arkitektonisk. Vi går gjennom den virtuelle kunnskapsgrafen som mønster, den lagdelte ontologien som strukturerer det semantiske innholdet, dataproduktene som bærer dataene, og hvordan disse byggeklossene henger sammen i en informasjonsarkitektur som kan vokse gradvis.

Seksjonen er den mest tekniske i denne konseptbeskrivelsen. Den er likevel skrevet for å være forståelig for arkitekturgruppa og fagledere som ikke er semantisk web-spesialister. Konkrete teknologivalg overlater vi til målbildearkitekturen.

### 4.1 Den virtuelle kunnskapsgrafen som arkitektur

En **kunnskapsgraf** er en graf der noder representerer begreper og entiteter, og kanter representerer relasjonene mellom dem. Når kunnskapsgrafen bygger på en eksplisitt **ontologi** – en formell modell av begrepene og hvordan de henger sammen – blir relasjonene maskinlesbart typede. Begrepene har en definert mening både mennesker og programmer kan resonnere over.

[Gioia](#gioia-2024) beskriver tre arkitektoniske varianter av kunnskapsgraf ([*Managing Data as a Product*](#gioia-2024), kap. 11):

1. **Datasentrisk (materialisert) kunnskapsgraf.** Data lever inni grafen. Applikasjoner skriver og leser direkte mot grafen. McCombs ideale tilstand.
2. **Knowledge warehouse (materialisert).** Data kopieres fra kildesystemene inn i grafen for lesetilgang. Eierskap forblir hos kildene.
3. **Logical knowledge warehouse / virtuell kunnskapsgraf.** Data forblir i kildesystemene. Grafen refererer til dem gjennom mapping-konsepter.

For SAMT-BU er valget av den virtuelle varianten ikke en pragmatisk innrømmelse, det er det riktige valget. Norsk offentlig sektor har autoritative registre – Folkeregisteret, Enhetsregisteret, Matrikkelen, Sikts registre – som hverken kan eller bør flyttes inn i én sentral graf. Den semantiske integrasjonen oppnås gjennom mapping mellom dataproduktene og en felles ontologi, ikke gjennom datasentralisering.

Konkret betyr det at:

- Data forblir lagret hos sine autoritative kilder, i sine eksisterende formater og systemer. (Hva som er en autoritativ kilde, og hva "eierskap" betyr i denne sammenheng, presiseres i 4.3.)
- En felles ontologi definerer hvilke begreper systemene snakker om.
- Et eget *mapping-lag* – mellom datakildene og ontologien – knytter elementer i dataene til konseptene i ontologien. Dette laget er en egen artefakt, ikke en del av selve ontologien.
- Konsumenter kan stille spørsmål mot ontologien som om data lå der som triplets, enten faktisk lagrede eller virtuelt beregnede; spørsmålene oversettes til operasjoner mot kildesystemene.

Gioia anbefaler selv denne arkitekturen som realistisk startpunkt for moderne organisasjoner, og peker på at den fullt datasentriske varianten (alternativ 1) kan være et potensielt *langtidsmål* etter at ontologi-infrastrukturen er moden. For SAMT-BUs tidsperspektiv er det den virtuelle varianten som er gjennomførbar og det den nedstrømsverdien skal hentes fra.

### 4.2 Den lagdelte ontologien

Én ontologi for hele offentlig sektor er hverken praktisk eller ønskelig. Ulike sektorer modellerer virkeligheten forskjellig fordi de har ulike formål – en pedagog tenker om "elev" annerledes enn en regnskapsfører eller en sosionom – og det er riktig at modellene reflekterer det. Samtidig må de henge sammen der det er behov for samhandling.

Den lagdelte tilnærmingen organiserer dette i fire lag:

**Øvre ontologi (upper ontology).**
Universelle begreper som overskrider domener: objekt, hendelse, tid, sted, agent, rolle. Etablerte standarder finnes ([BFO](#bfo) – Basic Formal Ontology, [GIST](#gist)). Et offentlig norsk konsept skal kunne uttrykkes som en spesialisering av disse abstrakte byggesteinene.

**Domeneontologi.**
Begreper som er felles for "offentlig forvaltning i Norge": person (med adresse, identifikator, statsborgerskap), virksomhet, tjeneste, vedtak, hendelse, samtykke, fullmakt, beslutning. Dette er kjernemodellen, og det er her det meste av det semantiske arbeidet skjer for prosjektets ambisjon om sammenhengende tjenester. SEMICs Core Vocabularies (Core Person, Core Public Service, Core Organization, Core Location, CCCEV) gir en EU-koblet startpakke for dette laget – ikke som krav vi underkaster oss, men som naturlige forankringspunkter som sparer arbeid og garanterer cross-border-kompatibilitet.

**Underdomeneontologier.**
Sektorspesifikke utvidelser: utdanning (elev, lærer, fag, vurdering, vitnemål, opptak), helse, sosial, justis, arbeid. Hver sektor modellerer sitt domene og utvider domeneontologien der det er behov for spesialisering. SAMT-BU starter naturligvis i utdanningsdomenet.

**Applikasjonsontologier.**
Modeller knyttet til en spesifikk tjeneste eller pilot, for eksempel "skolebytte ved flytting mellom kommuner" eller "deling av vitnemål til arbeidsgiver". Dette er der konkrete brukerreiser modelleres, og der det meste av prosjektets piloter vil leve.

Lagene står i et **utvidelsesforhold**: et underdomenebegrep utvider et domenebegrep, som utvider et øvre konsept. Det betyr at en applikasjon som arbeider med utdanningsspesifikke begreper, automatisk arver de generelle egenskapene fra domene- og øvre lag uten å måtte gjenta dem.

#### Hvorfor lagdelingen løser "samboer"-problemet

Et eksempel som illustrerer verdien: begrepet *samboer*. Domeneontologien kan definere et kjernebegrep "Samboer" med en minimumsdefinisjon – to personer som deler husstand uten å være gift. Skatteetatens underdomene kan utvide dette med skattemessige kriterier (sammenhengende botid, formuesfellesskap); NAVs underdomene med trygderettslige kriterier; folkeregisterets med adresse-baserte kriterier.

Begrepene er forskjellige – med rette, for de tjener forskjellige formål – men de er **eksplisitt knyttet** til samme kjernebegrep gjennom ontologien. Da kan systemer som henter data fra alle tre vite både hvor de er like og hvor de skiller seg. Det er denne typen presisjon dagens fragmenterte modelllandskap ikke gir.

#### Federerte modelleringsteam

Lagene har forskjellige eiere. Domeneontologien må eies sentralt – det er hele poenget at den er felles. Underdomeneontologiene eies av de respektive sektorene; applikasjonsontologiene av tjenesteansvarlige eller piloter.

Gioia kaller den sentrale modelleringsorganisasjonen et **føderert modelleringsteam**: representanter fra hver involvert sektor, med mandat til å forhandle om og forvalte de felles begrepene. For SAMT-BU vil dette være et fellesorgan med utsendinger fra [Digdir](#digdir), KS Digital, Udir, Sikt, HK-dir, STAF og SSB. Sammensetningen og styringen tilhører ikke konseptbeskrivelsen; men det er denne typen mekanisme som må etableres for at konseptet skal fungere i praksis.

### 4.3 Autoritative kilder, dataprodukter og applikasjoner

Ordet "eierskap" brukes om data så bredt i norsk offentlig sektor at det dekker tre forskjellige relasjoner som arkitektonisk må holdes adskilt. Konseptbeskrivelsen krever at vi gjør den distinksjonen tydelig, fordi det å samle de tre i ett begrep er en del av problemet vi vil løse.

#### 4.3.1 Tre meninger av "eierskap"

**Datasubjektets eierskap.**
Persondata tilhører den personen dataene handler om. Virksomhetsdata tilhører virksomheten. Dette er en grunnleggende rett. Den operative realiseringen i målbildearkitekturen er **digitale lommebøker** – EUDI Wallet for personer, og tilsvarende konstruksjoner for virksomheter. Det er datasubjektet som kontrollerer hvilke data som deles, med hvem, under hvilke vilkår.

**Forvaltningsansvar (hjemmel eller samtykke).**
En offentlig virksomhet kan ha *rett til å behandle* visse data – enten gjennom lovhjemmel eller gjennom samtykke fra subjektet. Dette er en juridisk-administrativ relasjon, ikke en eiendomsrett. Skatteetaten "eier" ikke skatteyterne eller deres inntektsopplysninger; etaten har hjemmel for spesifikk behandling for spesifikke formål. Når en kommune behandler data om elever, har den hjemmel eller samtykke – den er ikke "eier" i noen meningsfull forstand.

**Dataproduktansvar.**
Når denne konseptbeskrivelsen omtaler "dataprodukteier", mener vi noe mer spesifikt: den som har *operativt ansvar* for å forvalte et dataprodukt – kvalitet, tilgjengelighet, semantisk annotasjon, kontrakter og livssyklus. Dette er et forvaltnings- og leveranseansvar, ikke eiendomsrett. Folkeregisteret har dataproduktansvar for autoritativ personidentifikasjon på vegne av samfunnet; det "eier" ikke personene.

De tre relasjonene kan opptre samtidig på samme data, men de er forskjellige relasjoner og må kunne diskuteres adskilt. Mye av uklarheten i dagens debatt om datadeling, samtykke og dataminimering kommer av at de blandes sammen.

#### 4.3.2 Dagens fragmenterte situasjon

Norsk offentlig sektor har gjennom en applikasjonssentrisk utviklingshistorie endt med et stort antall fagsystemer som hver fungerer som *de facto* eier av "sine" data – med sine egne datamodeller, sine egne identifikatorer og sine egne tolkninger av delte begreper. Dette er ikke en uskyldig fragmentering. Det er det McComb diagnostiserer som det applikasjonssentriske kvagmyret ([*Software Wasteland*](#mccomb-2018), kap. 3): hver applikasjon skaper sin egen virkelighet av data, integrasjoner mellom dem multipliserer (N²), og fellesbegreper smelter sammen til lokale varianter som ikke lar seg sammenstille.

Tilnærmingen om å "samle metadata i en felles datakatalog og konsolidere over tid" har vist seg vanskelig å realisere i praksis, fordi konsolideringsarbeidet konkurrerer med løpende prioriteringer hos hver dataeier. Resultatet er at katalogen vokser med beskrivelser av overlappende og inkonsistente datasett uten at selve fragmenteringen reduseres.

Konseptbeskrivelsen aksepterer ikke denne tilstanden som utgangspunkt. Datasentrisk arkitektur forutsetter en ryddejobb der det etableres tydelige autoritative kilder, og der applikasjoner – nye eller gamle, tradisjonelle eller KI-baserte – er konsumenter, ikke eiere.

#### 4.3.3 Autoritative kilder og dataproduktansvar

Konseptet skiller mellom to grunnleggende roller i datalandskapet: **autoritative kilder** og **applikasjoner**.

Autoritative kilder har sannhetsmyndighet for et sett av begreper og tilbyr dem til resten av økosystemet. Eksempler vi allerede har i dag:

- *Folkeregisteret* for personidentifikasjon, navn og bostedsadresse
- *Enhetsregisteret* for virksomheter
- *Matrikkelen* for eiendom og bygninger
- *Sikts utdanningsregister* for utdanningstilbud og institusjoner
- *Sikts kompetansebevisregister* for vitnemål og resultater fra utdanning

Disse skal forbli autoritative. Ny autoritet for andre begreper skal etableres på samme måte: tydelig dataproduktansvar, dokumenterte kontrakter, semantisk annotasjon. Det er en sentral del av prosjektets arbeid å avklare hvor det mangler tydelige autoritative kilder – for eksempel for kommunale tjenester innen oppvekst – og å rydde der det i dag er flere overlappende autoriteter for samme begrep.

De autoritative kildene tilbyr seg som **dataprodukter** med egenskapene Gioia beskriver: tydelig dataproduktansvar (i tredje forstand av "eierskap"), eksplisitte kontrakter, selvbeskrivende metadata, og semantisk annotering som binder feltene til ontologien. Den siste – semantisk annotering, for eksempel gjennom Data Product Descriptor Specification (DPDS) med "s-context"-annotasjoner – er det som lenker det enkelte dataproduktet til den lagdelte ontologien beskrevet i 4.2. Et felt som *fødselsdato* i Folkeregisterets persondata kan annoteres som instans av *birthDate* i Core Person Vocabulary, som igjen er spesialisering av en tidsangivelse i øvre ontologi.

Den tekniske mapping-mekanismen mellom relasjonsdatabaser eller andre datakilder og den semantiske representasjonen kan formaliseres ved hjelp av etablerte standarder: **[R2RML](#r2rml-og-rml)** for relasjonsdata, **[RML](#r2rml-og-rml)** for semi-strukturert data (JSON, XML, CSV). Dette er praktiske verktøy som arkitekturgruppa kan bygge på, ikke konsernstrategiske valg.

Det er viktig å understreke: de autoritative kildene fortsetter å bruke sine eksisterende teknologier – relasjonsdatabaser, REST-API-er, hendelseskøer. Det er den **semantiske påklisteringen** (annotasjoner, mapping) som er ny, ikke selve datalageret.

#### 4.3.4 Applikasjoner som konsumenter – også KI-agenter

Alt som ikke er en autoritativ kilde, er en **applikasjon** i konseptets forstand: saksbehandlingssystemer, innbyggerflater, fagsystemer, analyse- og statistikkverktøy, dashboards, og **KI-agenter**.

For alle disse gjelder samme prinsipp: de er konsumenter, ikke eiere. Konkret:

- De skal *ikke* finne opp egne datamodeller for begreper som finnes i de delte ontologiene.
- De skal *ikke* opprette parallelle lagringer av data som er autoritative et annet sted.
- De skal *ikke* hente data, transformere dem til sin egen representasjon, og bli en de facto autoritet for "sin" versjon. Det er nettopp slik dagens kvagmyr har oppstått.
- De skal forholde seg til datasubjektets samtykker og fullmakter slik de er uttrykt i lommebøker eller tilsvarende mekanismer – ikke føre egne kopier av samtykkesregistre der det kan unngås.

For **KI-agenter** er dette særlig viktig fordi det pågår en betydelig markedshype rundt at agenter "lærer" og "husker" – som lett kan glide over i at agenter de facto eier eller skaper data. Datasentrisk arkitektur er sannsynligvis den eneste måten å integrere KI-agenter i norsk offentlig sektor på uten å skape en ny generasjon med innelåste, ikke-interoperable systemer som gjentar feilene fra første generasjon fagsystemer. En agent som svarer en innbygger om barnets skoletilbud, skal hente fakta fra autoritative kilder via kunnskapsgrafen, ikke fra et lokalt kunnskapslager den selv har konstruert. Den semantiske kunnskapsgrafen er det stabile fundamentet; agentene – som applikasjonene før dem – er erstattbare projeksjoner.

En konsekvens McComb gjør eksplisitt: i en datasentrisk arkitektur trenger man ikke flere applikasjoner over tid – man trenger færre, fordi mye av det dagens applikasjoner gjør, er å holde rede på sine egne lokale datamodeller. Når den jobben gjøres av det semantiske grunnlaget, blir applikasjoner enklere og mer utskiftbare.

### 4.4 Hvordan informasjonsarkitekturen henger sammen

Den datasentriske arkitekturen kan organiseres i fire lag (Gioia, kap. 11), som vist i tabellen. Kolonnen "ansvar" må her leses i tråd med distinksjonen i 4.3 – det er forvaltnings- og leveranseansvar, ikke eiendomsrett.

| Lag | Hva det er | Ansvar |
|---|---|---|
| Dataplan | Selve dataene i kildesystemene | Autoritative kilder / dataproduktansvarlige |
| Informasjonsplan | Data + metadata (struktur, kvalitet, tilgjengelighet, bruksvilkår) | Autoritative kilder / dataproduktansvarlige |
| Kunnskapsplan | Felles ontologi og semantiske koblinger | Føderert modelleringsteam |
| Intelligensplan | Tjenester, beslutninger, applikasjoner (inkl. KI-agenter), sluttbrukere | Tjenesteansvarlige og brukere |

Autoritative kilder og dataproduktansvarlige sørger for dataplan og informasjonsplan – de leverer data med beskrivelser av hva som ligger der. Kunnskapsplanet – ontologien – forvaltes federert av modelleringsteamet. Intelligensplanet er der verdien tas ut: sammenhengende tjenester, saksbehandling, statistikk, og KI-assisterte hjelpere som alle henter sin kunnskap fra de underliggende lagene.

#### Et arbeidende eksempel: skolebytte ved flytting

Vi tar et eksempel fra prosjektets aktuelle piloter for å vise hvordan det henger sammen. Et 14-årig barn flytter til en ny kommune midt i skoleåret.

- **I dataplan**: Folkeregisteret oppdaterer adresse. Den gamle kommunens fagsystem har eleven registrert med vurderinger og fagvalg. Den nye kommunen har skoler med ledige plasser registrert i sitt fagsystem.
- **I informasjonsplan**: Hver av disse er beskrevet som dataprodukter med metadata om hva som tilbys, hvem som eier, og hvordan tilgang fungerer.
- **I kunnskapsplan**: Domeneontologien har begreper for *person*, *bosted*, *hendelse*, *vedtak*. Underdomeneontologien for utdanning kobler dem sammen med begreper som *elev*, *skole*, *klasse*, *skolebytte*, og fastsetter relasjonen mellom "flytting" som hendelse og "skolebytte" som utløst tjenestebehov.
- **I intelligensplan**: En tjeneste – kanskje med en KI-assistert grensesnitt for foresatte – ser at hendelsen "flytting" hos en person under skolepliktig alder utløser behovet "skolebytte". Tjenesten finner relevante dataprodukter via kunnskapsgrafen, anvender forretningsregler om skolekrets, kapasitet og kontinuitet, og foreslår handlinger for kommunen og foresatte.

Vesentlig: ingen har bygget en spesifikk integrasjon "Folkeregister-X-Utdanningssystem-Y-Kommunesystem-Z". Verdien ligger i at brukerreisen settes sammen *på toppen* av en stabil semantisk infrastruktur. Nye brukerreiser – overgang fra grunnskole til videregående, oppfølging ved frafall, deling av vitnemål til arbeidsgiver – krever ikke nye integrasjoner; de krever nye spørsmål til kunnskapsgrafen, og ofte bare små utvidelser av applikasjonsontologien.

### 4.5 Gradvis utbygging – en evolusjonær arkitektur

Den lagdelte ontologien og den virtuelle kunnskapsgrafen utvikles **ikke som ett stort modellarbeid før noe leveres**. Det er en sentral del av konseptvalget, og det er det som gjør arkitekturen praktisk gjennomførbar på offentlig-sektor-skala.

Linked data og RDF har en avgjørende egenskap: **monoton vekst**. Et nytt begrep, en ny relasjon, en ny mapping kan legges til uten å invalidere det som allerede er der. Eksisterende systemer, eksisterende data, eksisterende spørringer fortsetter å fungere. Dette står i kontrast til kanoniske datamodeller, der modellendringer typisk bryter bakoverkompatibilitet, slik vi diskuterte under alternativ C i konseptvalget (seksjon 3).

Praktisk betyr dette at:

- **Pilotene driver modelleringen.** En ny pilot starter med å identifisere hvilke begreper som mangler i ontologien, og legger dem til. Ingen pilot venter på en "ferdig ontologi". Det er Gioias prinsipp om at ontologier modelleres bare når en konkret bruk krever det, anvendt på offentlig sektor.
- **Hver pilot bidrar til neste.** Begrepene som modelleres for skolebytte-piloten er tilgjengelige for senere piloter som involverer overgang mellom utdanningsnivåer, overgang til arbeidsliv, eller helt andre tjenester som drar nytte av samme begrepsapparat. Investeringene akkumulerer.
- **Eksisterende fellesløsninger utvides gradvis.** Felles datakatalog på data.norge.no får utvidelser for nye begrep- og modellkataloger. Sikts utdanningsregister får semantiske annotasjoner som kobler det til kunnskapsgrafen. Ingen av disse må endres på én gang.
- **Føderert modellering reduserer flaskehalser.** Når flere modelleringsteam jobber parallelt på ulike underdomener, og bare den sentrale domeneontologien krever bred konsensus, er det praktisk mulig å skalere modellarbeidet.

Det er denne kombinasjonen – semantisk grunnlag med monoton vekst, dataprodukter med eksisterende eierskap, og pilotdrevet modellering – som gjør den virtuelle kunnskapsgrafen til en realiserbar arkitektur for norsk offentlig sektor, ikke bare en akademisk modell.

Hvordan dette står i forhold til prosjektets eksisterende rammeverk – og særlig til "mellomlaget" og "felles informasjonsmodeller" som søknaden bruker – behandles i seksjon 5.

### 4.6 Datasentrisk tilgangsstyring

Tilgangsstyring følger samme logikk som resten av arkitekturen: det stabile er dataene, ikke tjenestene som eksponerer dem. Et applikasjonssentrisk landskap spør «har bruker X lov til å kalle tjeneste Y?». En datasentrisk arkitektur spør «har bruker X lov til å se disse dataene, uavhengig av hvilken tjeneste som eksponerer dem?». Distinksjonen er ikke akademisk i SAMT-BUs domene, der sensitive opplysninger om barn og unge flyter på tvers av barnehage, skole, kommune og stat: det er dataene og innholdet deres som er regulert, mens API-ene er utskiftbare projeksjoner. Tilgangsregler knyttet til tjenesten må bygges på nytt for hver nye tjeneste og passer dårlig med den virtuelle kunnskapsgrafens logikk.

Konsekvensen for konseptet er ett prinsipp: rettigheter knyttes til data, ikke til API-er. Det er meningsfullt å uttrykke en rettighet mot en abstrakt, persistent identifisert ressurs – et datasett – uavhengig av om det eksponeres via REST, et SPARQL-endepunkt eller filnedlasting. En regel kan da si at «saksbehandlere i barnevernstjenesten kan bruke opplysninger fra [datasett] til formål [Y] i periode [X]», og forbli gyldig når den tekniske distribusjonen skiftes ut. Dette knytter an til de tre betydningene av «eierskap» i 4.3.1: tilgangsstyringen håndhever den juridiske og forvaltningsmessige kontrollen over dataene, ikke et teknisk endepunkt. [ODRL](#odrl) er standarden som er bygget for å uttrykke slike rettigheter mot datasett.

Hvordan dette håndheves maskinelt – forholdet mellom policy-uttrykk og håndhevingsarkitektur, og hva dagens nasjonale infrastruktur støtter – er et målbilde- og arkitekturspørsmål, ikke et konseptvalg. Det behandles som åpent spørsmål i 8.2.

---

## 5. Sammenheng med konsept skissert i søknaden

Søknaden skisserer et konsept som er solid nok som utgangspunkt for prosjektet. Å videreutvikle og operasjonalisere konseptet er en sentral del av det prosjektet selv skal gjøre, og denne konseptbeskrivelsen er første skritt i den videreutviklingen. Den formelle konseptfasen er ivaretatt gjennom Bergen Kommunes utredning *Konseptforslag – felles kommunal dataforvaltning* (referert som vedlegg i søknaden), som etablerer behovet for en samordnet tilnærming til datadeling og dataforvaltning.

SAMT-BU bygger på denne grunntanken, men kan ikke ha kommunal sektor som avgrensing. Siktemålet om sammenhengende tjenester for brukerne tilsier at vi må tenke interoperabilitet i datadeling på tvers av sektorene. Dette utelukker ikke egne løsninger i kommunal sektor, men det utelukker løsninger som står i veien for tverrsektoriell samhandling.

I dette kapitlet viser vi hvordan begrepene i søknaden mapper mot dem vi har innført her, og hvor vi går utover det søknaden sier eksplisitt.

### 5.1 Det søknaden faktisk sier

I søknaden ble det sagt at "nye løsninger og tjenester utvikles mot et fast «mellomlag», frikoplet fra hvor eller hvordan data er lagret. Samtidig nås data der de er lagret, uten behov for lokale kopier." Konseptvalgutredningen som lå til grunn for søknaden, beskrives som "et konsept med felles informasjonsmodeller i kombinasjon med en felles tjenestekatalog, samt felles begreps- og metadatakataloger og tilhørende styringsmodeller for samarbeid". Som teknisk inspirasjon nevnes Novaris **FINT** (Felles INTegrasjoner).

Søknaden bruker også uttrykket **"datavirtualisering"** eksplisitt – både som arkivkrav (Digitaliseringsrundskrivet-tabellen) og som forutsetning for miljøgevinst (K7: data nås der de eies fremfor å kopieres).

Oppsummert handler dette om følgende elementer:

1. Et *"mellomlag"* som data nås gjennom
2. *Felles informasjonsmodeller*
3. *Felles tjenestekatalog*
4. *Felles begreps- og metadatakataloger*
5. *Datavirtualisering* som måten data nås på

FINT-referansen ligger som inspirasjon på siden av dette – vurdert som alternativ C i konseptvalget (seksjon 3).

### 5.2 Mapping av begrepene

Søknadens språk er pragmatisk og åpent. Konseptbeskrivelsen gir disse begrepene et presist arkitektonisk innhold:

**"Mellomlaget" → den virtuelle kunnskapsgrafen.**
Mellomlaget i søknaden var en velvalgt plassholder for noe det ikke fantes en etablert betegnelse for. Det vi nå konkretiserer det som, er en *virtuell kunnskapsgraf* der dataene fra autoritative kilder blir tilgjengelige gjennom semantiske koblinger til en felles ontologi. Egenskapen "data nås der de eies, uten lokale kopier" blir ivaretatt – og forsterket, fordi det nå er entydig hva slags struktur konsumenter ser når de når data gjennom mellomlaget.

**"Felles informasjonsmodeller" → den lagdelte ontologien.**
I søknadens språk er "felles informasjonsmodeller" en samlebetegnelse for delte representasjoner av begreper. I konseptet her er det realisert som en lagdelt ontologi (øvre, domene, underdomene, applikasjon) som lar både fellestrekk og sektorspesifikke utvidelser være eksplisitte. SEMICs Core Vocabularies gir EU-kompatible startpakker for domenelaget. Den lagdelte strukturen er den arkitektoniske egenskapen som lar modellene utvides monotont uten å bryte eksisterende bruk – noe en flat informasjonsmodell ikke gir.

**"Felles tjenestekatalog" → tjeneste-ontologi og dataproduktkontrakter.**
I søknaden er tjenestekatalogen tenkt som en oversikt over offentlige tjenester. I konseptet får tjenester sin semantiske representasjon i ontologien (på domene- og applikasjonslag, naturlig basert på CPSV-AP), mens de operative kontraktene knyttet til hver tjeneste og hvert dataprodukt får sin egen formalisering ([DPDS](#dpds), ODRL for bruksvilkår). Katalogen blir altså en sammensetning av semantiske beskrivelser og kontraktsbeskrivelser, ikke en flat liste.

**"Felles begreps- og metadatakataloger" → forvaltningsstruktur i og rundt kunnskapsgrafen.**
Begrepskatalogen er i praksis et menneskelig grensesnitt mot domeneontologien. Metadatakataloger som [DCAT-AP-NO](#dcat-ap-no) beskriver dataprodukter på et nivå konsumenter trenger for å finne fram. I konseptet er disse koblet til kunnskapsgrafen og ikke separate løsninger – noe som også løser problemet beskrevet i 4.3.2 om at en katalog uten en strukturell konsolideringsmekanisme har vist seg vanskelig å holde konsistent.

**"Datavirtualisering" → den virtuelle kunnskapsgrafen.**
Dette er en direkte oversettelse: søknadens datavirtualisering er nettopp den *virtuelle* varianten i Gioias tre-arkitekturer-typologi (4.1). Den semantiske rikheten kunnskapsgrafen tilfører, er en presisering av hva virtualisering må innebære når den skal være meningsfull på tvers av sektorer – ikke bare adgang til data uten kopiering, men adgang med felles mening.

### 5.3 Hvor vi går utover søknaden

Tre punkter der vi presiserer eller utvider språket vesentlig:

**Eierskap-distinksjonen** (4.3). Søknaden er taus om hva som menes når den sier "data nås der de eies" – den bruker uttrykket uten å presisere hva slags eierskap. Vår tre-deling – datasubjektets eierskap, forvaltningsansvar, og dataproduktansvar – plasserer prosjektets fellesløsninger i et tydeligere ansvarsbilde, og knytter EUDI Wallet og digitale lommebøker eksplisitt til konseptet på en måte søknaden ikke gjorde.

**Applikasjoner som konsumenter, inkludert KI-agenter** (4.3.4). Søknaden nevner ikke KI-agenter direkte. Vår presisering – at applikasjoner ikke skal være de facto eiere av data, og at KI-agenter er en applikasjonstype som ikke får unntak – legger til en arkitektonisk avgrensning som er kritisk for forsvarlig KI-bruk i offentlig sektor og som det blir vanskelig å rette opp i etterkant hvis vi venter.

**Internasjonal forankring** (6). Søknaden refererer til EU Data Spaces, SDGR, Skills Data Space og EUDI Wallet, men gjør ikke koblingen til MIMs Plus og SEMICs Core Vocabularies eksplisitt. Vår presisering av at konseptvalget faller sammen med EUs operative interoperabilitetsrammeverk, styrker både den politiske og den tekniske begrunnelsen.

Disse tre punktene videreutvikler søknadens språk på områder der arkitekturgruppa trenger mer presisjon for å kunne arbeide operativt med konseptet.

### 5.4 Kontinuiteten

Alle sentrale ambisjoner fra søknaden videreføres, men konkretisert og forsterket:

- *Data nås der de eies, uten lokale kopier* – ivaretatt i den virtuelle kunnskapsgraf-arkitekturen.
- *Redusert antall integrasjoner* – styrket: integrasjoner gjøres mot ontologien og dataproduktkontraktene, ikke mot hvert enkelt fagsystem.
- *Sluttbrukere skjermes fra et broket teknisk landskap* – styrket gjennom at brukerreiser komponeres semantisk, ikke gjennom å bygge nye integrasjoner per reise.
- *Reduserte utviklingskostnader gjennom mindre vedlikehold i sluttbrukersystemer* – ivaretatt: monoton utvidelse av ontologien gjør at endringer ett sted ikke automatisk forplanter seg som integrasjonsarbeid andre steder.
- *Bruk av nasjonale felleskomponenter* – styrket: konseptet bygger eksplisitt på data.norge.no (DCAT-AP-NO), Felles datakatalog, og pågående arbeid hos Sikt, Digdir og KS.

Søknaden var i denne forstand på rett vei. Konseptbeskrivelsen forteller hvor veien går.

---

## 6. Internasjonal forankring

Norge bygger ikke offentlig digital infrastruktur i isolasjon. Denne seksjonen viser hvordan konseptvalget vårt – datasentrisk tjenesteutvikling med dataproduktorientering og virtuell kunnskapsgraf – forholder seg til de internasjonale rammeverkene vi skal samhandle med, og hvilke konkrete standarder som er aktuelle for målbildet.

### 6.1 Hvorfor EU-perspektivet er førende

To av prosjektets mål gjør EU-tilkoblingen ikke-valgfri:

- *Cross-border-tjenester innen utdanning.* Studenter og elever krysser landegrenser. Vitnemål, kompetansebevis og opptak må kunne forstås på tvers. Skills Data Space, som søknaden eksplisitt peker på, er allerede et EU-initiativ.
- *Single Digital Gateway-forpliktelser.* SDG-forordningen gjelder også gjennom EØS-avtalen. Norge er forpliktet til å gjøre prosedyrene i Annex II tilgjengelige som fullt digitale, grensekryssende tjenester.

Det er teknisk og politisk lite hensiktsmessig å bygge en norsk særvariant og deretter mappe ut mot EU. Det er enklere, og strategisk klokere, å bygge på det semantiske grunnlaget EU-økosystemet allerede har etablert. Det betyr ikke at vi importerer alt – det betyr at vi tar utgangspunkt der i stedet for å oppfinne i parallell.

### 6.2 EU Data Spaces og DSSC Blueprint

**EU Data Spaces som rammeverkskonsept.** EUs datapolitikk siden 2020 er organisert rundt konseptet *data spaces* – fødererte, sektorspesifikke datadelingsinfrastrukturer der data forblir hos eier og deles gjennom standardiserte kontrakter og protokoller. EU finansierer i dag datarom på tvers av helse, utdanning og ferdigheter (Skills Data Space), mobilitet, landbruk, energi og industri. SAMT-BU er direkte berørt: Skills Data Space, som søknaden eksplisitt refererer til, er det europeiske datarommets svar på behovet for å dele utdannings- og kompetansedata på tvers av landegrenser – og det er arkitekturen SAMT-BU må kunne koble seg på.

**DSSC Blueprint som referansearkitektur.** Data Spaces Support Centre (DSSC), EU-finansiert, vedlikeholder [Blueprint for Data Spaces](https://blueprint.dssc.eu/) – den autoritative referansearkitekturen for europeiske datarom. Blueprint V3.0 organiserer tekniske kapabiliteter i tre søyler: *Data Interoperability* (felles datamodeller, semantikk og utvekslingsprotokoller), *Data Sovereignty and Trust* (identitet, tillitsrammeverk og policyhåndhevelse) og *Data Value Creation Enablers* (katalogoppdagelse, datatjenester og verdikjeder). Hvert av disse korresponderer direkte med begreper vi bruker i konseptet: informasjonsplan/kunnskapsplan, tilgangsstyring og dataproduktkontrakter, og kataloginfrastruktur.

**Sammenhengen med det datasentriske paradigmet.** Det som er slående ved Blueprint-arkitekturen er at dens tekniske fundament er det datasentriske paradigmet: RDF/OWL som kunnskapsrepresentasjon, ODRL for rettighetsuttrykk mot datasett, DCAT-AP for kataloger, og R2RML/RML for å mappe eksisterende datakilder til det semantiske laget. Dataspace Protocol (DSP) operasjonaliserer prinsippet om at data forblir hos eier mens kontrakter og rettigheter styrer aksess. SAMT-BU velger ikke en norsk særvariant av datasentrisk arkitektur – vi velger den samme teknologiske retningen som EU-dataromsøkosystemet bygger på. Det er dette som gjør internasjonal kompatibilitet til noe annet enn etterarbeid: vi er kompatible fordi vi bygger på felles grunnlag, ikke fordi vi etterpå mapper oss til det.

**DSSC Standards Landscape Update.** DSSC publiserer jevnlig en [Standards Landscape Update](https://dssc.eu/space/SE1/185794561/) (versjon 1.0, januar 2026) som kartlegger standardiseringsstatus og -gap i europeiske datarom. Dokumentet er en nyttig løpende referanse for arkitekturgruppa, men er en statusrapport snarere enn en normativ standard. De standardene som er mest relevante for det datasentriske paradigmet, er behandlet konkret i 6.6 nedenfor.

### 6.3 MIMs Plus som operativt rammeverk

**MIMs Plus** (Minimal Interoperability Mechanisms) er det operative interoperabilitetsrammeverket for offentlige tjenester i byer og kommuner, EU-finansiert og bygget på **ITU Y.4505**-standarden. Rammeverket spesifiserer for hvert mekanismeområde: objektiv, kapabilitet, krav, mekanisme, interoperabilitetsveiledning, og samsvarstesting.

MIMs Plus er strukturert i to lag:

**Foundational MIMs** dekker det grunnleggende dataforløpet:

- MIM0: Accessing Data – API-er til datakilder
- MIM1: Interlinking Data – persistente, unike identifikatorer som lar entiteter spores på tvers av systemer
- MIM2: Representing Data – felles datamodeller og ontologier
- MIM3: Exchanging Data – styringsmodeller, kontrakter og oppdagelse i dataøkosystem
- MIM6: Securing Data – sikkerhetskrav og autentisering

**Application-specific MIMs** adresserer spesifikke domener og bygger på de foundational:

- MIM4: Personal Data – personlig datahåndtering og samtykke
- MIM5: Interoperable AI – samvirkende AI-systemer
- MIM7: Geospatial Data – geografisk informasjon
- MIM8: Local Digital Twins – digitale tvillinger på lokalt nivå

Det viktigste for SAMT-BU er at MIMs Plus er **operativt og ikke bare regulatorisk**: det navngir konkrete standarder, beskriver hvordan kapabiliteter skal realiseres, og er praktisk anvendbart i pilotene. Det er den brikken som binder regulatoriske rammeverk (SDGR, Data Act, AI Act) til faktiske tekniske valg.

### 6.4 Mapping av kravene mot MIMs Plus

Kravene vi formulerte i konseptvalg-seksjonen er ikke ad hoc, men gjenfinnes i MIMs Plus. Følgende mapping viser sammenhengen:

| Vårt krav (seksjon 3) | Primær MIM-støtte | Hva MIM-en bidrar med |
|---|---|---|
| 1. Data nås der de eies | MIM0, MIM3 | API-tilgang til datakilder; dataøkosystem med føderert eierskap |
| 2. Semantisk interoperabilitet | MIM1, MIM2 | Persistente entitetsidentifikatorer; felles datamodeller med eksplisitt semantikk |
| 3. Gradvis utvidelse uten brudd | MIM2 | Standardiserte, utvidbare datamodeller |
| 4. Internasjonal samhandling | Hele MIMs-rammeverket | Konkrete standardvalg som er EU-omforente |
| 5. AI-etterrettelighet | MIM5 (kommende), MIM1, MIM2 | Semantisk grunnlag som lar AI-svar forankres i autoritative begreper |
| 6. Felles begreper for brukerreiser | MIM1, MIM2 | Delte vokabularer som lar tjenester sammenstilles på tvers |
| Tverrgående | MIM6 | Sikkerhet og autentisering for all dataaksess |

<br>

Mappingen viser at konseptvalget vårt ikke konkurrerer med MIMs Plus – det operasjonaliserer det. Når vi anbefaler "datasentrisk arkitektur med virtuell kunnskapsgraf og lagdelt ontologi", er det en konkretisering av hvordan MIMs 1 og 2 kan realiseres sammenhengende på norsk offentlig-sektor-skala.

### 6.5 Application-specific MIMs som er særlig relevante for SAMT-BU

Tre av de domenespesifikke MIM-ene er direkte relevante for prosjektets piloter:

**MIM4 – Personal Data.** Området barn og unge omhandler i stor grad sensitive personopplysninger og samtykker. MIM4 retter seg mot personlig datahåndtering, samtykke og kobling mot fremtidige EU-registrerte personlige dataformidlere (inkludert EUDI Wallet). MIM4 er foreløpig "under utvikling" i MIMs Plus-rammeverket, men retningen er sammenfallende med Sikts og Digdirs pågående arbeid med digitale lommebøker og samtykkeløsninger.

**MIM5 – Interoperable AI.** AI-agenter som skal hjelpe innbyggere, foresatte eller saksbehandlere i SAMT-BUs domene må kunne svare etterrettelig. MIM5 utgjør den semantiske grunnmuren for at AI-agenter kan referere til autoritative begreper, kilder og regelverk. Den semantiske rikheten vi argumenterer for, er det MIM5 forutsetter på en avansert måte.

**MIM7 – Geospatial Data.** Brukerreiser i utdanning er ofte geografisk forankret: skolekretser, kommunegrenser, regional inndeling, INSPIRE-pålegg. MIM7 anbefaler eksplisitt OGC-standarder (API Features, SensorThings API) og INSPIRE-konformitet, som er allerede etablert i norsk geodataforvaltning gjennom Geonorge.

MIM8 (Local Digital Twins) ligger noe mer på siden av kjerneområdet, men kan bli relevant for kommunale tjenesteflater, ungdomsklubber, og analoge brukerkontekster på lengre sikt.

### 6.6 Sentrale standarder for målbildet

MIMs Plus navngir konkrete standarder under MIM2. Følgende er særlig aktuelle for SAMT-BU, sortert etter hva de hjelper med:

**For offentlige tjenester og prosedyrer:**

- **CPSV-AP** (Core Public Service Vocabulary Application Profile) – grunnlaget for SDG-katalogen og tilsvarende tjenestebeskrivelser. RDF-basert. Relevant for prosjektets felles tjenestekatalog (Produkt 2).
- **CCCEV** (Core Criterion and Core Evidence Vocabulary) – brukes i OOTS-evidensutveksling. Relevant for vitnemål, kompetansebevis og dokumentasjon på tvers av forvaltning.

**For grunndata om aktører:**

- **Core Person Vocabulary**, **Core Business Vocabulary**, **Core Organization Vocabulary**, **Core Location Vocabulary** – minimumsvokabularer for personer, virksomheter, organisasjoner og lokasjoner. RDF-baserte. Egnet som forankringspunkter for norske kjernebegreper i den lagdelte ontologien.

**For datakataloger:**

- **DCAT-AP** og den norske profilen **DCAT-AP-NO** – allerede etablert i Felles datakatalog på data.norge.no. Vår datakatalog-utvidelse (Produkt 2) bygger på dette grunnlaget.

**For geografisk informasjon:**

- **INSPIRE Directive** – allerede gjeldende for norsk geodata gjennom Geonorge.
- **OGC API Features**, **OGC SensorThings API**, **GeoJSON**, **CityJSON** – anbefalte tekniske standarder.
- **ISO/IEC 5087 City Data Model** – relevant for kommunal datamodellering på lengre sikt.

**For domenespesifikke utvidelser:**

- **SAREF / SAREF4Cities** – mer relevant for IoT og smarte byer enn for SAMT-BUs kjerneområde, men nyttig for tilkoblingen til andre kommunale data.
- **NGSI-LD** – generisk kontekstinformasjonsmodell, mest relevant der real-time-data inngår i tjenestekomposisjonen.

For utdanningsdomenet spesifikt anbefaler vi at arkitekturgruppa også vurderer **PROV-O** (W3C-anbefalt provenans-vokabular for å spore datas opprinnelse og bearbeiding) og **ODRL** (Open Digital Rights Language for å uttrykke bruksvilkår), som begge er nevnt av Gioia og brukt i moderne dataproduktarkitekturer.

**For datarom-tilkobling og semantisk grunnlag (DSSC Blueprint):**

- **RDF/RDFS/OWL** – det triniteten av W3C-standarder som er Blueprint-arkitekturens kunnskapsrepresentasjonslag. RDF beskriver grafen; RDFS og OWL definerer vokabular og ontologi-egenskaper. Disse er grunnlaget for hele det semantiske laget i konseptet – det er ikke tilfeldig at Blueprint eksplisitt løfter dem frem som fundament.
- **[SHACL](#shacl)** (Shapes Constraint Language) – brukes til å validere at RDF-grafer er konformante med ontologikrav: kardinalitet, datatyper, tillatte verdier. Et nødvendig styringsverktøy når ontologien forvaltes av et føderert team og ulike aktører leverer data mot den.
- **Dataspace Protocol (DSP)** – spesifiserer hvordan DCAT-kataloger, ODRL-policyer og dataoverføringsavtaler koordineres mellom konnektorer i et datarom. Det er DSP som operasjonaliserer «data forblir hos eier» i Blueprint-arkitekturen, og det er protokollen Skills Data Space bruker for grensekryssende datadeling.
- **[LDES](#ldes)** (Linked Data Event Streams) – W3C-spesifikasjon for å publisere og konsumere datasett som evolusjonerende strømmer etter Linked Data-prinsippene. Relevant der autoritative kilder oppdateres løpende (for eksempel hendelsesstrømmer fra Folkeregisteret eller skoleregister) og konsumenter trenger å holde sin lokale tilstand synkronisert uten full re-last.

### 6.7 Forholdet til norsk infrastruktur og pågående arbeid

Flere norske initiativer ligger allerede tett opp mot EU-rammeverket og bør sees i sammenheng:

- **Felles datakatalog (data.norge.no)** er DCAT-AP-NO-basert. Det er det naturlige stedet for SAMT-BUs utvidelser under Produkt 2.
- **Sikts arbeid med utdanningsregister og kompetansebevisregister** er allerede orientert mot CCCEV-kompatible bevismodeller, særlig gjennom Europass Digital Credentials Framework.
- **EUDI Wallet** (Digdir leder norsk implementasjon) er den naturlige bæreren for digitale vitnemål og kompetansebevis fra Sikts registre.
- **Skills Data Space** (EU-initiativ, eksplisitt nevnt i søknaden) er den europeiske dataromsplattformen der norske utdanningsdata kan eksponeres etter datasentrisk arkitektur og felles vokabularer.
- **KS Fiks-plattform** og **Novaris FINT** er nasjonale komponenter som over tid bør evaluere overgang mot semantisk-baserte modeller, særlig på områder der cross-sektor-deling er sentral.

Konseptbeskrivelsen mener ikke at alle disse skal endres. Den mener at *retningen* skal være konsistent: nye løsninger og utvidelser bør bygge på det semantiske grunnlaget, og eksisterende komponenter bør gradvis tilpasses der det er behov og kost-nytte.

### 6.8 "Minimum-pluss"-posisjonen

Det er én viktig nyanse å være eksplisitt på. MIMs Plus er bevisst formulert som *"minimal but sufficient"* interoperabilitet. Det er et baseline-rammeverk for at byer og kommuner skal komme i gang uten å investere i fullskala semantisk infrastruktur fra dag én.

Vårt konseptvalg går utover MIMs Plus baseline. Datasentrisk tjenesteutvikling med en virtuell kunnskapsgraf og lagdelt ontologi krever mer semantisk modenhet enn det MIMs Plus minimumskrav fordrer. McComb og Gioia presser i samme retning – mot rikere semantikk, eksplisitte ontologier på flere nivåer, og dataproduktorientert organisering.

Vi forsvarer denne "minimum-pluss"-posisjonen slik:

- *MIMs Plus baseline er vår nedre grense.* Alt vi gjør skal være kompatibelt med rammeverket, slik at norsk offentlig sektor uten videre kan samhandle med europeiske partnere.
- *Datasentrisk + kunnskapsgraf er vår retning utover baseline.* Vi sikter på det MIMs Plus selv peker mot som "future-proof" interoperabilitet, og det Gioias logiske kunnskapsvarehus-arkitektur beskriver som realistisk mål for moderne datasentriske organisasjoner.
- *Vi bygger gradvis.* Vi krever ikke at hele økosystemet skal være på "pluss"-nivå fra dag én. Vi krever at retningen er konsistent, slik at investeringer bygger oppover og ikke trenger å gjøres på nytt.

Den praktiske konsekvensen er: alle MVP-er og piloter skal som minimum tilfredsstille MIMs Plus baseline (foundational MIMs 0–3 og 6 der de er relevante), og de skal demonstrere hvordan baseline kan utvides med kunnskapsgraf-egenskaper for de domenene der det gir verdi.

### 6.9 Hva som ikke er avklart

Tre forhold ligger utenfor det denne konseptbeskrivelsen kan avgjøre, og som arkitekturgruppa må vurdere:

- **Forholdet mellom NGSI-LD og en mer generell RDF-tilnærming.** NGSI-LD er sterkt forankret i smarte byer (FIWARE-økosystemet) og har egne API-er. For SAMT-BUs domene er det ikke åpenbart at NGSI-LD er det rette valget overalt – det kan være riktigere å bruke ren RDF/SPARQL med JSON-LD-fronter for utdanningsdata, og NGSI-LD der real-time og IoT-data inngår. Dette er et målbildevalg.
- **Hvilken upper ontology** (BFO, GIST, eller en pragmatisk variant av disse) som skal anbefales for det norske offentlige domenet. Gioia foreslår standardene; det er et reelt valg for arkitekturgruppa.
- **Implementeringsstack for den virtuelle kunnskapsgrafen.** Triplestores, virtual graph engines, R2RML/RML-mapping, eller alternative property-graph-løsninger er teknologivalg som hører til målbildet.

Disse er reelle åpne spørsmål, ikke retoriske. Konseptbeskrivelsen forplikter den semantiske retningen; den lar arkitekturgruppa bestemme hvilken stack som realiserer den.

---

## 7. Implikasjoner

Konseptet i denne beskrivelsen har konsekvenser som rekker utover den arkitektoniske kjernen. Denne seksjonen samler de viktigste, slik at arkitekturgruppa og pilotene har et klart bilde av hva konseptvalget betyr i praksis.

### 7.1 Datasentrisk er midlet, datadrevet er målet

Søknaden bruker betegnelsen "datadrevet tjenesteutvikling" som overordnet siktemål. Denne konseptbeskrivelsen er ikke en konkurrent til den frasen – den er en presisering av *hvordan* datadrevet tjenesteutvikling skal være mulig i offentlig-sektor-skala.

"Datadrevet" beskriver siktemålet: tjenester og beslutninger basert på data av god kvalitet. "Datasentrisk" beskriver den arkitektoniske disiplinen som gjør det realistisk: data, med felles eksplisitt mening, er det stabile, og applikasjoner er erstattbare projeksjoner. Uten den arkitektoniske disiplinen blir "datadrevet" en aspirasjon vi gjentar uten å oppnå.

Forholdet er middel til mål, ikke alternative paradigmer. Konseptbeskrivelsen forplikter datasentrisk arkitektur som det operative midlet for å nå datadrevet tjenesteyting.

### 7.2 Brukerorienterte dataprodukter

I konseptbeskrivelsen har vi tatt en eksplisitt posisjon om at applikasjoner – inkludert KI-agenter – er konsumenter, ikke eiere av data (4.3.4). Det er den ene siden av dataproduktorientering: at data leveres som produkter med tydelig forvaltningsansvar, kontrakter og semantisk annotasjon.

Det er en annen side som er like viktig for offentlig sektor: at dataproduktene må forstå og forholde seg til *sluttbrukerne* av tjenestene som hviler på dem. I privat sektor er det en åpen diskusjon om dataprodukteiere skal isolere seg fra sluttbrukere av hensyn til skalerbarhet. For offentlig sektor er den diskusjonen avklart: vi er der for innbyggerne, foresatte, elever, lærere og saksbehandlere. Dataproduktene må derfor være tjeneste- og brukerreiseorienterte, ikke bare effektive datatekniske leveranser.

Det betyr i praksis at:

- Dataprodukter må beskrives i et språk konsumenter på tvers av fagdomener forstår – ikke kun for andre data engineers
- Kontraktene må adressere reelle bruksbehov fra tjenester, ikke bare tekniske grensesnittspesifikasjoner
- Dataprodukteiere må ha relasjon til de som leverer tjenester til sluttbrukerne, ikke isolere seg av skalerbarhetshensyn

Dette er en norsk offentlig-sektor-presisering av dataproduktorienteringen, ikke en konkurrent til den.

### 7.3 KI og etterrettelighet

KI-agenter blir en stadig viktigere del av offentlig tjenesteyting. Konseptbeskrivelsen forutsetter at dette skjer på en måte som er forsvarlig: at agentene baserer sine svar og handlinger på autoritative data, og at deres svar kan etterprøves.

Datasentrisk arkitektur med en virtuell kunnskapsgraf er forutsetningen for at dette skal være mulig:

- KI-agenter henter fakta fra autoritative kilder gjennom det semantiske laget – ikke fra egne treningsdata eller lokale kunnskapslagre
- Svarene fra en agent kan spores tilbake til kilden gjennom semantiske referanser
- Begrepene agenten bruker, er forankret i en delt ontologi, ikke i agentens egne tolkninger

Dette samsvarer med tilnærminger som *GraphRAG* (Retrieval-Augmented Generation utvidet med kunnskapsgraf) og *neuro-symbolic AI* (kombinasjonen av nevrale modeller og symbolsk kunnskapsrepresentasjon). Det er ikke akademisk teori – det er den faglige retningen seriøse aktører innen forsvarlig KI i offentlig sektor beveger seg mot.

Konseptbeskrivelsen er sannsynligvis den eneste arkitektoniske retningen som lar offentlig sektor integrere KI-agenter uten å gjenta feilene fra første generasjon fagsystemer: nye låste systemer med egne datamodeller og ingen sammenheng med resten.

### 7.4 Gradvis verdihenting

En annen implikasjon er at konseptet ikke forutsetter en stor fullføring før verdi kan hentes. Den semantiske kunnskapsgrafens egenskap av monoton vekst (4.5) betyr at:

- Hver pilot kan levere verdi i sin egen kontekst, samtidig som den utvider grunnlaget for neste pilot
- Eksisterende fagsystemer kan kobles inn gradvis, etter prioritet og behov
- Det semantiske grunnlaget bygges opp domene for domene, ikke som ett stort modellarbeid på forhånd

Dette har konsekvenser for hvordan prosjektets piloter og MVP-er bør utformes: hver pilot bør ikke bare løse sitt umiddelbare brukerproblem, men også bidra konkret til det semantiske grunnlaget – nye begreper, nye relasjoner, nye dataproduktannotasjoner. Pilotene er ikke prøveballonger; de er byggesteiner i en akkumulerende infrastruktur.

### 7.5 Forutsetning om federert modelleringsstruktur

Konseptbeskrivelsen forutsetter at det etableres en **federert modelleringsstruktur** (4.2) der representanter fra de involverte sektorene har mandat til å forvalte de delte begrepene – særlig domeneontologien som er felles på tvers. Dette er ikke en organisasjonsmodell vi spesifiserer her; sammensetning, styring og beslutningsmekanismer hører til prosjektets organisatoriske arbeid og til SKATE/samstyringsstrukturen.

Det er likevel verdt å flagge at en slik struktur er nødvendig for at konseptet skal kunne realiseres operativt. Uten et organ med mandat til å forvalte felles begreper på tvers av sektorer, blir kunnskapsgrafen et fragmentert sett med isolerte underdomener – og vi gjenskaper koordineringsproblemet vi forsøker å løse. Dette er en av de viktigste organisatoriske konsekvensene av konseptvalget.

---

## 8. Avgrensning og åpne spørsmål

Denne seksjonen gjør eksplisitt hvor konseptbeskrivelsen slutter. En konseptbeskrivelse som ikke er tydelig på sine egne grenser, inviterer til å bli lest som mer – eller mindre – enn den er. Her trekker vi linjen mellom det konseptet forplikter og det som hører til arkitekturgruppas videre arbeid, målbildearkitekturen og pilotene. Vi samler de åpne spørsmålene som er reelle, ikke retoriske, og vi avslutter med den sterkeste innvendingen mot konseptvalget – fordi en konseptbeskrivelse som ikke tåler sin egen motstand, ikke er ferdig tenkt.

### 8.1 Konsept, ikke løsning – hvor grensen går

Konseptbeskrivelsen står på *konseptnivå*. Den forplikter til en paradigmatisk retning – datasentrisk tjenesteutvikling – og til et arkitektonisk mønster – en virtuell, lagdelt kunnskapsgraf med føderert ontologi og dataproduktorientering. Den forplikter **ikke** til konkrete teknologivalg, produkter, leverandører, lagringsløsninger, modelleringsverktøy eller infrastrukturoppsett.

Dette skillet er verdt å være eksplisitt på, fordi konseptet kan møtes med innvendingen om at vi allerede er på løsningsnivå når vi sier «virtuell kunnskapsgraf». Det er vi ikke. «Virtuell kunnskapsgraf» navngir et *mønster* – data forblir hos sine kilder, semantikken bor i en delt ontologi, og konsumenter når data gjennom det semantiske laget – ikke en implementasjon. Spørsmålet om RDF eller property graph, SPARQL eller Cypher, triplestore eller virtuell grafmotor, R2RML eller RML, er nettopp de valgene konseptet *ikke* tar. De hører hjemme i målbildet.

Vi har dermed to verktøy mot innvendingen om at vi forveksler konsept og løsning: vi *har* gjort et begrunnet konseptvalg (seksjon 3), og vi *holder oss* på konseptnivå og er eksplisitte om hvor grensen går (denne seksjonen). Det er en bevisst arbeidsdeling, ikke en utelatelse.

### 8.2 Hva som er overlatt til målbildet og arkitekturgruppa

Følgende er reelle åpne spørsmål som konseptbeskrivelsen med overlegg lar stå:

- **Implementeringsstack.** Triplestores, virtuelle grafmotorer, mapping-motorer (R2RML/RML) eller property-graph-baserte løsninger er teknologivalg for målbildet. Utdypet i 6.9.
- **Valg av øvre ontologi.** BFO, GIST eller en pragmatisk variant – standardene finnes, men valget for det norske offentlige domenet er arkitekturgruppas (6.9).
- **NGSI-LD kontra en mer generell RDF-tilnærming.** Trolig RDF/SPARQL med JSON-LD-fronter for utdanningsdata, og NGSI-LD der sanntids- og IoT-data inngår – men dette er et målbildevalg (6.9).
- **Identifikatorstrategi.** Hvilke persistente, unike identifikatorer som skal binde entiteter sammen på tvers (MIM1), og hvordan de forholder seg til eksisterende nasjonale identifikatorer, er ikke avklart her.
- **Forvaltning av mapping-laget.** Hvordan mappingene mellom datakilder og ontologi (R2RML/RML) skal versjoneres, testes og eies operativt, er en målbilde- og driftssak.
- **Materialiseringsgrad over tid.** Konseptet starter virtuelt. Når og om enkelte deler bør materialiseres – referert data kan materialiseres senere, men ikke omvendt (4.1) – er et veikartspørsmål, ikke et konseptvalg.
- **Håndheving av tilgangsstyring.** Rettigheter uttrykt mot datasett ([ODRL](#odrl)) må kunne håndheves maskinelt mot konkrete forespørsler, typisk ved å mappes til et håndhevingsrammeverk ([XACML](#xacml) med PEP/PDP). Valg av profil og arkitektur er en målbildesak.
- **Nasjonal tilgangsinfrastruktur.** [Altinn Autorisasjon](#altinn-autorisasjon)s ressursregister er i dag orientert mot tjenester og API-er, ikke mot datasett: det finnes ingen ressurstype for datasett, og ID-formatet tillater ikke IRIer. Arkitekturen er ressursbasert og utvidbar, så dette er ikke et prinsipielt hinder – men det er et nasjonalt infrastruktur-gap som må adresseres for at datasentrisk tilgangsstyring skal kunne realiseres i praksis.

Til dette hører også **nåsituasjon og posisjonering mot etablerte forløpere**. En grundig kartlegging av eksisterende fagsystemer, dataforvaltning og samhandlingsmønstre i de berørte sektorene – og en presis vurdering av hvordan SAMT-BU forholder seg til arbeider som FINT, KUDAF og FIKS-plattformen – er en del av arkitekturgruppas eget arbeid, ikke denne konseptbeskrivelsens. Det vi har sagt om forløperne, er holdt til det nødvendige: FINT er vurdert som alternativ C i konseptvalget (seksjon 3), og koblingen til pågående nasjonalt arbeid er skissert i seksjon 6. Den fulle posisjoneringen krever en nåsituasjonsbeskrivelse som hører hjemme i arkitekturarbeidet.

Ett tilgangsproblem er verken løst av konseptet eller av de etablerte europeiske rammeverkene vi forankrer oss i (6.2), og bør flagges eksplisitt. Når et API kan returnere ulike data avhengig av kontekst – et SPARQL-endepunkt eller et spørringsbasert API over kunnskapsgrafen – er tilgangskontroll ikke lenger et spørsmål om å tillate eller avslå et kall, men om å filtrere svaret slik at konsumenten kun ser det hun har rett til. Gapet er dokumentert: [IDSAs Dataspace Protocol](#idsa-dataspace-protocol) og [DSSC Blueprint](#dssc-blueprint) definerer tilgang på datasett-nivå, men overlater håndheving til konnektoren; [SIMPLs](#simpl) Policy Filter Service filtrerer hvilke ressurser som returneres i et katalogsøk etter brukerens rettigheter, men adresserer ikke filtrering av innholdet i det enkelte datasett; og [Catena-X' Knowledge Agents (CX-0084)](#catena-x-knowledge-agents-cx-0084) åpner for rad- og attributtnivå-tilgang som en mulighet, ikke en spesifisert mekanisme. For SAMT-BU er dette ikke et kanttilfelle: domenet kombinerer opplysninger med svært ulik sensitivitet – helse, skoleresultater, sosiale forhold – som kan berøres av samme spørring. Inntil mønstre for slik filtrering er standardisert, må dataproduktet selv (eller bindingslaget i en kunnskapsgraf) bære logikken; den tryggeste tilnærmingen i dag er separate, forhåndsannoterte distribusjoner med egne policyer for ulik tilgangsgrad framfor dynamisk filtrering av ett endepunkt. Behovet bør meldes inn i de europeiske standardiserings- og fellesskapskanalene (DSSC, IDSA), der Digdir kan løfte det som et krav fra offentlig sektor.

### 8.3 Organisatoriske og styringsmessige åpne spørsmål

Konseptet forutsetter en føderert modelleringsstruktur (4.2, 7.5), men spesifiserer den ikke. De åpne spørsmålene her er trolig de som avgjør om konseptet lykkes i praksis:

- Hvem eier domeneontologien – det laget som per definisjon er felles på tvers av sektorer?
- Hvilket organ har mandat til å beslutte når et kjernebegrep skal spesialiseres, og til å løse konflikter når to sektorer modellerer samme begrep ulikt?
- Hvordan forholder modelleringsstrukturen seg til eksisterende samstyring (SKATE) og til partnernes egne styringslinjer?

Dette er forvaltnings- og styringsspørsmål forkledd som tekniske. Erfaringen fra tilsvarende arbeid er at den største bremsen sjelden er teknologien, men koordineringen: hvem som har myndighet til å forplikte hvem. Konseptbeskrivelsen flagger behovet; den løser det ikke.

### 8.4 Juridiske og personvernmessige avklaringer

SAMT-BUs domene – barn og unge – innebærer omfattende behandling av sensitive personopplysninger. Konseptet beskriver en arkitektur for å dele data med felles mening; det avgjør ikke *når* slik deling er lovlig. Følgende avklaringer ligger utenfor konseptbeskrivelsen, men konseptets gjennomførbarhet avhenger av dem, og de bør følges tett av prosjektets juss-arbeidsstrøm og arkitekturgruppa:

- **Hjemmel kontra samtykke** for deling på tvers av sektorer, og forholdet til dataminimering. Skillet mellom de tre formene for «eierskap» (4.3.1) er et arkitektonisk bidrag til denne diskusjonen, ikke en juridisk konklusjon.
- **EUs KI-forordning (AI Act).** Forpliktelsene for høyrisiko-KI etter Annex III ble gjennom Digital Omnibus-enigheten i mai 2026 utsatt fra august 2026 til desember 2027 – omtrent sammenfallende med prosjektets slutt. Offentlige virksomheter som tar slike systemer i bruk, får like fullt registrerings- og konsekvensvurderingsplikter. KI-agentene konseptet beskriver (4.3.4, 7.3) må utformes med dette for øye.
- **Digitale lommebøker.** EUDI Wallet, som er den operative bæreren av datasubjektets kontroll i konseptet (4.3.1), har for EØS-land inkludert Norge en frist mot slutten av 2027, og var tidlig i 2026 ennå ikke satt i drift eller sertifisert noe sted. Konseptet forutsetter lommebøker som modningsavhengig infrastruktur, ikke som noe ferdig som finnes i dag.

### 8.5 Beslektede konseptbeskrivelser som bør følge

Denne konseptbeskrivelsen er den første i en kjede. Den forplikter retningen; flere begreper trenger sin egen presisering før målbildet kan bygges helt ut. I den rekkefølgen vi ser det:

- **Kunnskapsgraf** – realiseringen som eget konsept, der de tekniske valgene 8.2 lar stå, kan diskuteres på sine egne premisser.
- **Felles begrepsapparat / kjernebegreper** – det menneskelige grensesnittet mot domeneontologien.
- **Datavirtualisering** – teknikken for å eksponere grafen mot applikasjonene uten å flytte data.
- **Dataproduktorientering** – den organisatoriske strukturen med kontrakter, eierskap og federert governance.
- **Brukerreiser og tjenestekomposisjon** – hvordan sammenhengende tjenester settes sammen på toppen av den semantiske infrastrukturen.

Eventuelt også en egen presisering av **semantisk samhandlingsevne**, som kan låne mye fra Digdirs etablerte definisjon. Hver av disse kan skrives når et konkret behov krever det – samme prinsipp som styrer modelleringen i konseptet selv.

### 8.6 Den sterkeste innvendingen mot konseptet

En konseptbeskrivelse blir mer troverdig, ikke mindre, av å ta sin egen motstand på alvor. Den sterkeste innvendingen mot konseptvalget er denne:

Semantiske web-teknologier er over tjue år gamle, og bred adopsjon har uteblitt utenfor avgrensede lommer. Tilnærmingen kritiseres jevnlig for å være for akademisk, og den brede gjennomslagskraften har kommet via *lette* varianter – Schema.org, Linked Open Data, JSON-LD som et tynt semantisk lag på REST – ikke via formelle, lagdelte ontologier. Toppontologier som BFO og DOLCE har vært tilgjengelige hele veien uten å bli grunnmur i offentlig sektor noe sted. Pragmatiske alternativer – API-først med lette delte vokabularer, eller dataprodukter med kontraktsbaserte grensesnitt og minimalt semantisk lim – leverer ofte mesteparten av samhandlingsverdien til en brøkdel av kostnaden. Risikoen for å overingeniørere er reell: man kan ende med å bygge katedral mens andre bygger fungerende landsbyer.

Innvendingen fortjener et ærlig svar, og svaret er todelt.

For det første rammer den i hovedsak *ambisjonsnivå og tempo*, ikke retning. Ingen av de lette alternativene har faktisk demonstrert det SAMT-BU sikter mot: sammenhengende tjenester på tvers av sektor *og* landegrense, med maskinforståelig regelverk og automatisert resonnement over data. De skalerer godt for åpne data og enkle integrasjoner, men knirker når man må *resonnere* over dataene. Holder man fast ved ambisjonen om sammenhengende tjenester med brukeren i sentrum, har vi ikke sett et reelt alternativ til et semantisk lag i bunn.

For det andre følger det at konseptvalget ikke bør selges som teknisk uunngåelig. Det er det best dokumenterte valget *gitt ambisjonen* – ikke en logisk nødvendighet. Senkes ambisjonen, åpner alternative veier seg. Det er en ærligere og mer holdbar posisjon enn å hevde at det ikke finnes andre veier, og det er grunnen til at konseptbeskrivelsen gjennomgående har valgt formuleringer som «den mest robuste tilnærmingen vi kjenner» framfor «den eneste farbare vei».

Den praktiske konsekvensen av å ta innvendingen på alvor er den gradvise tilnærmingen konseptet allerede forplikter (4.5): vi bygger semantisk modenhet der ambisjonen krever det og verdien er størst, ikke overalt på én gang. Det er nettopp slik man unngår katedralen uten å gi opp sammenhengen.

---

## 9. Kildehenvisninger

Dette dokumentet bygger på et lite knippe kilder. Litteraturen forklarer paradigmet og den arkitektoniske strukturen konseptet hviler på; standardene og rammeverkene er de operative referansene konseptet forankres i. Henvisninger i den løpende teksten peker hit.

### Litteratur

#### McComb (2018)

Dave McComb: *Software Wasteland: How the Application-Centric Mindset is Hobbling our Enterprises.* Technics Publications, 2018. Argumentet for at det applikasjonssentriske tankesettet i seg selv er en hovedkilde til kostnad og kompleksitet i virksomheters informasjonssystemer.

#### McComb (2019)

Dave McComb: *The Data-Centric Revolution: Restoring Sanity to Enterprise Information Systems.* Technics Publications, 2019. Den sentrale framstillingen av det datasentriske paradigmet – «single but federated», forholdet til relasjonsmodellen, og kunnskapsgrafen som arkitektonisk grunnmur.

#### Gioia (2024)

Andrea Gioia: *Managing Data as a Product: A practical guide to enterprise data management.* Packt Publishing, november 2024. ISBN 978-1-83546-853-1. Kilde til dataproduktorienteringen, den lagdelte ontologien, de tre kunnskapsgraf-arkitekturene og det firedelte informasjonsarkitektur-planet (kapittel 11).

### Standarder og rammeverk

#### MIMs Plus

Minimal Interoperability Mechanisms Plus – Living-in.EU / OASC. EUs operative interoperabilitetsmekanismer, revidert årlig. <https://living-in.eu/>

#### SEMIC Core Vocabularies

Forenklede, gjenbrukbare kjernemodeller for blant annet person, virksomhet og lokasjon – Interoperable Europe (EU-kommisjonen). <https://interoperable-europe.ec.europa.eu/collection/semic-support-centre/core-vocabularies>

#### DCAT-AP-NO

Den norske applikasjonsprofilen av DCAT-AP for beskrivelse av datasett og datatjenester – Digdir. <https://data.norge.no/specification/dcat-ap-no>

#### DPDS

Data Product Descriptor Specification – Open Data Mesh Initiative. Standardisert beskrivelse av dataprodukter, inkludert semantiske koblinger mot ontologien. <https://dpds.opendatamesh.org/>

#### R2RML og RML

Standardspråk for å mappe henholdsvis relasjonsdata og semistrukturerte data til RDF – W3C. <https://www.w3.org/TR/r2rml/> · <https://rml.io/>

#### RDF og SPARQL

Grunnstandardene for å representere og spørre mot grafdata – W3C. <https://www.w3.org/TR/rdf11-concepts/> · <https://www.w3.org/TR/sparql11-query/>

#### GIST

Pragmatisk øvre ontologi utviklet for virksomheter – Semantic Arts. <https://www.semanticarts.com/gist/>

#### BFO

Basic Formal Ontology, en formell øvre ontologi – ISO/IEC 21838-2:2021. <https://basic-formal-ontology.org/>

#### Digdir

Rammeverk for digital samhandling og definisjonen av semantisk samhandlingsevne – Digitaliseringsdirektoratet. <https://www.digdir.no/>

#### ODRL

Open Digital Rights Language – W3C. Policy-språk for å uttrykke bruksvilkår og tilgangsrettigheter mot ressurser som datasett. <https://www.w3.org/TR/odrl-model/>

#### XACML

eXtensible Access Control Markup Language – OASIS. Rammeverk for å evaluere og håndheve tilgangspolicyer (PEP/PDP/PIP/PAP). <https://docs.oasis-open.org/xacml/3.0/xacml-3.0-core-spec-os-en.html>

#### IDSA Dataspace Protocol

Protokoll for datadeling mellom konnektorer i datarom – International Data Spaces Association. <https://kb.internationaldataspaces.org/>

#### DSSC Blueprint

Felles referansearkitektur for europeiske datarom – Data Spaces Support Centre. <https://blueprint.dssc.eu/>

#### Catena-X Knowledge Agents (CX-0084)

Standard for fødererte spørringer i datarom (compute-to-data over kunnskapsgraf) – Catena-X. <https://catenax-ev.github.io/docs/next/standards/CX-0084-FederatedQueriesInDataSpaces>

#### SIMPL

EUs mellomvareplattform for europeiske datarom – Europakommisjonen. Policy Filter Service beskrevet i Functional and Technical Architecture Specifications §9.2.5. <https://digital-strategy.ec.europa.eu/en/policies/simpl>

#### Altinn Autorisasjon

Nasjonal tilgangsstyrings- og ressursregister-infrastruktur – Digdir/Altinn. <https://docs.altinn.studio/authorization/>

#### SHACL

Shapes Constraint Language – W3C. Validerer at RDF-grafer er konformante med ontologikrav (kardinalitet, datatyper, tillatte verdier). <https://www.w3.org/TR/shacl/>

#### LDES

Linked Data Event Streams – W3C Community Group. Publiserer og konsumerer evolusjonerende datasett som strømmer etter Linked Data-prinsippene. <https://w3id.org/ldes/specification>

### Regelverk

*Dette underkapitlet er under utvikling. Bildet nedenfor er ikke komplett og vil endre seg i takt med at nytt regelverk trer i kraft og norsk gjennomføring avklares.*

Digdir vedlikeholder en løpende [oversikt over EU-regelverk om deling og bruk av data](https://www.digdir.no/datadeling/oversikt-over-eu-regelverk-om-deling-og-bruk-av-data/3251) som er relevant for norsk offentlig sektor. Per tidspunktet for denne konseptbeskrivelsen dekker oversikten ti forordninger og direktiver, gruppert i to lag: fire kjernelover som direkte regulerer personvern og datadeling – **GDPR** (personvernforordningen), **Åpne data-direktivet** (ODD), **Dataforvaltningsforordningen** (DGA) og **Dataforordningen** (Data Act) – og seks tilgrensende regelverk: KI-forordningen, eIDAS, Single Digital Gateway (SDG), Digital Markets Act (DMA), Digital Services Act (DSA) og Interoperable Europe Act. Merk at Digdir-lenker historisk har blitt ugyldige ved nettstedsoppdateringer – søk på tittelen hvis lenken er brutt.

Utover EU-regelverket er sektorspesifikke norske lover direkte relevante for SAMT-BUs domene: pasientjournalloven, helseregisterloven, opplæringsloven og barnevernsloven regulerer hvilke data som kan behandles og deles, og på hvilke vilkår. Disse, samt eventuelle nye hjemler som følger av prosjektets arbeid, vil bli lagt til etter hvert.

#### EUs KI-forordning (AI Act)

Forordning (EU) 2024/1689. Forpliktelsene for høyrisiko-KI etter Annex III ble gjennom Digital Omnibus-enigheten i mai 2026 utsatt til desember 2027. <https://eur-lex.europa.eu/eli/reg/2024/1689/oj> · <https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai>

#### EUDI Wallet

Den europeiske digitale lommeboken under eIDAS 2 (forordning (EU) 2024/1183). For EØS-land inkludert Norge gjelder en frist mot slutten av 2027. <https://digital-strategy.ec.europa.eu/en/policies/eudi-wallet-implementation>

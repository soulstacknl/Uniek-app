# Functionele eisen – Uniek-app

Status: **concept**, uitgewerkt in de klikbare demo (`demo/Uniek-app-demo.html`). Laatst bijgewerkt: 17 oktober 2026. Alle eisen staan nu op M (must); de prioriteiten voor de eerste versie moeten nog met Uniek worden vastgesteld.

Elke eis krijgt een nummer (F-01, F-02, ...) en een prioriteit volgens MoSCoW:
- **M**: must, nodig in de eerste versie
- **S**: should, graag in de eerste versie
- **C**: could, later
- **W**: won't, bewust niet

## 1. Doel van de app

De app brengt het contact tussen Opvang Uniek en ouders samen op één plek, en geeft medewerkers per locatie en onderdeel een helder overzicht. Concreet:
- **Ouders** zien hoe het met hun kind gaat, wat er gepland staat, en regelen administratie (vakantieplanning, medicatie, indicatie, akkoordverklaringen) zonder papier of losse e-mails.
- **Begeleiders** zien wie er vandaag is, wat ze over elk kind moeten weten (vooral medisch), en houden contact met ouders via een gedeeld teamgesprek en een dagelijkse groepschat.
- **Managers en beheerders** beheren locaties, medewerkers en gezinnen, en zien wat er openstaat aan planning en administratie.

_Aanname, te bevestigen met Uniek: wat gebeurt er nu zonder app (WhatsApp, e-mail, papier)?_

## 2. Rollen

| Rol | Wie | Logt in op |
| --- | --- | --- |
| Ouder / verzorger | Ouder of verzorger van een kind bij Uniek. Gekoppeld aan één of meer kinderen. | telefoon |
| Begeleider | Medewerker op de groep. Persoonlijk account, gekoppeld aan één of meer locaties. Kiest na het inloggen een locatie en daarna een onderdeel (F-16). | telefoon / browser |
| Manager | Medewerker van Uniek met beheerrechten. Gekoppeld aan locaties en kiest na het inloggen een locatie en een onderdeel, net als een begeleider. | telefoon / browser |
| Beheerder | Medewerker van Uniek met beheerrechten. **Locatie-onafhankelijk:** kiest geen locatie en ziet alle locaties, medewerkers en kinderen. | telefoon / browser |

Manager en beheerder hebben dezelfde beheerrechten. Het verschil: de manager werkt per locatie en onderdeel (kiest na het inloggen een locatie en een onderdeel, zoals een begeleider), de beheerder werkt locatie-onafhankelijk en begint op het Overzicht van alle locaties en onderdelen (F-09).

_Mag het kind of de jongere zelf inloggen?_

## 3. Rechten per rol

| Wat | Ouder | Begeleider | Manager | Beheerder |
| --- | --- | --- | --- | --- |
| Vandaag (aanwezigheid), chats en groepschat van de gekozen locatie en het gekozen onderdeel | Alleen eigen kind | Ja | Ja | Nee |
| Kinderen en kinddossier | Alleen eigen kind | Eigen locaties | Eigen locaties | Alle locaties |
| Goed om te weten bewerken | Nee | Ja | Ja | Alleen lezen |
| Kind toevoegen aan vandaag (keuze uit alle kinderen) | Nee | Ja | Ja | Nee |
| Overzicht van alle locaties, onderdelen, kinderen en acties | Nee | Nee | Nee | Ja |
| Administratie klaarzetten, goedkeuren en afkeuren | Invullen en akkoord geven | Ja | Ja | Ja |
| Locaties toevoegen en uitschrijven | Nee | Nee | Ja | Ja |
| Medewerkers toevoegen en uitschrijven, rol en locaties instellen | Nee | Nee | Ja | Ja |
| Ouders en kinderen inschrijven en uitschrijven | Nee | Nee | Ja | Ja |
| Koppelingen maken: medewerker ↔ locatie, ouder ↔ kind, kind ↔ vaste locatie | Nee | Nee | Ja | Ja |

## 4. Functies

| Nr | Functie | Rol | Prioriteit | Toelichting |
| --- | --- | --- | --- | --- |
| F-01 | **Groepschat van de dag** | Begeleider, ouder | M | Per locatie **en onderdeel** (F-16) wordt elke dag automatisch een groep gemaakt voor de ouders van de kinderen die die dag bij dat onderdeel op de locatie zijn (niet afgemeld). Zo heeft De Schuur op een doordeweekse dag een groep voor BSO en, als er kinderen zijn, aparte groepen voor Ambulant en Dag/Weekend opvang. De begeleider deelt er foto's en tekst in, in de stijl van een WhatsApp-groep. **Ouders kunnen niet reageren**; ze kunnen alleen lezen. **De groep is alleen die dag zichtbaar**: om 0:00 verdwijnen de berichten en foto's. Wordt een kind afgemeld, dan gaat de ouder uit de groep. Dit is een aparte functie naast de 1-op-1-chat tussen ouder en begeleiding. In de demo sinds 17-10-2026. |
| F-02 | **1-op-1-chat ouder en team** | Ouder, begeleider | M | Persoonlijke berichten over het eigen kind. **Teamgesprek per locatie en onderdeel:** de ouder chat met het team van het onderdeel op de locatie van het kind (bijvoorbeeld *Team BSO · De Schuur*), niet met één begeleider. Zit een kind bij twee onderdelen, dan heeft de ouder twee teamgesprekken. Elke begeleider die is ingelogd en die locatie en dat onderdeel heeft gekozen, ziet het hele gesprek, ook de berichten van collega's. Elk bericht staat op naam van de begeleider die het stuurde ('Ruben · begeleider'); collega's zie je in een andere kleur dan je eigen berichten. Hoe de dag ging, deelt de begeleider ook via deze chat; er zijn geen aparte dagverslagen. Staat in de demo. |
| F-03 | **Toestemming voor foto's in de groepschat** | Ouder, begeleider | M | Per kind wordt een aparte toestemming vastgelegd voor herkenbare foto's in de groepschat, los van andere toestemming voor beeldgebruik. De ouder geeft of trekt die zelf in de app in (Profiel). De begeleider ziet bij het delen van een foto en bij elk kind welke kinderen van vandaag geen toestemming hebben. |
| F-04 | **Persoonlijke inlog, locatie en onderdeel kiezen** | Begeleider, manager | M | Elke begeleider heeft een persoonlijk account (eigen e-mailadres en wachtwoord). Een begeleider kan aan meerdere locaties gekoppeld zijn. Elk gebouw is een eigen locatie, zoals op opvanguniek.nl: Ulft – Emailleplein 13, Ulft – Oersterk (Emailleplein 17), Didam – De Deel, Didam – Het Voorhuis, Didam – De Schuur, Bemmel – Het Dorpshuis en Bemmel – Het Glazenhuis. Na het inloggen kiest de begeleider eerst de locatie waar hij of zij die dag werkt, en daarna één van de drie onderdelen: **Ambulant**, **BSO** of **Dag/Weekend opvang** (F-16). Daarna zijn Vandaag, Kinderen, Berichten, verzoeken, de groepschat en Administratie beperkt tot die combinatie van locatie en onderdeel. Wisselen kan altijd, via de knop met locatie en onderdeel op Vandaag, via Profiel of (in de browser) onderaan het menu. Bij nieuwe berichten, verzoeken of te controleren administratie staat bij de keuze een teller. Is een begeleider aan maar één locatie gekoppeld, dan wordt de locatiekeuze overgeslagen; het onderdeel kies je altijd. In de demo sinds 17-10-2026. |
| F-05 | **Administratie** | Ouder, begeleider, manager, beheerder | M | Beide rollen krijgen een tab Administratie (eerder 'Acties' genoemd). Daarin staan losse acties. De begeleider of de organisatie zet een actie klaar voor één ouder, een paar ouders of alle ouders van een locatie en onderdeel, met uitleg en een uiterste datum. Soorten acties: **vakantieplanning doorgeven** (dagen kiezen of geen opvang nodig), **medicatie doorgeven of controleren** (medicijn, dosering, tijdstip, op de opvang geven ja of nee, bevestigen), **indicatie verlengen** (stand van zaken, datum van de aanvraag, nieuwe beschikking en einddatum), en **lezen en akkoord** (document of bijlage lezen en akkoord geven met een vinkje; bij vragen neemt de ouder contact op met de persoonlijk begeleider). **Documenten:** de begeleider kan bij elke actie documenten meesturen, bijvoorbeeld een zorgovereenkomst als pdf, die de ouder kan openen. De ouder kan bij het invullen zelf documenten of foto's meesturen; de begeleider ziet die bij het antwoord. De ouder krijgt een melding, ziet de actie onder Administratie bij Te doen en vult die in. **Scherm Administratie (begeleider, manager, beheerder):** eerst de kinderen van de locatie met hun ouder, en per kind de acties en documenten met de status **te controleren** (ouder heeft ingevuld), **klaargezet** (wacht op de ouder), **goedgekeurd** (klaar) of **afgekeurd** (teruggestuurd door Uniek, of de ouder gaat niet akkoord). Kinderen met iets te controleren staan bovenaan. Bovenaan staan de totalen per status; die werken ook als **filter**: tik een status aan of uit, of kies 'Alleen open' om goedgekeurde (afgeronde) acties te verbergen. Kinderen zonder acties met de gekozen status vallen dan weg. Begeleider en manager zien alleen de kinderen en acties van het gekozen onderdeel; elke actie hoort bij één onderdeel. De beheerder kiest eerst een locatie en ziet dan alle onderdelen, met het onderdeel bij elke actie; bij een nieuwe actie kiest de beheerder locatie én onderdeel. De ouder ziet bij elke actie bij welk onderdeel die hoort. De begeleider keurt een antwoord goed of keurt het af en stuurt het terug met een opmerking, en kan een herinnering sturen. Bij **lezen en akkoord** kan de ouder ook *niet akkoord* geven, met een verplichte toelichting; de begeleider neemt dan contact op en kan de actie opnieuw klaarzetten. In de demo sinds 17-10-2026. |
| F-06 | **Kind toevoegen aan vandaag** | Begeleider, manager | M | Op Vandaag kan de begeleider een kind toevoegen aan de lijst van vandaag op de gekozen locatie en het gekozen onderdeel. De keuzelijst bevat **alle kinderen van de hele organisatie** (alle locaties), met zoeken op naam van kind of ouder en een filter per locatie. Kinderen die vandaag al ergens op de lijst staan, zijn niet te kiezen. Bij toevoegen kiest de begeleider de soort opvang (passend bij het onderdeel), de reden (extra opvang, ruil van dag, noodopvang) en de tijd. Medische punten van het kind worden direct getoond. Het kind staat daarna als *extra* op de lijst, met de vaste locatie erbij als die anders is, en de ouder zit die dag in de groepschat van die locatie en dat onderdeel. In de demo sinds 17-10-2026. |
| F-07 | **Beheer** | Manager, beheerder | M | Managers en beheerders hebben een onderdeel Beheer. **Locaties:** toevoegen (naam, adres), uitschrijven en weer actief maken. Uitschrijven kan pas als er geen ingeschreven kinderen meer op de locatie staan. **Medewerkers:** toevoegen met naam, e-mail, rol (begeleider, manager of beheerder) en locaties; de medewerker krijgt een uitnodiging per e-mail. Rol en locaties zijn later te wijzigen; uitschrijven sluit het account af. Je eigen rol kun je niet wijzigen en jezelf niet uitschrijven. **Ouders en kinderen:** een kind inschrijven met vaste locatie en één of meer onderdelen, en een nieuwe ouder uitnodigen of een bestaande ouder koppelen (bij broers en zussen). Per kind de vaste locatie en de onderdelen wijzigen, ouders koppelen en ontkoppelen, het account van een ouder afsluiten of heropenen, en het kind uitschrijven. **Logboek:** elke wijziging wordt vastgelegd met naam en tijd. In de demo sinds 17-10-2026. |
| F-08 | **Contactgegevens van ouders** | Ouder, begeleider | M | Van elke ouder zijn een telefoonnummer en een e-mailadres bekend. De ouder ziet die in Profiel en kan ze zelf wijzigen. De begeleider ziet ze bij het kind (Kinderen › kind › Ouder en toestemming), per gekoppelde ouder, met bellen en mailen met één tik. Managers en beheerders vullen ze in bij het inschrijven of uitnodigen van een ouder. In de demo sinds 17-10-2026. |
| F-09 | **Overzicht voor de beheerder** | Beheerder | M | De beheerder ziet geen dagplanning (wie verwacht of aangekomen is) en geen status van vandaag bij kinderen. De tabs zijn Overzicht, Kinderen, Administratie, Beheer en Profiel. **Overzicht** (was eerder 'Planning'): per locatie en per onderdeel (Ambulant, BSO, Dag/Weekend opvang) welke kinderen eraan gekoppeld zijn, en hoeveel acties te controleren, klaargezet, afgekeurd en goedgekeurd zijn. Bovenaan staan de totalen; de beheerder filtert op locatie en op status van de acties (bijvoorbeeld *alleen open*, *alleen gesloten*, of alleen *afgekeurd*). Per onderdeel staan de acties met de gekozen status, met kind, titel en status; een tik opent de actie, een tik op een kind opent het kinddossier. **Kinderen:** een overzicht per locatie en onderdeel, met zoeken en een filter op locatie en onderdeel. Een kind dat bij twee onderdelen hoort, staat bij allebei. Een tik op een kind opent de gegevens van het kind: locatie, onderdelen, Goed om te weten, planning, administratie en de ouders met contactgegevens. **Administratie:** met 'Alle locaties' een totaal over de hele organisatie, en per locatie hoeveel acties te controleren, klaargezet, afgekeurd, open en gesloten zijn, met de voortgang en een uitsplitsing per soort actie. Open = te controleren, klaargezet of afgekeurd; gesloten = goedgekeurd. Kies je een locatie, dan zie je per kind de documenten (F-05). In de demo sinds 17-10-2026. |
| F-10 | **Goed om te weten bewerken** | Begeleider, manager | M | Bij elk kind staat 'Goed om te weten'. Begeleiders en managers kunnen dit bewerken met de knop Bewerken. Er zijn twee aparte delen: **Medisch** (allergieën, aandoeningen, noodmedicatie en waar die ligt) en **Overige punten**. Medische punten blijven altijd apart, in een rood blok bovenaan. Punten zijn toe te voegen, te wijzigen en te verwijderen. Onder het blok staat wie het het laatst heeft bijgewerkt en wanneer, en de wijziging komt in het logboek. De beheerder kan het alleen lezen. In de demo sinds 17-10-2026. |
| F-11 | **Vandaag: aanwezigheid op de locatie** | Begeleider, manager, ouder | M | De begeleider ziet per locatie en onderdeel de kinderen van vandaag met aantallen (aanwezig, verwacht, afgemeld), zet een kind op *aangekomen* en later op *opgehaald*, en ziet afmeldingen met de reden. De ouder ziet op Vandaag de status van het eigen kind en krijgt een melding bij aankomst en ophalen. De beheerder ziet deze dagplanning niet (F-09). In de demo. |
| F-12 | **Planning, afmelden en extra opvang aanvragen** | Ouder, begeleider, manager | M | De ouder ziet de komende opvang van het kind, meldt af met een reden en vraagt extra opvang aan (soort, datum, opmerking). De begeleider ziet de aanvragen op Vandaag en kiest *inplannen* of *niet mogelijk*; de ouder krijgt een melding. Een afmelding is direct zichtbaar voor de begeleider. In de demo. |
| F-13 | **Kinderen en kinddossier** | Begeleider, manager, beheerder | M | Lijst met de kinderen van de locatie die bij het gekozen onderdeel horen (beheerder: alle locaties, met filter en de onderdelen per kind). Per kind: leeftijd, onderdelen, status van vandaag, Goed om te weten (F-10), planning, administratie, de gekoppelde ouders met contactgegevens (F-08) en de toestemming voor foto's (F-03). In de demo. |
| F-14 | **Profiel** | Ouder, begeleider, manager, beheerder | M | De ouder ziet en wijzigt de eigen contactgegevens, ziet de gegevens van het kind, zet meldingen aan of uit en geeft of trekt de foto-toestemming in. Medewerkers zien hun rol en locaties, kunnen van locatie wisselen (niet de beheerder) en uitloggen. In de demo. |
| F-15 | **Nieuwsbrief van Uniek** | Ouder, manager, beheerder | M | Een algemene nieuwsbrief voor **alle ouders**, los van locaties en groepen. De ouder vindt die bij **Berichten**, als derde onderdeel onderaan: *Nieuws van Uniek*, onder de groep van vandaag en het teamgesprek. Daar staan alle edities, de nieuwste bovenaan; een ongelezen editie heeft het label *Nieuw* en telt mee in de teller op de tab Berichten. **Ouders kunnen niet reageren**; voor vragen verwijst de nieuwsbrief naar het teamgesprek. Managers en beheerders versturen een nieuwsbrief via Beheer › Nieuwsbrief (titel, samenvatting, tekst, bijlagen) en zien per editie hoeveel ouders hem hebben gelezen. Ouders krijgen een melding. In de demo sinds 17-10-2026. |
| F-16 | **Onderdelen per locatie** | Iedereen | M | Elke locatie heeft drie onderdelen: **Ambulant** (begeleiding thuis, op school of in de wijk), **BSO** (naschoolse begeleiding en vakantieopvang) en **Dag/Weekend opvang** (dagbesteding, zaterdagopvang, logeren). Een kind hoort bij één of meer onderdelen van zijn vaste locatie; elk opvangmoment in de planning hoort bij één onderdeel. Begeleiders en managers werken altijd binnen één combinatie van locatie en onderdeel (F-04): alle overzichten, berichten, groepschats, verzoeken en administratie zijn daarop gebaseerd. De ouder ziet bij de planning en de administratie bij welk onderdeel iets hoort, en heeft per onderdeel een teamgesprek (F-02). De beheerder werkt over alle locaties en onderdelen heen. In de demo sinds 17-10-2026. |


## 5. Schermen

| Rol | Tabs (menu) | Na het inloggen |
| --- | --- | --- |
| Ouder | Vandaag · Planning · Administratie · Berichten (groep van vandaag, teamgesprek, nieuws van Uniek) · Profiel | Vandaag |
| Begeleider | Vandaag · Kinderen · Administratie · Berichten · Profiel | Eerst locatie kiezen (als er meer dan één is), dan onderdeel kiezen |
| Manager | Vandaag · Kinderen · Administratie · Berichten · Profiel · Beheer (op de telefoon vervangt Beheer de tab Profiel) | Eerst locatie kiezen, dan onderdeel kiezen |
| Beheerder | Overzicht · Kinderen · Administratie · Beheer · Profiel | Overzicht van alle locaties en onderdelen |

Medewerkers kunnen de app ook in de webbrowser gebruiken; het menu staat dan links in een zijbalk (NF-01).

## 6. Buiten de eerste versie

- Aparte dagverslagen (met stemming en tags). Dat gaat via de 1-op-1-chat (besluit 17-10-2026).

## 7. Verschillen met de BPB-app

| BPB-app | Uniek-app |
| --- | --- |
| Rollen cliënt, professional en casehouder | Rollen ouder, begeleider, manager en beheerder |
| De cliënt gebruikt de app zelf | De ouder gebruikt de app voor het kind |
| Koppeling cliënt ↔ professional per discipline | Koppeling kind ↔ vaste locatie, ouder ↔ kind en medewerker ↔ locatie (7 locaties) |
| Berichten tussen cliënt en één professional | Teamgesprek per locatie en onderdeel: alle begeleiders van die combinatie zien het gesprek |
| Gedeelde bibliotheek en persoonlijke onderdelen | Groepschat van de dag met foto's (alleen lezen voor ouders) |
| Afspraken | Planning van opvang, afmelden en extra opvang aanvragen, aanwezigheid op Vandaag |
| — | Administratie met acties en documenten, status per kind |
| — | Beheer van locaties, medewerkers en gezinnen; overzicht voor de beheerder |

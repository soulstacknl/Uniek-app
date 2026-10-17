# Functionele eisen – Uniek-app

Status: **concept, nog in te vullen**. Laatst bijgewerkt: 17 oktober 2026.

Elke eis krijgt een nummer (F-01, F-02, ...) en een prioriteit volgens MoSCoW:
- **M**: must, nodig in de eerste versie
- **S**: should, graag in de eerste versie
- **C**: could, later
- **W**: won't, bewust niet

## 1. Doel van de app

_Wat moet de app oplossen voor ouders en begeleiders? Wat gebeurt er nu zonder app?_

## 2. Rollen

| Rol | Wie | Logt in op |
| --- | --- | --- |
| Ouder / verzorger | Ouder of verzorger van een kind bij Uniek. Gekoppeld aan één of meer kinderen. | telefoon |
| Begeleider | Medewerker op de groep. Persoonlijk account, gekoppeld aan één of meer locaties. | telefoon / browser |
| Manager | Medewerker van Uniek met beheerrechten. Gekoppeld aan locaties en kiest na het inloggen een locatie, net als een begeleider. | telefoon / browser |
| Beheerder | Medewerker van Uniek met beheerrechten. **Locatie-onafhankelijk:** kiest geen locatie en ziet alle locaties, medewerkers en kinderen. | telefoon / browser |

Manager en beheerder hebben dezelfde beheerrechten. Het verschil: de manager werkt per locatie (kiest na het inloggen een locatie, zoals een begeleider), de beheerder werkt locatie-onafhankelijk en begint op de Planning van alle locaties (F-09).

_Mag het kind of de jongere zelf inloggen?_

## 3. Rechten per rol

| Wat | Ouder | Begeleider | Manager | Beheerder |
| --- | --- | --- | --- | --- |
| Vandaag, kinderen, chats en groepschat van eigen locaties | Alleen eigen kind | Ja | Ja | Kinderen: alle locaties |
| Planning van de komende weken en administratie over alle locaties | Nee | Nee | Nee | Ja |
| Administratie klaarzetten en controleren | Invullen | Ja | Ja | Ja |
| Locaties toevoegen en uitschrijven | Nee | Nee | Ja | Ja |
| Medewerkers toevoegen en uitschrijven, rol en locaties instellen | Nee | Nee | Ja | Ja |
| Ouders en kinderen inschrijven en uitschrijven | Nee | Nee | Ja | Ja |
| Koppelingen maken: medewerker ↔ locatie, ouder ↔ kind, kind ↔ vaste locatie | Nee | Nee | Ja | Ja |

## 4. Functies

| Nr | Functie | Rol | Prioriteit | Toelichting |
| --- | --- | --- | --- | --- |
| F-01 | **Groepschat van de dag** | Begeleider, ouder | M | Per locatie wordt elke dag automatisch een groep gemaakt voor de ouders van de kinderen die die dag op de locatie zijn (niet afgemeld). De begeleider deelt er foto's en tekst in, in de stijl van een WhatsApp-groep. **Ouders kunnen niet reageren**; ze kunnen alleen lezen. **De groep is alleen die dag zichtbaar**: om 0:00 verdwijnen de berichten en foto's. Wordt een kind afgemeld, dan gaat de ouder uit de groep. Dit is een aparte functie naast de 1-op-1-chat tussen ouder en begeleiding. In de demo sinds 17-10-2026. |
| F-02 | 1-op-1-chat ouder en begeleiding | Ouder, begeleider | M | Persoonlijke berichten over het eigen kind. **Teamgesprek per locatie:** de ouder chat met het team van de locatie van het kind, niet met één begeleider. Elke begeleider die is ingelogd en die locatie heeft gekozen, ziet het hele gesprek, ook de berichten van collega's. Elk bericht staat op naam van de begeleider die het stuurde ('Ruben · begeleider'); collega's zie je in een andere kleur dan je eigen berichten. Hoe de dag ging, deelt de begeleider ook via deze chat; er zijn geen aparte dagverslagen. Staat in de demo. |
| F-03 | **Toestemming voor foto's in de groepschat** | Ouder, begeleider | M | Per kind wordt een aparte toestemming vastgelegd voor herkenbare foto's in de groepschat, los van andere toestemming voor beeldgebruik. De ouder geeft of trekt die zelf in de app in (Profiel). De begeleider ziet bij het delen van een foto en bij elk kind welke kinderen van vandaag geen toestemming hebben. |
| F-04 | **Locatie kiezen na inloggen** | Begeleider | M | Elke begeleider heeft een persoonlijk account (eigen e-mailadres en wachtwoord). Een begeleider kan aan meerdere locaties gekoppeld zijn. Elk gebouw is een eigen locatie, zoals op opvanguniek.nl: Ulft – Emailleplein 13, Ulft – Oersterk (Emailleplein 17), Didam – De Deel, Didam – Het Voorhuis, Didam – De Schuur, Bemmel – Het Dorpshuis en Bemmel – Het Glazenhuis. Na het inloggen kiest de begeleider de locatie waar hij of zij die dag werkt. Daarna zijn Vandaag, Kinderen, Berichten, verzoeken en de groepschat beperkt tot die locatie. Wisselen kan altijd, via de locatienaam op Vandaag of via Profiel. Bij nieuwe berichten of verzoeken staat bij de locatiekeuze een teller. Is een begeleider aan maar één locatie gekoppeld, dan wordt die keuze overgeslagen. In de demo sinds 17-10-2026. |
| F-05 | **Administratie** | Begeleider, ouder | M | Beide rollen krijgen een tab Administratie (eerder 'Acties' genoemd). Daarin staan losse acties. De begeleider of de organisatie zet een actie klaar voor één ouder, een paar ouders of alle ouders van een locatie, met uitleg en een uiterste datum. Soorten acties: **vakantieplanning doorgeven** (dagen kiezen of geen opvang nodig), **medicatie doorgeven of controleren** (medicijn, dosering, tijdstip, op de opvang geven ja of nee, bevestigen), **indicatie verlengen** (stand van zaken, datum van de aanvraag, nieuwe beschikking en einddatum), en **lezen en akkoord** (document of bijlage lezen en akkoord geven met een vinkje; bij vragen neemt de ouder contact op met de persoonlijk begeleider). **Documenten:** de begeleider kan bij elke actie documenten meesturen, bijvoorbeeld een zorgovereenkomst als pdf, die de ouder kan openen. De ouder kan bij het invullen zelf documenten of foto's meesturen; de begeleider ziet die bij het antwoord. De ouder krijgt een melding, ziet de actie onder Administratie bij Te doen en vult die in. **Scherm Administratie (begeleider, manager, beheerder):** eerst de kinderen van de locatie met hun ouder, en per kind de acties en documenten met de status **te controleren** (ouder heeft ingevuld), **klaargezet** (wacht op de ouder), **goedgekeurd** (klaar) of **afgekeurd** (teruggestuurd door Uniek, of de ouder gaat niet akkoord). Kinderen met iets te controleren staan bovenaan. Bovenaan staan de totalen per status. De beheerder kiest eerst een locatie. De begeleider keurt een antwoord goed of keurt het af en stuurt het terug met een opmerking, en kan een herinnering sturen. Bij **lezen en akkoord** kan de ouder ook *niet akkoord* geven, met een verplichte toelichting; de begeleider neemt dan contact op en kan de actie opnieuw klaarzetten. In de demo sinds 17-10-2026. |
| F-06 | **Kind toevoegen aan vandaag** | Begeleider | M | Op Vandaag kan de begeleider een kind toevoegen aan de lijst van vandaag op de gekozen locatie. De keuzelijst bevat **alle kinderen van de hele organisatie** (alle locaties), met zoeken op naam van kind of ouder en een filter per locatie. Kinderen die vandaag al ergens op de lijst staan, zijn niet te kiezen. Bij toevoegen kiest de begeleider de soort opvang, de reden (extra opvang, ruil van dag, noodopvang) en de tijd. Medische punten van het kind worden direct getoond. Het kind staat daarna als *extra* op de lijst, met de vaste locatie erbij als die anders is, en de ouder zit die dag in de groepschat van die locatie. In de demo sinds 17-10-2026. |
| F-07 | **Beheer** | Manager, beheerder | M | Managers en beheerders hebben een onderdeel Beheer. **Locaties:** toevoegen (naam, adres), uitschrijven en weer actief maken. Uitschrijven kan pas als er geen ingeschreven kinderen meer op de locatie staan. **Medewerkers:** toevoegen met naam, e-mail, rol (begeleider, manager of beheerder) en locaties; de medewerker krijgt een uitnodiging per e-mail. Rol en locaties zijn later te wijzigen; uitschrijven sluit het account af. Je eigen rol kun je niet wijzigen en jezelf niet uitschrijven. **Ouders en kinderen:** een kind inschrijven met vaste locatie, en een nieuwe ouder uitnodigen of een bestaande ouder koppelen (bij broers en zussen). Per kind de vaste locatie wijzigen, ouders koppelen en ontkoppelen, het account van een ouder afsluiten of heropenen, en het kind uitschrijven. **Logboek:** elke wijziging wordt vastgelegd met naam en tijd. In de demo sinds 17-10-2026. |
| F-08 | **Contactgegevens van ouders** | Ouder, begeleider | M | Van elke ouder zijn een telefoonnummer en een e-mailadres bekend. De ouder ziet die in Profiel en kan ze zelf wijzigen. De begeleider ziet ze bij het kind (Kinderen › kind › Ouder en toestemming), per gekoppelde ouder, met bellen en mailen met één tik. Managers en beheerders vullen ze in bij het inschrijven of uitnodigen van een ouder. In de demo sinds 17-10-2026. |
| F-09 | **Planning en totaaloverzicht voor de beheerder** | Beheerder | M | De beheerder ziet geen dagplanning (wie verwacht of aangekomen is). De tabs zijn Planning, Kinderen, Administratie, Beheer en Profiel. **Planning:** een totaaloverzicht van de komende 4 weken: totalen (locaties, ingeschreven kinderen, begeleiders en managers, geplande opvangmomenten) en een tabel met per locatie het aantal kinderen, begeleiders en managers, het aantal geplande opvangmomenten per week, de aanvragen en de afmeldingen. Kies je een locatie, dan zie je het adres, de opvangvormen, de medewerkers en de planning per dag met per kind de soort opvang en de status. **Administratie:** met 'Alle locaties' een totaal over de hele organisatie, en per locatie hoeveel acties te controleren, klaargezet, afgekeurd, open en gesloten zijn, met de voortgang en een uitsplitsing per soort actie. Open = te controleren, klaargezet of afgekeurd; gesloten = goedgekeurd. Kies je een locatie, dan zie je per kind de documenten (F-05). In de demo sinds 17-10-2026. |

_Mogelijke onderwerpen, om aan te vullen of te schrappen: berichten tussen ouder en begeleider, planning (logeren, dagopvang, vakantie- en zaterdagopvang), aan- en afmelden, foto's, doelen en voortgang, documenten, nieuws van Uniek, meldingen._

## 5. Schermen

_Welke hoofdschermen heeft elke rol?_

## 6. Buiten de eerste versie

- Aparte dagverslagen (met stemming en tags). Dat gaat via de 1-op-1-chat (besluit 17-10-2026).

## 7. Verschillen met de BPB-app

| BPB-app | Uniek-app |
| --- | --- |
| Cliënt, professional, casehouder | Ouder, begeleider, ... |
| Bibliotheek, persoonlijke onderdelen, berichten, afspraken | _..._ |

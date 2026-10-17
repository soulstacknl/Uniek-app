# Niet-functionele eisen – Uniek-app

Status: **concept**. Laatst bijgewerkt: 17 oktober 2026. De voorgestelde punten zijn ingevuld op basis van de BPB-app, de aard van de gegevens en de keuzes in de demo. Bevestig ze of pas ze aan.

| Nr | Onderwerp | Eis | Status |
| --- | --- | --- | --- |
| NF-01 | Platforms | Android en iPhone voor ouders en medewerkers. Medewerkers (begeleider, manager, beheerder) kunnen ook in de webbrowser werken, met dezelfde functies, het menu links in een zijbalk en meer ruimte om te typen (berichten, groepschat, administratie). | Besloten |
| NF-02 | Hosting | Data staat in de EU (Supabase, Frankfurt). | Voorstel |
| NF-03 | Privacy | Voldoet aan de AVG. Zorggegevens van kinderen zijn bijzondere persoonsgegevens. Alleen gegevens die nodig zijn worden bewaard. | Voorstel |
| NF-04 | Toegang | Iedereen ziet alleen wat bij de eigen rol hoort: de ouder het eigen kind, de begeleider en manager de kinderen van hun locaties, de beheerder alle locaties (zie de rechtentabel in `functioneel.md`). Uitzondering in de demo: bij 'Kind toevoegen aan vandaag' ziet een begeleider een keuzelijst met alle kinderen (naam, leeftijd, vaste locatie, ouder). Dit wordt in de database afgedwongen en getest. | Voorstel |
| NF-05 | Accounts | Een account ontstaat alleen op uitnodiging; zelf registreren kan niet. | Voorstel |
| NF-06 | Inloggen | Inloggen met e-mailadres en wachtwoord. Een tweede inlogstap is in te schakelen, eventueel verplicht voor begeleiders. | Te bespreken |
| NF-07 | Bewaartermijn | _Hoe lang blijven gegevens bewaard na het einde van de begeleiding?_ | Open |
| NF-08 | Toegankelijkheid | Teksten op B1-niveau. Voldoet aan WCAG 2.2 AA (contrast, lettergrootte, schermlezer). Rustig ontwerp met weinig prikkels. | Voorstel |
| NF-09 | Huisstijl | Herkenbaar Uniek (logo en hoofdkleuren), maar moderner en frisser dan de huidige website. | Besloten |
| NF-10 | Taal | Nederlands. _Andere talen nodig?_ | Open |
| NF-11 | Meldingen | Meldingen op de telefoon zonder gevoelige inhoud in de tekst (bijvoorbeeld 'Nieuw bericht over Liam', niet de inhoud). Meldingen voor: aankomst en ophalen, berichten, groepschat, nieuwe en teruggestuurde administratie, aanvragen en afmeldingen. | Voorstel |
| NF-12 | Kwaliteit en logboek | Past bij de ISO-certificering van Uniek. Wijzigingen in beheer (locaties, medewerkers, gezinnen, koppelingen) en in Goed om te weten worden vastgelegd met naam en tijd; bij administratie wordt vastgelegd wie wat wanneer heeft ingevuld, goedgekeurd of afgekeurd. | Voorstel |
| NF-13 | Aantallen | 7 locaties, ongeveer 150 cliënten en hun ouders, en ongeveer 65 medewerkers. | Voorstel |
| NF-14 | Beheer | Managers en beheerders beheren accounts, locaties en koppelingen in de app zelf (F-07). | Besloten |
| NF-15 | Koppelingen | _Koppeling met een bestaand cliëntsysteem of ECD? Zo ja, welk?_ | Open |

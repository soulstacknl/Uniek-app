# Besluiten en open vragen – Uniek-app

## Besluiten

| Datum | Besluit |
| --- | --- |
| 17-10-2026 | De app is voor ouders en begeleiders van Opvang Uniek. |
| 17-10-2026 | De BPB-app (`C:\GIT\BPB app`) is het voorbeeld voor techniek, opbouw, ontwerpdocumenten en demo. |
| 17-10-2026 | Huisstijl: gebaseerd op de website en het logo van Uniek, maar moderner en frisser. |
| 17-10-2026 | Requirements staan in `docs/eisen/`, met CLAUDE.md als korte wegwijzer. |
| 17-10-2026 | Groepschat van de dag: alleen de begeleiding plaatst berichten; ouders kunnen niet reageren. |
| 17-10-2026 | Groepschat van de dag is alleen die dag zichtbaar. |
| 17-10-2026 | Er komt een aparte toestemming voor foto's in de groepschat, per kind. |
| 17-10-2026 | Een begeleider kan op meerdere locaties werken en kiest na het inloggen een locatie. |
| 17-10-2026 | Ouder en begeleider krijgen een tab Administratie (eerst 'Acties' genoemd): Uniek zet een actie klaar, de ouder voert die uit, de begeleider ziet het resultaat en de status. |
| 17-10-2026 | Een begeleider kan op Vandaag een kind toevoegen; de keuzelijst bevat alle kinderen van de hele organisatie. |
| 17-10-2026 | De begeleider kan de app ook in de webbrowser gebruiken (zie NF-01). De demo laat beide weergaven zien. |
| 17-10-2026 | Bij administratieacties kunnen documenten worden meegestuurd, door Uniek en door de ouder. Akkoord geven gaat met een vinkje (geen getypte naam); de app legt vast wie en wanneer. |
| 17-10-2026 | Begeleiders hebben een persoonlijke inlog en kiezen daarna een locatie. Chats met ouders zijn teamgesprekken per locatie: alle begeleiders van die locatie zien alle berichten, met de naam van de afzender. |
| 17-10-2026 | Binnen Uniek zijn er drie rollen: begeleider, manager en beheerder. Managers en beheerders beheren locaties, medewerkers, ouders en kinderen, en de koppelingen daartussen (F-07). |
| 17-10-2026 | De beheerder is locatie-onafhankelijk en ziet geen dagplanning. Hij of zij ziet de planning van de komende weken per locatie, en de administratie (open en gesloten) per locatie en voor alle locaties samen (F-09). De manager werkt per locatie. |
| 17-10-2026 | Testgegevens in de demo: 6 tot 10 kinderen en 3 begeleiders per locatie, 1 of 2 managers per locatie, 5 beheerders. |
| 17-10-2026 | Elk gebouw is een eigen locatie, zoals op de website: 7 locaties (Ulft 2, Didam 3, Bemmel 2). |
| 17-10-2026 | Administratie is gegroepeerd per kind, niet per status. Statussen per actie: te controleren, klaargezet, goedgekeurd, afgekeurd. Bij lezen en akkoord kan een ouder ook niet akkoord geven. |
| 17-10-2026 | Geen aparte verslagen: hoe de dag ging, deelt de begeleider via de 1-op-1-chat. De ouder heeft de tabs Vandaag, Planning, Administratie, Berichten en Profiel. |

## Open vragen

- Welke functies heeft de eerste versie? (zie `functioneel.md`)
- Mag het kind of de jongere zelf inloggen?
- Is er een koppeling met een bestaand cliëntsysteem nodig?
- Welke bewaartermijn geldt voor de gegevens?
- Groepschat: wordt de foto-toestemming bij de intake op papier vastgelegd en door de begeleiding ingevoerd, of geeft de ouder die alleen in de app? (In de demo doet de ouder het in de app.)
- Groepschat: mogen ouders foto's uit de groep opslaan? Technisch is een screenshot nooit helemaal te voorkomen.
- Locatie kiezen: moet de app de laatst gekozen locatie onthouden, of telkens opnieuw vragen? (In de demo wordt het na elk inloggen gevraagd.)
- Locatie kiezen: wie koppelt een begeleider aan locaties: de planning of een beheerder?
- Locatie kiezen: krijgt een begeleider meldingen van een locatie waar hij of zij op dat moment niet werkt?
- Administratie: wie mag acties klaarzetten: elke begeleider, of ook (alleen) kantoor of planning? Ziet een begeleider ook acties die kantoor heeft klaargezet?
- Administratie: moeten ingevulde gegevens, zoals medicatie of de indicatie, automatisch naar het dossier of ECD van het kind?
- Administratie: zijn er nog andere soorten acties nodig, zoals een vragenlijst of het doorgeven van een adreswijziging?
- Administratie: medicatie is gevoelige informatie. Wie bij Uniek mag die antwoorden zien?
- Kind toevoegen: de keuzelijst laat begeleiders kinderen van alle locaties zien. Dat wijkt af van de privacyregel 'alleen eigen kinderen'. Voorstel: in de lijst alleen naam, leeftijd, vaste locatie en naam van de ouder; de rest pas na toevoegen. Akkoord?
- Kind toevoegen: moet de ouder (of de planning) het toevoegen eerst goedkeuren, of alleen een melding krijgen?
- Kind toevoegen: wordt een toegevoegd kind ook in de planning en de facturatie verwerkt?
- Documenten: welke bestandstypen en welke maximale grootte zijn toegestaan? Hoe lang bewaren we documenten die ouders meesturen?
- Akkoord met een vinkje: is dat juridisch voldoende voor bijvoorbeeld een zorgovereenkomst, of is een digitale handtekening nodig?
- Teamgesprek: moet een begeleider een gesprek kunnen 'oppakken' of markeren als afgehandeld, zodat collega's weten dat iemand al reageert?
- Teamgesprek: zijn berichten van ouders 'gelezen' als één begeleider ze heeft gelezen, of houdt elke begeleider een eigen leesstand bij?
- Beheer: mag een manager alleen de eigen locaties beheren (medewerkers en kinderen daarvan), en mag alleen de beheerder rollen toekennen en locaties toevoegen?
- Beheerder: mag de beheerder ook de chats met ouders en de groepschats van alle locaties lezen? (In de demo nu niet: de beheerder heeft geen tab Berichten.)
- Beheer: zien managers en beheerders de chats en medische gegevens van alle locaties, of alleen de locaties waaraan ze gekoppeld zijn?
- Ouder met meerdere kinderen: hoe kiest de ouder in de app tussen de kinderen? (In de demo kan een ouder al aan meerdere kinderen gekoppeld worden, maar de ouderapp toont nog alleen Liam.)
- Locaties: is 'Oersterk' hetzelfde als Emailleplein 17 in Ulft? De website zegt dat niet letterlijk. In de demo staat Oersterk op Emailleplein 17.
- Locaties: hebben De Deel en Het Voorhuis (Didam) elk een eigen team en groepschat, of horen ze voor de begeleiding bij elkaar?
- Planning beheerder: is 4 weken vooruit genoeg, of wil de beheerder een langere periode of een vrije keuze van periode? Is er een maximum aantal kinderen (capaciteit) per locatie dat we moeten tonen?
- Goed om te weten: mag de ouder dit ook zien, of zelf punten voorstellen? En moet medische informatie ook door de ouder bevestigd worden (bijvoorbeeld via de actie Medicatie)?

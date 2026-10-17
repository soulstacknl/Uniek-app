# Uniek-app

App voor ouders en medewerkers van Opvang Uniek. Ouders zien hoe het met hun kind gaat, wat er gepland staat en regelen administratie. Begeleiders zien wie er vandaag is en houden contact met ouders. Managers en beheerders beheren locaties, medewerkers en gezinnen.

De eisen staan in `docs/eisen/`, de klikbare demo in `demo/`. Werkafspraken voor Claude staan in `CLAUDE.md`.

## Stand van zaken

| Onderdeel | Status |
| --- | --- |
| Context van Opvang Uniek (locaties, adressen, opvangvormen) | Klaar: `docs/context-opvang-uniek.md` |
| Functionele eisen | Concept met 16 eisen (F-01 t/m F-16), rollen, rechten en schermen: `docs/eisen/functioneel.md` |
| Niet-functionele eisen | Concept (NF-01 t/m NF-15): `docs/eisen/niet-functioneel.md` |
| Besluiten en open vragen | Bijgehouden in `docs/eisen/besluiten.md` |
| Huisstijl | Logo, beeldmerk en kleuren in `assets/brand/` en in de demo. Lettertype in de demo: Plus Jakarta Sans (nog te bevestigen) |
| Klikbare demo | Klaar om te tonen: `demo/Uniek-app-demo.html` (zie hieronder) |
| Functioneel en technisch ontwerp (HTML, voor de klant) | Volgt, net als bij de BPB-app |
| App (Expo, React Native, Supabase) | Volgt |

## De klikbare demo

Eén los HTML-bestand, zonder backend: open `demo/Uniek-app-demo.html` in een browser. Links staat de telefoon van een ouder, rechts de begeleiderskant (als telefoon of als webbrowser). Wat je aan de ene kant doet, zie je meteen aan de andere kant.

**Locatie en onderdeel:** elke locatie heeft drie onderdelen: Ambulant, BSO en Dag/Weekend opvang. Een begeleider of manager kiest na het inloggen eerst de locatie en daarna het onderdeel. Vandaag, Kinderen, Berichten, de groepschat en Administratie gaan dan over die combinatie. Wisselen kan via de knop bovenaan Vandaag. **Opnieuw beginnen** zet alles terug.

**Demo-dag kiezen:** op het inlogscherm kies je een dag (vandaag en de 7 dagen daarna). Zo zie je hoe een zaterdag werkt (zaterdagopvang in De Schuur, logeren) of een doordeweekse dag (naschoolse begeleiding, dagbesteding in Oersterk). Op zondag is er alleen logeeropvang. De demo begint dan opnieuw op die dag; de gekozen dag staat bovenaan de pagina. Doordeweeks is er BSO en Ambulant op alle locaties; Dag/Weekend opvang verschilt per locatie.

### Inloggen in de demo

| Wie | Rol | Locaties |
| --- | --- | --- |
| Eva de Vries (moeder van Liam) | Ouder | Liam zit in Didam – De Schuur, bij BSO en Dag/Weekend opvang |
| Sanne Willemsen | Begeleider | De Schuur, De Deel, Ulft – Emailleplein 13 |
| Ruben Hendriksen | Begeleider | De Schuur, Het Voorhuis, Het Dorpshuis, Het Glazenhuis |
| Petra Kok | Manager | Didam (De Deel, Het Voorhuis, De Schuur) |
| Hanneke de Boer | Beheerder | Alle locaties (locatie-onafhankelijk) |

Via de keuzelijst op het inlogscherm kun je ook inloggen als een van de andere medewerkers.

### Wat zit erin

| Onderdeel | Eis |
| --- | --- |
| Vandaag: aanwezigheid, aangekomen en opgehaald, kind toevoegen aan vandaag | F-11, F-06 |
| Planning voor ouders: afmelden en extra opvang aanvragen; begeleider plant in | F-12 |
| Locatie en onderdeel kiezen (Ambulant, BSO, Dag/Weekend opvang) | F-04, F-16 |
| Teamgesprek per locatie en onderdeel tussen ouder en begeleiders | F-02 |
| Nieuwsbrief van Uniek voor alle ouders (bij Berichten) | F-15 |
| Groepschat van de dag met foto's, met toestemming per kind | F-01, F-03 |
| Administratie: vakantieplanning, medicatie, indicatie, lezen en akkoord; documenten; status per kind met filter | F-05 |
| Kinderen en kinddossier, met Goed om te weten (medisch apart, te bewerken) | F-13, F-10 |
| Contactgegevens van ouders | F-08 |
| Persoonlijke inlog; webbrowserweergave | F-04, NF-01 |
| Beheer: locaties, medewerkers, ouders en kinderen, koppelingen, logboek | F-07 |
| Beheerder: planning van de komende 4 weken en administratie over alle locaties | F-09 |

### Testgegevens

7 locaties met elk 3 onderdelen, ongeveer 50 kinderen (6 tot 10 per locatie, elk bij één of twee onderdelen), 3 begeleiders per locatie, 1 of 2 managers per locatie en 5 beheerders. Alle namen zijn verzonnen. De planning en de administratie worden met een vast patroon gemaakt, dus de demo ziet er elke keer hetzelfde uit.

## Indeling

| Map | Inhoud |
| --- | --- |
| `docs/eisen/` | Functionele en niet-functionele eisen, besluiten en open vragen |
| `docs/context-opvang-uniek.md` | Wat Uniek doet, locaties met adressen, huisstijl |
| `demo/` | Klikbare demo |
| `assets/brand/` | Logo en beeldmerk van Opvang Uniek |

Volgen bij de bouw, zoals bij de BPB-app: `app/`, `supabase/migrations/`, `supabase/demo/`, `tests/db/`, `tests/app/`.

## Begrippen en namen in code (voorstel)

De app en de ontwerpen zijn Nederlands, de code en de database Engels. Deze tabel wordt definitief bij de bouw.

| In de app | In code en database |
| --- | --- |
| Locatie | `locations` |
| Onderdeel (Ambulant, BSO, Dag/Weekend opvang) | `units` met `code`: `ambulatory`, `after_school`, `day_weekend` |
| Koppeling kind ↔ onderdeel | `child_units` |
| Medewerker (begeleider, manager, beheerder) | `staff` met `role`: `caregiver`, `manager`, `admin` |
| Koppeling medewerker ↔ locatie | `staff_locations` |
| Kind | `children` |
| Ouder | `parents` |
| Koppeling ouder ↔ kind | `child_parents` |
| Goed om te weten (medisch en overig) | `child_notes` met `is_medical` |
| Toestemming foto's in groepschat | `photo_consents` |
| Planning (opvangmoment, met onderdeel) | `bookings` met `unit` |
| Aanwezigheid vandaag | `attendance` |
| Teamgesprek met ouder (per kind en onderdeel) | `conversations` met `unit`, `messages` |
| Groepschat van de dag (per locatie en onderdeel) | `daily_group_posts` met `unit` |
| Administratie: actie en verzoek per kind | `tasks`, `task_requests` |
| Documenten bij een actie | `attachments` |
| Logboek | `audit_log` |

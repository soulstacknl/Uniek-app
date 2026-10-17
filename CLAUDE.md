# Uniek-app

App voor **ouders en begeleiders** van Opvang Uniek. Opvang Uniek begeleidt kinderen, jongeren en jongvolwassenen met onder meer ADHD, ASS, hechtingsproblematiek of trauma. Het doet dat vanuit 7 locaties in Ulft (Emailleplein 13, Oersterk), Didam (De Deel, Het Voorhuis, De Schuur) en Bemmel (Het Dorpshuis, Het Glazenhuis). Elk gebouw is in de app een eigen locatie.

## Waar staat wat

| Wat | Waar |
| --- | --- |
| Functionele eisen (wat de app doet, per rol) | `docs/eisen/functioneel.md` |
| Niet-functionele eisen (privacy, beveiliging, toegankelijkheid, huisstijl) | `docs/eisen/niet-functioneel.md` |
| Open vragen en genomen besluiten | `docs/eisen/besluiten.md` |
| Functioneel en technisch ontwerp (HTML, voor de klant) | `docs/` (volgt) |
| Klikbare demo (losse HTML, zonder backend) | `demo/` (volgt) |
| Logo en huisstijlbestanden | `assets/brand/` |

Lees de eisen voordat je iets bouwt of ontwerpt. Staat iets er niet in, vraag het dan. Verzin geen eisen; leg een aanname vast in `besluiten.md`.

## Voorbeeld: de BPB-app

Deze app volgt de opzet van de BPB-app in `C:\GIT\BPB app`: dezelfde techniek, mapindeling, manier van testen en soort ontwerpdocumenten en demo. Neem patronen daaruit over in plaats van iets nieuws te bedenken. Wijk alleen af waar de eisen van Uniek daarom vragen.

## Techniek

- Expo met React Native en TypeScript, en Expo Router voor de schermen.
- Supabase als backend, in regio **Central EU (Frankfurt)**. Toegang wordt per rij geregeld (RLS) en elke regel heeft tests.
- Mapindeling zoals bij BPB: `app/`, `supabase/migrations/`, `supabase/demo/`, `tests/db/`, `tests/app/`, `docs/`, `demo/`.

## Afspraken

- **Taal:** alle teksten in de app en de ontwerpen zijn Nederlands. Namen in code en database zijn Engels. Houd een vertaaltabel bij in de README, zoals bij BPB.
- **Toon:** warm, duidelijk en toegankelijk, op B1-niveau. Schrijf voor ouders, niet voor vakgenoten.
- **Huisstijl:** herkenbaar Uniek (logo en hoofdkleuren), maar moderner en frisser dan de huidige website. Logo: `assets/brand/logo-opvang-uniek.png`, beeldmerk (de twee figuren): `assets/brand/beeldmerk-uniek.png`. Kleuren uit het logo: blauw `#0A62AB` en magenta `#D92A82`. Aanvullend: donkerblauw `#0B2F5B` voor tekst, en lichte tinten `#E4EFFA` (blauw) en `#FCE6F1` (roze). Kleuren en lettertypes staan op één plek in `app/src/lib/theme.ts` en worden in de demo gelijk gehouden.
- **Rollen:** ouder, begeleider, manager en beheerder. De rechten per rol staan in `functioneel.md` (hoofdstuk 3).

## Privacy: altijd

Het gaat om zorggegevens van kinderen. Dat zijn bijzondere persoonsgegevens onder de AVG.

- Laat iemand alleen zien wat bij zijn of haar eigen kind of cliënten hoort. Toets dat in de database (RLS), niet alleen in de app.
- Gebruik nooit echte namen of gegevens in de demo, de tests of voorbeelden.
- Zet geen geheime sleutels in de code of in de app. Gebruik alleen de publieke Supabase-sleutel.
- Gebruik geen diensten buiten de EU zonder een besluit in `besluiten.md`.

## Werkwijze

- Werk de README bij met de stand van zaken na elke afgeronde bouwstap.
- Pas eerst de eisen aan als die veranderen, en daarna pas de code.

# Trainer-afbeeldingen maken

Alle PNG's: transparante achtergrond, **exact hetzelfde canvas** (bv. 800 x 1200 px, verhouding 2:3), personage vol in beeld, voeten onderaan, hoofd op dezelfde plek in elke afbeelding. Zo liggen de laagjes precies op elkaar.

## Bestanden (map `trainer/` naast index.html)

| Bestand | Wat |
|---|---|
| `base-idle.png`, `base-throw.png`, `base-happy.png`, `base-sad.png` | Lichaam + gezicht, kaal (alleen simpel ondergoed/basiskleding), 4 poses |
| `outfit-rood-{pose}.png` | Avonturier, 4 poses |
| `outfit-blauw-{pose}.png` | Sportief, 4 poses |
| `outfit-groen-{pose}.png` | Ontdekker, 4 poses |
| `outfit-geel-{pose}.png` | Regenjas, 4 poses |
| `hair-kort-back.png` / `hair-kort-front.png` | Kort haar |
| `hair-staart-back.png` / `hair-staart-front.png` | Paardenstaart |
| `hair-los-back.png` / `hair-los-front.png` | Los, lang haar |
| `hair-staartjes-back.png` / `hair-staartjes-front.png` | Twee staartjes |

`{pose}` = idle, throw, happy, sad. Totaal: 4 + 16 + 8 = 28 afbeeldingen.
Ontbreekt een bestand, dan toont de app gewoon een placeholder, je kunt dus stap voor stap vullen.

Haar teken je altijd in **één neutrale bruine kleur**: de app maakt er zwart, blond, rood, roze en blauw van.

## Tijdelijke placeholders

De PNG's in deze map zijn met code getekende chibi-anime-plaatjes (600x900), bedoeld als tijdelijke versie. Vervang ze één voor één door je eigen anime-afbeeldingen met **dezelfde bestandsnaam**.

## Hosten op GitHub (Pages)

- Zet de map `trainer/` in je repository naast `index.html` en commit/push alles.
- Bestandsnamen zijn hoofdlettergevoelig op GitHub: alles klein, precies zoals in de tabel.
- Houd elke afbeelding klein (liefst onder ~200 KB, bv. 600x900 of 800x1200 als PNG/WebP), want 28 stuks moeten op een telefoon snel laden.
- Na een update: even vernieuwen (op iPhone eventueel de site opnieuw openen) als je nog het oude plaatje ziet.

## Stijlprompt (plak dit bij elke afbeelding, houd het identiek)

> Anime-stijl illustratie, schone lijnen, zachte cel-shading, vrolijke kleuren, kindvriendelijk. Een jonge Pokémon-trainer van ongeveer 12 jaar, vriendelijk gezicht met grote ogen, volledig lichaam, staand, vooraanzicht in lichte driekwart, transparante achtergrond, geen tekst, geen logo's, geen bestaande personages. Hoofd en voeten op dezelfde plek in beeld als de referentie.

## Per pose (toevoegen aan de stijlprompt)

- **idle:** ontspannen, lichte glimlach, een hand losjes omhoog met een pokéballetje
- **throw:** gooit met één arm naar voren, gefocust, vastberaden blik
- **happy:** beide armen omhoog, grote lach, ogen dicht van blijdschap
- **sad:** schouders omlaag, kleine teleurgestelde blik, geen tranen

## Werkwijze (houdt het personage consistent)

1. Genereer eerst `base-idle.png` (kaal basispersonage) en keur het goed.
2. Gebruik die afbeelding als referentie voor de andere poses, met de opdracht: "zelfde personage, zelfde gezicht, zelfde proporties, andere pose".
3. Outfits: referentie = de bijbehorende basepose, opdracht: "teken alleen de kleding (zonder lichaam en zonder haar) op transparante achtergrond, exact op dezelfde plek".
4. Haar: referentie = `base-idle.png`, opdracht: "teken alleen het haar, bruin, op transparante achtergrond. Aparte afbeelding voor het deel dat achter het lichaam hoort (back) en het deel dat ervoor hoort (front: pony en lokken langs het gezicht)".
5. Verwijder achtergronden met een gratis tool (bv. remove.bg) en exporteer als PNG of WebP-met-transparantie (zet de extensie dan in de app op .webp).

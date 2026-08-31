# Prompt für Claude Design (Blank-Eingabe)

Alles ab hier 1:1 kopieren und in die leere Eingabe von Claude Design einfügen.

---

Du bist mein Lead Product Designer für den kompletten visuellen Neubau von **klair.ch** (Shopify). Es geht in diesem Auftrag **ausschliesslich um Gestaltung** — kein Code, keine Liquid-Templates, keine technische Architektur. Ich brauche ein vollständiges, in sich geschlossenes Design, das anschliessend **1:1** in Shopify nachgebaut wird. Alles, was du nicht zeichnest, existiert später nicht. Halte dich durchgehend an die KLAIR Brand Guideline, die dir vorliegt.

## Ausgangslage

Es gibt zwei Stände:

- **Der alte Shop** (Horizon-Theme mit vielen GemPages-/Shopify-Standardsektionen) definiert den **Funktionsumfang**: alles, was heute kann, muss die neue Seite auch können.
- **Der neue Prototyp** (eigene KLAIR-Sektionen, Navy/Emerald, League Spartan + Lato, GSAP-Scrollführung) definiert die **Bildsprache und das Niveau**. Er ist die Richtung — aber unvollständig. Du baust ihn zu einem geschlossenen Designsystem für den **gesamten** Shop aus.

Kurz: **Look vom neuen Prototyp, Funktionsumfang vom alten Shop, in einer einzigen konsistenten Sprache.**

## Design-Fundament (verbindlich)

- **Farben:** Navy #001F54 (Primär), Navy Light #00296B, Navy Deep #001233 (dunkle Flächen/Footer), Weiss #FFFFFF, Ink #303030 (Fliesstext), Mist #F2F4F6, Porcelain #ECECE7, Ice Mist #DDE8F2, Ice #A9C6E0, Blue Grey #4E5A70 (Sekundärtext), Emerald #00A876 und Emerald Deep #00714E (Bestätigung, Sparen, HEALTHKLAIR). HEALTHKLAIR-Welt läuft auf eigenem Grün-Set (#00281F / #00351F / #F4FAF7 / #EEF7F2).
- **Typografie:** League Spartan 600/700 für alle Headlines, Labels, Buttons, Preise, Zahlen — Zeilenhöhe ~1.02–1.16, Letterspacing −0.02em, Kicker in Versalien mit 0.16–0.24em. Lato 300/400 für Fliesstext, Zeilenhöhe 1.6–1.75.
- **Form:** Buttons als Pillen (999px). Karten/Panels mit grossen Radien — 18/22/28/36/40px je nach Fläche. Weiche, tiefe Schatten statt Rahmen. Rahmen nur als 1.5px-Inset für Ghost-Elemente.
- **Raum:** Sektionen atmen (vertikal clamp 110–220px). Content-Maximum 1400px, seitlich clamp 24–80px. Grosszügiger Weissraum ist Teil der Marke.
- **Ton der Bilder:** ruhig, produktnah, matt, kühles Licht, keine Stockfoto-Ästhetik.

Liefere zuerst ein **Token-Board**: Farben mit Rollen, Typo-Skala mit Beispielen, Radien, Schatten, Spacing-Skala, Icon-Stil (Outline, 1.8 Strichstärke), Grid und Breakpoints (1440 / 1024 / 768 / 390).

## Komponenten-Bibliothek

Zeichne jede Komponente in allen Zuständen — Default, Hover, Fokus (sichtbarer Fokusring), Aktiv, Deaktiviert, Laden, Fehler:

Buttons (Navy, Ghost, Weiss, Ghost-Weiss, Emerald, Gross, mit Icon) · Chips/Filter · Farb- und Aroma-Swatches · Pack-/Mengen-Selektor · Mengenspinner · Badges (Neu, Bestseller, Sale, Ausverkauft, Vorbestellung) · Preisdarstellung mit durchgestrichenem Vorher-Preis und Ersparnis · Formfelder auf hell und auf Navy (Input, Textarea, Select, Checkbox, Radio, Fehlermeldung, Hilfetext) · Accordion · Tabs · Fortschrittsbalken (Gratisversand, Füllstand, Geschmacksprofil) · Produktkarte (hell und auf dunklem Grund) · Bewertungssterne + Google-Badge · Toast/Benachrichtigung · Tooltip · Skeleton-Ladezustände · Scrim · Paginierung · Breadcrumb.

## Globale Elemente

1. **Ankündigungsbar** (schmal, Navy, optional mit Countdown).
2. **Header**, fix, 80px: Logo-Wortmarke, links „Shop" als Drawer-Auslöser, weitere Menüpunkte als Panel-Auslöser, rechts Suche, Warenkorb mit Zähler-Badge in Emerald, Primär-CTA, Burger ab Mobile. Drei Zustände zeichnen: **transparent über dunklem Hero**, **weiss mit Blur nach dem Scrollen**, **offen**. Aktiver Menüpunkt bekommt eine Unterstreichung, die von links einläuft.
3. **Dropdown / Mega-Panel von oben:** weisse Fläche, unten abgerundet (32px), 2–3 Linkspalten mit Versalien-Überschrift plus eine bebilderte Kachel. Übergang: nach unten einfahren, dahinter Scrim.
4. **Shop-Drawer von links** (max 580px, Navy Deep): grosse Menüeinträge in League Spartan mit Untertitel, Trennlinien, unten ein Bildbanner mit Kampagnen-Text.
5. **Suche von oben:** überbreites Eingabefeld mit Unterstrich, darunter Vorschlags-Chips; zusätzlich Zustand mit Live-Ergebnissen (Produkte, Aromen, Artikel, „keine Treffer").
6. **Warenkorb-Drawer von rechts** (480px, weiss) — siehe eigener Abschnitt.
7. **Schnellansicht-Drawer von rechts:** Produktbild, Kicker, Titel, Preis, Optionen als Pillen, „In den Warenkorb" + „Zur Produktseite".
8. **Footer** auf Navy Deep: Wortmarke, vier Linkspalten, Zahlungs- und Versand-Icons, Social, Sprach-/Marktumschalter CH/EU, Rechtszeile.
9. **Cookie-/Privacy-Banner**, **Newsletter-Popup** und **Chat-Bubble** — jeweils so platziert, dass sie sich nicht überlagern (Stapelreihenfolge und Abstände explizit zeigen).

## Seiten — jede als Desktop- und Mobile-Artboard

**Startseite** in dieser Reihenfolge: Motion-Hero mit vierstufiger Scroll-Story (Pen kommt aus der Box → Aroma klickt ein → zudrehen → Zug einstellen, mit Bildunterschriften links/rechts/mittig und Scroll-Hinweis) · Manifest-Textblock, dessen Wörter beim Scrollen von 12 % auf volle Deckkraft aufhellen, mit eingebetteten Pillen-Bildern · USP-Band · Bento-Grid (2×2, 2×1, 1×1 gemischt, dunkle, Emerald- und Ice-Kacheln, eine mit grosser Zahl) · horizontaler Produkt-Slider mit Intro-Spalte und CTA-Karte am Ende · Erklärstrecke auf Navy („Kein Feuerzeug. Keine Batterie. Kein Nikotin.") mit Vorteilsliste · Gegenüberstellung „Was KLAIR nicht ist / was KLAIR ist" als zwei grosse Karten · Sparvergleich mit hochzählender Zahl und zwei Vergleichskarten plus Fussnote „Beispielrechnung" · UGC-Video-Reihe im 9:16-Format zum Wischen · Schritt-für-Schritt als stapelnde Sticky-Karten · Kundenstimmen mit Google-Bewertungs-Badge · Wissen-Teaser · HEALTHKLAIR-Portal (schwebendes 3D-Logo, das der Maus folgt, Klick löst einen Farbübergang in die zweite Welt aus) · Marquee mit Outline-Typo · Schluss-CTA auf Navy Deep.

**Shop / Kollektionen:** Kollektions-Header, Filter- und Sortierleiste als Chips (Desktop-Sidebar und Mobile-Drawer), Produktraster mit Schnellansicht-Knopf beim Hover, eigener dunkelgrüner HEALTHKLAIR-Block innerhalb des Shops, Ladezustand, leeres Ergebnis.

**Aromen-Seite:** Mengenrabatt-Stufen (3 % / 5 % / 10 % / 20 %, oberste Stufe in Navy hervorgehoben), Aromen-Raster mit Geschmacksprofil-Balken (Süsse, Frische, Intensität), Etui-Split, Füllstand-Sektion mit Vorne/Hinten-Umschalter und Füllstandsanzeige, Schluss-CTA.

**Produktseiten** — zeichne jede Variante, sie unterscheiden sich stark:
- **KLAIR Pen:** Sticky-Galerie mit Thumbnails, Kicker/Titel/Preis, Farbswatches, Paketauswahl (1/2/3 Monate mit Ersparnis-Badge), Vertrauenszeile, Akkordeon (Details, Lieferung, Rückgabe), darunter Vergleichstabelle, Video, FAQ, „Passt dazu".
- **Nachfüll-Aromen mit Konfigurator:** Kern der Seite ist die Aromenauswahl mit *n* inkludierten Gratis-Slots und automatisch anspringenden Rabattstufen — zeige die Slot-Leiste (leer, teilbefüllt, voll), die Stufenanzeige („noch 2 bis 5 %"), den ausgelösten Rabatt, den Zustand „Rabatt konnte nicht angewendet werden" und die mobile Variante als aufziehbares Blatt.
- **Bundle-Seite** (Smile Bundle) mit 4 Gratis-Slots und eigenen Stufen, **Whitening Strips**, **Daily Defense**, **Sleep Well**, **Sommerpaket**, **Vorbestellung** (mit Lieferdatum-Hinweis und andersfarbigem CTA).
- Für alle: **mobile Sticky-Kaufleiste** am unteren Rand, Bild-Zoom, Ausverkauft- und Benachrichtigungs-Zustand.

**Warenkorb:**
- **Drawer:** Gratisversand-Fortschritt (unter Schwelle / erreicht / gefeiert), Positionen mit Bild, Variante, Mengenspinner, Entfernen, **Upsell-Block „Passt dazu"** mit kompakten Zeilen und „Dazu"-Knopf, Notizfeld, Rabattcode-Feld mit Erfolgs- und Fehlerzustand, Summenblock mit Zwischensumme/Versand/Rabatt/Total, Checkout-Button, Zahlungs-Icons, Vertrauenszeile. Zusätzlich: **leerer Warenkorb** und **Ladezustand**.
- **Warenkorb-Vollseite** in derselben Sprache, mit breiterer Empfehlungsleiste.

**Checkout-Design:** Shopify-Checkout-Branding vollständig gestalten — Kopfzeile mit Logo, Akzentfarbe, Button-Farbe und -Form, Typografie, Formfeld-Stil, Bestellzusammenfassung mit Produktkacheln, Rabattzeile, Versandoptionen, Zahlungsauswahl, Fehlerzustände, mobile Fassung mit aufklappbarer Zusammenfassung. Dazu: **Post-Purchase-Upsell-Screen** (ein Angebot, Preisvorteil, Ein-Klick-Annahme, Ablehnen), **Danke-/Bestellstatusseite** mit Sendungsverfolgung, Konto-Anlegen-Einladung und einem letzten Cross-Sell. Halte es ruhig — der Checkout darf nichts Verspieltes haben.

**Konto-Bereich:** Login · **Registrieren** (mit Vorteilstext, Newsletter-Opt-in, Fehlerzuständen, Passwortstärke) · Passwort zurücksetzen · Konto aktivieren · Kontoübersicht (Bestellungen, Nachbestell-Verknüpfung zu den Aromen, Adressen, Treuepunkte/Belohnungen) · Bestellliste · Bestelldetail · Adressverwaltung mit Formular im Overlay. Alles im gleichen Karten- und Pillen-Vokabular, nicht als Shopify-Standardformular.

**Rauchfrei-Check (Quiz-Funnel):** eigenes Layout ohne Header, ohne Footer, ohne Overlays und ohne Chat — nur Fortschrittsanzeige, Frage-Screens (Einzelauswahl, Mehrfachauswahl mit Maximum, Zwischenseiten mit Aufzählung, Slider), Reaktions-Einblendungen nach einer Antwort, eine ruhige Ladeanimation von rund 3.5 Sekunden („dein Bericht wird erstellt"), Ergebnis-/Berichtsseite mit persönlicher Auswertung und Produktempfehlung, E-Mail-Abfrage, Abschluss-CTA, dazu die schmale Rechtszeile am Seitenende.

**HEALTHKLAIR-Welt:** Portalübergang von der Startseite, eigener Hero auf dunklem Grün, Paketauswahl, „Fünf Erfahrungen", Vorher-Nachher-Vergleich mit Schieber, Zwei-Formeln-Erklärung, Produktslider, Zahnpflege-Strecke, „Warum HEALTHKLAIR", „Wie funktioniert's", Testimonials, FAQ, Abschluss-CTA und die Brücke zurück zu KLAIR.

**Wissen/Blog:** Übersicht mit Featured-Artikel und Raster, Artikelseite mit Lesefortschritt, Zitatband, Inhaltsverzeichnis, Autorenzeile, verwandte Artikel und produktnahem CTA; dazu die Cluster-/Themenseite mit Navigation zwischen zusammengehörenden Artikeln.

**Weitere Seiten:** Kontakt (Kontaktkacheln, Öffnungszeiten, Formular auf Navy) · Über uns · FAQ · Suchergebnisse · 404 · Passwortgeschützte Seite · Rechtstexte-Layout · Geschenkkarte · Kollektionsübersicht.

## Upsell- und Konversionsflächen (durchgehend gestalten)

Gratisversand-Fortschritt · Mengenrabatt-Stufen · Paket-/Abo-Auswahl mit Ersparnis-Badge · Cart-Drawer-Upsell · „Häufig zusammen gekauft" auf der Produktseite · Post-Purchase-Angebot · Cross-Sell auf der Dankesseite · Zuletzt angesehen · Newsletter mit Anreiz · Countdown-Band · Treueprogramm-Einstieg. Jede Fläche so, dass sie hilfreich wirkt und nicht drängt.

## Chat

Gestalte die Chat-Funktion vollständig: die Blase (ruhend, mit ungelesener Markierung, im Dunkel- und Hellkontext), das geöffnete Fenster (Begrüssung, Vorschlags-Chips wie „Lieferzeit", „Aroma wechseln", „Bestellung ändern", Nachrichtenblasen von Kunde und Team, Eingabezeile, Dateianhang), den Offline-Zustand mit Formular und Antwortzeit, sowie die Regel, wo die Blase **nicht** erscheint (Quiz-Funnel, Checkout). Positionierung mobil so, dass sie die Sticky-Kaufleiste nicht verdeckt.

## Bewegung

Beschreibe und zeige (Start-/Mittel-/Endbild) die Bewegungssprache: Scroll-gebundene Hero-Story, Manifest-Aufhellung, Marquee mit scrollabhängigem Tempo, stapelnde Sticky-Karten, horizontaler Scroll im Produktband, Bento-Hover-Zoom, Bild-Parallax, hochzählende Zahlen, einlaufende Fortschrittsbalken, Drawer-Kurven (0.55–0.6s, weiche Ein-/Ausblendung), Portal-Übergang zu HEALTHKLAIR. Definiere die Standard-Kurve und -Dauer, und zeige, wie alles bei reduzierter Bewegung aussieht.

## Rahmenbedingungen

- Sprache Deutsch (Schweiz), kein ß. Preise in CHF, zweiter Markt EU in EUR — zeige beide im Preis- und Versandkontext.
- Barrierefreiheit: Kontrast mindestens AA, sichtbarer Fokusring auf allen interaktiven Elementen, Tap-Ziele ab 44px, Textalternativen mitdenken.
- Rechtlich sauber: keine Heilversprechen, keine Nikotin-Behauptungen, die Sparrechnung immer als Beispielrechnung ausgewiesen.
- Der Prototyp hat Lücken (fehlende Filter, kein Konto-Design, kein Checkout-Branding, keine Chat-Gestaltung) — schliesse sie eigenständig im gleichen Stil, statt sie auszulassen.

## Lieferung

Ein durchgehendes Canvas, in dieser Reihenfolge: Token-Board → Komponenten-Bibliothek → globale Elemente inklusive aller Drawer- und Panel-Zustände → Startseite → Shop und Aromen → Produktseiten → Warenkorb → Checkout und Post-Purchase → Konto → Quiz-Funnel → HEALTHKLAIR → Wissen → Nebenseiten → Bewegungs-Storyboards. Jede Seite als Desktop (1440) **und** Mobile (390), Zustände als eigene Artboards, klar beschriftet. Ergänze knappe Massangaben dort, wo eine Nachbaubarkeit sonst Interpretationsspielraum hätte.

Arbeite die Liste vollständig ab. Wenn du eine Entscheidung treffen musst, triff sie und halte sie in einer kurzen Notiz am jeweiligen Artboard fest — frag nicht zurück.

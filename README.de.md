# Serponado — Der ultimative SERP-Entitätsstandard

> **Der Tornado, der jeden Winkel der Suchergebnisseite durchfegt und alles dokumentiert, was er findet.**

-[Serponado](https://serponado-agentur.de/) ist das umfassendste offene Entitäts-Repository für Wissen rund um Search Engine Results Pages (SERPs). Es definiert, klassifiziert und verknüpft jede Entität, jedes Attribut, jedes Feature, jedes Signal, jede Metrik und jeden Algorithmus, der für das moderne SERP-Ökosystem relevant ist. Jede Entität folgt dem [Serponado-Standard](STANDARD.md) — einem maschinenlesbaren, menschenfreundlichen Schema, das für KI-Grounding, SEO-Tooling, Knowledge-Graph-Befüllung und semantische Forschung entwickelt wurde.

Der Name **Serponado** ist bewusst gewählt: Wie ein Tornado sind SERPs chaotische, dynamische, sich ständig wandelnde Systeme mit Hunderten interagierender Kräfte — Features, die erscheinen und verschwinden, Algorithmen, die über Nacht die Regeln neu schreiben, KI, die neu definiert, was ein „Ergebnis" überhaupt bedeutet. Dieses Repository bringt Ordnung in dieses Chaos.

---

## Inhaltsverzeichnis

1. [Was ist Serponado?](#was-ist-serponado)
2. [Die Nado-Philosophie](#die-nado-philosophie)
3. [Repository-Architektur](#repository-architektur)
4. [Teil I — SERP-Feature-Taxonomie](#teil-i--serp-feature-taxonomie)
   - [Organische SERP-Features](#organische-serp-features)
   - [Rich Results & Strukturierte-Daten-Features](#rich-results--strukturierte-daten-features)
   - [Lokale SERP-Features](#lokale-serp-features)
   - [Bezahlte / Werbe-Features](#bezahlte--werbe-features)
   - [KI-augmentierte Features](#ki-augmentierte-features)
   - [Universal- & Vertikalsuch-Features](#universal---vertikalsuch-features)
   - [Utility- & Sofortantwort-Features](#utility---sofortantwort-features)
5. [Teil II — SERP-Rankingfaktoren](#teil-ii--serp-rankingfaktoren)
   - [On-Page-Rankingfaktoren](#on-page-rankingfaktoren)
   - [Off-Page-Rankingfaktoren](#off-page-rankingfaktoren)
   - [Technische Rankingfaktoren](#technische-rankingfaktoren)
   - [Nutzersignal-Faktoren](#nutzersignal-faktoren)
   - [Entitäts- & Semantikfaktoren](#entitäts---semantikfaktoren)
6. [Teil III — Google-Algorithmen & Core-Updates](#teil-iii--google-algorithmen--core-updates)
   - [Kern-Algorithmuskomponenten](#kern-algorithmuskomponenten)
   - [Benannte Algorithmus-Updates](#benannte-algorithmus-updates)
   - [Moderne Algorithmussysteme](#moderne-algorithmussysteme)
7. [Teil IV — Suchintentions-Framework](#teil-iv--suchintentions-framework)
8. [Teil V — SERP-Metriken & Messung](#teil-v--serp-metriken--messung)
9. [Teil VI — Technische SEO-Attribute](#teil-vi--technische-seo-attribute)
10. [Teil VII — KI-Suchlandschaft](#teil-vii--ki-suchlandschaft)
11. [Teil VIII — Knowledge Graph & Entitäts-Framework](#teil-viii--knowledge-graph--entitäts-framework)
12. [Teil IX — SERP-Layout-Anatomie](#teil-ix--serp-layout-anatomie)
13. [Teil X — Serponado-Entitätsstandard](#teil-x--serponado-entitätsstandard)
14. [Entitätsindex](#entitätsindex)
15. [Glossar](#glossar)
16. [Mitwirken](#mitwirken)
17. [Lizenz](#lizenz)

---

## Was ist Serponado?

Eine **Search Engine Results Page (SERP)** ist die Seite, die eine Suchmaschine als Antwort auf eine Nutzeranfrage anzeigt. Was auf dieser Seite erscheint — wie sie strukturiert ist, welche Features auftauchen, welche Signale das Ranking bestimmen und wie Ergebnisse bewertet werden — ist das Thema von Serponado.

Serponado ist kein Werkzeug. Es ist kein Plugin. Es ist ein **Standard** — ein autoritatives, versioniertes, gemeinschaftlich gepflegtes Entitäts-Repository, das jede Dimension des SERP-Universums abdeckt:

- Jedes **SERP-Feature**, das Google (und andere Suchmaschinen) anzeigen können
- Jeden dokumentierten **Rankingfaktor**, der die Position beeinflusst
- Jeden bedeutenden **Algorithmus und jedes Update**, das die Regeln veränderte
- Jeden **Suchintentionstyp**, der bestimmt, was Google anzeigt
- Jede **Metrik**, die zur Messung der SERP-Performance genutzt wird
- Jedes **technische Attribut**, das Crawling, Indexierung und Rendering beeinflusst
- Jeden **KI-Suchmechanismus**, der die Ergebnisgeneration neu gestaltet
- Jeden **Entitätstyp**, der in einer SERP erscheinen oder sich auf sie beziehen kann
- Jedes **Layout-Element**, das definiert, wo Ergebnisse erscheinen

Jede Entität in diesem Repository ist eine strukturierte Markdown-Datei, die dem [Serponado-Entitätsstandard](STANDARD.md) folgt. Dateien enthalten YAML-Frontmatter für Maschinenlesbarkeit und reichhaltige Prosa für menschliches Verständnis. Dies macht Serponado geeignet für:

- **KI-Grounding** — Autoritären SERP-Kontext in LLM-Prompts oder RAG-Pipelines einzuspeisen
- **Knowledge-Graph-Befüllung** — Typisierte Relationsprädikate ermöglichen Graph-Traversierung
- **SEO-Tooling** — Features, Faktoren und Signale programmatisch aufzulisten
- **Forschung & Bildung** — Maßgebliche Referenz für Praktiker, Akademiker und Studierende
- **Disambiguierung** — Kanonische Namen, Aliase und `sameAs`-Links zu Wikidata/Wikipedia

---

## Die Nado-Philosophie

Ein Tornado hält nicht bei den offensichtlichen Wahrzeichen. Er fegt durch jedes Feld, jeden Feldweg, jede vergessene Ecke. Serponado wendet denselben totalisierenden Ansatz auf SERP-Wissen an.

**Die drei Prinzipien von Serponado:**

1. **Vollständigkeit vor Kuratierung** — Wenn es in einer SERP existiert, gehört es hierher. Veraltete Features, obskure Rich-Result-Typen, experimentelle KI-Oberflächen — alles dokumentiert.
2. **Struktur vor Prosa** — Jede Entität hat typisierte, maschinenlesbare Attribute. Beziehungen sind explizite Prädikate, nicht durch Narrative impliziert.
3. **Grounding vor Meinung** — Entitätsseiten beschreiben, was Dinge *sind*, nicht, was SEOs *darüber denken*. Evidenzlinks sind Pflicht. Spekulation ist als solche gekennzeichnet.

---

## Repository-Architektur

```
Serponado/
├── README.md                          # Englische Version — die erschöpfende Referenz
├── README.de.md                       # Diese Datei — Deutsche Referenz
├── STANDARD.md                        # Der Serponado-Entitätsseitenstandard
├── CONTRIBUTING.md                    # Wie man Entitäten hinzufügt/bearbeitet
├── schema/
│   ├── entity.schema.json             # JSON Schema zur Frontmatter-Validierung
│   └── relation-predicates.json       # Alle gültigen Relationsprädikatwerte
├── templates/
│   └── entity-template.md             # Leere Entitätsseitenvorlage
├── entities/
│   ├── serp-features/                 # Alle organischen & KI-SERP-Features
│   ├── paid-features/                 # Werbung & bezahlte Platzierungen
│   ├── ranking-factors/               # Signale, die die Position beeinflussen
│   ├── algorithms/                    # Google-Algorithmussysteme & Updates
│   ├── intent/                        # Suchintentionstypen & Abfrageklassifizierungen
│   ├── metrics/                       # Performance- & Autoritätsmetriken
│   ├── technical/                     # Technische SEO-Attribute
│   ├── ai-search/                     # KI-augmentierte Such-Features & GEO
│   ├── layout/                        # SERP-Layout-Positionen & Anatomie
│   └── knowledge-entities/            # Entitätstypen im Knowledge Graph
└── index.json                         # Maschinenlesbarer Master-Entitätsindex
```

---

## Teil I — SERP-Feature-Taxonomie

Ein **SERP-Feature** ist jedes Element, das auf einer Suchergebnisseite erscheint, das über ein standardmäßiges blaues-Link-Ergebnis hinausgeht. Google hat derzeit über 60 verschiedene SERP-Features, die kontextuell basierend auf Abfragetyp, Intent, Gerät, Standort und Nutzerhistorie erscheinen.

### Organische SERP-Features

Diese Features erscheinen im organischen (unbezahlten) Bereich der SERP und beeinflussen, wie Standard-Ergebnisse angezeigt oder ergänzt werden.

---

#### Featured Snippet (Hervorgehobenes Snippet)

**Entitätsdatei:** [`entities/serp-features/featured-snippet.md`](entities/serp-features/featured-snippet.md)

Ein Featured Snippet ist ein ausgewähltes Suchergebnis, das über dem ersten organischen Ergebnis erscheint — manchmal als „Position 0" bezeichnet. Google extrahiert einen kurzen Inhalt von einer Webseite und zeigt ihn direkt in der SERP an, um die Anfrage des Nutzers zu beantworten, ohne dass ein Klick erforderlich ist.

**Untertypen:**
- **Paragraph** — Ein Textblock (typischerweise 40–60 Wörter), der eine Frage direkt beantwortet
- **Liste** — Eine nummerierte oder Aufzählungsliste von Schritten, Elementen oder Kategorien
- **Tabelle** — Tabellarische Daten, aus einer vergleichs- oder datenschweren Seite extrahiert
- **Video** — Ein YouTube-Videoclip mit Zeitstempel, der die Antwort hervorhebt
- **Akkordeon** — Erweiterbare Listenformat (selten, aufkommend)

**Schlüsselattribute:**
- `position`: Über dem ersten organischen Ergebnis (Position 0)
- `auslöser_intentionen`: Informationell, How-To, Definition, Vergleich
- `ctr_auswirkung`: Sehr variabel — kann CTR für wenig kompetitive Anfragen erhöhen, aber für hochvolumige Anfragen reduzieren, wo Nutzer die Antwort lesen, ohne zu klicken
- `eigentümer_signal`: Google kann Inhalte von jeder indizierten Seite anzeigen — kann nicht „angemeldet" werden, aber per `data-nosnippet` oder `max-snippet:-1` abgewählt werden
- `eingeführt`: ~2014

**Optimierungssignale:** Frage-und-Antwort-H2/H3-Struktur, prägnante direkte Antwortabsätze unter Frageüberschriften, strukturierte Listen und Tabellen-Markup erhöhen die Featured-Snippet-Berechtigung.

---

#### Knowledge Panel (Wissenspanel)

**Entitätsdatei:** [`entities/serp-features/knowledge-panel.md`](entities/serp-features/knowledge-panel.md)

Das Knowledge Panel ist ein großes Informationsfeld, das auf der rechten Seite von Desktop-SERPs (oder oben auf mobilen SERPs) für Entitäten erscheint — Personen, Orte, Organisationen, Dinge —, die Google in seinem Knowledge Graph identifiziert hat.

**Schlüsselattribute:**
- `quelle`: Google Knowledge Graph (Daten aus Wikipedia, Wikidata, offiziellen Websites und strukturierten Daten)
- `unterstützte_entitätstypen`: Person, Organisation, Ort, Produkt, Ereignis, Konzept, Werk
- `erscheint_für`: Marken-, Navigations- und entitätsbasierte Anfragen
- `beanspruchbar_von`: Verifizierten Entitätseigentümern über die Google Search Console
- `abschnitte`: Zusammenfassung, Bilder, Schlüsselfakten, Social-Profiles, Verwandte Entitäten
- `position`: Rechte Spalte (Desktop), Oben auf SERP (Mobil)

---

#### People Also Ask (Ähnliche Fragen)

**Entitätsdatei:** [`entities/serp-features/people-also-ask.md`](entities/serp-features/people-also-ask.md)

„Ähnliche Fragen" ist ein erweiterbares Frage-und-Antwort-Feld, das verwandte Fragen anzeigt, die Nutzer häufig zusammen mit der aktuellen Anfrage suchen. Jede Frage, wenn angeklickt, erweitert sich, um eine Antwort aus einer Webseite zu zeigen (ähnlich einem Featured Snippet).

**Schlüsselattribute:**
- `verhalten`: Erweitert sich dynamisch — das Anklicken einer Frage lädt weitere verwandte Fragen (potenziell unendlich)
- `anfangszahl`: Typischerweise 3–4 Fragen
- `position`: Variabel — häufig zwischen dem 1. und 3. organischen Ergebnis
- `auslöser`: Primär informationelle und kommerzielle Anfragen
- `ctr_auswirkung`: Gemischt — bietet Markenexposure und Featured-Snippet-ähnliche Sichtbarkeit

**Optimierung:** Strukturiertes FAQ- und Q&A-Schema, fragebasierte H2/H3-Überschriften, prägnante Antworten unter jeder Überschrift.

---

#### Image Pack (Bilderpaket)

**Entitätsdatei:** [`entities/serp-features/image-pack.md`](entities/serp-features/image-pack.md)

Eine horizontale Zeile von Bildergebnissen, die in die organische SERP eingebettet ist. Das Anklicken eines Bildes öffnet Google Images.

**Schlüsselattribute:**
- `quelle`: Google Images-Index
- `auslöser_intentionen`: Visuell, Navigational, Informationell
- `position`: Variabel — typischerweise innerhalb der top 5 organischen Ergebnisse
- `optimierungssignale`: Alt-Text, Dateiname, umgebender Seitenkontext, strukturierte Daten (ImageObject)

---

#### Video-Karussell

**Entitätsdatei:** [`entities/serp-features/video-carousel.md`](entities/serp-features/video-carousel.md)

Eine horizontal scrollbare Zeile von Videoergebnissen, typischerweise von YouTube, die in der SERP erscheint.

**Schlüsselattribute:**
- `primäre_quelle`: YouTube (dominant), aber auch Vimeo, Dailymotion und Publisher-Sites mit VideoObject-Schema
- `rich_result_signale`: VideoObject-Schema, Thumbnails, Dauer, Clip-Markup, SeekToAction-Markup
- `auslöser_intentionen`: How-to, Tutorial, Bewertung, Unterhaltung, News

---

#### News Box / Top Stories (Nachrichtenkasten / Wichtigste Meldungen)

**Entitätsdatei:** [`entities/serp-features/news-box.md`](entities/serp-features/news-box.md)

Ein Karussell oder eine Liste aktueller Nachrichtenartikel von Google News-indizierten Publishern. Erscheint oben in der SERP für zeitgemäße, nachrichtenbezogene Anfragen.

**Schlüsselattribute:**
- `berechtigung`: Erfordert Google News Publisher-Zulassung
- `aktualitätsgewicht`: Extrem hoch — Aktualität ist ein primäres Ranking-Signal
- `anzeige`: Schlagzeile, Quelle, Veröffentlichungszeit, Thumbnail
- `strukturierte_daten`: NewsArticle- oder Article-Schema
- `temporärer_auslöser`: Breaking News, aktuelle Ereignisse, benannte Ereignisse, aktuelle Ankündigungen

---

#### Sitelinks (Website-Links)

**Entitätsdatei:** [`entities/serp-features/sitelinks.md`](entities/serp-features/sitelinks.md)

Sitelinks sind Unterseiten-Links, die unter dem Hauptergebnis für Marken- oder Navigationsanfragen angezeigt werden. Sie helfen Nutzern, direkt zu bestimmten Abschnitten einer Website zu navigieren.

**Untertypen:**
- **Standard-Sitelinks** — Bis zu 6 Sub-Links mit kurzen Beschreibungen
- **Einzeilige Sitelinks** — Kompakte Version mit 2–4 Links in einer Zeile
- **Sitelinks-Suchfeld** — Bettet ein standortspezifisches Suchfeld in das Ergebnis ein

**Schlüsselattribute:**
- `auslöser`: Marken-/Navigationsanfragen, bei denen Google hohe Konfidenz über das Nutzerziel hat
- `kontrolle`: Können nicht manuell hinzugefügt werden; Google generiert sie automatisch

---

#### Ähnliche Suchanfragen (Related Searches)

**Entitätsdatei:** [`entities/serp-features/related-searches.md`](entities/serp-features/related-searches.md)

Ein Feld am Ende der SERP, das 6–8 verwandte Anfragen zeigt. Hilft Nutzern, ihre Suche zu verfeinern oder zu erweitern.

**Schlüsselattribute:**
- `position`: Unten in der SERP (primär), gelegentlich in der Mitte
- `quelle`: Googles Anfragenzuordnungsgraph / Suchko-Vorkommensdaten
- `seo_wert`: Forschungswerkzeug zur Identifizierung verwandter Themen und semantischer Cluster

---

#### People Also Search For (Ähnliche Suchanfragen nach Rückklick)

**Entitätsdatei:** [`entities/serp-features/people-also-search-for.md`](entities/serp-features/people-also-search-for.md)

Erscheint, wenn ein Nutzer auf ein Suchergebnis klickt und dann zur SERP zurückkehrt (Rückklick-Verhalten). Zeigt alternative Websites, die Nutzer auch für dieselbe Anfrage besucht haben.

---

#### Perspectives / Forum-Ergebnisse

**Entitätsdatei:** [`entities/serp-features/perspectives.md`](entities/serp-features/perspectives.md)

2023 eingeführt, ist Perspectives ein SERP-Feature, das Inhalte aus Foren, sozialen Medien und Diskussionsplattformen (Reddit, Quora, Stack Exchange, TikTok, YouTube) für Erstpersonen-Erfahrungsanfragen anzeigt.

---

#### Web Stories

**Entitätsdatei:** [`entities/serp-features/web-stories.md`](entities/serp-features/web-stories.md)

Visueller Story-Inhalt im AMP-Stories-Format, der als tippbares Story-Karussell in Suchergebnissen angezeigt wird.

---

#### Bewertungs-Snippets (Review Snippets)

**Entitätsdatei:** [`entities/serp-features/review-snippets.md`](entities/serp-features/review-snippets.md)

Sternebewertungen und Bewertungsanzahl, die unter der URL eines organischen Ergebnisses angezeigt werden. Werden durch strukturiertes Daten-Markup betrieben.

**Schlüsselattribute:**
- `schema_typen`: `Product`, `Recipe`, `Movie`, `Book`, `Software`, `LocalBusiness`, `Course`, `Event`
- `anzeige`: Sternebewertung (1–5), numerische Punktzahl, Bewertungsanzahl
- `auswirkung_auf_ctr`: Erhöht die CTR signifikant — starkes visuelles Signal in wettbewerbsintensiven SERPs

---

#### FAQ-Ergebnisse

**Entitätsdatei:** [`entities/serp-features/faq-results.md`](entities/serp-features/faq-results.md)

Erweiterbare Frage-und-Antwort-Akkordeons unter einem Standard-Ergebnis, betrieben durch `FAQPage`-strukturierte Daten.

**Status-Hinweis:** Google schränkte FAQ-Rich-Results im August 2023 ein — jetzt nur noch für Regierungs- und Gesundheitsseiten angezeigt.

---

#### How-To-Ergebnisse

**Entitätsdatei:** [`entities/serp-features/how-to-results.md`](entities/serp-features/how-to-results.md)

Schritt-für-Schritt-Anleitungsergebnisse, betrieben durch `HowTo`-strukturierte Daten.

---

#### Stellenanzeigen (Job Listings)

**Entitätsdatei:** [`entities/serp-features/job-listings.md`](entities/serp-features/job-listings.md)

Ein Rich-Result-Feld, das Stellenangebote direkt in der SERP anzeigt, aggregiert aus Arbeitgeber-Websites, die `JobPosting`-strukturierte Daten implementieren.

---

#### Veranstaltungs-Listings (Event Listings)

Strukturierte Veranstaltungsinformationen, die inline in der SERP für veranstaltungsbezogene Anfragen angezeigt werden.

---

#### Rezeptkarten (Recipe Cards)

**Entitätsdatei:** [`entities/serp-features/recipe-cards.md`](entities/serp-features/recipe-cards.md)

Rich-Rezeptergebnisse mit Kochdetails, Bewertungen und Bildern, häufig als Karussell angezeigt.

---

#### Produkt-Rich-Results

Erweiterte Produktinformationen in organischen Ergebnissen, einschließlich Preis, Verfügbarkeit, Bewertungen und Händlerinformationen.

---

### Lokale SERP-Features

---

#### Local Pack (Lokales Paket / Map Pack / 3er-Paket)

**Entitätsdatei:** [`entities/serp-features/local-pack.md`](entities/serp-features/local-pack.md)

Das Local Pack ist ein SERP-Feature, das einen Google Maps-Embed mit 3 lokalen Unternehmenslistings für standortbasierte Anfragen anzeigt.

**Schlüsselattribute:**
- `ergebnisanzahl`: 3 (früher 7)
- `auslöser_intentionen`: Lokaler Intent, „in meiner Nähe"-Anfragen, standortmodifizierte Anfragen
- `datenquelle`: Google Business Profile (ehemals Google My Business)
- `ranking_faktoren`:
  - Relevanz (wie gut das Listing zur Anfrage passt)
  - Distanz (Nähe des Unternehmens zum Suchenden)
  - Prominenz (Online- und Offline-Reputation, Bewertungen, Links)
- `anzeige`: Karten-Embed, Unternehmensname, Kategorie, Bewertung, Bewertungsanzahl, Adresse, Öffnungszeiten, Klick-zum-Anruf

---

#### Google Business Profile (GBP)

Das kostenlose Unternehmenseintrag-Produkt von Google, das Local Pack und Local Knowledge Panel-Erscheinungen betreibt. Früher Google My Business (GMB), 2021 umbenannt.

---

### Bezahlte / Werbe-Features

---

#### Textanzeigen (Responsive Search Ads / RSA)

**Entitätsdatei:** [`entities/paid-features/text-ads.md`](entities/paid-features/text-ads.md)

Das primäre Google Ads-Format — textbasierte Anzeigen, die oben und unten in der SERP erscheinen, mit einem „Gesponsert"-Label versehen.

**Schlüsselattribute:**
- `format`: RSA — bis zu 15 Überschriften (3 angezeigt), 4 Beschreibungen (2 angezeigt)
- `position`: Oben in der SERP (bis zu 4 Anzeigen) und unten (bis zu 3 Anzeigen)
- `auktionsmechanismus`: Zweitpreis-Auktion basierend auf Qualitätspunktzahl × Max.-CPC-Gebot = Anzeigenrang
- `qualitätspunktzahl_komponenten`: Erwartete CTR, Anzeigenrelevanz, Landingpage-Erfahrung

---

#### Shopping-Anzeigen (Product Listing Ads / PLAs)

Visuelle Produktanzeigen mit Bildern, Preisen, Händlernamen und Bewertungen oben in SERPs für kommerzielle Anfragen.

---

#### Local Service Ads (LSAs / Lokale Dienstleistungsanzeigen)

Pay-per-Lead-Anzeigen für lokale Dienstleistungsunternehmen (Klempner, Elektriker, Anwälte usw.), die ganz oben in SERPs erscheinen.

**Schlüsselattribute:**
- `abrechnungsmodell`: Pay-per-Lead (nicht Pay-per-Click)
- `verifizierung`: Google Guarantee / Google Screened Badge — Hintergrundüberprüfungen erforderlich

---

#### Performance Max (PMax)

Googles vollautomatisierter, zielorientierter Kampagnentyp, der Anzeigen auf allen Google-Oberflächen aus einer einzigen Kampagne schaltet.

---

### KI-augmentierte Features

---

#### KI-Übersicht (AI Overview)

**Entitätsdatei:** [`entities/serp-features/ai-overview.md`](entities/serp-features/ai-overview.md)

Googles KI-generierte Antwort, die über organischen Ergebnissen für viele Anfragen erscheint, betrieben von Gemini. Als „Search Generative Experience" (SGE) im Mai 2023 gestartet, im Mai 2024 in „AI Overviews" umbenannt und global ausgerollt.

**Schlüsselattribute:**
- `betrieben_von`: Google Gemini
- `position`: Oben in der SERP, über allen organischen und bezahlten Ergebnissen
- `anzeige`: Generativer Absatz mit Inline-Zitaten und erweiterbarem Quellen-Panel
- `zero_click_risiko`: Hoch — umfassende Antworten können den Klickbedarf eliminieren
- `optimierungsdisziplin`: Generative Engine Optimization (GEO)

---

### Universal- & Vertikalsuch-Features

---

#### Flüge-Box (Flights Box)

Interaktives Flugsuche-Widget, eingebettet in die SERP für flugbezogene Anfragen, betrieben von Google Flights.

---

#### Hotels-Pack

Hotelsuchergebnisse mit Preisen, Verfügbarkeit, Bewertungen und Buchungslinks für Unterkunftsanfragen.

---

#### Sport-Ergebnisse (Sports Scores)

Live- und aktuelle Sport-Ergebnisse, Spielpläne und Tabellen, direkt in der SERP für Team-, Liga- und Spielanfragen angezeigt.

---

#### Finanz-Box / Aktien-Panel

Live-Aktienkurse, Charts, Finanzdaten und Unternehmensübersichten für Finanzanfragen, betrieben von Google Finance.

---

### Utility- & Sofortantwort-Features

---

#### Wetterbox

Aktuelle Wetterbedingungen und Vorhersagen, direkt in der SERP für Wetteranfragen angezeigt.

---

#### Rechner (Calculator)

Ein interaktives Rechner-Widget, in die SERP für mathematische Ausdrucksanfragen eingebettet.

---

#### Definitions-Box

Wörterbuchdefinition, Ausspracheführer, Wortherkunft und Synonyme für „define [Wort]"-Anfragen angezeigt.

---

#### Übersetzungsbox

Google Translate-Widget, in die SERP für Übersetzungsanfragen eingebettet.

---

#### Einheitenumrechner

Interaktives Konversionswerkzeug für Maßeinheiten (Länge, Gewicht, Temperatur, Währung usw.).

---

## Teil II — SERP-Rankingfaktoren

Rankingfaktoren sind die Signale, die Googles Algorithmen verwenden, um Relevanz, Autorität, Qualität und Vertrauenswürdigkeit einer Webseite zu bestimmen — und damit ihre Position in der SERP.

### On-Page-Rankingfaktoren

---

#### E-E-A-T (Erfahrung, Expertise, Autorität, Vertrauenswürdigkeit)

**Entitätsdatei:** [`entities/ranking-factors/e-e-a-t.md`](entities/ranking-factors/e-e-a-t.md)

E-E-A-T ist Googles Qualitätsbewertungsrahmen, der primär von Suchqualitätsbewertern verwendet wird, um Inhaltsqualität zu beurteilen. Ursprünglich E-A-T (ohne „Erfahrung"), wurde das erste „E" für Erfahrung im Dezember 2022 hinzugefügt.

**Komponenten:**
- **Erfahrung (Experience)** — Hat der Autor Ersthand- oder Lebenserfahrung mit dem Thema?
- **Expertise** — Hat der Autor formales oder demonstriertes Wissen/Fähigkeiten?
- **Autorität (Authoritativeness)** — Wird der Autor oder die Seite als Autorität auf seinem Gebiet von anderen anerkannt?
- **Vertrauenswürdigkeit (Trustworthiness)** — Ist die Seite ehrlich, transparent, genau und sicher?

**YMYL (Your Money Your Life / Ihr Geld, Ihr Leben):** E-E-A-T-Standards sind am höchsten für Inhalte, die Gesundheit, finanzielle Stabilität, Sicherheit oder Gesellschaft beeinflussen können.

---

#### Inhaltsrelevanz (Content Relevance)

Wie gut der Inhalt einer Seite die Suchanfragen-Intention semantisch trifft, einschließlich Keyword-Nutzung, Themenabdeckung, semantischer Tiefe und Entitätsabdeckung.

---

#### Inhaltsqualität (Content Quality)

Googles Bewertung, ob Inhalte wirklich hilfreich, originell und primär für Menschen erstellt wurden und nicht für Suchmaschinen.

---

#### Inhaltliche Aktualität (Content Freshness)

Die Auswirkung des Veröffentlichungsdatums und der Aktualisierungsfrequenz auf Rankings, insbesondere für zeitkritische Anfragen.

**Query Deserves Freshness (QDF):** Google identifiziert Anfragen, bei denen Aktualität wichtig ist (Nachrichten, Trends, sich entwickelnde Themen) und bevorzugt kürzlich veröffentlichte oder aktualisierte Inhalte.

---

#### Title-Tag (Seitentitel)

Das HTML-`<title>`-Element ist ein kritisches On-Page-Signal, das als anklickbare Überschrift in SERP-Ergebnissen angezeigt wird. Google kann Titel umschreiben, die irreführend, zu lang oder keyword-überfüllt sind.

**Best Practices:**
- 50–60 Zeichen
- Primäres Keyword nahe dem Anfang
- Markenname am Ende (für Nicht-Startseiten)
- Einzigartig pro Seite
- Beschreibt den Seiteninhalt genau

---

#### Meta-Description (Meta-Beschreibung)

Das HTML-`<meta name="description">`-Tag. Kein direktes Ranking-Signal, beeinflusst aber CTR — das Snippet, das Google unter dem Titel anzeigt.

**Schlüsselattribute:**
- `ranking_faktor`: Indirekt (über CTR-Auswirkung)
- `länge`: 150–160 Zeichen
- `google_umschreibungsrate`: ~70% der Zeit schreibt Google Meta-Beschreibungen um

---

#### H1 und Überschriftenstruktur

Korrekte Verwendung von H1–H6-Überschriften-Tags für Inhaltsstruktur und thematische Signalverstärkung.

---

#### Interne Verlinkung

Die Praxis, zwischen Seiten innerhalb derselben Domain zu verlinken, PageRank zu verteilen, thematische Autoritätscluster zu etablieren und Crawlbarkeit zu verbessern.

---

#### URL-Struktur

Das Format und der Inhalt einer Seiten-URL als Relevanz- und Usability-Signal.

**Best Practices:**
- Kurz, beschreibend, keyword-relevant
- Kleinbuchstaben mit Bindestrichen (keine Unterstriche)
- Logische Hierarchie, die die Site-Struktur widerspiegelt

---

### Off-Page-Rankingfaktoren

---

#### Backlinks (Eingehende Links)

**Entitätsdatei:** [`entities/ranking-factors/backlinks.md`](entities/ranking-factors/backlinks.md)

Der kollektive Satz externer Links, die auf eine Domain oder Seite verweisen. Googles ursprünglicher Kern-Ranking-Einblick (PageRank) basiert auf dem Prinzip, dass ein Link von einer Seite zu einer anderen eine Vertrauensstimme ist.

**Qualitätssignale:**
- **Linkautorität** — Die Autorität der verlinkenden Seite/Domain
- **Thematische Relevanz** — Behandelt die verlinkende Seite verwandte Themen?
- **Link-Diversität** — Breite Vielfalt verlinkender Root-Domains
- **Anchor-Text-Verteilung** — Natürliche Mischung aus Marken-, Exact-Match-, Partial-Match-, generischen Ankern
- **Link-Platzierung** — Redaktionelle (inhaltliche) Links überwiegen Footer-/Sidebar-Links
- **Follow vs. Nofollow** — `dofollow`-Links übertragen Eigenkapital; `nofollow`, `ugc`, `sponsored` nicht

---

#### PageRank

**Entitätsdatei:** [`entities/ranking-factors/pagerank.md`](entities/ranking-factors/pagerank.md)

Googles grundlegender linkbasierter Ranking-Algorithmus, 1998 von Larry Page und Sergey Brin eingeführt. Weist jeder Webseite eine relative Wichtigkeitspunktzahl basierend auf Anzahl und Qualität eingehender Links zu.

---

#### Markensignale (Brand Signals)

Signale, die darauf hinweisen, dass eine Domain eine echte, anerkannte Marke repräsentiert.

**Signale:**
- Markenbezogenes Suchvolumen und CTR
- Google Knowledge Panel-Existenz
- Social-Media-Präsenz und Verifizierung
- Presseberichterstattung und Zitate
- Ko-Auftreten mit Branchenbegriffen in Texten (ohne Links)
- Direktverkehrsmuster

---

### Technische Rankingfaktoren

---

#### Core Web Vitals (Kern-Web-Metriken)

**Entitätsdatei:** [`entities/ranking-factors/core-web-vitals.md`](entities/ranking-factors/core-web-vitals.md)

Googles Satz von Nutzererfahrungs-Metriken, die Ladeperformance, Interaktivität und visuelle Stabilität messen. Wurden im Juni 2021 über das Page Experience Update zu einem offiziellen Google-Ranking-Faktor.

**Aktuelle Metriken:**
- **LCP (Largest Contentful Paint / Größte inhaltliche Darstellung)** — Ladeperformance. Ziel: < 2,5 Sekunden
- **INP (Interaction to Next Paint / Interaktion bis zur nächsten Darstellung)** — Interaktivität. Ziel: < 200 ms. Ersetzte FID im März 2024
- **CLS (Cumulative Layout Shift / Kumulative Layoutverschiebung)** — Visuelle Stabilität. Ziel: < 0,1

---

#### Mobile-First-Indexierung

Seit 2019 verwendet Google die mobile Version einer Seite als primäre Version für Indexierung und Ranking.

---

#### HTTPS / SSL

Verwendung von HTTPS (über SSL/TLS-Zertifikat) als leichtes Ranking-Signal seit 2014.

---

#### Strukturierte Daten / Schema-Markup

**Entitätsdatei:** [`entities/technical/structured-data.md`](entities/technical/structured-data.md)

Maschinenlesbares Markup mit Schema.org-Vokabular (JSON-LD empfohlen), das Google hilft, Seiteninhalte zu verstehen und Rich Results zu aktivieren.

---

### Nutzersignal-Faktoren

---

#### Click-Through-Rate (CTR)

**Entitätsdatei:** [`entities/metrics/ctr.md`](entities/metrics/ctr.md)

Der Prozentsatz der Impressionen, der zu einem Klick führt. Formel: CTR = (Klicks ÷ Impressionen) × 100

---

#### Verweildauer (Dwell Time)

Die Zeit zwischen einem Nutzerklick auf ein Suchergebnis und der Rückkehr zur SERP. Längere Verweildauer deutet auf Nutzerzufriedenheit mit dem Inhalt hin.

---

#### Pogo-Sticking

Wenn ein Nutzer auf ein Ergebnis klickt, schnell zur SERP zurückkehrt und auf ein anderes Ergebnis klickt — signalisiert Unzufriedenheit mit dem ersten Ergebnis.

---

### Entitäts- & Semantikfaktoren

---

#### Topische Autorität (Topical Authority)

**Entitätsdatei:** [`entities/ranking-factors/topical-authority.md`](entities/ranking-factors/topical-authority.md)

Die Breite und Tiefe der Abdeckung eines Themenbereichs durch eine Website. Sites mit umfassenden, intern verlinkten Inhalten zu einem Thema erwerben thematische Autorität.

**Aufbausignale:** Content-Cluster (Pillar + unterstützende Seiten), interne Verlinkung innerhalb von Themenclustern, konsistentes Veröffentlichen zu verwandten Themen, Expertenautorschaft.

---

#### Entitätserkennung (Entity Recognition)

Googles Fähigkeit, benannte Entitäten (Personen, Orte, Organisationen, Produkte, Konzepte) auf einer Seite zu identifizieren und zu klassifizieren.

---

#### Passage-Ranking

Googles System zur Ranglistenerstellung einzelner Abschnitte innerhalb eines langen Dokuments.

---

## Teil III — Google-Algorithmen & Core-Updates

Googles Ranking-System ist kein einzelner Algorithmus — es ist ein geschichtetes System aus Algorithmen, Filtern, Qualitätsbewertern und maschinellen Lernmodellen.

### Kern-Algorithmuskomponenten

---

#### RankBrain

**Entitätsdatei:** [`entities/algorithms/rankbrain.md`](entities/algorithms/rankbrain.md)

Googles erste maschinelle Lernkomponente, die direkt im Such-Ranking-System eingesetzt wird, im Oktober 2015 angekündigt. Interpretiert die Bedeutung von Suchanfragen — insbesondere neue, mehrdeutige oder konversationelle Anfragen.

---

#### BERT (Bidirektionale Encoder-Darstellungen von Transformatoren)

**Entitätsdatei:** [`entities/algorithms/bert.md`](entities/algorithms/bert.md)

Googles NLP-Durchbruchmodell (2018 veröffentlicht, im Oktober 2019 in der Suche eingesetzt). Ermöglicht Google, den Kontext und die Nuance von Wörtern in Anfragen zu verstehen.

**Schlüsselattribute:**
- `modelltyp`: Transformer-basiertes NLP-Modell (für Suche feinabgestimmt)
- `abdeckung`: ~10% der englischen Anfragen (2019), später erweitert
- `schlüsselfähigkeit`: Kontextverständnis — „can you get medicine for someone pharmacy"

---

#### MUM (Multitask Unified Model / Multitask-Einheitsmodell)

**Entitätsdatei:** [`entities/algorithms/mum.md`](entities/algorithms/mum.md)

Googles multimodales KI-Modell (2021 angekündigt), beschrieben als 1000× leistungsfähiger als BERT. Versteht und generiert Text über 75+ Sprachen gleichzeitig.

---

#### Gemini in der Suche

Googles neuestes großes Sprachmodell, in die Suche integriert, um AI Overviews und andere generative Features zu betreiben.

---

### Benannte Algorithmus-Updates

---

#### Google Panda (2011)

**Entitätsdatei:** [`entities/algorithms/panda.md`](entities/algorithms/panda.md)

Großes Update, das auf minderwertige, dünne und doppelte Inhalte abzielt. Strafte Content-Farmen und Sites mit hohem Anteil minderwertiger Seiten.

**Schlüsselattribute:**
- `erstmals_gestartet`: 24. Februar 2011
- `ziel`: Dünne Inhalte, duplizierte Inhalte, Content-Farmen, minderwertiger UGC
- `mechanismus`: Siteweite Qualitätspunktzahl — ein einziger schlechter Abschnitt konnte die gesamte Domain schädigen
- `in_kern_integriert`: 2016

---

#### Google Penguin (2012)

**Entitätsdatei:** [`entities/algorithms/penguin.md`](entities/algorithms/penguin.md)

Großes Update gegen Webspam, insbesondere manipulative Link-Building-Praktiken (bezahlte Links, Link-Netzwerke, keyword-überfüllter Anchor-Text).

**Schlüsselattribute:**
- `erstmals_gestartet`: 24. April 2012
- `ziel`: Unnatürliche Linkprofile, Link-Schemata, Anchor-Text-Überoptimierung
- `in_kern_integriert`: September 2016 (Echtzeit, läuft kontinuierlich)

---

#### Google Hummingbird (2013)

Ein kompletter Algorithmus-Neuschrieb (kein Update) mit Fokus auf konversationelle Suche und semantisches Verständnis.

---

#### Google Pigeon (2014)

Ein lokales Such-Algorithmus-Update, das die Integration lokaler Ergebnisse mit Kern-Web-Ranking-Signalen verbesserte.

---

#### Mobilegeddon (2015)

Googles erstes offizielles Mobile-Freundlichkeits-Ranking-Update.

---

#### Medic-Update (2018)

Ein bedeutendes breites Core-Algorithmus-Update, das Gesundheits-, Medizin- und YMYL-Websites überproportional beeinflusste.

---

#### BERT-Update (2019)

Einsatz des BERT NLP-Modells in der Google-Suche.

---

#### Hilfreiches Inhaltssystem (Helpful Content System, 2022–2023)

**Entitätsdatei:** [`entities/algorithms/helpful-content.md`](entities/algorithms/helpful-content.md)

Eine Reihe von Updates, die einen siteweiten Klassifikator einführten, der Inhalte identifiziert und abwertet, die primär für Suchmaschinen und nicht für Menschen geschrieben wurden.

**Schlüsselattribute:**
- `erstmals_gestartet`: 25. August 2022
- `mechanismus`: ML-Klassifikator weist siteweites „Nützlichkeits"-Signal zu
- `in_kern_integriert`: März 2024 Core Update

---

#### Core-Update März 2024

Das größte dokumentierte Google Core-Algorithmus-Update, das 45 Tage für den vollständigen Rollout benötigte. Ziel war die Reduzierung von unnützlichen, minderwertigen und KI-generierten Spam-Inhalten um 40%.

---

#### SpamBrain

Googles KI-basiertes Spam-Erkennungssystem zur Identifizierung und Neutralisierung von Link-Spam und inhaltlichem Spam im großen Maßstab.

---

### Moderne Algorithmussysteme

---

#### Hilfreiches Inhaltssystem (als Kern-Algorithmus)

Nach der Absorption in den Core-Algorithmus im März 2024 läuft das Hilfreiche Inhaltssystem kontinuierlich als Teil des Kern-Rankings — es gibt keine separaten „Hilfreiche Inhalte Update"-Ankündigungen mehr.

---

## Teil IV — Suchintentions-Framework

Die Suchintention (auch als Anfragen-Intent oder Nutzer-Intent bezeichnet) beschreibt das Ziel hinter einer Suchanfrage eines Nutzers.

---

#### Informationeller Intent

**Entitätsdatei:** [`entities/intent/informational.md`](entities/intent/informational.md)

Der Nutzer möchte etwas lernen. Die Anfrage sucht nach Wissen, Erklärungen, Definitionen oder Antworten.

**Signale:** Fragewörter (wer, was, wann, wo, warum, wie), „Definition von", „Bedeutung von", „Was ist", „Wie funktioniert"
**Ausgelöste SERP-Features:** Featured Snippet, People Also Ask, Knowledge Panel, AI Overview, Bilderpaket
**Inhaltstyp:** Artikel, Erklärungen, Tutorials, Leitfäden, Enzyklopädieeinträge

---

#### Navigationaler Intent

**Entitätsdatei:** [`entities/intent/navigational.md`](entities/intent/navigational.md)

Der Nutzer möchte eine bestimmte Website oder Seite erreichen. Er kennt das Ziel bereits.

**Signale:** Markennamen, Website-Namen, „[Marke] Login", „[Marke] Karriere"
**Ausgelöste SERP-Features:** Sitelinks, Knowledge Panel, Sitelinks-Suchfeld

---

#### Transaktionaler Intent

**Entitätsdatei:** [`entities/intent/transactional.md`](entities/intent/transactional.md)

Der Nutzer beabsichtigt, eine Aktion abzuschließen — typischerweise einen Kauf, Download, eine Anmeldung oder Buchung.

**Signale:** „kaufen", „bestellen", „herunterladen", „abonnieren", „anmelden", „[Produkt] Preis", „[Produkt] Angebot"
**Ausgelöste SERP-Features:** Shopping-Anzeigen, Produkt-Rich-Results
**Inhaltstyp:** Produktseiten, Checkout-Seiten, Landingpages, Preisseiten

---

#### Kommerzieller Untersuchungsintent

**Entitätsdatei:** [`entities/intent/commercial-investigation.md`](entities/intent/commercial-investigation.md)

Der Nutzer recherchiert Produkte oder Dienstleistungen, bevor er eine Kaufentscheidung trifft.

**Signale:** „beste", „vs", „Bewertung", „Vergleich", „Top", „günstigste", „[Produkt] Alternative"
**Ausgelöste SERP-Features:** Bewertungs-Snippets, Produkt-Rich-Results, Perspectives/Forum-Ergebnisse
**Inhaltstyp:** Vergleichsartikel, Bewertungsposts, „Beste X für Y"-Leitfäden, Listicles

---

#### Lokaler Intent

**Entitätsdatei:** [`entities/intent/local.md`](entities/intent/local.md)

Der Nutzer sucht nach Produkten, Dienstleistungen oder Informationen in einem bestimmten geografischen Bereich.

**Signale:** „in meiner Nähe", „[Dienstleistung] in [Stadt]", Standortmodifikatoren, Anfragen mit implizitem lokalem Intent
**Ausgelöste SERP-Features:** Local Pack, Local Finder, Local Knowledge Panel, Local Service Ads

---

#### Saisonaler / Zeitlicher Intent

Der Intent des Nutzers wird durch zeitkritische Ereignisse, Jahreszeiten oder wiederkehrende Muster angetrieben.

---

#### Visueller / Bild-Intent

Der Nutzer möchte primär Bilder oder visuelle Inhalte für das Anfragegebiet.

---

#### Sprachsuch-Intent

Anfragen, die konversationell formuliert sind, oft länger und in natürlicher Sprache, typischerweise aus Sprachassistenten stammend.

---

## Teil V — SERP-Metriken & Messung

---

#### Impressionen (Impressions)

**Entitätsdatei:** [`entities/metrics/impressions.md`](entities/metrics/impressions.md)

Die Anzahl, wie oft eine URL in den Suchergebnissen für eine Anfrage erschien. In der Google Search Console gemeldet.

---

#### Klicks (Clicks)

Die Anzahl, wie oft ein Nutzer auf eine URL aus der SERP auf deine Website geklickt hat. In der Google Search Console gemeldet.

---

#### Click-Through-Rate (CTR)

**Entitätsdatei:** [`entities/metrics/ctr.md`](entities/metrics/ctr.md)

**Formel:** CTR = (Klicks ÷ Impressionen) × 100%

**Benchmark-CTRs nach Position (ungefähr):**
- Position 1: ~27–39%
- Position 2: ~15–18%
- Position 3: ~10–12%
- Position 4: ~7–9%
- Position 5: ~5–6%
- Positionen 6–10: 2–4%
- Featured Snippet: Stark variabel

---

#### Durchschnittliche Position (Average Position)

Die mittlere Position einer URL in den Suchergebnissen über alle Anfragen, die eine Impression ausgelöst haben. In der Google Search Console gemeldet.

---

#### Sichtbarkeitsindex (Visibility Index)

**Entitätsdatei:** [`entities/metrics/visibility-index.md`](entities/metrics/visibility-index.md)

Eine zusammengesetzte Metrik, die die geschätzte Sichtbarkeit einer Domain in der organischen Suche misst, gewichtet nach Keyword-Suchvolumen und Position. Verwendet von Tools wie SISTRIX (Sichtbarkeitsindex) und Semrush.

---

#### Share of Voice (Stimmenanteil)

Der Prozentsatz der gesamten verfügbaren organischen Klicks für einen definierten Keyword-Satz, der von einer bestimmten Domain im Vergleich zu Wettbewerbern erfasst wird.

---

#### Organischer Traffic (Organic Traffic)

Sitzungen oder Nutzer, die über unbezahlte Suchergebnisse auf einer Website ankommen. Die primäre Konversionsmetrik für SEO.

---

#### Verweildauer (Dwell Time)

Die Dauer zwischen einem Nutzerklick auf ein Ergebnis und der Rückkehr zur SERP.

---

#### Absprungrate (Bounce Rate)

Der Prozentsatz der Sitzungen, bei denen der Nutzer die Website nach dem Anzeigen nur einer Seite verließ.

---

#### Domain Rating (DR) / Domain Authority (DA)

Drittanbieter-Metriken, die die Link-Autorität einer Domain annähern:
- **Domain Rating (DR)** — Ahrefs' Metrik, 0–100 logarithmische Skala
- **Domain Authority (DA)** — Mozs Metrik, 0–100 logarithmische Skala
- **Trust Flow / Citation Flow** — Majestiks duales Metriken-System

**Wichtig:** Dies sind proprietäre Schätzungen, keine Google-Signale.

---

#### Core Web Vitals-Punktzahl

CWV-Bewertung (Bestanden/Nicht bestanden pro Metrik) aus dem Chrome User Experience Report (CrUX) — Felddaten echter Nutzer.

---

## Teil VI — Technische SEO-Attribute

Technische SEO-Attribute regeln, wie Suchmaschinen Web-Inhalte entdecken, crawlen, rendern und indizieren.

---

#### Crawlbarkeit (Crawlability)

**Entitätsdatei:** [`entities/technical/crawlability.md`](entities/technical/crawlability.md)

Die Fähigkeit von Suchmaschinen-Crawlern (Googlebot, Bingbot), Seiten auf einer Website zu entdecken und darauf zuzugreifen.

---

#### Crawl-Budget

Die Anzahl der Seiten, die Googlebot auf einer Site innerhalb eines bestimmten Zeitrahmens crawlt. Bestimmt durch Crawl-Rate-Limit und Crawl-Nachfrage.

---

#### Indexierbarkeit (Indexability)

Ob eine gecrawlte Seite in Googles Suchindex aufgenommen und in Ergebnissen angezeigt werden kann.

---

#### robots.txt

**Entitätsdatei:** [`entities/technical/robots-txt.md`](entities/technical/robots-txt.md)

Eine Klartextdatei im Root einer Domain (`/robots.txt`), die Crawlern anweist, welche Seiten/Verzeichnisse gecrawlt oder vermieden werden sollen.

**Kritische Unterscheidung:** robots.txt kontrolliert das *Crawling*, nicht das *Indexieren*. Eine Seite, die in robots.txt gesperrt ist, kann dennoch indiziert werden, wenn sie von externen Seiten verlinkt wird.

---

#### XML-Sitemap

Eine XML-Datei, die URLs auf einer Site zur Entdeckungs- und Crawling-Führung auflistet.

**Typen:** Standard-Sitemap, Bild-Sitemap, Video-Sitemap, News-Sitemap, Index-Sitemap

---

#### Canonical-Tag (Kanonisches Tag)

**Entitätsdatei:** [`entities/technical/canonical.md`](entities/technical/canonical.md)

Das `<link rel="canonical" href="...">` Tag signalisiert Google die bevorzugte Version einer URL, wenn doppelte oder ähnliche Inhalte über mehrere URLs vorhanden sind.

**Behandlung:** Starker Hinweis — Google kann überschreiben, wenn es anderer Meinung ist.

---

#### Hreflang-Tags

HTML-Attribute, die Google signalisieren, welche Sprach-/Regionsversion einer Seite für bestimmte internationale Zielgruppen angezeigt werden soll.

**Format:** `<link rel="alternate" hreflang="de" href="...">`

---

#### Strukturierte Daten (JSON-LD)

**Entitätsdatei:** [`entities/technical/structured-data.md`](entities/technical/structured-data.md)

Maschinenlesbarer Code (JSON-LD ist Googles empfohlenes Format), der das Schema.org-Vokabular implementiert, um Seiteninhalt-Typ und -Attribute explizit an Suchmaschinen zu kommunizieren.

---

#### Open Graph Protokoll

Facebooks Metadaten-Protokoll (`og:title`, `og:image`, `og:description`, `og:url`) zur Kontrolle, wie Seiten erscheinen, wenn sie auf sozialen Plattformen geteilt werden.

---

#### Core Web Vitals (Technische Optimierung)

Technische Implementierungspraktiken zur Erfüllung der Core Web Vitals-Schwellenwerte:
- **LCP-Optimierung:** Server-Antwortzeit, Render-blockierende Ressourcen, Ressourcen-Ladezeit, Element-Render-Zeit
- **INP-Optimierung:** Lange JavaScript-Aufgaben minimieren, Hauptthread-Blockierung reduzieren
- **CLS-Optimierung:** Größenattribute auf Bildern/Videos, kein Einfügen von Inhalten über bestehenden Inhalten

---

#### JavaScript SEO

Die Herausforderung, sicherzustellen, dass JavaScript-gerenderter Inhalt von Suchmaschinen gecrawlt und indiziert werden kann.

---

#### AMP (Accelerated Mobile Pages / Beschleunigte Mobile Seiten)

Googles Open-Source-Framework (2015 gestartet) für schnell ladende mobile Webseiten.

**Aktueller Status:** Nicht mehr als Ranking-Faktor oder Top-Stories-Anforderung seit 2021.

---

## Teil VII — KI-Suchlandschaft

Die KI-Suchlandschaft beschreibt, wie große Sprachmodelle und generative KI die SERP transformieren.

---

#### KI-Übersicht (Google AI Overview)

**Entitätsdatei:** [`entities/ai-search/ai-overview.md`](entities/ai-search/ai-overview.md)

Googles Implementierung von Retrieval-Augmented Generation (RAG) in seinem Suchprodukt — der Mechanismus, durch den Google Gemini Informationen aus indizierten Web-Quellen synthetisiert, um geerdete, zitierte generative Antworten oben in der SERP zu produzieren.

---

#### Generative Engine Optimization (GEO)

**Entitätsdatei:** [`entities/ai-search/geo.md`](entities/ai-search/geo.md)

Die aufkommende Disziplin der Optimierung von Web-Inhalten, um die Wahrscheinlichkeit zu erhöhen, in KI-generierten Suchantworten zitiert, zitiert oder referenziert zu werden.

**GEO-Signale (forschungsbasiert):**
- Zitieren von autoritativen Quellen und Statistiken
- Einbeziehen von Experten-Zitaten
- Klare, fließende Prosa
- Umfassende Themenabdeckung
- Starkes zugrunde liegendes SEO
- Entitätsautorität (Knowledge-Graph-Präsenz)

---

#### Answer Engine Optimization (AEO)

Optimierung für Antwort-Engines — Suchschnittstellen, die direkte Antworten statt Linklisten zurückgeben.

---

#### LLM-Optimierung (LLMO)

Die Praxis der Optimierung von Marken- und Inhaltspräsenz innerhalb der Trainings- und Abrufmechanismen großer Sprachmodelle.

---

#### ChatGPT Search

OpenAIs Websuche-Integration in ChatGPT (Oktober 2024 gestartet), die Echtzeit-Web-Zitate in ChatGPT-Antworten bereitstellt.

---

#### Perplexity AI

Eine KI-betriebene Antwort-Engine, die das Web durchsucht und Antworten mit Inline-Zitaten synthetisiert.

---

#### Bing Copilot / Microsoft Copilot Search

Microsofts KI-augmentierte Sucherfahrung in Bing, betrieben von OpenAI GPT-4.

---

#### KI-Zitationsfaktoren

Die Signale, die beeinflussen, ob eine KI-Suchmaschine eine bestimmte Web-Quelle in ihrer generierten Antwort zitiert.

**Bekannte Faktoren:**
- Quellenautorität (Domain-Autorität, E-E-A-T-Signale)
- Thematische Spezifität und Relevanz
- Inhaltliche Aktualität
- Strukturelle Klarheit (Überschriften, Listen, Q&A-Formate)
- Faktische Genauigkeit und Zitationsdichte

---

## Teil VIII — Knowledge Graph & Entitäts-Framework

Der Knowledge Graph ist Googles semantische Datenbank realer Entitäten und Beziehungen.

---

#### Google Knowledge Graph

**Entitätsdatei:** [`entities/knowledge-entities/knowledge-graph.md`](entities/knowledge-entities/knowledge-graph.md)

Eine massive Graphdatenbank von Entitäten (Personen, Orte, Organisationen, Dinge, Konzepte) und den Beziehungen zwischen ihnen, die Googles entitätsbasiertes Suchverständnis antreibt.

**Schlüsselattribute:**
- `gestartet`: Mai 2012
- `quellen`: Wikipedia, Wikidata, Freebase (jetzt integriert), CIA World Factbook, offizielle Websites, strukturierte Daten
- `größe`: Geschätzte Hunderte von Milliarden Fakten über Milliarden von Entitäten
- `gründungseinsicht`: „Dinge, nicht Strings" — Entitäten verstehen, nicht Keywords abgleichen

---

#### Entitätstypen (Schema.org-Hierarchie)

Die wichtigsten Entitätstypkategorien, die für SERPs relevant sind:

- **Thing** — Basistyp für alle Entitäten
  - **Person** — Einzelpersonen (Autoren, öffentliche Personen, Fachleute)
  - **Organization** — Unternehmen, Institutionen, NGOs, Regierungsstellen
    - **LocalBusiness** — Physische Standortunternehmen
  - **Place** — Geografische Standorte
  - **Product** — Physische oder digitale Waren
  - **Event** — Ereignisse an einem Ort und zu einer Zeit
  - **CreativeWork** — Inhaltliche Artefakte
  - **Intangible** — Konzepte, Rollen, Mengen, strukturierte Werte

---

#### Benannte Entitätserkennung (Named Entity Recognition / NER)

Googles Prozess der Identifizierung und Klassifizierung benannter Entitäten in Text, verwendet für Anfrageinterpretation und Inhaltsrelevanzbeurteilung.

---

#### Entitätsdisambiguierung

Der Prozess der Auflösung, auf welche spezifische Entität sich eine Anfrage oder Erwähnung bezieht, wenn mehrere Entitäten ähnliche Namen teilen.

---

#### Entitätsetablierung (Knowledge Graph Entity Establishment)

Der Prozess, durch den eine reale Entität eine Darstellung im Google Knowledge Graph erhält.

**Etablierungssignale:**
- Wikipedia-Artikel
- Wikidata-Eintrag mit strukturierten Eigenschaften
- Strukturiertes Daten-Markup auf der offiziellen Website
- Presseberichterstattung und Erwähnungen von autoritativen Quellen
- Social-Profile-Verifizierung

---

## Teil IX — SERP-Layout-Anatomie

Das SERP-Layout beschreibt, wo verschiedene Ergebnistypen und Features auf der Suchergebnisseite erscheinen.

---

#### Position Null (Position Zero)

**Entitätsdatei:** [`entities/layout/position-zero.md`](entities/layout/position-zero.md)

Das Featured Snippet erscheint „über" Position 1, daher als Position Null bezeichnet. Die Seite, die Position Null hält, hält gleichzeitig ein organisches Ranking (typischerweise Positionen 1–5).

Mit dem Aufstieg der KI-Übersichten (2024) wurde eine neue Ebene über Position Null hinzugefügt — KI-Übersichten erscheinen über Featured Snippets, was effektiv eine „Position -1" für KI-generierte Antworten schafft.

---

#### Oberhalb des sichtbaren Bereichs (Above the Fold)

Der Teil der SERP, der ohne Scrollen sichtbar ist. Zunehmend dominiert von Anzeigen, KI-Übersichten und Featured Snippets — organische Ergebnisse erscheinen möglicherweise nicht oberhalb des sichtbaren Bereichs bei wettbewerbsintensiven Anfragen.

---

#### Blaue Links (Blue Links)

Die traditionellen organischen Suchergebnisse — URL, Titel und Snippet — das Format, das Google seit 1998 verwendet und immer noch das primäre Ergebnisformat für die meisten Anfragen ist.

---

#### SERP Desktop vs. Mobil-Layout

Das SERP-Layout unterscheidet sich erheblich zwischen Desktop und Mobil:
- **Desktop:** Zweispaltiges Layout mit Knowledge Panel rechts, organische Ergebnisse links
- **Mobil:** Einspaltig, sequenziell; KI-Übersichten und Local Pack erscheinen prominenter

---

#### SERP-Karussell

Eine horizontal scrollbare Reihe von Ergebnissen (Video, Bilder, Rezepte, Produkte, Nachrichten).

---

## Teil X — Serponado-Entitätsstandard

Der Serponado-Standard definiert das Schema und Format für alle Entitätsseiten in diesem Repository.

**Vollständige Spezifikation:** Siehe [STANDARD.md](STANDARD.md)

### Entitäts-Frontmatter-Schema

Jede Entitätsdatei beginnt mit YAML-Frontmatter nach folgendem Schema:

```yaml
---
entityId: string          # Eindeutiger kebab-case-Bezeichner (erforderlich)
name: string              # Anzeigename (erforderlich)
type: EntityType          # Siehe EntityType-Enum (erforderlich)
schemaType: string        # Schema.org-Typ oder DefinedTerm
version: semver           # Semantische Version dieses Entitätsdatensatzes
status: Status            # active | deprecated | emerging | experimental
aliases: string[]         # Alternative Namen
sameAs: URI[]             # Externe Knowledge-Base-URIs (Wikipedia, Wikidata)
parent: entityId          # Übergeordnete Entitätsreferenz
namespace: string         # Unterordnerpfad innerhalb von entities/
relations: Relation[]     # Typisierte Beziehungen zu anderen Entitäten
attributes: object        # Typspezifische Schlüssel-Wert-Attribute
evidence: Evidence[]      # Quellenangaben zur Unterstützung der wichtigsten Behauptungen
lastReviewed: date        # ISO 8601-Datum der letzten Überprüfung
---
```

### EntityType-Enum

```
SERP_Feature          # Ein Feature, das in der SERP erscheint
Paid_Feature          # Eine Werbe-/bezahlte SERP-Platzierung
Ranking_Factor        # Ein Signal, das die Position in Ergebnissen beeinflusst
Algorithm             # Eine Kern-Algorithmuskomponente
Algorithm_Update      # Ein benanntes Update-Ereignis
Search_Intent         # Eine Suchintentionsklassifizierung
Metric                # Ein messbares Performance- oder Autoritätssignal
Technical_Attribute   # Ein technisches SEO-Attribut oder eine Konfiguration
AI_Search_Feature     # Ein KI-augmentiertes Such-Feature oder Konzept
Layout_Element        # Eine SERP-Layout-Position oder anatomische Komponente
Entity_Type           # Eine Kategorie realer Entitäten
Tool                  # Ein SEO- oder suchbezogenes Tool oder eine Plattform
Concept               # Ein abstraktes SERP- oder SEO-Konzept
```

### Relationsprädikate

```
IS_TYPE_OF          # Diese Entität ist ein Untertyp/eine Instanz des Ziels
HAS_SUBTYPE         # Diese Entität hat das Ziel als benannten Untertyp
PART_OF             # Diese Entität ist eine Komponente des Ziels
CONTAINS            # Diese Entität enthält das Ziel als Komponente
TRIGGERS            # Diese Entität verursacht oder aktiviert das Ziel
TRIGGERED_BY        # Diese Entität wird durch das Ziel verursacht/aktiviert
COMPETES_WITH       # Diese Entität und das Ziel konkurrieren um denselben SERP-Raum
REQUIRES            # Diese Entität erfordert das Ziel zum Funktionieren
POWERS              # Diese Entität treibt das Ziel an oder ermöglicht es
POWERED_BY          # Diese Entität wird durch das Ziel angetrieben/ermöglicht
REPLACED_BY         # Diese Entität wurde durch das Ziel ersetzt
REPLACES            # Diese Entität hat das Ziel ersetzt
MEASURES            # Diese Metrik quantifiziert das Ziel
MEASURED_BY         # Diese Entität wird durch die Zielmetrik quantifiziert
OPTIMIZED_BY        # Diese Entität wird durch die Zielpraxis optimiert
AFFECTS             # Diese Entität beeinflusst das Ziel
INTRODUCED_BY       # Diese Entität wurde durch das Ziel eingeführt
DEPRECATED_BY       # Diese Entität wurde durch das Ziel obsolet gemacht
RELATED_TO          # Allgemeine semantische Beziehung
ANALOGOUS_TO        # Funktional ähnlich dem Ziel in einem anderen Kontext
```

---

## Entitätsindex

### SERP-Features

| Entität | Datei | Status |
|---------|-------|--------|
| Featured Snippet | [serp-features/featured-snippet.md](entities/serp-features/featured-snippet.md) | aktiv |
| Knowledge Panel | [serp-features/knowledge-panel.md](entities/serp-features/knowledge-panel.md) | aktiv |
| People Also Ask | [serp-features/people-also-ask.md](entities/serp-features/people-also-ask.md) | aktiv |
| Bilderpaket | [serp-features/image-pack.md](entities/serp-features/image-pack.md) | aktiv |
| Video-Karussell | [serp-features/video-carousel.md](entities/serp-features/video-carousel.md) | aktiv |
| News Box / Top Stories | [serp-features/news-box.md](entities/serp-features/news-box.md) | aktiv |
| Local Pack | [serp-features/local-pack.md](entities/serp-features/local-pack.md) | aktiv |
| Sitelinks | [serp-features/sitelinks.md](entities/serp-features/sitelinks.md) | aktiv |
| Ähnliche Suchanfragen | [serp-features/related-searches.md](entities/serp-features/related-searches.md) | aktiv |
| People Also Search For | [serp-features/people-also-search-for.md](entities/serp-features/people-also-search-for.md) | aktiv |
| Perspectives / Forum-Ergebnisse | [serp-features/perspectives.md](entities/serp-features/perspectives.md) | aktiv |
| Shopping-Ergebnisse | [serp-features/shopping-results.md](entities/serp-features/shopping-results.md) | aktiv |
| Bewertungs-Snippets | [serp-features/review-snippets.md](entities/serp-features/review-snippets.md) | aktiv |
| FAQ-Ergebnisse | [serp-features/faq-results.md](entities/serp-features/faq-results.md) | veraltet |
| Rezeptkarten | [serp-features/recipe-cards.md](entities/serp-features/recipe-cards.md) | aktiv |
| Stellenanzeigen | [serp-features/job-listings.md](entities/serp-features/job-listings.md) | aktiv |
| KI-Übersicht (SERP) | [serp-features/ai-overview.md](entities/serp-features/ai-overview.md) | aktiv |

### Bezahlte Features

| Entität | Datei | Status |
|---------|-------|--------|
| Textanzeigen (RSA) | [paid-features/text-ads.md](entities/paid-features/text-ads.md) | aktiv |

### Rankingfaktoren

| Entität | Datei | Status |
|---------|-------|--------|
| E-E-A-T | [ranking-factors/e-e-a-t.md](entities/ranking-factors/e-e-a-t.md) | aktiv |
| Core Web Vitals | [ranking-factors/core-web-vitals.md](entities/ranking-factors/core-web-vitals.md) | aktiv |
| Backlinks | [ranking-factors/backlinks.md](entities/ranking-factors/backlinks.md) | aktiv |
| Topische Autorität | [ranking-factors/topical-authority.md](entities/ranking-factors/topical-authority.md) | aktiv |

### Algorithmen

| Entität | Datei | Status |
|---------|-------|--------|
| RankBrain | [algorithms/rankbrain.md](entities/algorithms/rankbrain.md) | aktiv |
| BERT | [algorithms/bert.md](entities/algorithms/bert.md) | aktiv |
| Hilfreiches Inhaltssystem | [algorithms/helpful-content.md](entities/algorithms/helpful-content.md) | aktiv |
| Google Panda | [algorithms/panda.md](entities/algorithms/panda.md) | veraltet |
| Google Penguin | [algorithms/penguin.md](entities/algorithms/penguin.md) | veraltet |

### Suchintentionen

| Entität | Datei | Status |
|---------|-------|--------|
| Informationeller Intent | [intent/informational.md](entities/intent/informational.md) | aktiv |
| Navigationaler Intent | [intent/navigational.md](entities/intent/navigational.md) | aktiv |
| Transaktionaler Intent | [intent/transactional.md](entities/intent/transactional.md) | aktiv |
| Kommerzieller Untersuchungsintent | [intent/commercial-investigation.md](entities/intent/commercial-investigation.md) | aktiv |
| Lokaler Intent | [intent/local.md](entities/intent/local.md) | aktiv |

### Metriken

| Entität | Datei | Status |
|---------|-------|--------|
| Impressionen | [metrics/impressions.md](entities/metrics/impressions.md) | aktiv |
| Click-Through-Rate | [metrics/ctr.md](entities/metrics/ctr.md) | aktiv |
| Sichtbarkeitsindex | [metrics/visibility-index.md](entities/metrics/visibility-index.md) | aktiv |

### Technische Attribute

| Entität | Datei | Status |
|---------|-------|--------|
| Strukturierte Daten (JSON-LD) | [technical/structured-data.md](entities/technical/structured-data.md) | aktiv |
| Canonical-Tag | [technical/canonical.md](entities/technical/canonical.md) | aktiv |
| robots.txt | [technical/robots-txt.md](entities/technical/robots-txt.md) | aktiv |

### KI-Such-Features

| Entität | Datei | Status |
|---------|-------|--------|
| GEO (Generative Engine Optimization) | [ai-search/geo.md](entities/ai-search/geo.md) | aufkommend |
| KI-Übersicht (KI-Such-Entität) | [ai-search/ai-overview.md](entities/ai-search/ai-overview.md) | aktiv |

### Knowledge-Entitäten

| Entität | Datei | Status |
|---------|-------|--------|
| Google Knowledge Graph | [knowledge-entities/knowledge-graph.md](entities/knowledge-entities/knowledge-graph.md) | aktiv |

### Layout-Elemente

| Entität | Datei | Status |
|---------|-------|--------|
| Position Null | [layout/position-zero.md](entities/layout/position-zero.md) | aktiv |

---

## Glossar

| Begriff | Definition |
|---------|------------|
| **AEO** | Answer Engine Optimization — Optimierung für direkte Antwortoberflächen |
| **AIO** | AI Overview — Googles KI-generierter SERP-Antwortblock |
| **AMP** | Accelerated Mobile Pages — Googles schnell ladendes mobiles Webformat |
| **BERT** | Bidirectional Encoder Representations from Transformers — Googles NLP-Modell |
| **CLS** | Cumulative Layout Shift — Core Web Vitals Metrik für visuelle Stabilität |
| **CTR** | Click-Through-Rate — Klicks geteilt durch Impressionen |
| **CWV** | Core Web Vitals — LCP, INP, CLS |
| **DA** | Domain Authority — Mozs Domain-Stärke-Metrik |
| **DR** | Domain Rating — Ahrefs' Domain-Stärke-Metrik |
| **DSA** | Dynamic Search Ads — auto-generierte Google Ads aus Website-Inhalten |
| **E-E-A-T** | Experience, Expertise, Authoritativeness, Trustworthiness |
| **FID** | First Input Delay — veraltete CWV-Metrik, ersetzt durch INP |
| **GBP** | Google Business Profile — früher Google My Business |
| **GEO** | Generative Engine Optimization — Optimierung für KI-generierte Antworten |
| **GSC** | Google Search Console — Googles Webmaster-Analysetool |
| **INP** | Interaction to Next Paint — Core Web Vitals Interaktivitätsmetrik |
| **KG** | Knowledge Graph — Googles Entitäts-Beziehungsdatenbank |
| **KP** | Knowledge Panel — Entitätsinformationsfeld rechts der SERP |
| **LCP** | Largest Contentful Paint — Core Web Vitals Lademetrik |
| **LLMO** | Large Language Model Optimization — Markenoptimierung im LLM-Kontext |
| **LSA** | Local Service Ads — Pay-per-Lead-Anzeigen für lokale Dienstleistungsunternehmen |
| **MUM** | Multitask Unified Model — Googles multimodales KI-Modell |
| **NER** | Named Entity Recognition — Entitäten in Text identifizieren |
| **PAA** | People Also Ask — erweiterbare Frage-und-Antwort-SERP-Feature |
| **PASF** | People Also Search For — verwandte Suchvorschläge beim Rückklick |
| **PLA** | Product Listing Ad — visuelle Produktanzeige (jetzt Shopping Ads) |
| **PMax** | Performance Max — Googles kanalübergreifender automatisierter Kampagnentyp |
| **QDF** | Query Deserves Freshness — Googles temporales Aktualitätssystem |
| **RSA** | Responsive Search Ads — aktuelles Google Ads-Textformat |
| **SERP** | Search Engine Results Page — die von einer Suchmaschine zurückgegebene Seite |
| **SGE** | Search Generative Experience — jetzt AI Overviews genannt |
| **SOV** | Share of Voice — % der verfügbaren organischen Klicks erfasst |
| **TTFB** | Time to First Byte — Server-Antwortgeschwindigkeitsmetrik |
| **YMYL** | Your Money Your Life — Hochrisiko-Inhaltskategorie (Gesundheit, Finanzen, Sicherheit) |

---

## Mitwirken

Siehe [CONTRIBUTING.md](CONTRIBUTING.md) für den vollständigen Beitragsleitfaden.

**Kurzübersicht:**
1. Repository forken
2. [`templates/entity-template.md`](templates/entity-template.md) in das entsprechende `entities/[namespace]/`-Verzeichnis kopieren
3. Alle erforderlichen Frontmatter-Felder ausfüllen und einen umfassenden Prosa-Abschnitt schreiben
4. Frontmatter gegen [`schema/entity.schema.json`](schema/entity.schema.json) validieren
5. Entität zur Indextabelle in dieser README und zu `index.json` hinzufügen
6. Pull Request mit der Entitäts-ID und dem Namen als PR-Titel einreichen

**Qualitätsstandards für Entitäten:**
- Alle erforderlichen Frontmatter-Felder müssen vorhanden sein
- `sameAs`-Links zu Wikipedia und/oder Wikidata sind erforderlich, wo Entitäten dort existieren
- Mindestens 2 `evidence`-Zitate mit Quell-URL, Titel und Abrufdatum
- Prosa-Abschnitt muss wirklich erklärend sein — keine Liste von Keywords
- Veraltete Entitäten müssen erklären, was sie ersetzte und warum

---

## Lizenz

Serponado wird unter der [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)-Lizenz veröffentlicht.

Es ist erlaubt, dieses Material zu teilen und anzupassen — unter der Bedingung, dass Serponado angemessen kreditiert wird.

---

*Serponado — Denn der einzige Weg, einen Tornado zu verstehen, ist, jedes Trümmerstück zu kartieren, das er hinterlässt.*

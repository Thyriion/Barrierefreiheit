## Barrierefreiheitsstärkungsgesetz (BFSG)

- 22.06.2022 verabschiedet
- 2025 Pflicht für alle
- Betroffen sind Hersteller von Produkten wie Fahrkartenautomaten oder EBooks
    - Telekommunikationsdienste
    - Bankdienstleistungen
    - Onlinehandel
    - Ausgenommen:
        - Kleinstunternehmer mit weniger als 10 Mitarbeiter:innen
        - Wenn die Barrierefreiheit eine unverhältnismäßige Belastung darstellt
    
## Standard für Web-accessibility

- World Wide Web Consortium (W3C) gründet Web Accessibility Initiative (WAI)
- Guidelines (WCAG) veröffentlicht

### Prinzipien der WCAG

- Wahrnehmbar (z.B. Untertitel bei Videos für Gehörlose)
- Bedienbar (z.B. Benutzung der Website nur mit Tastatur)
- Verständlich (einfache Sprache)
- Robust (muss mit einer vielzahl von Technologien inkl. assistiver Technologie funktionieren)

## Einstieg für Barrierefreiheit

- https://www.a11yproject.com/
- https://www.w3.org/WAI/standards-guidelines/wcag/
- https://www.w3.org/WAI/design-develop/
- https://inclusive-components.design/

## Seitenstruktur

- verschiedene Personen profitieren von einer guten Seitenstruktur
    - Menschen mit kognitiver Einschränkung oder Lernbehinderung können Inhalte besser finden und priorisieren
    - Nutzer von Screenreadern können unwichtige Passagen überspringen
    - Tastaturnutzer können effektiver durch Seite navigieren
    - Menschen mit visuellen Einschränkungen haben eine bessere Orientierung
    - Mobile Users im "reading" oder "reader" Modus sehen nur den Hauptinhalt (wenn Markup stimmt)

### Aussehen einer Seite

```
<header role="banner"></header>
<main role="main"></main>
<nav role="navigation"></navigation>
<footer role="contentinfo"></footer>
```

### Beschriftung einzelner Abschnitte

```
<nav aria-labelledby="regionheading">
    <h2 id="regionheading">On this Page</h2>
</nav>

<nav aria-label="main">
</nav>
```

### informative Bilder

- Bilder übertragen Infos zum Text
- Alt Text setzen

### dekorative Bilder

- kein alt-tag setzen
- egal, ob bild auf seite ist, da Bild für Workflow auf Seite nicht wichtig ist
- für nutzer nicht relevant, dienen lediglich dem design und transportieren keine info

### komplexe Bilder

- HTML5 Standard :

```
<figure role="group">
    <img src="" alt="beschreibender alt text" />
    <figcaption>
        <a href="diest ist ein link">Text zur verlinkenden Seite</a>
    </figcaption>
</figure>
```

### Multimedia

- Bereitstellung von Untertitel, Texttranskripte, Audiodeskription für Podcasts
- Untertitel:
    - Synchron
    - Zugänglich (kontrast von Text und Hintergrund)
    - Gleicher Inhalt muss transportiert werden
- Texttranskripte
    - zusätzliche Infos müssen geliefert werden (wann gibt es Musik, Sound)

→ Video erst dann Barrierefrei, wenn Untertitel UND Transskripte vorhanden

- Audiodeskription
    - richtet sich an blinde/schlecht sehende Menschen
    - Szenen ohne Dialog aber mit Hintergrundmusik sind für diese Gruppe nicht eindeutig verständlich

### Navigation

- Reihenfolge der Navigationselemente spielt keine Rolle
- Menü mit einem label versehen
- klar erkennbare aktive Links bzw. hover-state

### Checkliste für Projekte

- https://a11yprojects.com/checklist/
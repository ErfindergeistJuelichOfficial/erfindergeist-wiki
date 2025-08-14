---
title: "g-calendar"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

## Einrichten

- im Admin Bereich von Wordpress gibt es einen "Erfindergeist" Bereich mit dem Unterpunkt "Google Calendar"
- zu hinterlegen ist:
  - ApiKey
  - google calendar id

### ApiKey

- Der ApiKey kann unter [console](https://console.cloud.google.com/apis/api/calendar-json.googleapis.com) eingerichtet werden
- Es wird der google account vom Verein genutzt.

### google calendar id

- Im Vereins Google Account
- Google Kalender öffnen
- Meine Kalender öffnen
- Über den Kalender hovern den man nutzen möchten
- Die drei vertikalen Punkte klicken
- Wähle Einstellungen und Freigabe
- Runter scrollen bis man die Kalender ID findet
- Beispiel Kalender ID: `{hash}@group.calendar.google.com`

## Termin Einstellen

Die Tags sind nicht fest programmiert. Diese sind Dynamisch je Kalender einstellbar. Um es einheitlich zu machen sollten Folgende Tags verwendet werden:

- Projekt: (nur ein Tag pro Termin verwenden)
  - `#OffeneWerkstatt`
  - `#Repaircafe`
  - `#KreativTag`
  - `#Mobilitaetstag`
- Ort (nur ein Tag pro Termin verwenden)
  - `#Awo`
  - `#Stadtbücherei`

## Verwendung

- Es gibt zwei Verwendungen:
  - `index.php` => Wordpress Plugin
  - `index.html` => eigenständige Webseite

### Verwendung als Wordpress Plugin

- Auf einer Seite "individuelles HTML" Block hinzufügen
- Es muss einen script Block geben mit der id `gcalendarTemplate`
- im script block muss ein [Handlebars](https://handlebarsjs.com/) Template hinterlegt sein.
- [Bootsrap 5](https://getbootstrap.com/docs/5.3/getting-started/introduction/) wird zur verfügung gestellt und kann im template genutzt werden.
- Es muss ein div element geben mit der id `gcalendarList`
- Im div können Lade animationen hinterlegt werden. Der Inhalt wird nach erfolgreichem laden durch den gerenderten Kalender ersetzt.
- in der css-datei `loading-shimmer.css` sind lade animationen hinterlegt
- folgend ein minimalistisches Komplett Beispiel:

```javascript
<script id="gcalendarTemplate" type="text/x-handlebars-template">
 <div class="container text-dark p-0">
    {{#each items}}
      <span>{{summary}}</span>
    {{/each}}
  </div>
</script>


<div
  style="margin-left: auto; margin-right: auto; max-width: 1312px; width: 90vw"
  id="gcalendarList"
>
  <div class="shimmerBG content-line"></div>
  <div class="shimmerBG content-line"></div>
  <div class="shimmerBG content-line end"></div>
</div>
```

### Verwendung als eigenständige Webseite

- einfach die index.html aufrufen
- eingerichtet unter [Termine](https://termine.erfindergeist.org)

### Handlebars Helper

neben den normalen Handlebars Helpers gibt es auch folgende:

### include

- Aufruf: `include {array} {string}` returns boolean
- prüft ob in einem string array ein string vorhanden ist.
- Beispiel:

```javascript
  {{#each items}} 
    {{#if (include tags "KreativTag")}} 
      <span> Heute KreativTag </span> 
    {{/if}}
   {{/each}}
```

### filter

- Aufruf: `filter {array} {string}` returns filtered array
- erwartet das array vom typ object ist und das propety tags existiert.
- prüft ob im property, string vorkommt.

```javascript
  {{#each (filter items "KreativTag")}} 
    <span> Ich bin ein KreativTag element </span> 
  {{/each}}
```

### first

- Aufruf: `first {array} {number}` returns number elemente von array, number ist optional default ist 1
- Beispiel 1 element:

```javascript
  {{#each (first items)}} 
    <span> Ich bin ein KreativTag element </span> 
  {{/each}}
```

- Beispiel 3 Elemente:

```javascript
  {{#each (first items 3)}} 
    <span> Ich bin ein KreativTag element </span> 
  {{/each}}
```

### isOdd / isEven

- Aufruf: `isOdd {number}` returns boolean
- Beispiel:

```javascript
  {{#each items}}
    {{#if (isOdd @index)}} 
      <div class="container text-dark bd-container-even"> 
    {{/if}}
    {{#if (isEven @index)}} 
      <div class="container text-dark bd-container-odd" > 
    {{/if}}
      <span> {{this}} </span> 
    </div>

  {{/each}}
```

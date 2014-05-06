# Le calendrier des événements autour du journalisme et des médias

C'est un fork de sheetsee.js + calendar développé par @jlord .

![ss-cal](ss-cal.png)

**Sheetsee.js Calendar**

Sheetsee.js est une librairie qui permet d'extraire des données des documents google, en l'occurence ici des feuilles de calcul.

**Il est 'localisé' en français, vous pouvez le forker bien sûr !**

Pas trop le temps de traduire les explications de Jessica là tout de suite, mais à savoir
. mon repository n'est pas très clean parce qu'il fait appel à des css hébergées ailleurs, du coup  [https://newsresources.github.io/journalism-events-calendar/](cette url sur github est assez sale). 
. la version hébergée est plus propre, elle est accessible ici -> http://www.newsresources.org/journalism-events-calendar/

This repository contains webfiles on a branch named `gh-pages`, which means GitHub hosts them for free at: [jlord.github.io/sheetsee-calendar](jlord.github.io/sheetsee-calendar). When you fork the project to your account, you too can have a hosted site -- easy peasy!

## Set Up

Here's how to get going with your version:

### 1. Create spreadsheet

Create a new spreadsheet for your data on Google Docs. It should contain these headers (case and order of columns do not mattter, spelling does):

```
Start Date | End Date |  Name | Location | Tickets | Contact
```

#### Dates

Your dates should be in the `mm/dd/yyyy` format. If your day is multiple days, use both the Start and End Date columns, if it's just one day, leave End Date blank.

### 2. Publish spreadsheet

In order to fetch your spreadsheet's data you'll need to click File > Publish to the Web > Start Publishing. This just means when asked for the data in the spreadsheet, Google returns it.

![publish](publish.png)

### 3. Fork this repository

From this page, click the "Fork" button at the top right. Bam!

### 4. Add your spreadsheet key

- From your fork's page on GitHub, click to view the `index.html` file.
- When it opens, click "Edit"

You'll see code near the bottom that looks like this:

```JAVASCRIPT
document.addEventListener('DOMContentLoaded', function() {
  var URL = "0AuOjlXjUrSbAdE1XRFJkeEJZQ1NSelhILUR0NXdBWUE"
  Tabletop.init( { key: URL, callback: generateCalendar, simpleSheet: true } )
})
```

The variable `URL` is your spreadsheet's key, which is the long set of letters and numbers in the middle of your spreadsheet's url.

- Copy and paste your spreadsheet's key in place of the existing one.
- Click "Commit changes" at the bottom of the page.

#### Ta Da!

In a few minutes you'll be able to visit your site at: yourgithubname.github.io/sheetsee-calendar.

**Pro-tip** You can click "Settings" on your fork's page and rename it to a more appropriate-to-you name than _sheetsee-calendar_ :)

## Styling

Included in this repository is a stylesheet for the calendar. You can keep the style as is or make it your own! Classes are like so:

![css](calendar-css.png)

## Map

| Include a Map | Map Documentation |
| ------------- | ----------------- |
| ![map](with-map.png) | If you want to include a map, you can do so! There is a map version on the `with-map` [branch](https://github.com/jlord/sheetsee-calendar/tree/with-map). Read `map-doc.md` for [instructions](https://github.com/jlord/sheetsee-calendar/blob/with-map/map-doc.md). |

## Use cases

1. http://calendar.codebar.io/
2. http://findyourfitwichita.com/bike

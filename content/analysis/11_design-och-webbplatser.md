---
Title: Valfri analys
Description: Projektet - Valfri analys
Template: kmom
---

Projektet - Valfri analys - Laddningstider
==========================

Min webbplats i projektet har analyserats med avseende på bilder och laddningstider. Webbplatsen har sedan optimerats med mål att minska storlek, laddningstider och få bättre poäng i kategorin performance i Lighthouse.

## Metod

Jag undersökte den webbplats som jag gjort som del i projektet i kursen Teknisk webbdesign och användbarhet med avseende på laddningstider. De tre viktigaste sidorna från min webbplats i projektet har analyserats (index, book och members). Samtliga sidor har besökts med Chrome webbläsare. Via dev-tools har sidans storlek och laddningstid noterats. Samtliga sidor har också testats med Lighthouse och förbättringsförslag har noterats. Testerna har gjorts efter att webbplatsen var nästintill färdigställd. Härefter har några av förbättringsförslagen implementerats och testerna har sedan gjorts om.

## Resultat

<div class="framesheet2">
    <iframe class="resultsheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTqaHSb2616f1WGyy_3ohh9Tp7Vwiegl_sf89ccf9899HWiHq2mdU26iHLwyTg1wWaX2-UXaOF0DN-1/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>

Förbättringsförslag var:
- Reducera renderingsblockerande CSS
- Använda nyare bild-format såsom AVIF och WebP
- Sätta vidd och höjd på bilderna för att förbättra CLS
- Förladda bakgrundsbilden via html-filen istället för css-filen

## Analys

Vad som tyngde min webbplats verkade framförallt vara den stora hero-bilden, men också fontawesome-ikonerna.

Förbättringar som implementerades:
- Fontawesome-ikonerna togs bort och SCSS-filerna rensades. Storleken på CSS-filen minskade från 15 till 2,8 kB
- Fonterna länkades direkt i head-elementet i html-filen istället för i CSS-filen.
- Cimage användes redan på webbplatsen, men några bilder kunde minskas ytterligare något.
- Kvalitet och storlek på hero-bilden minskades via cimage och en mindre bild användes för mobila enheter. Genom att sätta kvaliteten till 50% kunde storleken minskas från 1,5 MB till ca 600 kB. För mobila enheter kunde bredden minskas och storleken minskade till 72 kB. Laborerade med att förladda bakgrunds-bilden via head-elementet i html-filen istället för i CSS-filen, men då gick det inte att ha en egen version för mobila enheter så detta implementerades inte.

Att ändra bild-format kändes inte aktuellt då cimage inte stöjder dessa. Ange bredd och höjd på bilder gick inte eftersom jag valt att de ska anpassa storleken något efter vilken enhet som används, men det är något jag kommer ta med mig till framtida projekt.

Med hjälp av ovanstående förbättringsförlag kunde storleken på sidorna minskas med drygt hälften. Laddningstiderna minskade också, men inte lika mycket. Poängen på performance i Lighthouse-testet kunde öka till mellan 96 och 100. Särskilt LCP kunde minskas mycket, men CLS förblev oförändrat eller något sämre.

Med hjälp av relativt enkla medel kunde alltså sidans storlek och laddningstider minska och performance förbättras väsentligt. Cimage verkar vara till stor hjälp för att förbättra webbplatsens prestanda.

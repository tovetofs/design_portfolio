---
Title: Laddningstid
Description: Kmom05 - Webbplatsers laddningstid och användbarhet
Template: kmom
---

Kmom05 - Webbplatsers laddningstid
==========================

Uppgiften handlade om att testa hur snabbt några olika webbsidor laddas och undersöka vad som går att förbättra med avseende på laddningstid och användbarhet.

## Urval

För den här rapporten valdes samma webbplatser som förra veckan, nämligen tre stycken svenska skiddestinationer. Webbplatserna hittades via google, sökning på 'skidresa Sverige', 'skidresa Härjedalen' och 'skidresa Dalarna'. De webbplatser som valdes var: Funäsfjällen (funasfjallen.se), Lofsdalen (lofsdalen.com) och Fjätervålen (fjatervalen.se).

## Metod

För varje webbplats har tre stycken sidor undersökts, förstasidan, en sida som nås med länk från förstasidan och en som nås via länk från sida två. Alla sidor har testats på PageSpeed Insights. Samtliga sidor har också besökts med webbläsaren Chrome och via dev-tools har laddningstid, antal resurser som laddats och sidans totala storlek noterats. För varje sida har mätningen gjorts tre gånger och medelvärdena presenteras. Mätningarna gjordes 1 dec 2023.

## Resultat

![Funäsfjällen](%base_url%/image/funasfjallen.png){.colorclass}

### Funäsfjällen

<table class="loadtable">
    <tr>
        <th colspan="2">Undersökta sidor:</th>
    </tr>
    <tr>
        <td>Sida 1
        </td>
        <td>https://www.funasfjallen.se/vinter/
        </td>
    </tr>
    <tr>
        <td>Sida 2
        </td>
        <td>https://www.funasfjallen.se/vinter/gora/
        </td>
    </tr>
    <tr>
        <td>Sida 3
        </td>
        <td>https://www.funasfjallen.se/vinter/gora/myskoxar/
        </td>
    </tr>
</table>


<iframe class="resultsheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRrKvNIYxD5N8_-RxtQp4VXxWazXzsIdX_5jYZ_300FGvOzjn36u5jtDg6twCMV4jQr5WhOzFHlg1rA/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

Förbättringsförslag: Använda bilder i rätt storlek och rätt format.

![Fjätervålen](%base_url%/image/fjatervalen.png){.colorclass}

### Fjätervålen

<table class="loadtable">
    <tr>
        <th colspan="2">Undersökta sidor:</th>
    </tr>
    <tr>
        <td>Sida 1
        </td>
        <td>https://fjatervalen.se/
        </td>
    </tr>
    <tr>
        <td>Sida 2
        </td>
        <td>https://fjatervalen.se/utforsakning/
        </td>
    </tr>
    <tr>
        <td>Sida 3
        </td>
        <td>https://fjatervalen.se/nedfarter/
        </td>
    </tr>
</table>

<iframe class="resultsheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRrKvNIYxD5N8_-RxtQp4VXxWazXzsIdX_5jYZ_300FGvOzjn36u5jtDg6twCMV4jQr5WhOzFHlg1rA/pubhtml?gid=1688105049&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

Förbättringsförslag: Undvika renderings-blockerande resurser och förbättra serverns responstid.

![Lofsdalen](%base_url%/image/lofsdalen2.png){.colorclass}

### Lofsdalen

<table class="loadtable">
    <tr>
        <th colspan="2">Undersökta sidor:</th>
    </tr>
    <tr>
        <td>Sida 1
        </td>
        <td>https://www.lofsdalen.com/sv/
        </td>
    </tr>
    <tr>
        <td>Sida 2
        </td>
        <td>https://www.lofsdalen.com/en/skiing
        </td>
    </tr>
    <tr>
        <td>Sida 3
        </td>
        <td>https://www.lofsdalen.com/en/ski-school
        </td>
    </tr>
</table>

<iframe class="resultsheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRrKvNIYxD5N8_-RxtQp4VXxWazXzsIdX_5jYZ_300FGvOzjn36u5jtDg6twCMV4jQr5WhOzFHlg1rA/pubhtml?gid=233347740&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

Förbättringsförslag: Reducera javascript som ej används och minska antalet inbäddade video-klipp.

## Analys

Alla tre webbplatser verkar ha problem med Cumulative Layout Shift (CLS) och det är därför bara Lofsdalens webbplats som klarar Core Web Vitals Assessment på Page Speed Insights för några av mättillfällena. Både Funäsfjällen och Fjätervålen har också problem med Time To First Byte (TTFB). Fjätervålen och Lofsdalen får överlag riktigt dåliga poäng i kategorin performance. Således verkar det finnas stor förbättringspotential för alla tre webbplatserna.

Förbättringsförslagen överlappar en hel del. Stor förbättringspotential finns för bildhantering, särskilt på Fulufjällens webbplats. Att presentera bilder i rätt storlek och kvalitet samt använda sig av nyare bild-format såsom AVIF och WebP skulle kunna förbättra laddningstiderna.

Att reducera oanvänd JavaScript är också ett viktigt förslag och ta bort renderings-blockerande resurser såsom JavaScript och CSS som inte är omedelbart nödvändig. Här verkar Lofsdalens webbplats kunna rensa rejält i sina JavaScript-filer och Fjätervålen bland CSS. Förbättra serverns responstid föreslås för Funäsfjällen och Fjätervålen.

Lofsdalen har några sidor som är väldigt stora. Det verkar som att det är flera inbäddade video-klipp som drar upp storleken och det känns ganska onödigt. Man kanske kunde länka till filmerna på något smartare sätt.

Avseende användbarhet finns en del som borde vara enkelt att åtgärda, exempelvis att använda alt-attribut till bilder, åtgärda dålig kontrast-ratio och att ge länkar en beskrivande text. 

Det är svårt att utse någon riktig vinnare, tycker det är rätt jämt mellan Lofsdalen och Funäsfjällen och på sista plats Fjätervålen.

Laddningstid på mer än 2 sekunder uppfattar jag som långsamt. Webbplatserna i testet klarar oftast detta, men någon sida med video och mycket bilder tar betydligt längre tid att ladda. 

## Övrigt

Deltagare: Tove Lernvall
